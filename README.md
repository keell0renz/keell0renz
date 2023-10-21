<h1 align="center">Bohdan Agarkov</h1>

```python
from pydantic import BaseModel
from datetime import timedelta


class Developer(BaseModel):
    language: str = "Python"
    platform: str = "Linux"
    code_editor: str = "Cursor"
    shell: str = "zsh"
    experience: timedelta = timedelta(days=365*3)
    tech_stack: list[str] = [
        "FastAPI",
        "TortoiseORM / PostgreSQL",
        "Beanie / MongoDB",
        "Pydantic",
        "Prometheus / Grafana",
        "Render / Neon / MongoDB Atlas",
        "Docker",
        "Git",
        "JavaScript / TypeScript",
        "Next.js / Vercel"
    ]


class Entrepreneur(BaseModel):
    startup: str = "Cognitar"
    positions: list[str] = [
        "CEO", "CTO"
    ]


class Person(Developer, Entrepreneur):
    full_name: str = "Bohdan Agarkov"
    born: str = "Kyiv, Ukraine"
    age: int = 17
    university: str = "University of Amsterdam"
    languages: list[tuple[str, str]] = [
        ("Russian", "native"),
        ("Ukrainian", "native"),
        ("English", "C1")
    ]
```
