# Tech Stack Configuration

## Frontend Stack
```rules
frontend: {
  framework: "SvelteKit 5",
  language: "TypeScript",
  styling: {
    framework: "Tailwind CSS",
    components: "Shadcn UI"
  },
  features: {
    ssr: true,
    runes: true,
    state_machines: true
  }
}
```

## Backend Stack
```rules
backend: {
  core: {
    language: "Golang",
    framework: "Encore"
  },
  database: {
    main: "PocketBase/LibSQL",
    cache: "Redis"
  },
  features: {
    microservices: true,
    grpc: true,
    rest: true
  }
}
```

## Development Standards
### TypeScript Configuration
```rules
typescript: {
  strict: true,
  preferences: {
    use_interfaces: true,
    explicit_types: true,
    error_handling: "comprehensive"
  },
  features: {
    strict_null_checks: true,
    no_implicit_any: true,
    strict_function_types: true
  }
}
```

### Project Structure
```rules
structure: {
  frontend: {
    components: "src/components",
    lib: "src/lib",
    routes: "src/routes",
    state: "src/state",
    types: "src/types"
  },
  backend: {
    api: "src/api",
    core: "src/core",
    db: "src/db",
    cache: "src/cache",
    auth: "src/auth"
  }
}
```

### Git Conventions
```rules
git: {
  commit_types: {
    feat: "New features",
    fix: "Bug fixes",
    perf: "Performance",
    docs: "Documentation",
    style: "Formatting",
    refactor: "Code changes",
    test: "Testing",
    chore: "Maintenance"
  },
  branch_naming: {
    feature: "feature/*",
    bugfix: "bugfix/*",
    hotfix: "hotfix/*"
  }
}
```

### Testing Framework
```rules
testing: {
  unit: {
    scope: "utilities",
    framework: "vitest"
  },
  integration: {
    scope: "api",
    framework: "supertest"
  },
  e2e: {
    scope: "critical_flows",
    framework: "playwright"
  },
  security: {
    scope: "penetration",
    tools: ["snyk", "owasp"]
  },
  performance: {
    scope: "benchmarks",
    tools: ["lighthouse", "k6"]
  }
}
```

### Development Tools
```rules
tools: {
  ide: "VSCode",
  extensions: [
    "svelte",
    "typescript",
    "eslint",
    "prettier"
  ],
  linting: {
    javascript: "eslint",
    style: "stylelint",
    commit: "commitlint"
  },
  formatting: {
    code: "prettier",
    style: "prettier-plugin-tailwindcss"
  }
}
```

### Performance Optimization
```rules
performance: {
  frontend: {
    bundling: {
      code_splitting: true,
      tree_shaking: true,
      lazy_loading: true
    },
    caching: {
      service_worker: true,
      static_assets: true,
      api_responses: true
    },
    monitoring: {
      web_vitals: true,
      error_tracking: true,
      performance_metrics: true
    }
  },
  
  backend: {
    caching: {
      redis: {
        data_types: ["string", "hash", "list", "set"],
        persistence: true,
        eviction: "lru"
      },
      memory: {
        type: "in_memory",
        size: "adaptive",
        cleanup: "smart"
      }
    },
    optimization: {
      query_caching: true,
      connection_pooling: true,
      request_batching: true
    }
  }
}
```

### Security Configuration
```rules
security: {
  authentication: {
    jwt: {
      algorithm: "RS256",
      expiry: "24h",
      refresh: true
    },
    oauth: {
      providers: ["github", "google"],
      scope: ["email", "profile"]
    }
  },
  
  authorization: {
    rbac: true,
    permissions: {
      granular: true,
      hierarchical: true
    }
  },
  
  data_protection: {
    encryption: {
      at_rest: true,
      in_transit: true,
      end_to_end: true
    },
    sanitization: {
      input: true,
      output: true
    }
  }
}
```

### Development Environment
```rules
environment: {
  local: {
    containers: {
      docker: true,
      compose: true
    },
    databases: {
      development: "sqlite",
      testing: "postgres"
    }
  },
  
  ci_cd: {
    github_actions: {
      test: true,
      build: true,
      deploy: true
    },
    quality: {
      sonarqube: true,
      code_coverage: true
    }
  },
  
  monitoring: {
    logging: {
      structured: true,
      centralized: true
    },
    metrics: {
      system: true,
      business: true
    },
    alerting: {
      threshold: true,
      anomaly: true
    }
  }
}
```

### API Standards
```rules
api: {
  rest: {
    versioning: true,
    documentation: "openapi",
    response_format: {
      consistent: true,
      typed: true
    }
  },
  
  grpc: {
    protocols: ["http2", "websocket"],
    streaming: {
      bidirectional: true,
      server_side: true
    }
  },
  
  graphql: {
    schema: {
      typed: true,
      documented: true
    },
    features: {
      subscriptions: true,
      batching: true
    }
  }
}
```

### Technology Stack Rules

## Frontend Framework (Svelte 5)

### State Management
- State Organization:
  - Folder: `state/`
  - File naming: `${state_name}.svelte`
  - Grouping enabled
  - Validation required
- Context Usage:
  - Use setContext/getContext
  - Global scope
  - Validation required

### Feature Management
- Unready Features:
  - Alert popup required
  - Modal style with dismiss
  - Message: "Feature in development"
  - Tag: `// TODO: Feature WIP`

### UI Requirements
- Responsive Design:
  - Required for all components
  - Breakpoints: mobile, tablet, desktop
  - Testing and validation required
- Asset Management:
  - Dummy images from:
    - dicebear.com
    - lucide.dev/icons
  - Format checking enabled
  - Non-webp warning with comment
- Rendering:
  - Prevent unnecessary rerenders
  - Client/Server tagging
  - Performance checks
  - Optimal cache strategy

### Testing Requirements
- API Cache Testing:
  - Response caching
  - Request deduplication
  - Cache invalidation
- UI Rerender Testing:
  - Component check
  - Update tracking
  - Prevent cascading updates
- Behavior Testing:
  - Unwanted behavior detection
  - Error handling
  - Edge cases

## Development Standards

### Code Improvement
- Detection Enabled:
  - Performance
  - Effectiveness
  - Security
  - Maintainability
- TODO tags with reasons required

### Naming Conventions
- Functions: camelCase
- States: camelCase
- Variables: camelCase
- Constants: UPPERCASE
- Files: kebab-case
- Folders: kebab-case
- Validation required

### Data Management
- Dummy Data:
  - Minimum 5 examples
  - Realistic values
  - Comment: `// dummy data`
  - Validation required

## Documentation Structure

### Required Files
- README.md
- API.md
- COMPONENTS.md

### Content Requirements
- Function Documentation:
  - Name and purpose
  - Dependencies
  - Side effects
- API Documentation:
  - Endpoints and methods
  - Parameters
  - Response formats
- Component Documentation:
  - Props and events
  - Slots
  - Dependencies

### Maintenance
- Update on change
- Version tracking
- Review required
