# Use a Python base image
FROM python:3.12-slim-bookworm

# Set the working directory inside the container
WORKDIR /workspaces/dev-env-py

# Install git and other essential tools
RUN apt-get update && apt-get install -y --no-install-recommends \
    git \
    && rm -rf /var/lib/apt/lists/*

# Install uv globally in the container using the recommended multi-stage approach for efficiency
COPY --from=docker.io/astral/uv:latest /uv /usr/local/bin/uv

# Set environment variables
ENV PATH="/usr/local/bin:$PATH"
ENV UV_COMPILE_BYTECODE=1

# Dependencies will be installed via postCreateCommand after the workspace is mounted
