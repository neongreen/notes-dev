# commented magics

First, create IPython profile:

```bash
uv run ipython profile create
```

Then add this code to `~/.ipython/profile_default/startup/50-magic.py`:

```python
import re


ip = get_ipython()


# allow -- %% and # %%
def commented_magic(input: list[str]) -> list[str]:
    if len(input) > 0:
        input[0] = re.sub(r"^(--|#) %%", r"%%", input[0])
    return input


ip.input_transformers_cleanup.append(commented_magic)  # type: ignore
```
