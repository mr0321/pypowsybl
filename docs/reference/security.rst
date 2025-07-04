Security analysis
=================

.. module:: pypowsybl.security

The security analysis module allows to simulate contingencies (the loss of a line or a generator, for example)
in a "batch" mode, in AC mode.

Run a security analysis
-----------------------

You can run a security analysis using the following methods:

.. autosummary::
   :nosignatures:
   :toctree: api/

    create_analysis
    SecurityAnalysis.run_ac
    SecurityAnalysis.run_dc
    set_default_provider
    get_default_provider
    get_provider_names


Parameters
----------

The execution of the security analysis can be customized using security analysis parameters.

.. autosummary::
   :nosignatures:
   :toctree: api/

    Parameters
    IncreasedViolationsParameters
    get_provider_parameters_names

Define contingencies and monitored elements
-------------------------------------------

You can define contingencies to be simulated, as well as network elements to be monitored,
with the following methods:

.. autosummary::
   :nosignatures:
   :toctree: api/

    SecurityAnalysis.add_single_element_contingency
    SecurityAnalysis.add_multiple_elements_contingency
    SecurityAnalysis.add_single_element_contingencies
    SecurityAnalysis.add_monitored_elements
    SecurityAnalysis.add_precontingency_monitored_elements
    SecurityAnalysis.add_postcontingency_monitored_elements

Define operator strategies and remedial actions
------------------------------------------------

You can define operator strategies and remedial actions with the following methods:

.. autosummary::
   :nosignatures:
   :toctree: api/

    SecurityAnalysis.add_load_active_power_action
    SecurityAnalysis.add_load_reactive_power_action
    SecurityAnalysis.add_generator_active_power_action
    SecurityAnalysis.add_switch_action
    SecurityAnalysis.add_operator_strategy

Results
-------

When the security analysis is completed, you can inspect its results:

.. autosummary::
   :nosignatures:
   :toctree: api/

    SecurityAnalysisResult
    SecurityAnalysisResult.limit_violations
    SecurityAnalysisResult.pre_contingency_result
    SecurityAnalysisResult.post_contingency_results
    SecurityAnalysisResult.operator_strategy_results
    SecurityAnalysisResult.find_post_contingency_result
    SecurityAnalysisResult.find_operator_strategy_results
    SecurityAnalysisResult.branch_results
    SecurityAnalysisResult.bus_results
    SecurityAnalysisResult.three_windings_transformer_results
    SecurityAnalysisResult.export_to_json

