# CC Lab 2 - Monolithic Architecture

SRN: PES1UG23CS209

This project demonstrates monolithic application failure and performance optimization using FastAPI and Locust.

## Screenshots
SS1 - Events page loaded  
SS2 - Checkout crash  
SS3 - Checkout fixed  
SS4 - Checkout load test before optimization  
SS5 - Checkout load test after optimization  
SS6 - Events load test before optimization  
SS7 - Events load test after optimization  
SS8 - My-events load test before optimization  
SS9 - My-events load test after optimization  

## Optimizations

### Checkout Route
- Bottleneck: Crash line and inefficient loop.
- Change made: Commented crash line and optimized fee calculation.
- Why performance improved: Reduced CPU usage and prevented server crash.

### Events Route
- Bottleneck: Artificial waste loop causing delay.
- Change made: Removed waste loop.
- Why performance improved: Faster response time.

### My-events Route
- Bottleneck: Dummy loop causing CPU delay.
- Change made: Removed dummy loop.
- Why performance improved: Reduced execution time and improved throughput.

## How to Run
1. Create virtual environment  
2. Install requirements: `pip install -r requirements.txt`  
3. Run database script: `python insert_events.py`  
4. Start server: `python -m uvicorn main:app --reload`  
5. Open browser at `http://localhost:8000`
