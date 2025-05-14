# Build stage - Node.js 16 with compatible Angular CLI
FROM node:16.16.0 AS build

WORKDIR /app

# Install specific Angular CLI version first
RUN npm install -g @angular/cli@13

# Copy package files
COPY package*.json ./

# Install with legacy peer deps flag
RUN npm install --legacy-peer-deps

# Copy source
COPY . .

# Build with explicit output path
RUN ng build --output-path=dist/client

# Production stage
FROM nginx:alpine

# Clear default content
RUN rm -rf /usr/share/nginx/html/*

# Copy built files (adjust path if needed)
COPY --from=build /app/dist/client /usr/share/nginx/html

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]