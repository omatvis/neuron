# API contract (draft)

Base URL (local dev): set after Visual Studio project creation.
Example placeholder: `https://localhost:{PORT}`

All endpoints use **lowercase** paths.

## POST /predict

Purpose: return a prediction for an input vector.

### Request (JSON)
- `x` (number[]): input vector

Example:
```json
{ "x": [0, 1] }
```

### Response (JSON)
- `y` (number): predicted value

Example:
```json
{ "y": 0.5 }
```

### Notes
- Phase 1: `y` is computed by a dummy rule (placeholder).
- Phase 2+: `y` comes from a trained neural network model.

## POST /train (Phase 2+)

Purpose: train a tiny model on a toy dataset (XOR).

### Response idea (JSON)
- `epochs` (number)
- `finalLoss` (number)

Example:
```json
{ "epochs": 2000, "finalLoss": 0.03 }
```