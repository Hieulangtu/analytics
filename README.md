## Execution

### Basic functional tests

```bash
pytest --cov-report term-missing --cov=src tests --log-cli-level=INFO -x
```

### Tests for integration

```bash
pytest tests/test_integration --log-cli-level=INFO -x
```

```bash
uvicorn main:app --env-file environment.txt --port 8008 --reload
# Ý nghĩa các tham số:
# main:app: main là tên file Python (main.py), và app là tên của ứng dụng FastAPI hoặc ASGI trong file đó.
# --env-file environment.txt: Chỉ định file chứa các biến môi trường (ví dụ: thông tin cấu hình, cơ sở dữ liệu, API keys).
# --port 8008: Chạy ứng dụng trên cổng 8008 thay vì cổng mặc định 8000.
# --reload: Tự động reload server khi có thay đổi trong mã nguồn. Điều này hữu ích khi phát triển.
```

Nếu không chạy được lệnh ở dòng 16 do lỗi về PATH và biến môi trường thì chạy lệnh:
python -m uvicorn main:app --env-file environment.txt --port 8008 --reload

```bash
panel serve src/analysis_101/query_presences_.ipynb --autoreload
```

```bash
streamlit run src/streamlit/app.py --server.port=8501 --server.address=0.0.0.0
```
