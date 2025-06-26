# ontolux Tech Radar

[![Build Status](https://github.com/Neofonie/tech-radar/workflows/deploy/badge.svg)](https://github.com/Neofonie/tech-radar/actions)

![Screenshot](../main/public/screenshots/ontoluxtechradar.png?raw=true)

# Motivation

At [Ontolux](https://ontolux.de), we maintain a Tech Radar to help our engineering teams align on technology choices for our specialized focus on **NLP, Machine Learning, LLM Integration, and Search Technologies**. It is based on the [pioneering work by ThoughtWorks](https://www.thoughtworks.com/radar) and [Zalando](https://zalando.github.io/tech-radar/).

This repository is a ES6 refactoring of the original Neofonie Tech Radar, customized for Ontolux's technology stack.

## Our Tech Radar Quadrants

Our Tech Radar is organized into four specialized quadrants:

1. **Infrastructure & MLOps** - DevOps, Cloud Services, and MLOps tools
2. **Search, Retrieval & Data** - Search technologies, vector databases, and data processing
3. **AI, ML & NLP** - Machine Learning frameworks, NLP tools, and AI technologies
4. **(Large) Language Models** - Various (Large) Language Models

## Usage

#### 1. install

```
git clone https://github.com/neofonie-research/tech-radar.git
cd tech-radar
npm install
```

#### 2. start local dev server

Open the url: **[http://localhost:8080](http://localhost:8080)**

```
npm start
```

#### 3. make build

Create some distribution files in: `/dist` and copy it to `/docs`  
At the moment - it is a must. Later we will use TravisCI. Then this step is obsolete.

```
npm run build
```

The Difference between the `/dist` and the `/docs` folder are the different url paths in the css files.
The `/docs` folder is only for github pages.

## The Data
- must be served by a server
- will be loaded as fetch request
- is mainly located in `public/radar/` - edit these files
- `public/radar/` will be copied to the `dist/` and `docs/` folder on a `npm run build`
- the all over data index is `public/radar/index.json`
- any data group is represented by a folder like `public/radar/ontolux/`
- in this folder there is a config file for the group `public/radar/config.json`
- any group can have unlimited datasets.
- the dataset filename without the file extension must be an entry in `public/radar/index.json` in `"versions": ["2025.06"]`


## The Theme
- take a look in the webpack config, there are multiple entry points for the css
- a theme override the default css. it is a second css file that will be injected
- any theme css has a root scss file like `src/scss/dark.scss` or `src/scss/forest.scss`

## License

```
The MIT License (MIT)

Copyright (c) 2022 Neofonie GmbH

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```
