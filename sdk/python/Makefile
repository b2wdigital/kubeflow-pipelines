dist:
	python3.7 setup.py bdist_wheel
	python3.8 setup.py bdist_wheel

# USar keyring de uma conta de serviço para fazer upload sem por senha e poder fazer remotamente
deploy: dist
	twine upload --repository-url="http://nexus3.b2w.io/repository/pypi-private/" dist/*

install:
	pip3 install  --index-url="http://nexus3.b2w.io/repository/pypi-private/" --trusted-host=nexus3.b2w.io kfp