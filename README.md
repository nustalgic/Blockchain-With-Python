# Module-18-Challenge

[![18-4-application-image.png](https://i.postimg.cc/SKwfxGnh/18-4-application-image.png)](https://postimg.cc/t1NxrWdS)

# Background

In this Challenge, I'm a fintech engineer who’s working at one of the five largest banks in the world. I was recently promoted to act as the lead developer on their decentralized finance team. The task is to build a blockchain-based ledger system, complete with a user-friendly web interface. This ledger should allow partner banks to conduct financial transactions (that is, to transfer money between senders and receivers) and to verify the integrity of the data in the ledger.

---

## Technologies

We'll be using Python and the following libraries to run and read our data. 

* [Streamlit](https://streamlit.io/)  - turns data scripts into shareable web apps in minutes. All in pure Python. No front‑end experience required.

* [Data Classes](https://docs.python.org/3/library/dataclasses.html)  - provides a decorator and functions for automatically adding generated special methods.

* [hashlib](https://docs.python.org/3/library/hashlib.html) - Secure hashes and message digests.
  
* [datetime](https://docs.python.org/3/library/datetime.html)  - Basic date and time types.

* [typing](https://docs.python.org/3/library/typing.html)  - Support for type hints.

* [pandas](https://pandas.pydata.org/docs/)  - an open source, BSD-licensed library providing high-performance, easy-to-use data structures and data analysis tools for the Python programming language.


## Installation Guide

In order for us to get the data we need we must import proper libraries.

```python
import streamlit as st
from dataclasses import dataclass
from typing import Any, List
import datetime as datetime
import pandas as pd
import hashlib
```


---
## Usage
* Create additional user input areas in the Streamlit application. 

```python
if st.button("Add Block"):
    prev_block = pychain.chain[-1]
    prev_block_hash = prev_block.hash_block()

    # Update `new_block` so that `Block` consists of an attribute named `record`
    # which is set equal to a `Record` that contains the `sender`, `receiver`,
    # and `amount` values

    new_block = Block(
        record= Record(sender,receiver,amount),
        creator_id=42,
        prev_hash=prev_block_hash
    )

    pychain.add_block(new_block)
    st.balloons()
```
---

[![Screen-Shot-2022-05-08-at-12-12-52-PM.png](https://i.postimg.cc/bY4yzCHJ/Screen-Shot-2022-05-08-at-12-12-52-PM.png)](https://postimg.cc/s19dmJLd)

[![Screen-Shot-2022-05-08-at-12-11-46-PM.png](https://i.postimg.cc/KjkHq5Rp/Screen-Shot-2022-05-08-at-12-11-46-PM.png)](https://postimg.cc/N2tDLm8R)



---

## Contributors

Brought to you by Elgin Braggs Jr.

---
## License

MIT