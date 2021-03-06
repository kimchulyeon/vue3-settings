# vue-settings

## __Vue CLI__
https://cli.vuejs.org/guide/installation.html
```
π vue create νλ‘μ νΈλͺ
```
### [1] .eslintrc.js
---
```
module.exports = {
	root: true,
	env: {
		node: true,
	},
	extends: ['plugin:vue/vue3-essential', 'eslint:recommended', 'plugin:prettier/recommended'],
	parserOptions: {
		parser: '@babel/eslint-parser',
	},
	rules: {
		'no-console': process.env.NODE_ENV === 'production' ? 'warn' : 'off',
		'no-debugger': process.env.NODE_ENV === 'production' ? 'warn' : 'off',
		'vue/multi-word-component-names': 0,
		'prettier/prettier': [
			'error',
			{
				singleQuote: true,
				semi: false,
				useTabs: true,
				tabWidth: 2,
				trailingComma: 'all',
				printWidth: 120,
				bracketSpacing: true,
				arrowParens: 'avoid',
			},
		],
	},
	overrides: [
		{
			files: ['**/__tests__/*.{j,t}s?(x)', '**/tests/unit/**/*.spec.{j,t}s?(x)'],
			env: {
				jest: true,
			},
		},
	],
}

```

### [2] vue.config.js
---
```
const { defineConfig } = require('@vue/cli-service')
module.exports = defineConfig({
	transpileDependencies: true,
	devServer: {
		client: {
			overlay: false,
		},
	},
})

```

### [3] jsconfig.json
```
{
  "compilerOptions": {
    "target": "es5",
    "module": "esnext",
    "baseUrl": ".",
    "moduleResolution": "node",
    "paths": {
      "~/*": [
        "./*"
      ],
      "@/*": [
        "./src/*"
      ],
    },
    "lib": [
      "esnext",
      "dom",
      "dom.iterable",
      "scripthost"
    ],
  },
  "exclude": [
    "node_modules",
    "dist"
  ]
}

```

### [4] κ·Έ μΈ μ€μ 
---
- prettier νμ₯νλ‘κ·Έλ¨ : μμμμ­ μ¬μ© μν¨ μ€μ 
- format on save : μ²΄ν¬ν΄μ 
