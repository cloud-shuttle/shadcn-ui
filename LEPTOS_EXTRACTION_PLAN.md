# 🚀 Leptos shadcn/ui Extraction Plan

## Overview
Create a new, focused repository `leptos-shadcn-ui` containing only Leptos components and essential infrastructure, removing Yew dependencies and multi-framework abstractions.

## 📁 New Repository Structure

```
leptos-shadcn-ui/
├── packages/
│   ├── leptos/              # All 47 Leptos components
│   ├── shadcn/              # Leptos-focused CLI tool
│   ├── registry/            # Component registry (Leptos-only)
│   ├── component-generator/ # Code generation (Leptos templates)
│   ├── test-utils/          # Testing utilities
│   └── utils/               # Shared utilities
├── examples/                 # Leptos-specific examples
├── docs/                    # Leptos-focused documentation
├── tests/                   # Test infrastructure
├── .github/                 # GitHub workflows
├── scripts/                 # Build and development scripts
├── flake.nix               # Nix development environment
├── package.json            # Node.js dependencies
├── Cargo.toml              # Rust workspace
└── README.md               # Leptos-focused documentation
```

## 🎯 Benefits of This Approach

### 1. **Focused Value Proposition**
- "The definitive UI library for Leptos applications"
- No confusion about framework support
- Clear positioning in the Leptos ecosystem

### 2. **Simplified Maintenance**
- Single framework focus
- Easier dependency management
- Faster iteration cycles

### 3. **Better Community Fit**
- Leptos developers will immediately understand the value
- Can integrate with Leptos conventions and tooling
- Potential for official Leptos ecosystem status

### 4. **Business Opportunities**
- Premium support for Leptos teams
- Consulting on Leptos UI implementation
- Training and workshops

## 🚀 Launch Strategy

### Week 1: Repository Setup
- Create new repository
- Extract Leptos components
- Update configuration files

### Week 2: Documentation & Testing
- Update all documentation
- Verify all tests pass
- Create Leptos-specific examples

### Week 3: Launch Preparation
- Final testing and validation
- Prepare launch announcement
- Update package metadata

### Week 4: Launch
- Publish to crates.io
- Announce on Leptos community channels
- Begin community building

## 🔧 Technical Considerations

### 1. **Package Naming**
- Consider renaming packages to `leptos-shadcn-ui-{component}`
- This makes the Leptos focus clear in dependency lists

### 2. **Version Management**
- Start fresh with version 0.1.0
- This gives you a clean versioning slate

### 3. **Migration Path**
- Provide migration guide for existing users
- Consider maintaining compatibility layer if needed

---

*This document will be updated as the extraction progresses.*
