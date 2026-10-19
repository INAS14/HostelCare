# HostelCare
Django hostel complaint management website starter with student registration, complaint tracking, staff/admin workflows, activity timeline, CSV export and responsive Bootstrap interface.

## Windows setup
Extract the ZIP. Open Command Prompt in the folder containing `manage.py`, then run one command at a time:
```cmd
py -m venv .venv
.venv\Scripts\activate.bat
python -m pip install --upgrade pip
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```
Open http://127.0.0.1:8000/ . Admin: http://127.0.0.1:8000/admin/

## Live deployment
1. Create a GitHub repository and upload the contents of this folder (manage.py must be in the repository root).
2. In Render, choose New + → Blueprint and connect that repository. Render reads `render.yaml` and creates the web service and PostgreSQL database.
3. Wait for the deployment to finish and use the real URL shown by Render.
4. Create the production administrator from the Render service shell: `python manage.py createsuperuser`.
5. Test account permissions before sharing. Do not put real student information into an untested deployment.

## Notes
The project uses SQLite locally and PostgreSQL when `DATABASE_URL` is set. A real public URL is only created after you complete deployment. Set a strong secret key, use HTTPS, and confirm backups and access permissions before real use.
