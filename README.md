Options for molecular visualizer / editord that work with Colab / locked machines:

JSME for drawing molecules (does not work for me)
from jsme_notebook import JSMENotebook
smiles = 'CCO' #@param {type:"string"}
jsme = JSMENotebook(smiles)
print('Change the molecule!')


RDKit for 3D structure generation
pip install rdeditor (works locally as a python based editor, works on the locked win machines, installed via jupyter lab)
#does not work in colab because it runs on QT

py3Dmol for interactive 3D visualization and small dynamics


https://molview.org/
https://app.molview.com/
online integration via IFrame
from IPython.display import IFrame
# Embed MolView inside Colab
IFrame("https://app.molview.com/", width=1000, height=600)

https://ketcher-editor.streamlit.app/
pip install streamlit-ketcher
import streamlit as st
from streamlit_ketcher import st_ketcher
molecule = st.text_input("Molecule", "CCO")
smile_code = st_ketcher(molecule)
st.markdown(f"Smile code: ``{smile_code}``")
#does not work in calab, can be opened as stanalone app via IFrame, not sure how to get the structure in colab

Avogadro as a standalone molecular editor

Ovito as a standalone molecular editor

Kekule.js

