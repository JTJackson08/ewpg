web: gunicorn ewpg.wsgi --chdir backend --limit-request-line 8188 --log-file -
worker: REMAP_SIGTERM=SIGQUIT celery --workdir backend --app=ewpg worker --loglevel=info
beat: REMAP_SIGTERM=SIGQUIT celery --workdir backend --app=ewpg beat -S redbeat.RedBeatScheduler --loglevel=info
