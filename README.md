# Terminal Setups

A basic VSCode extension to open up multiple terminals from a configuration.

[Marketplace](https://marketplace.visualstudio.com/items?itemName=linderjohan.terminal-setups)

### Features

Command palette

![Command palette](images/command-palette.png)

Choose setup

![Setups](images/setups.png)

Done

![Terminals](images/terminals.png)

### Usage

A terminal setup:

```jsonc
{
	"name": "<Setup name>",
	"terminals": [
		{
			"cmd": "<Command sent to the terminal on startup>",
			"color": "<Color>",
			"icon": "<Icon>",
			"name": "<Name>"
		},
		{
			// ... another terminal
		}
	]
}
```

Colors: [Integrated terminal colors](https://code.visualstudio.com/api/references/theme-color#integrated-terminal-colors)

Icons: [Built in icons](https://code.visualstudio.com/api/references/icons-in-labels#icon-listing)

Example:

```jsonc
//settings.json

"terminalSetups": {
		"setups": [
			{
				"name": "Project Z",
				"terminals" : [
					{
						"cmd": "git status",
						"color": "terminal.ansiRed",
						"icon": "github-inverted",
						"name": "git",
					},
					{
						"color": "terminal.ansiCyan",
						"icon": "zap",
						"name": "app",
					},
				]
			},
			{
				"name": "Project X",
				"terminals" : [
					{
						"cmd": "git status",
						"color": "terminal.ansiYellow",
						"icon": "github-inverted",
						"name": "git",
					},
					{
						"color": "terminal.ansiRed",
						"icon": "database",
						"name": "mysql",
					},
					{
						"color": "terminal.ansiGreen",
						"icon": "zap",
						"name": "api",
					},
					{
						"color": "terminal.ansiCyan",
						"icon": "zap",
						"name": "ui",
					},
					{
						"cmd": "Good morning!",
						"color": "terminal.ansiWhite",
						"icon": "terminal",
						"name": "bash",
					},
				]
			}
		]
	},
```
