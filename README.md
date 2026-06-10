# Effect of Tensile Testing Parameters on the Mechanical Performance of Poulsenia Armata Fiber Cloth: Experimental Analysis and Machine Learning Modeling
This study investigates the influence of tensile testing parameters on the mechanical response of Poulsenia armata fiber cloth (PAFC), a novel lignocellulosic material sourced from the Ecuadorian Amazon. A Taguchi L9 design of experiments was employed to systematically evaluate the effects of gauge length (25–75 mm) and crosshead speed (2.5–10 mm/min) on ultimate tensile strength (UTS), tensile modulus, and elongation at fracture. Microstructural analysis demonstrates a hierarchical fibrillar architecture with inherent defects, which govern damage initiation and promote progressive failure mechanisms such as microfibril debonding, pull-out, and fibrillation. The tensile behavior of PAFC is governed by a coupled interaction between defect-controlled size effects and strain-rate-dependent viscoelasticity. Increasing gauge length reduced UTS by up to 28% and elongation at fracture by up to 55%, while increasing crosshead speed enhanced tensile strength and modulus by up to 43% and 23%, respectively, due to the suppression of microfibril relaxation and improved load transfer efficiency. Statistical analysis confirmed that both parameters were significant (p < 0.05), with gauge length exerting the dominant influence. A suite of machine learning regressors, including Random Forest, Gaussian Process, K-Nearest Neighbors, and Multi-Layer Perceptron, was developed to predict tensile strength. After hyperparameter optimization, Random Forest and Gaussian Process Regression achieved the best predictive performance, reaching test-set R² values of 0.863 and maintaining robust behavior during cross-validation. The integration of experimental design, microstructural characterization, and machine learning establishes a robust framework for understanding, predicting, and optimizing the mechanical performance of natural fiber systems, highlighting the critical importance of testing parameter standardization for reliable material characterization.

# Models
The following models are implemented and included in this repository:

K-Nearest Neighbors (KNN): hyperparameters for KNN: {'n_neighbors=7'}

RandomForestRegressor (RFR): hyperparameters for RandomForestRegressor: {'max_depth': 30, 'min_samples_leaf': 2, 'min_samples_split': 2, 'n_estimators': 2000}

Gaussian process regressor (GPR): hyperparameters for KNN: {kernel=kernel, n_restarts_optimizer=20, alpha=0.001, normalize_y=True}, kernel = C(1.0, (1e-2, 1e2)) * RBF(10, (1e-2, 1e2))

Multi-layer perceptron (MLP): hyperparameters for KNN: {activation='relu', alpha=0.0001, batch_size='auto', beta_1=0.9,
             beta_2=0.999, early_stopping=False, epsilon=1e-08,
             hidden_layer_sizes=4, learning_rate='adaptive',
             learning_rate_init=0.001, max_fun=15000, max_iter=1000,
             momentum=0.9, n_iter_no_change=10, nesterovs_momentum=True,
             power_t=0.5, random_state=4321, shuffle=True, solver='lbfgs',
             tol=0.0001, validation_fraction=0.1, }

# Usage: 
All files can be opened and edited using Jupyter or similar editing software. The code can then be run directly. Note that you will need to manually install any packages not already installed during the import step.
