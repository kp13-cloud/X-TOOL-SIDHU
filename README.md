X-TOOL-SIDHU

A modern Python 3 command-line tool for organizing, discovering, and viewing information about security and system tools.

X-TOOL-SIDHU provides a simple CLI with tool categories, descriptions, installation suggestions, and an interactive menu.

Features

- Python 3.10+ CLI
- Termux/Android support
- Linux support
- Tool listing by category
- Tool information and descriptions
- Platform-aware installation suggestions
- Interactive terminal menu
- JSON-based tool configuration
- Lightweight project structure

Requirements

- Python 3.10 or newer
- Linux or Termux
- Git

Check your Python version:

python3 --version

Installation

Clone the repository:

git clone https://github.com/kp13-cloud/X-TOOL-SIDHU.git

Enter the project directory:

cd X-TOOL-SIDHU

Usage

Show help

python3 -m darkfly.cli --help

List available tools

python3 -m darkfly.cli list

This displays the tools currently defined in:

darkfly_tools.json

Show information about a tool

First list the available tools:

python3 -m darkfly.cli list

Then use the tool ID:

python3 -m darkfly.cli info <tool_id>

Example:

python3 -m darkfly.cli info nmap

The "info" command can display:

- Tool ID
- Tool name
- Category
- Description
- Recommended installation commands
- Alternative installation commands

The CLI detects whether it is running under Termux or Linux and selects appropriate installation suggestions when they are available.

Interactive menu

Run:

python3 -m darkfly.cli menu

The menu allows you to select a tool by number and view its information.

Enter:

q

to quit the menu.

Configuration

Tools are defined in:

darkfly_tools.json

The configuration is organized into categories.

A tool can contain:

- "id"
- "name"
- "description"
- "category"
- "install_commands"

Example structure:

{
  "categories": [
    {
      "id": "examples",
      "name": "Example Tools",
      "tools": [
        {
          "id": "example",
          "name": "Example Tool",
          "description": "Example tool description.",
          "install_commands": [
            "sudo apt install example",
            "pkg install example"
          ]
        }
      ]
    }
  ]
}

Project Structure

X-TOOL-SIDHU/
├── darkfly/
│   ├── __init__.py
│   └── cli.py
├── darkfly_tools.json
├── install.py
├── lib/
├── .module/
├── tests/
├── pyproject.toml
├── LICENSE
└── README.md

Main Commands

Command| Purpose
"python3 -m darkfly.cli --help"| Show help
"python3 -m darkfly.cli list"| List available tools
"python3 -m darkfly.cli info <tool_id>"| Show tool information
"python3 -m darkfly.cli menu"| Open interactive menu

Python Package Installation

The project also provides a Python package configuration through "pyproject.toml".

For a local editable installation:

python3 -m pip install -e .

After installation, the configured CLI entry point is:

DarkFly5

You can then use:

DarkFly5 --help

DarkFly5 list

DarkFly5 info <tool_id>

DarkFly5 menu

Development

Install development dependencies:

python3 -m pip install -e ".[dev]"

Run the test suite:

pytest

Security and Responsible Use

X-TOOL-SIDHU is intended for security education, research, system administration, and authorized testing.

Only use security-related tools against systems, networks, applications, or devices that you own or have explicit permission to test.

Do not use this project to gain unauthorized access, disrupt services, steal information, or violate applicable laws.

The project provides information and launcher functionality; users are responsible for how they use the tools and commands available through their configuration.

License

This project is distributed under the GNU General Public License v3.0 or later.

See ""LICENSE"" (LICENSE) for the full license text.

Author

KRISHAN SINGH SIDHU

GitHub:

https://github.com/kp13-cloud

Project:

https://github.com/kp13-cloud/X-TOOL-SIDHU
