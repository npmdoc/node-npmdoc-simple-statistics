# api documentation for  [simple-statistics (v3.0.0)](https://github.com/simple-statistics/simple-statistics#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-simple-statistics.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-simple-statistics) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-simple-statistics.svg)](https://travis-ci.org/npmdoc/node-npmdoc-simple-statistics)
#### Simple Statistics

[![NPM](https://nodei.co/npm/simple-statistics.png?downloads=true)](https://www.npmjs.com/package/simple-statistics)

[![apidoc](https://npmdoc.github.io/node-npmdoc-simple-statistics/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-simple-statistics_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-simple-statistics/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-simple-statistics/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-simple-statistics/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Tom MacWright",
        "email": "tom@macwright.org",
        "url": "http://macwright.org/"
    },
    "bugs": {
        "url": "https://github.com/simple-statistics/simple-statistics/issues"
    },
    "config": {
        "commitizen": {
            "path": "./node_modules/cz-conventional-changelog"
        }
    },
    "dependencies": {},
    "description": "Simple Statistics",
    "devDependencies": {
        "are-we-flow-yet": "^1.0.0",
        "browserify": "^14.1.0",
        "bundle-collapser": "^1.0.0",
        "cz-conventional-changelog": "^1.2.0",
        "eslint": "^3.8.1",
        "exorcist": "^0.4.0",
        "flow-bin": "^0.39.0",
        "jsdoctest": "1.7.0",
        "mocha": "3.2.0",
        "random-js": "^1.0.4",
        "standard-changelog": "^0.0.1",
        "tap": "^10.1.1",
        "uglify-js": "^2.6.2"
    },
    "directories": {},
    "dist": {
        "shasum": "54b66d2655b2a21125600dc0d02be764a3a73a3d",
        "tarball": "https://registry.npmjs.org/simple-statistics/-/simple-statistics-3.0.0.tgz"
    },
    "engines": {
        "node": "*"
    },
    "files": [
        "bower.json",
        "src",
        "dist"
    ],
    "gitHead": "9bb0cda4c8b64bbc1924c7270f6beeee0be1411a",
    "homepage": "https://github.com/simple-statistics/simple-statistics#readme",
    "keywords": [
        "descriptive",
        "linear",
        "math",
        "probability",
        "regression",
        "statistics"
    ],
    "license": "ISC",
    "main": "index.js",
    "maintainers": [
        {
            "name": "tmcw",
            "email": "macwright@gmail.com"
        }
    ],
    "name": "simple-statistics",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/simple-statistics/simple-statistics.git"
    },
    "scripts": {
        "build": "npm run bundle && npm run minify",
        "bundle": "mkdir -p dist && browserify -p bundle-collapser/plugin -s ss index.js --debug | exorcist dist/simple-statistics.js.map > dist/simple-statistics.js",
        "changelog": "standard-changelog -i CHANGELOG.md --overwrite",
        "jsdoctest": "mocha --require jsdoctest index.js",
        "minify": "uglifyjs dist/simple-statistics.js -c -m --in-source-map=dist/simple-statistics.js.map --source-map=dist/simple-statistics.min.js.map -o dist/simple-statistics.min.js",
        "prepublish": "npm run build && ./scripts/update_readme.js",
        "test": "are-we-flow-yet src && flow check src && eslint index.js src/*.js test/*.js && tap --coverage test/*.js && npm run jsdoctest",
        "test-sauce": "node scripts/browser_test.js"
    },
    "version": "3.0.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module simple-statistics](#apidoc.module.simple-statistics)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>addToMean (mean, n, newValue)](#apidoc.element.simple-statistics.addToMean)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>average (x)](#apidoc.element.simple-statistics.average)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>bayesian ()](#apidoc.element.simple-statistics.bayesian)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>bernoulliDistribution (p)](#apidoc.element.simple-statistics.bernoulliDistribution)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>binomialDistribution ( trials, probability)](#apidoc.element.simple-statistics.binomialDistribution)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>bisect ( func/*: (x: any)](#apidoc.element.simple-statistics.bisect)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>chiSquaredGoodnessOfFit ( data, distributionType, significance)](#apidoc.element.simple-statistics.chiSquaredGoodnessOfFit)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>chunk (x, chunkSize)](#apidoc.element.simple-statistics.chunk)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>ckmeans (x, nClusters)](#apidoc.element.simple-statistics.ckmeans)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>combinations (x, k)](#apidoc.element.simple-statistics.combinations)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>combinationsReplacement ( x, k)](#apidoc.element.simple-statistics.combinationsReplacement)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>combineMeans (mean1, n1, mean2, n2)](#apidoc.element.simple-statistics.combineMeans)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>combineVariances ( variance1, mean1, n1, variance2, mean2, n2)](#apidoc.element.simple-statistics.combineVariances)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>cumulativeStdNormalProbability (z)](#apidoc.element.simple-statistics.cumulativeStdNormalProbability)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>equalIntervalBreaks (x, nClasses)](#apidoc.element.simple-statistics.equalIntervalBreaks)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>erf (x)](#apidoc.element.simple-statistics.erf)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>errorFunction (x)](#apidoc.element.simple-statistics.errorFunction)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>factorial (n)](#apidoc.element.simple-statistics.factorial)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>geometricMean (x)](#apidoc.element.simple-statistics.geometricMean)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>harmonicMean (x)](#apidoc.element.simple-statistics.harmonicMean)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>interquartileRange (x)](#apidoc.element.simple-statistics.interquartileRange)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>inverseErrorFunction (x)](#apidoc.element.simple-statistics.inverseErrorFunction)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>iqr (x)](#apidoc.element.simple-statistics.iqr)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>linearRegression (data)](#apidoc.element.simple-statistics.linearRegression)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>linearRegressionLine (mb)](#apidoc.element.simple-statistics.linearRegressionLine)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>mad (x)](#apidoc.element.simple-statistics.mad)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>max (x)](#apidoc.element.simple-statistics.max)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>maxSorted (x)](#apidoc.element.simple-statistics.maxSorted)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>mean (x)](#apidoc.element.simple-statistics.mean)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>median (x)](#apidoc.element.simple-statistics.median)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>medianAbsoluteDeviation (x)](#apidoc.element.simple-statistics.medianAbsoluteDeviation)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>medianSorted (sorted)](#apidoc.element.simple-statistics.medianSorted)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>min (x)](#apidoc.element.simple-statistics.min)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>minSorted (x)](#apidoc.element.simple-statistics.minSorted)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>mixin (ss, array)](#apidoc.element.simple-statistics.mixin)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>mode (x)](#apidoc.element.simple-statistics.mode)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>modeFast (x)](#apidoc.element.simple-statistics.modeFast)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>modeSorted (sorted)](#apidoc.element.simple-statistics.modeSorted)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>perceptron ()](#apidoc.element.simple-statistics.perceptron)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>permutationsHeap (elements)](#apidoc.element.simple-statistics.permutationsHeap)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>poissonDistribution (lambda)](#apidoc.element.simple-statistics.poissonDistribution)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>probit (p)](#apidoc.element.simple-statistics.probit)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>product (x)](#apidoc.element.simple-statistics.product)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>quantile (x, p)](#apidoc.element.simple-statistics.quantile)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>quantileSorted (x, p)](#apidoc.element.simple-statistics.quantileSorted)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>rSquared (x, func)](#apidoc.element.simple-statistics.rSquared)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>rms (x)](#apidoc.element.simple-statistics.rms)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>rootMeanSquare (x)](#apidoc.element.simple-statistics.rootMeanSquare)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>sample ( x, n, randomSource)](#apidoc.element.simple-statistics.sample)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>sampleCorrelation (x, y)](#apidoc.element.simple-statistics.sampleCorrelation)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>sampleCovariance (x, y)](#apidoc.element.simple-statistics.sampleCovariance)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>sampleSkewness (x)](#apidoc.element.simple-statistics.sampleSkewness)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>sampleStandardDeviation (x)](#apidoc.element.simple-statistics.sampleStandardDeviation)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>sampleVariance (x)](#apidoc.element.simple-statistics.sampleVariance)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>sampleWithReplacement (x, n, randomSource)](#apidoc.element.simple-statistics.sampleWithReplacement)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>shuffle (x, randomSource)](#apidoc.element.simple-statistics.shuffle)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>shuffleInPlace (x, randomSource)](#apidoc.element.simple-statistics.shuffleInPlace)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>standardDeviation (x)](#apidoc.element.simple-statistics.standardDeviation)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>subtractFromMean (mean, n, value)](#apidoc.element.simple-statistics.subtractFromMean)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>sum (x)](#apidoc.element.simple-statistics.sum)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>sumNthPowerDeviations (x, n)](#apidoc.element.simple-statistics.sumNthPowerDeviations)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>sumSimple (x)](#apidoc.element.simple-statistics.sumSimple)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>tTest (x, expectedValue)](#apidoc.element.simple-statistics.tTest)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>tTestTwoSample ( sampleX, sampleY, difference)](#apidoc.element.simple-statistics.tTestTwoSample)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>uniqueCountSorted (x)](#apidoc.element.simple-statistics.uniqueCountSorted)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>variance (x)](#apidoc.element.simple-statistics.variance)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>zScore (x, mean, standardDeviation)](#apidoc.element.simple-statistics.zScore)
1.  number <span class="apidocSignatureSpan">simple-statistics.</span>epsilon
1.  object <span class="apidocSignatureSpan">simple-statistics.</span>bayesian.prototype
1.  object <span class="apidocSignatureSpan">simple-statistics.</span>perceptron.prototype
1.  object <span class="apidocSignatureSpan">simple-statistics.</span>standardNormalTable

#### [module simple-statistics.bayesian](#apidoc.module.simple-statistics.bayesian)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>bayesian ()](#apidoc.element.simple-statistics.bayesian.bayesian)

#### [module simple-statistics.bayesian.prototype](#apidoc.module.simple-statistics.bayesian.prototype)
1.  [function <span class="apidocSignatureSpan">simple-statistics.bayesian.prototype.</span>score (item)](#apidoc.element.simple-statistics.bayesian.prototype.score)
1.  [function <span class="apidocSignatureSpan">simple-statistics.bayesian.prototype.</span>train (item, category)](#apidoc.element.simple-statistics.bayesian.prototype.train)

#### [module simple-statistics.perceptron](#apidoc.module.simple-statistics.perceptron)
1.  [function <span class="apidocSignatureSpan">simple-statistics.</span>perceptron ()](#apidoc.element.simple-statistics.perceptron.perceptron)

#### [module simple-statistics.perceptron.prototype](#apidoc.module.simple-statistics.perceptron.prototype)
1.  [function <span class="apidocSignatureSpan">simple-statistics.perceptron.prototype.</span>predict (features)](#apidoc.element.simple-statistics.perceptron.prototype.predict)
1.  [function <span class="apidocSignatureSpan">simple-statistics.perceptron.prototype.</span>train (features, label)](#apidoc.element.simple-statistics.perceptron.prototype.train)



# <a name="apidoc.module.simple-statistics"></a>[module simple-statistics](#apidoc.module.simple-statistics)

#### <a name="apidoc.element.simple-statistics.addToMean"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>addToMean (mean, n, newValue)](#apidoc.element.simple-statistics.addToMean)
- description and source-code
```javascript
function addToMean(mean, n, newValue)/*: number */ {
    return mean + ((newValue - mean) / (n + 1));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.average"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>average (x)](#apidoc.element.simple-statistics.average)
- description and source-code
```javascript
function mean(x)/*:number*/ {
    // The mean of no numbers is null
    if (x.length === 0) {
        throw new Error('mean requires at least one data point');
    }

    return sum(x) / x.length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.bayesian"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>bayesian ()](#apidoc.element.simple-statistics.bayesian)
- description and source-code
```javascript
function BayesianClassifier() {
    // The number of items that are currently
    // classified in the model
    this.totalCount = 0;
    // Every item classified in the model
    this.data = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.bernoulliDistribution"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>bernoulliDistribution (p)](#apidoc.element.simple-statistics.bernoulliDistribution)
- description and source-code
```javascript
function bernoulliDistribution(p) {
    // Check that 'p' is a valid probability (0 ≤ p ≤ 1)
    if (p < 0 || p > 1 ) {
        throw new Error('bernoulliDistribution requires probability to be between 0 and 1 inclusive');
    }

    return binomialDistribution(1, p);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.binomialDistribution"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>binomialDistribution ( trials, probability)](#apidoc.element.simple-statistics.binomialDistribution)
- description and source-code
```javascript
function binomialDistribution( trials, probability)/*: ?Object */ {
    // Check that 'p' is a valid probability (0 ≤ p ≤ 1),
    // that 'n' is an integer, strictly positive.
    if (probability < 0 || probability > 1 ||
        trials <= 0 || trials % 1 !== 0) {
        return undefined;
    }

    // We initialize 'x', the random variable, and 'accumulator', an accumulator
    // for the cumulative distribution function to 0. 'distribution_functions'
    // is the object we'll return with the 'probability_of_x' and the
    // 'cumulativeProbability_of_x', as well as the calculated mean &
    // variance. We iterate until the 'cumulativeProbability_of_x' is
    // within 'epsilon' of 1.0.
    var x = 0,
        cumulativeProbability = 0,
        cells = {};

    // This algorithm iterates through each potential outcome,
    // until the 'cumulativeProbability' is very close to 1, at
    // which point we've defined the vast majority of outcomes
    do {
        // a [probability mass function](https://en.wikipedia.org/wiki/Probability_mass_function)
        cells[x] = factorial(trials) /
            (factorial(x) * factorial(trials - x)) *
            (Math.pow(probability, x) * Math.pow(1 - probability, trials - x));
        cumulativeProbability += cells[x];
        x++;
    // when the cumulativeProbability is nearly 1, we've calculated
    // the useful range of this distribution
    } while (cumulativeProbability < 1 - epsilon);

    return cells;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.bisect"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>bisect ( func/*: (x: any)](#apidoc.element.simple-statistics.bisect)
- description and source-code
```javascript
function bisect( func/*: (x: any) => number */,
    start/*: number */,
    end/*: number */,
    maxIterations/*: number */,
    errorTolerance/*: number */)/*:number*/ {

    if (typeof func !== 'function') throw new TypeError('func must be a function');

    for (var i = 0; i < maxIterations; i++) {
        var output = (start + end) / 2;

        if (func(output) === 0 || Math.abs((end - start) / 2) < errorTolerance) {
            return output;
        }

        if (sign(func(output)) === sign(func(start))) {
            start = output;
        } else {
            end = output;
        }
    }

    throw new Error('maximum number of iterations exceeded');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.chiSquaredGoodnessOfFit"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>chiSquaredGoodnessOfFit ( data, distributionType, significance)](#apidoc.element.simple-statistics.chiSquaredGoodnessOfFit)
- description and source-code
```javascript
function chiSquaredGoodnessOfFit( data, distributionType, significance)/*: boolean */ {
    // Estimate from the sample data, a weighted mean.
    var inputMean = mean(data),
        // Calculated value of the χ2 statistic.
        chiSquared = 0,
        // Degrees of freedom, calculated as (number of class intervals -
        // number of hypothesized distribution parameters estimated - 1)
        degreesOfFreedom,
        // Number of hypothesized distribution parameters estimated, expected to be supplied in the distribution test.
        // Lose one degree of freedom for estimating 'lambda' from the sample data.
        c = 1,
        // The hypothesized distribution.
        // Generate the hypothesized distribution.
        hypothesizedDistribution = distributionType(inputMean),
        observedFrequencies = [],
        expectedFrequencies = [],
        k;

    // Create an array holding a histogram from the sample data, of
    // the form '{ value: numberOfOcurrences }'
    for (var i = 0; i < data.length; i++) {
        if (observedFrequencies[data[i]] === undefined) {
            observedFrequencies[data[i]] = 0;
        }
        observedFrequencies[data[i]]++;
    }

    // The histogram we created might be sparse - there might be gaps
    // between values. So we iterate through the histogram, making
    // sure that instead of undefined, gaps have 0 values.
    for (i = 0; i < observedFrequencies.length; i++) {
        if (observedFrequencies[i] === undefined) {
            observedFrequencies[i] = 0;
        }
    }

    // Create an array holding a histogram of expected data given the
    // sample size and hypothesized distribution.
    for (k in hypothesizedDistribution) {
        if (k in observedFrequencies) {
            expectedFrequencies[+k] = hypothesizedDistribution[k] * data.length;
        }
    }

    // Working backward through the expected frequencies, collapse classes
    // if less than three observations are expected for a class.
    // This transformation is applied to the observed frequencies as well.
    for (k = expectedFrequencies.length - 1; k >= 0; k--) {
        if (expectedFrequencies[k] < 3) {
            expectedFrequencies[k - 1] += expectedFrequencies[k];
            expectedFrequencies.pop();

            observedFrequencies[k - 1] += observedFrequencies[k];
            observedFrequencies.pop();
        }
    }

    // Iterate through the squared differences between observed & expected
    // frequencies, accumulating the 'chiSquared' statistic.
    for (k = 0; k < observedFrequencies.length; k++) {
        chiSquared += Math.pow(
            observedFrequencies[k] - expectedFrequencies[k], 2) /
            expectedFrequencies[k];
    }

    // Calculate degrees of freedom for this test and look it up in the
    // 'chiSquaredDistributionTable' in order to
    // accept or reject the goodness-of-fit of the hypothesized distribution.
    degreesOfFreedom = observedFrequencies.length - c - 1;
    return chiSquaredDistributionTable[degreesOfFreedom][significance] < chiSquared;
}
```
- example usage
```shell
...
 * var data1019 = [
 *     0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,
 *     0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,
 *     1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1,
 *     2, 2, 2, 2, 2, 2, 2, 2, 2,
 *     3, 3, 3, 3
 * ];
 * ss.chiSquaredGoodnessOfFit(data1019, ss.poissonDistribution, 0.05)); //= false
 */
function chiSquaredGoodnessOfFit(
data/*: Array<number> */,
distributionType/*: Function */,
significance/*: number */)/*: boolean */ {
// Estimate from the sample data, a weighted mean.
var inputMean = mean(data),
...
```

#### <a name="apidoc.element.simple-statistics.chunk"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>chunk (x, chunkSize)](#apidoc.element.simple-statistics.chunk)
- description and source-code
```javascript
function chunk(x, chunkSize)/*:?Array<Array<any>>*/ {

    // a list of result chunks, as arrays in an array
    var output = [];

    // 'chunkSize' must be zero or higher - otherwise the loop below,
    // in which we call 'start += chunkSize', will loop infinitely.
    // So, we'll detect and throw in that case to indicate
    // invalid input.
    if (chunkSize < 1) {
        throw new Error('chunk size must be a positive number');
    }

    if (Math.floor(chunkSize) !== chunkSize) {
        throw new Error('chunk size must be an integer');
    }

    // 'start' is the index at which '.slice' will start selecting
    // new array elements
    for (var start = 0; start < x.length; start += chunkSize) {

        // for each chunk, slice that part of the array and add it
        // to the output. The '.slice' function does not change
        // the original array.
        output.push(x.slice(start, start + chunkSize));
    }
    return output;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.ckmeans"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>ckmeans (x, nClusters)](#apidoc.element.simple-statistics.ckmeans)
- description and source-code
```javascript
function ckmeans(x, nClusters)/*: Array<Array<number>> */ {

    if (nClusters > x.length) {
        throw new Error('cannot generate more classes than there are data values');
    }

    var sorted = numericSort(x),
        // we'll use this as the maximum number of clusters
        uniqueCount = uniqueCountSorted(sorted);

    // if all of the input values are identical, there's one cluster
    // with all of the input in it.
    if (uniqueCount === 1) {
        return [sorted];
    }

    // named 'S' originally
    var matrix = makeMatrix(nClusters, sorted.length),
        // named 'J' originally
        backtrackMatrix = makeMatrix(nClusters, sorted.length);

    // This is a dynamic programming way to solve the problem of minimizing
    // within-cluster sum of squares. It's similar to linear regression
    // in this way, and this calculation incrementally computes the
    // sum of squares that are later read.
    fillMatrices(sorted, matrix, backtrackMatrix);

    // The real work of Ckmeans clustering happens in the matrix generation:
    // the generated matrices encode all possible clustering combinations, and
    // once they're generated we can solve for the best clustering groups
    // very quickly.
    var clusters = [],
        clusterRight = backtrackMatrix[0].length - 1;

    // Backtrack the clusters from the dynamic programming matrix. This
    // starts at the bottom-right corner of the matrix (if the top-left is 0, 0),
    // and moves the cluster target with the loop.
    for (var cluster = backtrackMatrix.length - 1; cluster >= 0; cluster--) {

        var clusterLeft = backtrackMatrix[cluster][clusterRight];

        // fill the cluster from the sorted input by taking a slice of the
        // array. the backtrack matrix makes this easy - it stores the
        // indexes where the cluster should start and end.
        clusters[cluster] = sorted.slice(clusterLeft, clusterRight + 1);

        if (cluster > 0) {
            clusterRight = clusterLeft - 1;
        }
    }

    return clusters;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.combinations"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>combinations (x, k)](#apidoc.element.simple-statistics.combinations)
- description and source-code
```javascript
function combinations(x, k) {
    var i;
    var subI;
    var combinationList = [];
    var subsetCombinations;
    var next;

    for (i = 0; i < x.length; i++) {
        if (k === 1) {
            combinationList.push([x[i]])
        } else {
            subsetCombinations = combinations(x.slice( i + 1, x.length ), k - 1);
            for (subI = 0; subI < subsetCombinations.length; subI++) {
                next = subsetCombinations[subI];
                next.unshift(x[i]);
                combinationList.push(next);
            }
        }
    }
    return combinationList;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.combinationsReplacement"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>combinationsReplacement ( x, k)](#apidoc.element.simple-statistics.combinationsReplacement)
- description and source-code
```javascript
function combinationsReplacement( x, k) {

    var combinationList = [];

    for (var i = 0; i < x.length; i++) {
        if (k === 1) {
            // If we're requested to find only one element, we don't need
            // to recurse: just push 'x[i]' onto the list of combinations.
            combinationList.push([x[i]])
        } else {
            // Otherwise, recursively find combinations, given 'k - 1'. Note that
            // we request 'k - 1', so if you were looking for k=3 combinations, we're
            // requesting k=2. This -1 gets reversed in the for loop right after this
            // code, since we concatenate 'x[i]' onto the selected combinations,
            // bringing 'k' back up to your requested level.
            // This recursion may go many levels deep, since it only stops once
            // k=1.
            var subsetCombinations = combinationsReplacement(
                x.slice(i, x.length),
                k - 1);

            for (var j = 0; j < subsetCombinations.length; j++) {
                combinationList.push([x[i]]
                    .concat(subsetCombinations[j]));
            }
        }
    }

    return combinationList;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.combineMeans"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>combineMeans (mean1, n1, mean2, n2)](#apidoc.element.simple-statistics.combineMeans)
- description and source-code
```javascript
function combineMeans(mean1, n1, mean2, n2)/*: number */ {
    return (mean1 * n1 + mean2 * n2) / (n1 + n2);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.combineVariances"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>combineVariances ( variance1, mean1, n1, variance2, mean2, n2)](#apidoc.element.simple-statistics.combineVariances)
- description and source-code
```javascript
function combineVariances( variance1, mean1, n1, variance2, mean2, n2)/*: number */ {

    var newMean = combineMeans(mean1, n1, mean2, n2);

    return (
      n1 * (variance1 + Math.pow(mean1 - newMean, 2)) +
      n2 * (variance2 + Math.pow(mean2 - newMean, 2))
    ) / (n1 + n2);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.cumulativeStdNormalProbability"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>cumulativeStdNormalProbability (z)](#apidoc.element.simple-statistics.cumulativeStdNormalProbability)
- description and source-code
```javascript
function cumulativeStdNormalProbability(z)/*:number */ {

    // Calculate the position of this value.
    var absZ = Math.abs(z),
        // Each row begins with a different
        // significant digit: 0.5, 0.6, 0.7, and so on. Each value in the table
        // corresponds to a range of 0.01 in the input values, so the value is
        // multiplied by 100.
        index = Math.min(Math.round(absZ * 100), standardNormalTable.length - 1);

    // The index we calculate must be in the table as a positive value,
    // but we still pay attention to whether the input is positive
    // or negative, and flip the output value as a last step.
    if (z >= 0) {
        return standardNormalTable[index];
    } else {
        // due to floating-point arithmetic, values in the table with
        // 4 significant figures can nevertheless end up as repeating
        // fractions when they're computed here.
        return +(1 - standardNormalTable[index]).toFixed(4);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.equalIntervalBreaks"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>equalIntervalBreaks (x, nClasses)](#apidoc.element.simple-statistics.equalIntervalBreaks)
- description and source-code
```javascript
function equalIntervalBreaks(x, nClasses)/*: Array<number> */ {

    if (x.length < 2) {
        return x;
    }

    var theMin = min(x),
        theMax = max(x);

    // the first break will always be the minimum value
    // in the xset
    var breaks = [theMin];

    // The size of each break is the full range of the x
    // divided by the number of classes requested
    var breakSize = (theMax - theMin) / nClasses;

    // In the case of nClasses = 1, this loop won't run
    // and the returned breaks will be [min, max]
    for (var i = 1; i < nClasses; i++) {
        breaks.push(breaks[0] + breakSize * i);
    }

    // the last break will always be the
    // maximum.
    breaks.push(theMax);

    return breaks;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.erf"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>erf (x)](#apidoc.element.simple-statistics.erf)
- description and source-code
```javascript
function errorFunction(x)/*: number */ {
    var t = 1 / (1 + 0.5 * Math.abs(x));
    var tau = t * Math.exp(-Math.pow(x, 2) -
        1.26551223 +
        1.00002368 * t +
        0.37409196 * Math.pow(t, 2) +
        0.09678418 * Math.pow(t, 3) -
        0.18628806 * Math.pow(t, 4) +
        0.27886807 * Math.pow(t, 5) -
        1.13520398 * Math.pow(t, 6) +
        1.48851587 * Math.pow(t, 7) -
        0.82215223 * Math.pow(t, 8) +
        0.17087277 * Math.pow(t, 9));
    if (x >= 0) {
        return 1 - tau;
    } else {
        return tau - 1;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.errorFunction"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>errorFunction (x)](#apidoc.element.simple-statistics.errorFunction)
- description and source-code
```javascript
function errorFunction(x)/*: number */ {
    var t = 1 / (1 + 0.5 * Math.abs(x));
    var tau = t * Math.exp(-Math.pow(x, 2) -
        1.26551223 +
        1.00002368 * t +
        0.37409196 * Math.pow(t, 2) +
        0.09678418 * Math.pow(t, 3) -
        0.18628806 * Math.pow(t, 4) +
        0.27886807 * Math.pow(t, 5) -
        1.13520398 * Math.pow(t, 6) +
        1.48851587 * Math.pow(t, 7) -
        0.82215223 * Math.pow(t, 8) +
        0.17087277 * Math.pow(t, 9));
    if (x >= 0) {
        return 1 - tau;
    } else {
        return tau - 1;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.factorial"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>factorial (n)](#apidoc.element.simple-statistics.factorial)
- description and source-code
```javascript
function factorial(n)/*: number */ {

    // factorial is mathematically undefined for negative numbers
    if (n < 0) {
        throw new Error('factorial requires an integer input');
    }

    if (Math.floor(n) !== n) {
        throw new Error('factorial requires a non-negative value');
    }

    // typically you'll expand the factorial function going down, like
    // 5! = 5 * 4 * 3 * 2 * 1. This is going in the opposite direction,
    // counting from 2 up to the number in question, and since anything
    // multiplied by 1 is itself, the loop only needs to start at 2.
    var accumulator = 1;
    for (var i = 2; i <= n; i++) {
        // for each number up to and including the number 'n', multiply
        // the accumulator my that number.
        accumulator *= i;
    }
    return accumulator;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.geometricMean"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>geometricMean (x)](#apidoc.element.simple-statistics.geometricMean)
- description and source-code
```javascript
function geometricMean(x) {
    // The mean of no numbers is null
    if (x.length === 0) {
        throw new Error('geometricMean requires at least one data point');
    }

    // the starting value.
    var value = 1;

    for (var i = 0; i < x.length; i++) {
        // the geometric mean is only valid for positive numbers
        if (x[i] <= 0) {
            throw new Error('geometricMean requires only positive numbers as input');
        }

        // repeatedly multiply the value by each number
        value *= x[i];
    }

    return Math.pow(value, 1 / x.length);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.harmonicMean"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>harmonicMean (x)](#apidoc.element.simple-statistics.harmonicMean)
- description and source-code
```javascript
function harmonicMean(x) {
    // The mean of no numbers is null
    if (x.length === 0) {
        throw new Error('harmonicMean requires at least one data point');
    }

    var reciprocalSum = 0;

    for (var i = 0; i < x.length; i++) {
        // the harmonic mean is only valid for positive numbers
        if (x[i] <= 0) {
            throw new Error('harmonicMean requires only positive numbers as input');
        }

        reciprocalSum += 1 / x[i];
    }

    // divide n by the the reciprocal sum
    return x.length / reciprocalSum;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.interquartileRange"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>interquartileRange (x)](#apidoc.element.simple-statistics.interquartileRange)
- description and source-code
```javascript
function interquartileRange(x) {
    // Interquartile range is the span between the upper quartile,
    // at '0.75', and lower quartile, '0.25'
    var q1 = quantile(x, 0.75),
        q2 = quantile(x, 0.25);

    if (typeof q1 === 'number' && typeof q2 === 'number') {
        return q1 - q2;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.inverseErrorFunction"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>inverseErrorFunction (x)](#apidoc.element.simple-statistics.inverseErrorFunction)
- description and source-code
```javascript
function inverseErrorFunction(x)/*: number */ {
    var a = (8 * (Math.PI - 3)) / (3 * Math.PI * (4 - Math.PI));

    var inv = Math.sqrt(Math.sqrt(
        Math.pow(2 / (Math.PI * a) + Math.log(1 - x * x) / 2, 2) -
        Math.log(1 - x * x) / a) -
        (2 / (Math.PI * a) + Math.log(1 - x * x) / 2));

    if (x >= 0) {
        return inv;
    } else {
        return -inv;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.iqr"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>iqr (x)](#apidoc.element.simple-statistics.iqr)
- description and source-code
```javascript
function interquartileRange(x) {
    // Interquartile range is the span between the upper quartile,
    // at '0.75', and lower quartile, '0.25'
    var q1 = quantile(x, 0.75),
        q2 = quantile(x, 0.25);

    if (typeof q1 === 'number' && typeof q2 === 'number') {
        return q1 - q2;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.linearRegression"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>linearRegression (data)](#apidoc.element.simple-statistics.linearRegression)
- description and source-code
```javascript
function linearRegression(data)/*: { m: number, b: number } */ {

    var m, b;

    // Store data length in a local variable to reduce
    // repeated object property lookups
    var dataLength = data.length;

    //if there's only one point, arbitrarily choose a slope of 0
    //and a y-intercept of whatever the y of the initial point is
    if (dataLength === 1) {
        m = 0;
        b = data[0][1];
    } else {
        // Initialize our sums and scope the 'm' and 'b'
        // variables that define the line.
        var sumX = 0, sumY = 0,
            sumXX = 0, sumXY = 0;

        // Use local variables to grab point values
        // with minimal object property lookups
        var point, x, y;

        // Gather the sum of all x values, the sum of all
        // y values, and the sum of x^2 and (x*y) for each
        // value.
        //
        // In math notation, these would be SS_x, SS_y, SS_xx, and SS_xy
        for (var i = 0; i < dataLength; i++) {
            point = data[i];
            x = point[0];
            y = point[1];

            sumX += x;
            sumY += y;

            sumXX += x * x;
            sumXY += x * y;
        }

        // 'm' is the slope of the regression line
        m = ((dataLength * sumXY) - (sumX * sumY)) /
            ((dataLength * sumXX) - (sumX * sumX));

        // 'b' is the y-intercept of the line.
        b = (sumY / dataLength) - ((m * sumX) / dataLength);
    }

    // Return both values as an object.
    return {
        m: m,
        b: b
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.linearRegressionLine"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>linearRegressionLine (mb)](#apidoc.element.simple-statistics.linearRegressionLine)
- description and source-code
```javascript
function linearRegressionLine(mb)/*: Function */ {
    // Return a function that computes a 'y' value for each
    // x value it is given, based on the values of 'b' and 'a'
    // that we just computed.
    return function(x) {
        return mb.b + (mb.m * x);
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.mad"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>mad (x)](#apidoc.element.simple-statistics.mad)
- description and source-code
```javascript
function medianAbsoluteDeviation(x) {
    // The mad of nothing is null
    var medianValue = median(x),
        medianAbsoluteDeviations = [];

    // Make a list of absolute deviations from the median
    for (var i = 0; i < x.length; i++) {
        medianAbsoluteDeviations.push(Math.abs(x[i] - medianValue));
    }

    // Find the median value of that list
    return median(medianAbsoluteDeviations);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.max"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>max (x)](#apidoc.element.simple-statistics.max)
- description and source-code
```javascript
function max(x) /*:number*/ {
    var value;
    for (var i = 0; i < x.length; i++) {
        // On the first iteration of this loop, max is
        // undefined and is thus made the maximum element in the array
        if (value === undefined || x[i] > value) {
            value = x[i];
        }
    }
    if (value === undefined) {
        throw new Error('max requires at least one data point');
    }
    return value;
}
```
- example usage
```shell
...

matrix[cluster][i] = matrix[cluster - 1][i - 1];
backtrackMatrix[cluster][i] = i;

var jlow = cluster; // the lower end for j

if (iMin > cluster) {
    jlow = Math.max(jlow, backtrackMatrix[cluster][iMin - 1] || 0);
}
jlow = Math.max(jlow, backtrackMatrix[cluster - 1][i] || 0);

var jhigh = i - 1; // the upper end for j
if (iMax < matrix.length - 1) {
    jhigh = Math.min(jhigh, backtrackMatrix[cluster][iMax + 1] || 0);
}
...
```

#### <a name="apidoc.element.simple-statistics.maxSorted"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>maxSorted (x)](#apidoc.element.simple-statistics.maxSorted)
- description and source-code
```javascript
function maxSorted(x)/*:number*/ {
    return x[x.length - 1];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.mean"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>mean (x)](#apidoc.element.simple-statistics.mean)
- description and source-code
```javascript
function mean(x)/*:number*/ {
    // The mean of no numbers is null
    if (x.length === 0) {
        throw new Error('mean requires at least one data point');
    }

    return sum(x) / x.length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.median"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>median (x)](#apidoc.element.simple-statistics.median)
- description and source-code
```javascript
function median(x)/*:number*/ {
    return +quantile(x, 0.5);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.medianAbsoluteDeviation"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>medianAbsoluteDeviation (x)](#apidoc.element.simple-statistics.medianAbsoluteDeviation)
- description and source-code
```javascript
function medianAbsoluteDeviation(x) {
    // The mad of nothing is null
    var medianValue = median(x),
        medianAbsoluteDeviations = [];

    // Make a list of absolute deviations from the median
    for (var i = 0; i < x.length; i++) {
        medianAbsoluteDeviations.push(Math.abs(x[i] - medianValue));
    }

    // Find the median value of that list
    return median(medianAbsoluteDeviations);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.medianSorted"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>medianSorted (sorted)](#apidoc.element.simple-statistics.medianSorted)
- description and source-code
```javascript
function medianSorted(sorted)/*:number*/ {
    return quantileSorted(sorted, 0.5);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.min"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>min (x)](#apidoc.element.simple-statistics.min)
- description and source-code
```javascript
function min(x)/*:number*/ {
    var value;
    for (var i = 0; i < x.length; i++) {
        // On the first iteration of this loop, min is
        // undefined and is thus made the minimum element in the array
        if (value === undefined || x[i] < value) {
            value = x[i];
        }
    }
    if (value === undefined) {
        throw new Error('min requires at least one data point');
    }
    return value;
}
```
- example usage
```shell
...
if (iMin > cluster) {
    jlow = Math.max(jlow, backtrackMatrix[cluster][iMin - 1] || 0);
}
jlow = Math.max(jlow, backtrackMatrix[cluster - 1][i] || 0);

var jhigh = i - 1; // the upper end for j
if (iMax < matrix.length - 1) {
    jhigh = Math.min(jhigh, backtrackMatrix[cluster][iMax + 1] || 0);
}

var sji;
var sjlowi;
var ssqjlow;
var ssqj;
for (var j = jhigh; j >= jlow; --j) {
...
```

#### <a name="apidoc.element.simple-statistics.minSorted"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>minSorted (x)](#apidoc.element.simple-statistics.minSorted)
- description and source-code
```javascript
function minSorted(x)/*:number*/ {
    return x[0];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.mixin"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>mixin (ss, array)](#apidoc.element.simple-statistics.mixin)
- description and source-code
```javascript
function mixin(ss, array)<span class="apidocCodeCommentSpan">/*: any */ {
    var support = !!(Object.defineProperty && Object.defineProperties);
    // Coverage testing will never test this error.
    /* istanbul ignore next */
</span>    if (!support) {
        throw new Error('without defineProperty, simple-statistics cannot be mixed in');
    }

    // only methods which work on basic arrays in a single step
    // are supported
    var arrayMethods = ['median', 'standardDeviation', 'sum', 'product',
        'sampleSkewness',
        'mean', 'min', 'max', 'quantile', 'geometricMean',
        'harmonicMean', 'root_mean_square'];

    // create a closure with a method name so that a reference
    // like 'arrayMethods[i]' doesn't follow the loop increment
    function wrap(method) {
        return function() {
            // cast any arguments into an array, since they're
            // natively objects
            var args = Array.prototype.slice.apply(arguments);
            // make the first argument the array itself
            args.unshift(this);
            // return the result of the ss method
            return ss[method].apply(ss, args);
        };
    }

    // select object to extend
    var extending;
    if (array) {
        // create a shallow copy of the array so that our internal
        // operations do not change it by reference
        extending = array.slice();
    } else {
        extending = Array.prototype;
    }

    // for each array function, define a function that gets
    // the array as the first argument.
    // We use [defineProperty](https://developer.mozilla.org/en-US/docs/JavaScript/Reference/Global_Objects/Object/defineProperty
)
    // because it allows these properties to be non-enumerable:
    // 'for (var in x)' loops will not run into problems with this
    // implementation.
    for (var i = 0; i < arrayMethods.length; i++) {
        Object.defineProperty(extending, arrayMethods[i], {
            value: wrap(arrayMethods[i]),
            configurable: true,
            enumerable: false,
            writable: true
        });
    }

    return extending;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.mode"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>mode (x)](#apidoc.element.simple-statistics.mode)
- description and source-code
```javascript
function mode(x)/*:number*/ {
    // Sorting the array lets us iterate through it below and be sure
    // that every time we see a new number it's new and we'll never
    // see the same number twice
    return modeSorted(numericSort(x));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.modeFast"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>modeFast (x)](#apidoc.element.simple-statistics.modeFast)
- description and source-code
```javascript
function modeFast(x)/*: ?T */ {

    // This index will reflect the incidence of different values, indexing
    // them like
    // { value: count }
    var index = new Map();

    // A running 'mode' and the number of times it has been encountered.
    var mode;
    var modeCount = 0;

    for (var i = 0; i < x.length; i++) {
        var newCount = index.get(x[i]);
        if (newCount === undefined) {
            newCount = 1;
        } else {
            newCount++;
        }
        if (newCount > modeCount) {
            mode = x[i];
            modeCount = newCount;
        }
        index.set(x[i], newCount);
    }

    if (modeCount === 0) {
        throw new Error('mode requires at last one data point');
    }

    return mode;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.modeSorted"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>modeSorted (sorted)](#apidoc.element.simple-statistics.modeSorted)
- description and source-code
```javascript
function modeSorted(sorted)/*:number*/ {

    // Handle edge cases:
    // The mode of an empty list is undefined
    if (sorted.length === 0) {
        throw new Error('mode requires at least one data point');
    } else if (sorted.length === 1) {
        return sorted[0];
    }

    // This assumes it is dealing with an array of size > 1, since size
    // 0 and 1 are handled immediately. Hence it starts at index 1 in the
    // array.
    var last = sorted[0],
        // store the mode as we find new modes
        value = NaN,
        // store how many times we've seen the mode
        maxSeen = 0,
        // how many times the current candidate for the mode
        // has been seen
        seenThis = 1;

    // end at sorted.length + 1 to fix the case in which the mode is
    // the highest number that occurs in the sequence. the last iteration
    // compares sorted[i], which is undefined, to the highest number
    // in the series
    for (var i = 1; i < sorted.length + 1; i++) {
        // we're seeing a new number pass by
        if (sorted[i] !== last) {
            // the last number is the new mode since we saw it more
            // often than the old one
            if (seenThis > maxSeen) {
                maxSeen = seenThis;
                value = last;
            }
            seenThis = 1;
            last = sorted[i];
        // if this isn't a new number, it's one more occurrence of
        // the potential mode
        } else { seenThis++; }
    }
    return value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.perceptron"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>perceptron ()](#apidoc.element.simple-statistics.perceptron)
- description and source-code
```javascript
function PerceptronModel() {
    // The weights, or coefficients of the model;
    // weights are only populated when training with data.
    this.weights = [];
    // The bias term, or intercept; it is also a weight but
    // it's stored separately for convenience as it is always
    // multiplied by one.
    this.bias = 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.permutationsHeap"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>permutationsHeap (elements)](#apidoc.element.simple-statistics.permutationsHeap)
- description and source-code
```javascript
function permutationsHeap(elements)/*: Array<Array<T>> */ {
    var indexes = new Array(elements.length);
    var permutations = [elements.slice()];

    for (var i = 0; i < elements.length; i++) {
        indexes[i] = 0;
    }

    for (i = 0; i < elements.length;) {
        if (indexes[i] < i) {

            // At odd indexes, swap from indexes[i] instead
            // of from the beginning of the array
            var swapFrom = 0;
            if (i % 2 !== 0) {
                swapFrom = indexes[i];
            }

            // swap between swapFrom and i, using
            // a temporary variable as storage.
            var temp = elements[swapFrom];
            elements[swapFrom] = elements[i];
            elements[i] = temp;

            permutations.push(elements.slice());
            indexes[i]++;
            i = 0;

        } else {
            indexes[i] = 0;
            i++;
        }
    }

    return permutations;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.poissonDistribution"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>poissonDistribution (lambda)](#apidoc.element.simple-statistics.poissonDistribution)
- description and source-code
```javascript
function poissonDistribution(lambda) {
    // Check that lambda is strictly positive
    if (lambda <= 0) { return undefined; }

    // our current place in the distribution
    var x = 0,
        // and we keep track of the current cumulative probability, in
        // order to know when to stop calculating chances.
        cumulativeProbability = 0,
        // the calculated cells to be returned
        cells = {};

    // This algorithm iterates through each potential outcome,
    // until the 'cumulativeProbability' is very close to 1, at
    // which point we've defined the vast majority of outcomes
    do {
        // a [probability mass function](https://en.wikipedia.org/wiki/Probability_mass_function)
        cells[x] = (Math.pow(Math.E, -lambda) * Math.pow(lambda, x)) / factorial(x);
        cumulativeProbability += cells[x];
        x++;
    // when the cumulativeProbability is nearly 1, we've calculated
    // the useful range of this distribution
    } while (cumulativeProbability < 1 - epsilon);

    return cells;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.probit"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>probit (p)](#apidoc.element.simple-statistics.probit)
- description and source-code
```javascript
function probit(p)/*: number */ {
    if (p === 0) {
        p = epsilon;
    } else if (p >= 1) {
        p = 1 - epsilon;
    }
    return Math.sqrt(2) * inverseErrorFunction(2 * p - 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.product"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>product (x)](#apidoc.element.simple-statistics.product)
- description and source-code
```javascript
function product(x)/*: number */ {
    var value = 1;
    for (var i = 0; i < x.length; i++) {
        value *= x[i];
    }
    return value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.quantile"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>quantile (x, p)](#apidoc.element.simple-statistics.quantile)
- description and source-code
```javascript
function quantile(x, p) {
    var copy = x.slice();

    if (Array.isArray(p)) {
        // rearrange elements so that each element corresponding to a requested
        // quantile is on a place it would be if the array was fully sorted
        multiQuantileSelect(copy, p);
        // Initialize the result array
        var results = [];
        // For each requested quantile
        for (var i = 0; i < p.length; i++) {
            results[i] = quantileSorted(copy, p[i]);
        }
        return results;
    } else {
        var idx = quantileIndex(copy.length, p);
        quantileSelect(copy, idx, 0, copy.length - 1);
        return quantileSorted(copy, p);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.quantileSorted"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>quantileSorted (x, p)](#apidoc.element.simple-statistics.quantileSorted)
- description and source-code
```javascript
function quantileSorted(x, p)/*:number*/ {
    var idx = x.length * p;
    if (x.length === 0) {
        throw new Error('quantile requires at least one data point.');
    } else if (p < 0 || p > 1) {
        throw new Error('quantiles must be between 0 and 1');
    } else if (p === 1) {
        // If p is 1, directly return the last element
        return x[x.length - 1];
    } else if (p === 0) {
        // If p is 0, directly return the first element
        return x[0];
    } else if (idx % 1 !== 0) {
        // If p is not integer, return the next element in array
        return x[Math.ceil(idx) - 1];
    } else if (x.length % 2 === 0) {
        // If the list has even-length, we'll take the average of this number
        // and the next value, if there is one
        return (x[idx - 1] + x[idx]) / 2;
    } else {
        // Finally, in the simple case of an integer value
        // with an odd-length list, return the x value at the index.
        return x[idx];
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.rSquared"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>rSquared (x, func)](#apidoc.element.simple-statistics.rSquared)
- description and source-code
```javascript
function rSquared(x, func) /*: number */ {
    if (x.length < 2) { return 1; }

    // Compute the average y value for the actual
    // data set in order to compute the
    // _total sum of squares_
    var sum = 0, average;
    for (var i = 0; i < x.length; i++) {
        sum += x[i][1];
    }
    average = sum / x.length;

    // Compute the total sum of squares - the
    // squared difference between each point
    // and the average of all points.
    var sumOfSquares = 0;
    for (var j = 0; j < x.length; j++) {
        sumOfSquares += Math.pow(average - x[j][1], 2);
    }

    // Finally estimate the error: the squared
    // difference between the estimate and the actual data
    // value at each point.
    var err = 0;
    for (var k = 0; k < x.length; k++) {
        err += Math.pow(x[k][1] - func(x[k][0]), 2);
    }

    // As the error grows larger, its ratio to the
    // sum of squares increases and the r squared
    // value grows lower.
    return 1 - err / sumOfSquares;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.rms"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>rms (x)](#apidoc.element.simple-statistics.rms)
- description and source-code
```javascript
function rootMeanSquare(x)/*:number*/ {
    if (x.length === 0) {
        throw new Error('rootMeanSquare requires at least one data point');
    }

    var sumOfSquares = 0;
    for (var i = 0; i < x.length; i++) {
        sumOfSquares += Math.pow(x[i], 2);
    }

    return Math.sqrt(sumOfSquares / x.length);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.rootMeanSquare"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>rootMeanSquare (x)](#apidoc.element.simple-statistics.rootMeanSquare)
- description and source-code
```javascript
function rootMeanSquare(x)/*:number*/ {
    if (x.length === 0) {
        throw new Error('rootMeanSquare requires at least one data point');
    }

    var sumOfSquares = 0;
    for (var i = 0; i < x.length; i++) {
        sumOfSquares += Math.pow(x[i], 2);
    }

    return Math.sqrt(sumOfSquares / x.length);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.sample"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>sample ( x, n, randomSource)](#apidoc.element.simple-statistics.sample)
- description and source-code
```javascript
function sample( x, n, randomSource) /*: Array<T> */ {
    // shuffle the original array using a fisher-yates shuffle
    var shuffled = shuffle(x, randomSource);

    // and then return a subset of it - the first 'n' elements.
    return shuffled.slice(0, n);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.sampleCorrelation"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>sampleCorrelation (x, y)](#apidoc.element.simple-statistics.sampleCorrelation)
- description and source-code
```javascript
function sampleCorrelation(x, y)/*:number*/ {
    var cov = sampleCovariance(x, y),
        xstd = sampleStandardDeviation(x),
        ystd = sampleStandardDeviation(y);

    return cov / xstd / ystd;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.sampleCovariance"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>sampleCovariance (x, y)](#apidoc.element.simple-statistics.sampleCovariance)
- description and source-code
```javascript
function sampleCovariance(x, y)/*:number*/ {

    // The two datasets must have the same length which must be more than 1
    if (x.length !== y.length) {
        throw new Error('sampleCovariance requires samples with equal lengths');
    }

    if (x.length < 2) {
        throw new Error('sampleCovariance requires at least two data points in each sample');
    }

    // determine the mean of each dataset so that we can judge each
    // value of the dataset fairly as the difference from the mean. this
    // way, if one dataset is [1, 2, 3] and [2, 3, 4], their covariance
    // does not suffer because of the difference in absolute values
    var xmean = mean(x),
        ymean = mean(y),
        sum = 0;

    // for each pair of values, the covariance increases when their
    // difference from the mean is associated - if both are well above
    // or if both are well below
    // the mean, the covariance increases significantly.
    for (var i = 0; i < x.length; i++) {
        sum += (x[i] - xmean) * (y[i] - ymean);
    }

    // this is Bessels' Correction: an adjustment made to sample statistics
    // that allows for the reduced degree of freedom entailed in calculating
    // values from samples rather than complete populations.
    var besselsCorrection = x.length - 1;

    // the covariance is weighted by the length of the datasets.
    return sum / besselsCorrection;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.sampleSkewness"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>sampleSkewness (x)](#apidoc.element.simple-statistics.sampleSkewness)
- description and source-code
```javascript
function sampleSkewness(x)/*:number*/ {
    // The skewness of less than three arguments is null
    var theSampleStandardDeviation = sampleStandardDeviation(x);

    if (x.length < 3) {
        throw new Error('sampleSkewness requires at least three data points');
    }

    var n = x.length,
        cubedS = Math.pow(theSampleStandardDeviation, 3),
        sumCubedDeviations = sumNthPowerDeviations(x, 3);

    return n * sumCubedDeviations / ((n - 1) * (n - 2) * cubedS);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.sampleStandardDeviation"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>sampleStandardDeviation (x)](#apidoc.element.simple-statistics.sampleStandardDeviation)
- description and source-code
```javascript
function sampleStandardDeviation(x)/*:number*/ {
    // The standard deviation of no numbers is null
    var sampleVarianceX = sampleVariance(x);
    return Math.sqrt(sampleVarianceX);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.sampleVariance"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>sampleVariance (x)](#apidoc.element.simple-statistics.sampleVariance)
- description and source-code
```javascript
function sampleVariance(x)/*:number*/ {
    // The variance of no numbers is null
    if (x.length < 2) {
        throw new Error('sampleVariance requires at least two data points');
    }

    var sumSquaredDeviationsValue = sumNthPowerDeviations(x, 2);

    // this is Bessels' Correction: an adjustment made to sample statistics
    // that allows for the reduced degree of freedom entailed in calculating
    // values from samples rather than complete populations.
    var besselsCorrection = x.length - 1;

    // Find the mean value of that list
    return sumSquaredDeviationsValue / besselsCorrection;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.sampleWithReplacement"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>sampleWithReplacement (x, n, randomSource)](#apidoc.element.simple-statistics.sampleWithReplacement)
- description and source-code
```javascript
function sampleWithReplacement(x, n, randomSource) {

    if (x.length === 0) {
        return [];
    }

    // a custom random number source can be provided if you want to use
    // a fixed seed or another random number generator, like
    // [random-js](https://www.npmjs.org/package/random-js)
    randomSource = randomSource || Math.random;

    var length = x.length;
    var sample = [];

    for (var i = 0; i < n; i++) {
        var index = Math.floor(randomSource() * length);

        sample.push(x[index]);
    }

    return sample;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.shuffle"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>shuffle (x, randomSource)](#apidoc.element.simple-statistics.shuffle)
- description and source-code
```javascript
function shuffle(x, randomSource) {
    // slice the original array so that it is not modified
    var sample = x.slice();

    // and then shuffle that shallow-copied array, in place
    return shuffleInPlace(sample.slice(), randomSource);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.shuffleInPlace"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>shuffleInPlace (x, randomSource)](#apidoc.element.simple-statistics.shuffleInPlace)
- description and source-code
```javascript
function shuffleInPlace(x, randomSource)/*:Array<any>*/ {

    // a custom random number source can be provided if you want to use
    // a fixed seed or another random number generator, like
    // [random-js](https://www.npmjs.org/package/random-js)
    randomSource = randomSource || Math.random;

    // store the current length of the x to determine
    // when no elements remain to shuffle.
    var length = x.length;

    // temporary is used to hold an item when it is being
    // swapped between indices.
    var temporary;

    // The index to swap at each stage.
    var index;

    // While there are still items to shuffle
    while (length > 0) {
        // chose a random index within the subset of the array
        // that is not yet shuffled
        index = Math.floor(randomSource() * length--);

        // store the value that we'll move temporarily
        temporary = x[length];

        // swap the value at 'x[length]' with 'x[index]'
        x[length] = x[index];
        x[index] = temporary;
    }

    return x;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.standardDeviation"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>standardDeviation (x)](#apidoc.element.simple-statistics.standardDeviation)
- description and source-code
```javascript
function standardDeviation(x)/*:number*/ {
    if (x.length === 1) {
        return 0;
    }
    var v = variance(x);
    return Math.sqrt(v);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.subtractFromMean"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>subtractFromMean (mean, n, value)](#apidoc.element.simple-statistics.subtractFromMean)
- description and source-code
```javascript
function subtractFromMean(mean, n, value)/*: number */ {
    return ((mean * n) - value) / (n - 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.sum"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>sum (x)](#apidoc.element.simple-statistics.sum)
- description and source-code
```javascript
function sum(x)/*: number */ {

    // like the traditional sum algorithm, we keep a running
    // count of the current sum.
    var sum = 0;

    // but we also keep three extra variables as bookkeeping:
    // most importantly, an error correction value. This will be a very
    // small number that is the opposite of the floating point precision loss.
    var errorCompensation = 0;

    // this will be each number in the list corrected with the compensation value.
    var correctedCurrentValue;

    // and this will be the next sum
    var nextSum;

    for (var i = 0; i < x.length; i++) {
        // first correct the value that we're going to add to the sum
        correctedCurrentValue = x[i] - errorCompensation;

        // compute the next sum. sum is likely a much larger number
        // than correctedCurrentValue, so we'll lose precision here,
        // and measure how much precision is lost in the next step
        nextSum = sum + correctedCurrentValue;

        // we intentionally didn't assign sum immediately, but stored
        // it for now so we can figure out this: is (sum + nextValue) - nextValue
        // not equal to 0? ideally it would be, but in practice it won't:
        // it will be some very small number. that's what we record
        // as errorCompensation.
        errorCompensation = nextSum - sum - correctedCurrentValue;

        // now that we've computed how much we'll correct for in the next
        // loop, start treating the nextSum as the current sum.
        sum = nextSum;
    }

    return sum;
}
```
- example usage
```shell
...
 * @throws {Error} if the JavaScript environment doesn't support Object.defineProperty
 * @returns {*} the extended Array, or Array.prototype if no object
 * is given.
 *
 * @example
 * var myNumbers = [1, 2, 3];
 * mixin(ss, myNumbers);
 * console.log(myNumbers.sum()); // 6
 */
function mixin(ss /*: Object */, array /*: ?Array<any> */)/*: any */ {
var support = !!(Object.defineProperty && Object.defineProperties);
// Coverage testing will never test this error.
/* istanbul ignore next */
if (!support) {
    throw new Error('without defineProperty, simple-statistics cannot be mixed in');
...
```

#### <a name="apidoc.element.simple-statistics.sumNthPowerDeviations"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>sumNthPowerDeviations (x, n)](#apidoc.element.simple-statistics.sumNthPowerDeviations)
- description and source-code
```javascript
function sumNthPowerDeviations(x, n)/*:number*/ {
    var meanValue = mean(x),
        sum = 0;

    for (var i = 0; i < x.length; i++) {
        sum += Math.pow(x[i] - meanValue, n);
    }

    return sum;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.sumSimple"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>sumSimple (x)](#apidoc.element.simple-statistics.sumSimple)
- description and source-code
```javascript
function sumSimple(x)/*: number */ {
    var value = 0;
    for (var i = 0; i < x.length; i++) {
        value += x[i];
    }
    return value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.tTest"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>tTest (x, expectedValue)](#apidoc.element.simple-statistics.tTest)
- description and source-code
```javascript
function tTest(x, expectedValue)/*:number*/ {
    // The mean of the sample
    var sampleMean = mean(x);

    // The standard deviation of the sample
    var sd = standardDeviation(x);

    // Square root the length of the sample
    var rootN = Math.sqrt(x.length);

    // returning the t value
    return (sampleMean - expectedValue) / (sd / rootN);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.tTestTwoSample"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>tTestTwoSample ( sampleX, sampleY, difference)](#apidoc.element.simple-statistics.tTestTwoSample)
- description and source-code
```javascript
function tTestTwoSample( sampleX, sampleY, difference) {
    var n = sampleX.length,
        m = sampleY.length;

    // If either sample doesn't actually have any values, we can't
    // compute this at all, so we return 'null'.
    if (!n || !m) { return null; }

    // default difference (mu) is zero
    if (!difference) {
        difference = 0;
    }

    var meanX = mean(sampleX),
        meanY = mean(sampleY),
        sampleVarianceX = sampleVariance(sampleX),
        sampleVarianceY = sampleVariance(sampleY);

    if (typeof meanX === 'number' &&
        typeof meanY === 'number' &&
        typeof sampleVarianceX === 'number' &&
        typeof sampleVarianceY === 'number') {
        var weightedVariance = ((n - 1) * sampleVarianceX +
            (m - 1) * sampleVarianceY) / (n + m - 2);

        return (meanX - meanY - difference) /
            Math.sqrt(weightedVariance * (1 / n + 1 / m));
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.uniqueCountSorted"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>uniqueCountSorted (x)](#apidoc.element.simple-statistics.uniqueCountSorted)
- description and source-code
```javascript
function uniqueCountSorted(x)/*: number */ {
    var uniqueValueCount = 0,
        lastSeenValue;
    for (var i = 0; i < x.length; i++) {
        if (i === 0 || x[i] !== lastSeenValue) {
            lastSeenValue = x[i];
            uniqueValueCount++;
        }
    }
    return uniqueValueCount;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.variance"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>variance (x)](#apidoc.element.simple-statistics.variance)
- description and source-code
```javascript
function variance(x)/*:number*/ {
    // The variance of no numbers is null
    if (x.length === 0) {
        throw new Error('variance requires at least one data point');
    }

    // Find the mean of squared deviations between the
    // mean value and each value.
    return sumNthPowerDeviations(x, 2) / x.length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.zScore"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>zScore (x, mean, standardDeviation)](#apidoc.element.simple-statistics.zScore)
- description and source-code
```javascript
function zScore(x, mean, standardDeviation)/*:number*/ {
    return (x - mean) / standardDeviation;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.simple-statistics.bayesian"></a>[module simple-statistics.bayesian](#apidoc.module.simple-statistics.bayesian)

#### <a name="apidoc.element.simple-statistics.bayesian.bayesian"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>bayesian ()](#apidoc.element.simple-statistics.bayesian.bayesian)
- description and source-code
```javascript
function BayesianClassifier() {
    // The number of items that are currently
    // classified in the model
    this.totalCount = 0;
    // Every item classified in the model
    this.data = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.simple-statistics.bayesian.prototype"></a>[module simple-statistics.bayesian.prototype](#apidoc.module.simple-statistics.bayesian.prototype)

#### <a name="apidoc.element.simple-statistics.bayesian.prototype.score"></a>[function <span class="apidocSignatureSpan">simple-statistics.bayesian.prototype.</span>score (item)](#apidoc.element.simple-statistics.bayesian.prototype.score)
- description and source-code
```javascript
score = function (item) {
    // Initialize an empty array of odds per category.
    var odds = {}, category;
    // Iterate through each key in the item,
    // then iterate through each category that has been used
    // in previous calls to '.train()'
    for (var k in item) {
        var v = item[k];
        for (category in this.data) {
            // Create an empty object for storing key - value combinations
            // for this category.
            odds[category] = {};

            // If this item doesn't even have a property, it counts for nothing,
            // but if it does have the property that we're looking for from
            // the item to categorize, it counts based on how popular it is
            // versus the whole population.
            if (this.data[category][k]) {
                odds[category][k + '_' + v] = (this.data[category][k][v] || 0) / this.totalCount;
            } else {
                odds[category][k + '_' + v] = 0;
            }
        }
    }

    // Set up a new object that will contain sums of these odds by category
    var oddsSums = {};

    for (category in odds) {
        // Tally all of the odds for each category-combination pair -
        // the non-existence of a category does not add anything to the
        // score.
        oddsSums[category] = 0;
        for (var combination in odds[category]) {
            oddsSums[category] += odds[category][combination];
        }
    }

    return oddsSums;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.bayesian.prototype.train"></a>[function <span class="apidocSignatureSpan">simple-statistics.bayesian.prototype.</span>train (item, category)](#apidoc.element.simple-statistics.bayesian.prototype.train)
- description and source-code
```javascript
train = function (item, category) {
    // If the data object doesn't have any values
    // for this category, create a new object for it.
    if (!this.data[category]) {
        this.data[category] = {};
    }

    // Iterate through each key in the item.
    for (var k in item) {
        var v = item[k];
        // Initialize the nested object 'data[category][k][item[k]]'
        // with an object of keys that equal 0.
        if (this.data[category][k] === undefined) {
            this.data[category][k] = {};
        }
        if (this.data[category][k][v] === undefined) {
            this.data[category][k][v] = 0;
        }

        // And increment the key for this key/value combination.
        this.data[category][k][v]++;
    }

    // Increment the number of items classified
    this.totalCount++;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.simple-statistics.perceptron"></a>[module simple-statistics.perceptron](#apidoc.module.simple-statistics.perceptron)

#### <a name="apidoc.element.simple-statistics.perceptron.perceptron"></a>[function <span class="apidocSignatureSpan">simple-statistics.</span>perceptron ()](#apidoc.element.simple-statistics.perceptron.perceptron)
- description and source-code
```javascript
function PerceptronModel() {
    // The weights, or coefficients of the model;
    // weights are only populated when training with data.
    this.weights = [];
    // The bias term, or intercept; it is also a weight but
    // it's stored separately for convenience as it is always
    // multiplied by one.
    this.bias = 0;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.simple-statistics.perceptron.prototype"></a>[module simple-statistics.perceptron.prototype](#apidoc.module.simple-statistics.perceptron.prototype)

#### <a name="apidoc.element.simple-statistics.perceptron.prototype.predict"></a>[function <span class="apidocSignatureSpan">simple-statistics.perceptron.prototype.</span>predict (features)](#apidoc.element.simple-statistics.perceptron.prototype.predict)
- description and source-code
```javascript
predict = function (features) {

    // Only predict if previously trained
    // on the same size feature array(s).
    if (features.length !== this.weights.length) { return null; }

    // Calculate the sum of features times weights,
    // with the bias added (implicitly times one).
    var score = 0;
    for (var i = 0; i < this.weights.length; i++) {
        score += this.weights[i] * features[i];
    }
    score += this.bias;

    // Classify as 1 if the score is over 0, otherwise 0.
    if (score > 0) {
        return 1;
    } else {
        return 0;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.simple-statistics.perceptron.prototype.train"></a>[function <span class="apidocSignatureSpan">simple-statistics.perceptron.prototype.</span>train (features, label)](#apidoc.element.simple-statistics.perceptron.prototype.train)
- description and source-code
```javascript
train = function (features, label) {
    // Require that only labels of 0 or 1 are considered.
    if (label !== 0 && label !== 1) { return null; }
    // The length of the feature array determines
    // the length of the weight array.
    // The perceptron will continue learning as long as
    // it keeps seeing feature arrays of the same length.
    // When it sees a new data shape, it initializes.
    if (features.length !== this.weights.length) {
        this.weights = features;
        this.bias = 1;
    }
    // Make a prediction based on current weights.
    var prediction = this.predict(features);
    // Update the weights if the prediction is wrong.
    if (prediction !== label) {
        var gradient = label - prediction;
        for (var i = 0; i < this.weights.length; i++) {
            this.weights[i] += gradient * features[i];
        }
        this.bias += gradient;
    }
    return this;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
