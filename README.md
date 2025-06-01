# Hot Reload with Air

Air is a live reload tool for Go applications. It watches for changes in your code and automatically restarts your application.

## Installation

1. **Install Air**  
   Use the following command to install Air:

```bash
go install github.com/cosmtrek/air@latest
```

Ensure that `$GOPATH/bin` is in your `PATH` so you can run the `air` command.

2. **Verify Installation**  
   Run the following command to check if Air is installed:

```bash
air -v
```

## Usage

1. **Create an Air Configuration File**  
   Generate a default `.air.toml` configuration file in your project directory:

```bash
air init
```

This file allows you to customize how Air watches your project.

2. **Run Your Project with Air**  
   Start your Go application with Air:

```bash
air
```

Air will monitor your project for changes and automatically reload the application.

## Tips

- Customize the `.air.toml` file to exclude unnecessary directories or files from being watched.
- Use Air during development to speed up your workflow.

For more details, visit the [Air GitHub repository](https://github.com/cosmtrek/air).

# How to Use Direnv

Direnv is a tool that helps manage environment variables automatically based on the directory you are working in. Here are the steps to use Direnv:

## Installation

1. **Install Direnv**  
   Use the package manager appropriate for your operating system:

- **Ubuntu/Debian**:
  ```bash
  sudo apt install direnv
  ```
- **MacOS**:
  ```bash
  brew install direnv
  ```
- **Windows**:  
  Use WSL or download it from the [official Direnv website](https://direnv.net/).

2. **Integrate with Shell**  
   Add the following line to your shell configuration file:

- **Bash** (`~/.bashrc`):
  ```bash
  eval "$(direnv hook bash)"
  ```
- **Zsh** (`~/.zshrc`):
  ```bash
  eval "$(direnv hook zsh)"
  ```
- **Fish** (`~/.config/fish/config.fish`):
  ```fish
  eval (direnv hook fish)
  ```

Then, reload your shell:

```bash
source ~/.bashrc  # or ~/.zshrc, depending on your shell
```

## Usage

1. **Create a `.envrc` File**  
   Inside your project directory, create a `.envrc` file and add the required environment variables. Example:

```bash
export DATABASE_URL="postgres://user:password@localhost:5432/dbname"
export API_KEY="your-api-key"
```

2. **Allow the `.envrc` File**  
   After creating or modifying the `.envrc` file, run the following command to allow Direnv to load it:

```bash
direnv allow
```

3. **Automatically Load Variables**  
   Every time you enter the directory, Direnv will automatically load the variables from `.envrc`.

## Tips

- Use `.envrc` for variables that are only relevant to a specific project.
- Don't forget to add `.envrc` to `.gitignore` if it contains sensitive information.

For more information, visit the [official Direnv documentation](https://direnv.net/).
