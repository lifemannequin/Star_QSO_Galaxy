# MLphotometry
Using ML and photometry to estimate redshift and spectral classification. This is just an excercise since the SDSS where I get the data has already deleted the redshifts determined using Random Forest because it does poorly with BOSS galaxies.

I realised that the first determining_redshifht had mostly bright sources (< 17 mag). More sources were added to push the mean dered_r band magnitude to 20 and increase number of sources. How the final data set was put together can be seen in the creating_data_sets notebook. The new study of the sources was done in the determining_redshift_less_bias notebook. 
determining_redshift_withDNN is the same study as in determining_redshift_less_bias but using Deep Neural Networks. And to have a look at the BOSS galaxies, there is the notebook  determining_redshift_BOSSgalaxies.
Please comment on any improvement I could make as I am new to machine learning. Thanks :)
