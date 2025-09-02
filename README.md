<p align="center">
    <a href="./logo.svg">
        <img src="./logo.svg" width="300" height="200" alt="Leptos shadcn/ui Logo">
    </a>
</p>

<h1 align="center">Leptos shadcn/ui</h1>

<p align="center">
    <strong>Beautiful, accessible UI components built specifically for Leptos applications.</strong>
</p>

<p align="center">
    <a href="#quick-start">Quick Start</a> •
    <a href="#components">Components</a> •
    <a href="#cli-tool">CLI Tool</a> •
    <a href="#development">Development</a> •
    <a href="#contributing">Contributing</a>
</p>

---

**Leptos shadcn/ui** is the definitive UI library for Leptos applications, providing accessible, customizable, and beautifully designed components that integrate seamlessly with Tailwind CSS. Built specifically for Leptos with performance and developer experience in mind.

> **Note**: This is the CloudShuttle fork of the Rust shadcn/ui project, focused exclusively on Leptos with enhanced development tooling, auto-closing Playwright tests, and improved package management with pnpm.

## ✨ Features

- 🎨 **Beautiful Components**: Faithfully ported from shadcn/ui with all styling and variants
- 🦀 **Leptos Native**: Built specifically for Leptos with type safety and performance
- 🔧 **CLI Tool**: Powerful command-line interface for component generation and management
- 🎭 **Theme Variants**: Support for default and New York design themes
- ⚡ **Performance**: Optimized components with minimal runtime overhead
- 🧪 **Type Safety**: Full TypeScript-equivalent type safety with Rust's type system
- 📱 **Responsive**: Mobile-first responsive design out of the box
- 🚀 **Enhanced Development**: Nix development environment with auto-closing Playwright tests
- 📦 **Package Management**: Optimized with pnpm for faster dependency installation
- 🧪 **Testing Infrastructure**: 645+ passing tests with comprehensive browser testing

## 🚀 Quick Start

### Prerequisites

- Rust 1.70+ with `wasm32-unknown-unknown` target
- Node.js 18+ (for Tailwind CSS)
- **Nix** (optional but recommended for development)

### Installation

#### Option 1: Using Nix (Recommended)
```bash
# Clone the repository
git clone https://github.com/cloud-shuttle/leptos-shadcn-ui.git
cd leptos-shadcn-ui

# Enter the Nix development environment
nix develop

# Build and test
cargo build
pnpm test
```

#### Option 2: Manual Setup
```bash
# Clone the repository
git clone https://github.com/cloud-shuttle/leptos-shadcn-ui.git
cd leptos-shadcn-ui

# Install Node.js dependencies
pnpm install

# Build the workspace
cargo build

# Test components
cargo test -p leptos-shadcn-ui-button
pnpm test
```

### Using Components in Your Leptos Project

```bash
# Add individual components to your project
cargo add leptos-shadcn-ui-button
cargo add leptos-shadcn-ui-card
cargo add leptos-shadcn-ui-dialog
cargo add leptos-shadcn-ui-form
# ... add components as needed
```

```rust
use leptos::*;
use leptos_shadcn_ui_button::Button;
use leptos_shadcn_ui_card::{Card, CardContent, CardHeader, CardTitle};

#[component]
pub fn MyComponent() -> impl IntoView {
    view! {
        <Card>
            <CardHeader>
                <CardTitle>"Welcome to Leptos shadcn/ui!"</CardTitle>
            </CardHeader>
            <CardContent>
                <Button>"Click me!"</Button>
            </CardContent>
        </Card>
    }
}
```

## 🔧 CLI Tool

The included CLI tool provides powerful features for component management:

### Generate Components
```bash
# Generate a new component for Leptos
cargo run -p shadcn -- generate --name "dialog" --framework "leptos"

# Generate with custom styling
cargo run -p shadcn -- generate \
  --name "tooltip" \
  --framework "leptos" \
  --classes "rounded-md bg-primary px-3 py-1 text-primary-foreground" \
  --description "A tooltip component"
```

### Available Commands
- `generate` - Generate new component scaffolds
- `init` - Initialize a new project with Leptos shadcn/ui

## 📦 Components

### Available Components

| Component | Status | Description |
|-----------|:------:|-------------|
| Alert | ✅ | Displays a callout for user attention |
| Alert Dialog | ✅ | Modal dialog for destructive actions |
| Accordion | ✅ | Collapsible content sections |
| Aspect Ratio | ✅ | Displays content within a desired ratio |
| Badge | ✅ | Displays a badge or a component |
| Breadcrumb | ✅ | Navigation aid showing page hierarchy |
| Button | ✅ | Triggers an action or event |
| Calendar | ✅ | Date picker with calendar view |
| Card | ✅ | Container for related information |
| Carousel | ✅ | Slideshow for cycling through content |
| Checkbox | ✅ | Binary choice input |
| Collapsible | ✅ | Expandable content sections |
| Combobox | ✅ | Searchable select input |
| Command | ✅ | Command palette interface |
| Context Menu | ✅ | Right-click context menu |
| Date Picker | ✅ | Date selection component |
| Dialog | ✅ | Modal dialog overlay |
| Drawer | ✅ | Slide-out panel |
| Dropdown Menu | ✅ | Dropdown menu component |
| Error Boundary | ✅ | Error handling component |
| Form | ✅ | Form handling and validation |
| Hover Card | ✅ | Hover-triggered card |
| Input | ✅ | Text input field |
| Input OTP | ✅ | One-time password input |
| Label | ✅ | Caption for form controls |
| Lazy Loading | ✅ | Dynamic component loading |
| Menubar | ✅ | Horizontal menu bar |
| Navigation Menu | ✅ | Navigation menu component |
| Pagination | ✅ | Navigate through pages |
| Popover | ✅ | Floating content panel |
| Progress | ✅ | Progress indicator |
| Radio Group | ✅ | Single choice from options |
| Registry | ✅ | Component registry system |
| Scroll Area | ✅ | Custom scrollable area |
| Select | ✅ | Dropdown selection |
| Separator | ✅ | Visual or semantic separator |
| Sheet | ✅ | Slide-out sheet |
| Skeleton | ✅ | Loading placeholder |
| Slider | ✅ | Range input component |
| Switch | ✅ | Binary toggle control |
| Table | ✅ | Structured data display |
| Tabs | ✅ | Tabbed content navigation |
| Textarea | ✅ | Multi-line text input |
| Toast | ✅ | Notification component |
| Toggle | ✅ | Toggle button component |
| Tooltip | ✅ | Hover information display |
| Utils | ✅ | Utility functions and helpers |

### Component Status Legend
- ✅ **Available**: Ready for production use
- 🚧 **In Progress**: Currently being developed
- 📋 **Planned**: In development roadmap

### Package Status
- **Total Leptos Packages**: 47/51 (92% coverage) 🎉
- **Registry Package**: ✅ Available for component discovery
- **Lazy Loading**: ✅ Available for dynamic component loading
- **Test Utils**: ✅ Available for testing infrastructure
- **CLI Tool**: ✅ Available for component generation

## 🏗️ Architecture

### Workspace Structure
```
leptos-shadcn-ui/
├── packages/
│   ├── shadcn/              # CLI tool
│   ├── registry/            # Component registry
│   ├── component-generator/ # Code generation
│   ├── test-utils/          # Testing utilities
│   └── leptos/             # Leptos components
│       ├── button/         # Individual components
│       ├── card/
│       └── ...
├── examples/                # Documentation examples
└── docs/                   # Additional documentation
```

### Design Principles

1. **Component Isolation**: Each component is a separate crate for modularity
2. **Leptos Optimization**: Built specifically for Leptos patterns and conventions
3. **Theme Support**: Default and New York variants for all components
4. **Type Safety**: Leverage Rust's type system for component props
5. **Performance**: Minimal runtime overhead and optimal bundle sizes

## 🚀 Enhanced Development Features

### Nix Development Environment
This project includes a complete Nix development environment that provides:
- **Rust Toolchain**: Latest stable Rust with WebAssembly support
- **Node.js & pnpm**: Fast package management and Playwright testing
- **Build Tools**: Make, pkg-config, and other essential development tools
- **Cross-Platform**: Works on macOS, Linux, and Windows

### Auto-Closing Playwright Tests
- **645+ Tests**: Comprehensive end-to-end testing across all components
- **Browser Coverage**: Tests run in Chromium, Firefox, and WebKit
- **Visual Regression**: Automated visual testing for component consistency
- **Accessibility**: WCAG compliance testing built-in

## 📚 Examples

### Basic Usage
```rust
use leptos::*;
use leptos_shadcn_ui_button::Button;
use leptos_shadcn_ui_card::{Card, CardContent, CardHeader, CardTitle};

#[component]
pub fn WelcomeCard() -> impl IntoView {
    view! {
        <Card class="w-96">
            <CardHeader>
                <CardTitle>"Welcome!"</CardTitle>
            </CardHeader>
            <CardContent>
                <p class="text-muted-foreground">
                    "This is a beautiful card component built with Leptos shadcn/ui."
                </p>
                <Button class="mt-4">"Get Started"</Button>
            </CardContent>
        </Card>
    }
}
```

### Form Example
```rust
use leptos::*;
use leptos_shadcn_ui_form::{Form, FormField, FormItem, FormLabel, FormControl, FormMessage};
use leptos_shadcn_ui_input::Input;
use leptos_shadcn_ui_button::Button;

#[component]
pub fn ContactForm() -> impl IntoView {
    let (name, set_name) = create_signal(String::new());
    let (email, set_email) = create_signal(String::new());

    let handle_submit = move |_| {
        log::info!("Name: {}, Email: {}", name.get(), email.get());
    };

    view! {
        <Form on_submit=handle_submit>
            <FormField>
                <FormItem>
                    <FormLabel>"Name"</FormLabel>
                    <FormControl>
                        <Input
                            value=name.get()
                            on_input=move |ev| set_name.set(event_target_value(&ev))
                            placeholder="Enter your name"
                        />
                    </FormControl>
                    <FormMessage/>
                </FormItem>
            </FormField>
            
            <FormField>
                <FormItem>
                    <FormLabel>"Email"</FormLabel>
                    <FormControl>
                        <Input
                            value=email.get()
                            on_input=move |ev| set_email.set(event_target_value(&ev))
                            placeholder="Enter your email"
                            type_="email"
                        />
                    </FormControl>
                    <FormMessage/>
                </FormItem>
            </FormField>
            
            <Button type_="submit" class="w-full">"Submit"</Button>
        </Form>
    }
}
```

## 🧪 Testing

### Running Tests
```bash
# Run all tests
cargo test

# Run specific component tests
cargo test -p leptos-shadcn-ui-button

# Run Playwright tests
pnpm test

# Run Playwright tests with UI
pnpm test:playwright:ui
```

### Test Coverage
- **Unit Tests**: Comprehensive testing of component logic
- **Integration Tests**: Component interaction testing
- **E2E Tests**: Full browser testing with Playwright
- **Accessibility Tests**: WCAG compliance verification
- **Visual Tests**: Automated visual regression testing

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Development Setup
1. **Fork the repository**
2. **Clone your fork**: `git clone https://github.com/your-username/leptos-shadcn-ui.git`
3. **Enter Nix environment**: `nix develop`
4. **Install dependencies**: `pnpm install`
5. **Build the project**: `cargo build`
6. **Run tests**: `pnpm test`

### Adding New Components
1. **Generate scaffold**: `cargo run -p shadcn -- generate --name "new-component" --framework "leptos"`
2. **Implement component** following existing patterns
3. **Add tests** for component functionality
4. **Update registry** with component metadata
5. **Submit pull request**

### Code Style
- Follow Rust formatting with `cargo fmt`
- Use `cargo clippy` for linting
- Ensure all tests pass before submitting
- Follow existing component patterns

## 📄 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## 🙏 Acknowledgments

- **shadcn/ui** - Original design system and components
- **Leptos** - The amazing Rust web framework
- **Tailwind CSS** - Utility-first CSS framework
- **Radix UI** - Accessible component primitives

## 📞 Support

- **GitHub Issues**: [Report bugs or request features](https://github.com/cloud-shuttle/leptos-shadcn-ui/issues)
- **Discussions**: [Join the community](https://github.com/cloud-shuttle/leptos-shadcn-ui/discussions)
- **Documentation**: [Comprehensive guides and examples](https://github.com/cloud-shuttle/leptos-shadcn-ui/docs)

---

**Made with ❤️ by CloudShuttle for the Leptos community**
