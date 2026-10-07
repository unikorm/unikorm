<pre>
<b>adamko@unikorm</b>:<b>~</b>$ dmesg | tail -8
[    0.000000] kernel: booting unikorm ...
[    0.000137] mount  /home/adamko .............................. [  OK  ]
[    0.000256] load   typescript · java · go · linux ............ [  OK  ]
[    0.000512] start  momentkaph_fe.service ..................... [  OK  ]
[    0.000513] start  momentkaph_be.service ..................... [  OK  ]
[    0.001024] start  my_web.service ............................ [ BUSY ]
[    0.002048] start  witche_tui.service ........................ [ WAIT ]
[    0.004096] start  serv_my_way.service ....................... [ WAIT ]

██╗   ██╗███╗   ██╗██╗██╗  ██╗ ██████╗ ██████╗ ███╗   ███╗
██║   ██║████╗  ██║██║██║ ██╔╝██╔═══██╗██╔══██╗████╗ ████║
██║   ██║██╔██╗ ██║██║█████╔╝ ██║   ██║██████╔╝██╔████╔██║
██║   ██║██║╚██╗██║██║██╔═██╗ ██║   ██║██╔══██╗██║╚██╔╝██║
╚██████╔╝██║ ╚████║██║██║  ██╗╚██████╔╝██║  ██║██║ ╚═╝ ██║
 ╚═════╝ ╚═╝  ╚═══╝╚═╝╚═╝  ╚═╝ ╚═════╝ ╚═╝  ╚═╝╚═╝     ╚═╝
  i'd rather read the rfc than install the package.

<b>adamko@unikorm</b>:<b>~</b>$ whoami --verbose
  user     adamko
  writes   typescript · java · synapse xml · go (learning, on purpose)
  likes    zero dependencies · linux internals · anything in a terminal
  method   model the domain first · plan backwards from v1.0
  prod     <a href="https://www.momentkaph.sk">momentkaph.sk</a>   photography portfolio, built for my wife

<b>adamko@unikorm</b>:<b>~</b>$ ps -u adamko -o pid,stat,cmd
  PID  STAT  CMD
  101  Ss    <a href="https://github.com/unikorm/momentkaph_fe">momentkaph_fe</a>    static site      live · momentkaph.sk
  102  Ss    <a href="https://github.com/unikorm/momentkaph_be">momentkaph_be</a>    zero-dep api     live · api.momentkaph.sk
  201  R+    <a href="https://github.com/unikorm/my_web">my_web</a>           shell-as-site    building · unikorm.eu
  301  D     <a href="https://github.com/unikorm/witche_tui">witche_tui</a>       linux monitor    designing · go tui
  302  D     <a href="https://github.com/unikorm/serv_my_way">serv_my_way</a>      mini-nginx       designing · go stdlib
  <i># Ss = up in prod   R+ = in the foreground   D = deep in design docs</i>

<b>adamko@unikorm</b>:<b>~</b>$ cat ~/projects/*/README

╭─ <b>momentkaph</b> ──────────────────────────────────────────────── [ LIVE ] ─╮
│ photography portfolio for my wife. two repos, one product.             │
│                                                                        │
│   browser ──► momentkaph.sk ───────── fe  html · css · vanilla js      │
│      │                                                                 │
│      └──────► api.momentkaph.sk ───── nginx ──► be ──┬──► DO Spaces    │
│                                                      └──► Resend       │
│                                                                        │
│   fe   no framework · avif galleries · sk/en i18n · sftp deploy        │
│   be   typescript on bare node with ZERO runtime dependencies:         │
│        hand-rolled aws sigv4, resend client and avif header parser     │
│        nginx + app as two layers of one defense · gh actions ci/cd     │
│                                                                        │
│   repo <a href="https://github.com/unikorm/momentkaph_fe">momentkaph_fe</a> · <a href="https://github.com/unikorm/momentkaph_be">momentkaph_be</a>        site <a href="https://www.momentkaph.sk">momentkaph.sk</a>         │
╰────────────────────────────────────────────────────────────────────────╯

╭─ <b>my_web</b> ──────────────────────────────────────────────── [ BUILDING ] ─╮
│ unikorm.eu · a personal site that is one long shell session.           │
│                                                                        │
│   visitor@unikorm:~$ ls /                                              │
│   boot  dev  etc  home  lost+found  opt  proc  tmp  usr  var           │
│   visitor@unikorm:~$ ls /var/log        # the blog. posts are logs.    │
│   visitor@unikorm:~$ cat /dev/urandom   # one random thought           │
│                                                                        │
│   vanilla es modules · no framework · no bundler · no backend          │
│   fake ubuntu fs as the content model · commands are pure functions    │
│   (argv, ctx) =&gt; Line[] · the renderer is the only thing touching DOM  │
│                                                                        │
│   repo <a href="https://github.com/unikorm/my_web">my_web</a>                                                          │
╰────────────────────────────────────────────────────────────────────────╯

╭─ <b>witche_tui</b> ────────────────────────────────────────────── [ DESIGN ] ─╮
│ witcher's medallion · your linux box, drawn as the Continent.          │
│                                                                        │
│   MAHAKAM FORGES     cpu    forge 2  ▓▓▓▓▓▓▓▓▓▓▓░  92% !               │
│   REDANIAN TREASURY  mem    in use   ▓▓▓▓▓▓▓░░░░░  9.8G                │
│   TOXICITY           load    1 min   ▓▓▓▓░░░░░░░░  1.92                │
│   NOTICE BOARD       procs  » 41872  go build     hunting              │
│   SIGNS              Aard = SIGTERM   Igni = SIGKILL   Axii = renice   │
│                                                                        │
│   go · bubble tea · lip gloss · reads /proc straight from the kernel   │
│   every number is real · press L for the linux lesson under the skin   │
│                                                                        │
│   repo <a href="https://github.com/unikorm/witche_tui">witche_tui</a>                                                      │
╰────────────────────────────────────────────────────────────────────────╯

╭─ <b>serv_my_way</b> ───────────────────────────────────────────── [ DESIGN ] ─╮
│ mini-nginx · a reverse proxy rebuilt from raw tcp, to really get it.   │
│                                                                        │
│   client ──tcp/tls──► master ──spawns──► worker ──┬──► backend A       │
│                       signals            http/1.1 ├──► backend B       │
│                       reload             by hand  └──► backend C       │
│                                                                        │
│   go stdlib only · no net/http on the proxy path · sni parsed by hand  │
│   master/worker processes · load balancing · health checks             │
│   rate limiting · caching · one static linux binary                    │
│                                                                        │
│   repo <a href="https://github.com/unikorm/serv_my_way">serv_my_way</a>                                                     │
╰────────────────────────────────────────────────────────────────────────╯

<b>adamko@unikorm</b>:<b>~</b>$ tree /usr/local/stack
/usr/local/stack
├── lang/    typescript · javascript · java · go · bash · synapse xml
├── front/   html · css · vanilla js   (no framework is a feature)
├── back/    node (builtins only) · rest · aws sigv4 · resend
├── infra/   linux · nginx · systemd · gh actions
└── head/    domain modeling · backwards planning · reading about stuff

<b>adamko@unikorm</b>:<b>~</b>$ cat ~/.plan
  [ live ]  keep momentkaph.sk fast, boring and online
  [ wip  ]  turn unikorm.eu into a shell worth exploring
  [ next ]  learn go by forging the medallion
  [ next ]  rebuild nginx from raw bytes until it clicks

<b>adamko@unikorm</b>:<b>~</b>$ █
</pre>
