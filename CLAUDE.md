# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Spring Boot 3.5.6 application using Java 21, built with Gradle. The project is an investment management application in early development stages, currently implementing authentication functionality with Thymeleaf templates.

## Build System

**Build Tool**: Gradle with Wrapper

### Common Commands

```bash
# Build the project
./gradlew build

# Run the application (with live reload enabled via Spring Boot DevTools)
./gradlew bootRun

# Run tests
./gradlew test

# Run a single test class
./gradlew test --tests ClassName

# Clean build artifacts
./gradlew clean

# Check dependencies
./gradlew dependencies
```

## Architecture

**Framework**: Spring Boot 3.5.6
**Template Engine**: Thymeleaf
**Base Package**: `study.investment`

### Package Structure

- `study.investment` - Root package containing the main application class
- `study.investment.controller` - Controllers for handling HTTP requests
  - Currently contains `AuthController` for authentication-related routes

### Key Technologies

- **Spring Boot DevTools**: Enabled for automatic restart and live reload during development
- **Lombok**: Used for reducing boilerplate code (requires annotation processor)
- **Thymeleaf**: Server-side template engine with caching disabled in development

### Application Configuration

Configuration is in `src/main/resources/application.yml`:
- Thymeleaf caching is disabled for development
- Spring Boot DevTools restart is enabled
- Application name: "investment"

### Static Resources

- Templates: `src/main/resources/templates/`
- Static assets (CSS, JS): `src/main/resources/static/`

### Current Implementation

The application currently has a basic login page accessible at `/auth/login` that renders the `login.html` Thymeleaf template with custom CSS styling.

## Development Notes

- Java toolchain is set to Java 21
- Spring Boot DevTools provides automatic restart when classpath files change
- Lombok annotations are processed at compile time via `annotationProcessor`
- 이 프로젝트의 목적은 Thymeleaf와 CSS를 학습하는 것이야. 특히 나는 CSS에 미숙한 사람이기 때문에 네가 강사 역할이 되어 구현한 CSS코드에 관한 개념에 대해 간략히 설명해줘야해.
- CSS로 UI를 구성할 때에는 여러 해상도를 가진 디바이스에 대응할 수 있도록 코드를 작성해야 하고 이와 관련된 개념을 나한테 간략히 소개해줘야해.
- 모바일 우선 UI로 구성해줘.