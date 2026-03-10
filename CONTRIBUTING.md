# Contributing to Socialler

## Branches

| Branch | Propósito |
|--------|-----------|
| `main` | Producción — siempre estable |
| `develop` | Integración — base para features |
| `feature/*` | Nuevas funcionalidades |
| `fix/*` | Bug fixes |
| `chore/*` | Mantenimiento, dependencias, CI |
| `release/*` | Preparación de release |

## Convención de commits (Conventional Commits)

```
<tipo>(<scope>): <descripción corta>

[cuerpo opcional]

[footer opcional]
```

### Tipos

| Tipo | Uso |
|------|-----|
| `feat` | Nueva funcionalidad |
| `fix` | Corrección de bug |
| `chore` | Mantenimiento, sin cambio funcional |
| `refactor` | Refactor sin cambio de comportamiento |
| `style` | Formato, espacios, sin cambio lógico |
| `test` | Agregar o corregir tests |
| `docs` | Documentación |
| `ci` | Cambios en CI/CD |
| `perf` | Mejoras de rendimiento |
| `revert` | Revertir commit anterior |

### Ejemplos

```
feat(auth): add biometric login support
fix(feed): resolve infinite scroll crash on iOS
chore(deps): upgrade flutter to 3.22
refactor(profile): extract avatar widget
ci: add android build workflow
```

## Pull Requests

- Usa la plantilla provista al abrir un PR
- El PR debe apuntar a `develop`, nunca directamente a `main`
- Mínimo **1 aprobación** antes de mergear
- Squash merge obligatorio para mantener historial limpio
- El título del PR debe seguir Conventional Commits

## Code Review

- Revisa en máximo **24 horas** en días hábiles
- Sé constructivo y específico en los comentarios
- Usa `nit:` para comentarios opcionales no bloqueantes

## Releases

- Se crean desde `develop` → rama `release/vX.X.X`
- Se mergea a `main` con tag de versión
- Seguimos [Semantic Versioning](https://semver.org): `MAJOR.MINOR.PATCH`
