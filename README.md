<h1 align="center">Bohdan Agarkov</h1>

```python
from pydantic import BaseModel


class Developer(BaseModel):
    language: str = "Python"
    platform: str = "Linux"
    code_editor: str = "Cursor"
    shell: str = "zsh"
    experience: str = "Since 2020"
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
    birth_date: str = "23.12.2005"
    university: str = "University of Amsterdam"
    languages: list[tuple[str, str]] = [
        ("Russian", "native"),
        ("Ukrainian", "native"),
        ("English", "C1")
    ]
```
