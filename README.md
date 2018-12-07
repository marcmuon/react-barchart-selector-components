# bar-chart-selector-react 

This component is a button selector system that will re-draw bar charts from a JSON on click. Supports arbitrary number of chart elements along with vertical scaling. Useful for displaying scientific data along an interactive second dimension. 

### Demo

A demo using CDC survey data on childhood vaccination levels by insurance type is here: https://marcmuon.github.io/react-barchart-selector-components/index.html

### Installation

```
npm install --save bar-chart-selector-react   # using NPM
```

### Example use

```
import React, {Component} from 'react'
import { BarChart } from 'bar-chart-selector-react';
import "typeface-special-elite";

class App extends Component {
  state = {
    vac: [[ 
      {
        "insurance": "Private Only",
        "pct_est": 96.5,
        "vaccine": "DTaP (≥3)"
      },
      {
        "insurance": "Any Medicaid",
        "pct_est": 92.6,
        "vaccine": "DTaP (≥3)"
      },
      {
        "insurance": "No Insurance",
        "pct_est": 78.2,
        "vaccine": "DTaP (≥3)"
      }
  ],
  [ 
      {
        "insurance": "Private Only",
        "pct_est": 88.1,
        "vaccine": "HepA (≥1)"
      },
      {
        "insurance": "Any Medicaid",
        "pct_est": 85.3,
        "vaccine": "HepA (≥1)"
      },
      {
        "insurance": "No Insurance",
        "pct_est": 63.3,
        "vaccine": "HepA (≥1)"
      }
  ],
  [ 
      {
        "insurance": "Private Only",
        "pct_est": 73,
        "vaccine": "HepB Birth"
      },
      {
        "insurance": "Any Medicaid",
        "pct_est": 74.7,
        "vaccine": "HepB Birth"
      },
      {
        "insurance": "No Insurance",
        "pct_est": 68.7,
        "vaccine": "HepB Birth"
      }
  ],
  [ 
      {
        "insurance": "Private Only",
        "pct_est": 95.5,
        "vaccine": "Hib Primary"
      },
      {
        "insurance": "Any Medicaid",
        "pct_est": 91.1,
        "vaccine": "Hib Primary"
      },
      {
        "insurance": "No Insurance",
        "pct_est": 78,
        "vaccine": "Hib Primary"
      }
  ],
  [ 
      {
        "insurance": "Private Only",
        "pct_est": 93.7,
        "vaccine": "MMR"
      },
      {
        "insurance": "Any Medicaid",
        "pct_est": 90.4,
        "vaccine": "MMR"
      },
      {
        "insurance": "No Insurance",
        "pct_est": 74.6,
        "vaccine": "MMR"
      }
  ],
  [ 
      {
        "insurance": "Private Only",
        "pct_est": 94.5,
        "vaccine": "PCV (≥3)"
      },
      {
        "insurance": "Any Medicaid",
        "pct_est": 90.5,
        "vaccine": "PCV (≥3)"
      },
      {
        "insurance": "No Insurance",
        "pct_est": 75.2,
        "vaccine": "PCV (≥3)"
      }
  ],
  [ 
      {
        "insurance": "Private Only",
        "pct_est": 95.2,
        "vaccine": "Poliovirus"
      },
      {
        "insurance": "Any Medicaid",
        "pct_est": 91.2,
        "vaccine": "Poliovirus"
      },
      {
        "insurance": "No Insurance",
        "pct_est": 77.9,
        "vaccine": "Poliovirus"
      }
  ],
  [ 
      {
        "insurance": "Private Only",
        "pct_est": 81.8,
        "vaccine": "Rotavirus"
      },
      {
        "insurance": "Any Medicaid",
        "pct_est": 66.8,
        "vaccine": "Rotavirus"
      },
      {
        "insurance": "No Insurance",
        "pct_est": 51.5,
        "vaccine": "Rotavirus"
      }
  ],
  [ 
      {
        "insurance": "Private Only",
        "pct_est": 92.9,
        "vaccine": "Varicella"
      },
      {
        "insurance": "Any Medicaid",
        "pct_est": 90.4,
        "vaccine": "Varicella"
      },
      {
        "insurance": "No Insurance",
        "pct_est": 69.5,
        "vaccine": "Varicella"
      }
  ],
  [ 
      {
        "insurance": "Private Only",
        "pct_est": 76,
        "vaccine": "Combined 7-vaccine"
      },
      {
        "insurance": "Any Medicaid",
        "pct_est": 66.5,
        "vaccine": "Combined 7-vaccine"
      },
      {
        "insurance": "No Insurance",
        "pct_est": 48.5,
        "vaccine": "Combined 7-vaccine"
      }
  ]],
    track: 0,
    mult: 1,
  }
 

  barGen = (index) => {
    this.setState({
      track: index,
    });
  }

  render() {    
    return (
        <BarChart
          array={this.state.vac}
          multiplier={this.state.mult}
          track={this.state.track}
          gotClicked={this.barGen}
        >
        </BarChart>
      </div>
    );
  }
}

```

## License

```bar-chart-selector-react``` is licensed under a MIT license.


## Authors

* **Marc Kelechava** - *Initial work* - [Marc Muon](https://github.com/marcmuon)


