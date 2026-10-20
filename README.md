# Online Food Order Processing System

A small, menu-driven Python project demonstrating the **Queue** data structure and the **First-In-First-Out (FIFO)** principle for food order processing. This project follows the scope of the supplied mini-project report and is ready to upload to GitHub.

## Features

- Place an order with customer name, food item, and quantity
- Generate a unique, incrementing order ID during the current run
- View pending orders
- Process the oldest pending order first (FIFO)
- Keep completed orders in a separate queue
- Validate empty names/items and non-positive quantities
- Handle an empty pending queue and invalid menu choices
- Unit tests using Python's built-in `unittest` framework

## Requirements

- Python 3.10 or newer
- No third-party packages required

## Run the project

1. Install Python 3.10+ if it is not already installed.
2. Open a terminal in this repository folder.
3. Run:

   ```bash
   python main.py
   ```

On some systems, use `python3 main.py` instead.

## Run tests

```bash
python -m unittest discover -s tests -v
```

## How the queue works

`place_order()` adds each order to the rear of `pending_orders` using `deque.append()` (enqueue). `process_next_order()` removes the oldest order from the front using `deque.popleft()` (dequeue), updates its status to `Completed`, and adds it to `completed_orders`.

```text
Place Order -> Enqueue -> Pending Queue -> Dequeue -> Completed Queue
```

Enqueue and dequeue operations are approximately **O(1)**. Displaying orders takes **O(n)** time.

## Repository structure

```text
food-order-processing-system/
├── main.py
├── tests/
│   └── test_order_system.py
├── README.md
├── .gitignore
└── LICENSE
```

## Scope and limitations

This is an educational, console-based prototype. Orders are held in memory and are lost when the program exits. It does not include a database, login/authentication, online payments, delivery tracking, or a graphical user interface.

## GitHub upload

Create a new empty repository on GitHub, then from this folder run:

```bash
git init
git add .
git commit -m "Add online food order processing system"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

Replace the example remote URL with your own repository URL.
[README.md](https://github.com/user-attachments/files/33711460/README.md)
[main.py](https://github.com/user-attachments/files/33711458/main.py)
