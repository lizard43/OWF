# OWF

github limits files to be 100MB so the OWF tarball has been split in 3 pieces and then re-assembled in the image.

The OWF tar.gz was split into the files in this folder like this:

	split --bytes=45M OWF-bundle-7.17.0.tar.gz split/OWF

And then in the image, re-assembled like this:

	cat split/OWF* > OWF-bundle-7.17.0.tar.gz

