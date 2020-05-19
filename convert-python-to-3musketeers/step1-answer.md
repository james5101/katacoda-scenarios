```
FROM python:3

ADD printvar.py /

CMD ["python", "./printvar.py"]
```