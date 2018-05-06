.. ---------------------------------------------------------------------------
.. Copyright 2017-2018 Intel Corporation
..
.. Licensed under the Apache License, Version 2.0 (the "License");
.. you may not use this file except in compliance with the License.
.. You may obtain a copy of the License at
..
..      http://www.apache.org/licenses/LICENSE-2.0
..
.. Unless required by applicable law or agreed to in writing, software
.. distributed under the License is distributed on an "AS IS" BASIS,
.. WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
.. See the License for the specific language governing permissions and
.. limitations under the License.
.. ---------------------------------------------------------------------------

API
###

This API documentation covers each model within the Intel AI NLP Architect. Most modules have a
corresponding user guide section that introduces the main concepts. See this
API for specific function definitions.

.. .. csv-table::
..    :header: "Module API", "Description"
..    :widths: 20, 40
..    :delim: |
..
..    :py:mod:`nlp_architect.models` | Model architecture
..    :py:mod:`nlp_architect.layers` | Model layers
..    :py:mod:`nlp_architect.data` | Data loading and handling

``nlp_architect.models``
---------------
.. py:module:: models

Model classes stores a list of layers describing the model. Methods are provided
to train the model weights, perform inference, and save/load the model.

.. autosummary::
   :toctree: generated/
   :nosignatures:

   nlp_architect.models.chunker_model.ChunkerModel
   nlp_architect.models.intent_extraction.JointSequentialLSTM
   nlp_architect.models.intent_extraction.EncDecTaggerModel
   nlp_architect.models.np2vec.NP2vec
   nlp_architect.models.semantic_segmentation.NpSemanticSegClassifier
   nlp_architect.bist.bmstparser.mstlstm.MSTParserLSTM
   nlp_architect.models.memn2n_dialogue.MemN2N_Dialog
   nlp_architect.models.kvmemn2n.KVMemN2N


``nlp_architect.layers``
---------------------------
.. py:module:: nlp_architect.layers

In addition to imported layers, the Intel AI Architect contains its own set of layers.
These are currently stored in the various models

.. autosummary::
   :toctree: generated/
   :nosignatures:

   nlp_architect.models.chunker_model.TimeDistributedRecurrentOutput
   nlp_architect.models.chunker_model.TimeDistributedRecurrentLast
   nlp_architect.models.chunker_model.TimeDistBiLSTM
   nlp_architect.contrib.ngraph.match_lstm.MatchLSTMCell_withAttention
   nlp_architect.contrib.ngraph.match_lstm.AnswerPointer_withAttention
   nlp_architect.contrib.ngraph.match_lstm.Dropout_Modified
   nlp_architect.contrib.ngraph.match_lstm.LookupTable
   nlp_architect.contrib.ngraph.modified_lookup_table.ModifiedLookupTable



``nlp_architect.data``
---------------------------
.. py:module:: nlp_architect.data

Currently datasets are distributed among the various models. In future versions of the code
these will be placed into a central repository.

.. autosummary::
    :toctree: generated/
    :nosignatures:

    nlp_architect.data.conll2000.TaggedTextSequence
    nlp_architect.data.conll2000.MultiSequenceDataIterator
    nlp_architect.data.conll2000.CONLL2000
    nlp_architect.data.conll2000.DataInput
    nlp_architect.data.intent_extraction.IntentDataset
    nlp_architect.data.intent_extraction.ATIS
    nlp_architect.data.intent_extraction.data.SNIPS
    nlp_architect.data.semantic_seg_data.NpSemanticSegData
    nlp_architect.data.babi_dialog.BABI_Dialog
    nlp_architect.data.wikimovies.WIKIMOVIES