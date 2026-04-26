# Project: [Project Name]

## What This Is
[One or two sentences. What does this service do?]

## Architecture
[e.g. Reactive MongoDB change stream → Kafka publisher using Cake Pattern DI]

## Key Commands
```bash
# Build
sbt compile

# Test
sbt test

# Run
sbt run
```

## Stack
- Scala, Akka, Spring WebFlux / Reactor
- MongoDB (reactive), Kafka
- Cake Pattern for DI
- Protobuf for serialisation

## Code Conventions
- Idiomatic Scala only. No `asInstanceOf`, no unsafe casting.
- Sealed traits + exhaustive pattern matching over `instanceof`.
- Cake Pattern for DI — follow the existing module structure. Don't introduce new DI approaches.
- Functional style. Avoid mutable state unless there is a clear documented reason.
- Prefer `Either` / `Option` / `Try` over exceptions for expected failure paths.
- Reactive pipelines only — never introduce blocking calls on reactive/Akka threads.
- For blocking work (e.g. external APIs): wrap in `Future`, use a dedicated blocking dispatcher.

## Project Structure
```
src/
  main/scala/
    components/   ← Cake Pattern modules
    domain/       ← sealed trait ADTs
    pipeline/     ← reactive stream stages
  test/scala/
```

## Things Claude Got Wrong Before
[Add lines here as you go. This is the most valuable section.]
