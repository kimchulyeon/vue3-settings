# vue-settings

## __Vue CLI__
https://cli.vuejs.org/guide/installation.html
```
📌 vue create 프로젝트명
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

### [4] 그 외 설정
---
- prettier 확장프로그램 : 작업영역 사용 안함 설정
- format on save : 체크해제
