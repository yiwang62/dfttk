Elastic constant calculation
============

Here we take pure Al as the elastic constant calculation example

- check and find the tag of the materials

.. code-block:: bash

     dfttk thfind

Then the collection of result will be shown, for example
"found complete calculations in the collection: phonon {'tag': 'e868bb8d-a9aa-41b2-bcaa-70328218c82d'}, phonon:  7, static:  8, SN:  64, qha_phonon: F, Al_Fm-3m_225PBE"

- Submit the target job with specific tag to the workflow

.. code-block:: bash

   dfttk run -wf elastic -a -l -tag e868bb8d-a9aa-41b2-bcaa-70328218c82d

The elastic constant will be calculated for different volumes

- Check the workflow

.. code-block:: bash

     lpad get_wflows
     
- launch the work

.. code-block:: bash

     qlaunch singleshot

- Recheck the workflow and make the sure state changing to "state": "RUNNING"

.. code-block:: bash

     lpad get_wflows
          
- Check the elastic constant result on MongoDB database


