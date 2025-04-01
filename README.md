# CausalDiscoveryTS

CausalDiscoveryTS is a Python library for causal discovery on time series and groups of time series. It provides tools for identifying causal relationships, automating benchmarks, and evaluating causal inference methods. The library is designed for researchers and practitioners in causal inference, machine learning, and time series analysis. Check the [docs](https://joaquinmateosbarroso.github.io/group-causation/) for more detailed information.

![image](https://github.com/user-attachments/assets/acfe13b0-9209-4d8c-bd5d-4e29e2c0687e)

## Features
- **Causal Discovery**: Implements various causal discovery algorithms tailored for time series and grouped time series.
- **Benchmark Automation**: Automates benchmarking of causal inference methods across multiple datasets and configurations.
- **Evaluation Metrics**: Provides standardized evaluation metrics for assessing causal discovery performance.
- **Dataset Handling**: Supports synthetic and real-world datasets with preprocessing utilities.

## Installation

You can install the library via pip:
```sh
pip install git+https://github.com/JoaquinMateosBarroso/group-causation
```

Or install from source for development purposes:
```sh
git clone https://github.com/yourusername/CausalDiscoveryTS.git
cd CausalDiscoveryTS
pip install -e .
```

## Usage

### Example: Running a Causal Discovery Algorithm

```python
from causaldiscoveryts import CausalDiscovery

data = load_time_series_data("your_dataset.csv")
model = CausalDiscovery(method="GrangerCausality")
causal_graph = model.fit(data)
model.plot_graph()
```

### Example: Running Benchmarks

```python
from causaldiscoveryts import Benchmark

benchmark = Benchmark(methods=["PCMCI", "GrangerCausality"], datasets=["synthetic", "real"])
benchmark.run()
benchmark.report_results()
```

## Supported Time Series Causal Discovery Methods
- PC-Stable
- PCMCI
- LPCMCI
- Granger Causality
- VARLiNGAM
- DYNOTEARS

## Supported Group Time Series Causal Discovery Methods
- Micro-level
- Dimensionality Reduction + Causal Discovery
- Subgroups
- Group Embedding

## Benchmarking
The benchmarking framework allows for easy comparison of different causal discovery methods. It includes:
- Generation of synthetic datasets based on time series directed acyclic graphs
- Test of algorithms in both static and dynamic hyperparameters conditions
- Plotting of results in atractive graphs
![image](https://github.com/user-attachments/assets/5fc44e5a-6488-4454-854d-e5737a290426)


## Contributing
Contributions are welcome! If you want to contribute:
1. Fork the repository
2. Create a new branch
3. Make your changes
4. Submit a pull request

## License
This project is licensed under the MIT License.

## Contact
For questions or collaborations, feel free to open an issue or contact us at [jmateosbarroso@gmail.com].


