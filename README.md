```text
most of my code is written by machines now.
my work is the system around them.
```

```text
                         intent
                            │
                       ┌────┴────┐
                       │  plan   │
                       └────┬────┘
        ┌─────────┬─────────┼─────────┬─────────┐
      agent     agent     agent     agent      agent        dozens in flight · one human
        │         │         │         │          │
      tree      tree      tree      tree       tree         one git worktree each
        │         │         │         │          │
     db·port   db·port   db·port   db·port    db·port       nothing shared that can collide
        └─────────┴────┬────┴─────────┴──────────┘
                    ┌──┴──┐
                    │queue│                                 priority · ram · load · machines
                    └──┬──┘
                  merge train
                       │
                     prod
```

<sub>field notes</sub>

- the expensive part of parallel agents isn't tokens. it's contention.
- a lock that doesn't know priority is just a polite race.
- the database is the real shared state. everything else is a file.
- if two agents can collide, eventually they will — at 3am, on the one run that mattered.
- the queue is the product.

<sub>parts of this machine are open source — pinned below.</sub>

<sub>systems @ [DataZen Tech](https://datazen.vn) · Vietnam · [thanhlc@datazen.vn](mailto:thanhlc@datazen.vn)</sub>
