**iTransformer**

The **iTransformer** is an advanced neural network architecture designed for multivariate time series forecasting, particularly known for its unique approach to attention. Unlike traditional transformer models, which apply attention across temporal tokens (time steps), the iTransformer inverts this approach by applying self-attention across variate tokens (input features), such as those representing different variables at each time step. This inversion allows the model to capture complex interactions between variables rather than focusing solely on temporal patterns, making it highly effective for multivariate datasets.

The self-attention mechanism enables the model to dynamically weigh the importance of each input feature at every time step, learning how they influence each other across different sources, like multiple transects or locations. After the attention step, each data source is processed through its own linear projection layer, ensuring that both global interactions between features and local patterns specific to each transect are learned. This design gives the iTransformer flexibility in learning both shared relationships and source-specific details, enhancing its ability to model complex, multivariate time series data.

The iTransformer architecture includes multi-head self-attention layers, feedforward networks for non-linear transformations, and various adjustable parameters, such as attention heads, hidden units, and dropout rates. These customizable components make it highly adaptable to different forecasting tasks while providing a robust framework for capturing intricate patterns in the data.

### Model classification
#### Model mechanics
- [ ] Process-Based Models (PBM): couple hydrodynamics, waves, and morphodynamics through mass and momentum conservation laws.
- [ ] Hybrid Models (HM): use observational data to calibrate free parameters in the equilibrium configuration of a system.
- [x] Data-Driven Models (DDM): use observational data to train regression models (e.g. machine learning, statistical downscaling).
#### Model elements (multiple choices)
- [x] Cross-shore: model the shoreline position for each transect independently.
- [x] Long-shore: incorporate the interaction of shoreline position across different transects.
- [ ] Sea level: consider the impact of sea level rise on shoreline position.
