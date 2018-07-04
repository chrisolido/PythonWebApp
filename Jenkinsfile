sh """
. .env/bin/activate
if [[ -f requirements/preinstall.txt ]]; then
    pip install -r requirements/preinstall.txt
fi
pip install -r requirements/test.txt
./manage.py test --noinput
"""
