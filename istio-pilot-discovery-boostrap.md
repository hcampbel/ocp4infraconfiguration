```bash
      1 2020-09-11T12:59:38.892217Z     info    FLAG: --appNamespace=""
      2 2020-09-11T12:59:38.892244Z     info    FLAG: --clusterRegistriesNamespace=""
      3 2020-09-11T12:59:38.892248Z     info    FLAG: --configDir=""
      4 2020-09-11T12:59:38.892252Z     info    FLAG: --consulserverInterval="2s"
      5 2020-09-11T12:59:38.892255Z     info    FLAG: --consulserverURL=""
      6 2020-09-11T12:59:38.892258Z     info    FLAG: --ctrlz_address="localhost"
      7 2020-09-11T12:59:38.892262Z     info    FLAG: --ctrlz_port="9876"
      8 2020-09-11T12:59:38.892265Z     info    FLAG: --disable-install-crds="false"
      9 2020-09-11T12:59:38.892268Z     info    FLAG: --discoveryCache="true"
     10 2020-09-11T12:59:38.892271Z     info    FLAG: --domain="cluster.local"
     11 2020-09-11T12:59:38.892274Z     info    FLAG: --grpcAddr=":15010"
     12 2020-09-11T12:59:38.892276Z     info    FLAG: --help="false"
     13 2020-09-11T12:59:38.892279Z     info    FLAG: --httpAddr=":8080"
     14 2020-09-11T12:59:38.892281Z     info    FLAG: --keepaliveInterval="30s"
     15 2020-09-11T12:59:38.892284Z     info    FLAG: --keepaliveMaxServerConnectionAge="30m0s"
     16 2020-09-11T12:59:38.892287Z     info    FLAG: --keepaliveTimeout="10s"
     17 2020-09-11T12:59:38.892289Z     info    FLAG: --kubeconfig=""
     18 2020-09-11T12:59:38.892291Z     info    FLAG: --log_as_json="false"
     19 2020-09-11T12:59:38.892296Z     info    FLAG: --log_caller=""
     20 2020-09-11T12:59:38.892298Z     info    FLAG: --log_output_level="default:info"
     21 2020-09-11T12:59:38.892301Z     info    FLAG: --log_rotate=""
     22 2020-09-11T12:59:38.892304Z     info    FLAG: --log_rotate_max_age="30"
     23 2020-09-11T12:59:38.892307Z     info    FLAG: --log_rotate_max_backups="1000"
     24 2020-09-11T12:59:38.892310Z     info    FLAG: --log_rotate_max_size="104857600"
     25 2020-09-11T12:59:38.892312Z     info    FLAG: --log_stacktrace_level="default:none"
     26 2020-09-11T12:59:38.892319Z     info    FLAG: --log_target="[stdout]"
     27 2020-09-11T12:59:38.892321Z     info    FLAG: --mcpInitialConnWindowSize="1048576"
     28 2020-09-11T12:59:38.892324Z     info    FLAG: --mcpInitialWindowSize="1048576"
     29 2020-09-11T12:59:38.892326Z     info    FLAG: --mcpMaxMsgSize="4194304"
     30 2020-09-11T12:59:38.892329Z     info    FLAG: --memberRollName="default"
     31 2020-09-11T12:59:38.892332Z     info    FLAG: --meshConfig="/etc/istio/config/mesh"
     32 2020-09-11T12:59:38.892334Z     info    FLAG: --monitoringAddr=":15014"
     33 2020-09-11T12:59:38.892337Z     info    FLAG: --namespace=""
     34 2020-09-11T12:59:38.892339Z     info    FLAG: --networksConfig="/etc/istio/config/meshNetworks"
     35 2020-09-11T12:59:38.892344Z     info    FLAG: --plugins="[authn,authz,health,mixer]"
     36 2020-09-11T12:59:38.892347Z     info    FLAG: --podLocalitySource="pod"
     37 2020-09-11T12:59:38.892349Z     info    FLAG: --profile="true"
     38 2020-09-11T12:59:38.892355Z     info    FLAG: --registries="[Kubernetes]"
     39 2020-09-11T12:59:38.892358Z     info    FLAG: --resync="1m0s"
     40 2020-09-11T12:59:38.892360Z     info    FLAG: --secureGrpcAddr=""
     41 2020-09-11T12:59:38.892363Z     info    FLAG: --trust-domain=""
     42 2020-09-11T12:59:38.972142Z     info    mesh configuration (*v1alpha1.MeshConfig)(0xc000024240)(mixer_check_server:"istio-policy.istio-system.svc.cluster.local:9091" mixer_report_server:"istio-telemetry.istio-system.svc.cluster.lo
     43 
     44 2020-09-11T12:59:38.972182Z     info    version OSSM_1.1.7-827d7a950192ea3691313ffc34b5a42adcacc362-Clean
2020-09-11T12:59:38.972256Z     info    flags (*bootstrap.PilotArgs)(0xc00051e200)({
     46  DiscoveryOptions: (envoy.DiscoveryServiceOptions) {
     47   HTTPAddr: (string) (len=5) ":8080",
     48   GrpcAddr: (string) (len=6) ":15010",
     49   SecureGrpcAddr: (string) "",
     50   MonitoringAddr: (string) (len=6) ":15014",
     51   EnableProfiling: (bool) true,
     52   EnableCaching: (bool) true
     53  },
     54  Namespace: (string) (len=12) "istio-system",
     55  Mesh: (bootstrap.MeshArgs) {
     56   ConfigFile: (string) (len=22) "/etc/istio/config/mesh",
     57   MixerAddress: (string) "",
     58   RdsRefreshDelay: (*types.Duration)(<nil>)
     59  },
     60  Config: (bootstrap.ConfigArgs) {
     61   ControllerOptions: (controller.Options) {
     62    WatchedNamespace: (string) "",
     63    WatchedNamespaces: (string) (len=12) "istio-system",
     64    PodLocalitySource: (string) (len=3) "pod",
     65    MemberRollName: (string) (len=7) "default",
     66    ResyncPeriod: (time.Duration) 1m0s,
     67    DomainSuffix: (string) (len=13) "cluster.local",
     68    ClusterID: (string) "",
     69    XDSUpdater: (model.XDSUpdater) <nil>,
     70    TrustDomain: (string) ""
     71   },
     72   ClusterRegistriesNamespace: (string) (len=12) "istio-system",
     73   KubeConfig: (string) "",
     74   FileDir: (string) "",
     75   Controller: (model.ConfigStoreCache) <nil>,
     76   DistributionCacheRetention: (time.Duration) 1m0s,
     77   DisableInstallCRDs: (bool) false,
     78   DistributionTrackingEnabled: (bool) true
     79  },
     80  Service: (bootstrap.ServiceArgs) {
     81   Registries: ([]string) (len=1 cap=1) {
     82    (string) (len=10) "Kubernetes"
     83   },
     84   Consul: (bootstrap.ConsulArgs) {
     85    Config: (string) "",
     86    ServerURL: (string) "",
     87    Interval: (time.Duration) 2s
     88   }
     89  },
     90  MeshConfig: (*v1alpha1.MeshConfig)(<nil>),
     91  NetworksConfigFile: (string) (len=30) "/etc/istio/config/meshNetworks",
     92  CtrlZOptions: (*ctrlz.Options)(0xc000619720)({
     93   Port: (uint16) 9876,
     94   Address: (string) (len=9) "localhost"
     95  }),
     96  Plugins: ([]string) (len=4 cap=4) {
     97   (string) (len=5) "authn",
     98   (string) (len=5) "authz",
     99   (string) (len=6) "health",
    100   (string) (len=5) "mixer"
    101  },
    102  MCPMaxMessageSize: (int) 4194304,
    103  MCPInitialWindowSize: (int) 1048576,
    104  MCPInitialConnWindowSize: (int) 1048576,
    105  KeepaliveOptions: (*keepalive.Options)(0xc000645a60)({
    106   Time: (time.Duration) 30s,
    107   Timeout: (time.Duration) 10s,
    108   MaxServerConnectionAge: (time.Duration) 30m0s,
    109   MaxServerConnectionAgeGrace: (time.Duration) 10s
    110  }),
    111  ForceStop: (bool) false
    112 })
    113 
    114 2020-09-11T12:59:38.972365Z     info    mesh networks configuration (*v1alpha1.MeshNetworks)(0xc000163d10)()
    115 
    116 2020-09-11T12:59:38.972376Z     info    mesh networks configuration post-resolution (*v1alpha1.MeshNetworks)(0xc000163d10)()
    117 
    118 2020-09-11T12:59:38.972402Z     info    nil certificate config
    119 2020-09-11T12:59:38.972429Z     info    parsed scheme: ""
    120 2020-09-11T12:59:38.972436Z     info    scheme "" not registered, fallback to default scheme
    121 2020-09-11T12:59:38.972452Z     info    ccResolverWrapper: sending update to cc: {[{istio-galley.istio-system.svc:9901 0  <nil>}] <nil>}
    122 2020-09-11T12:59:38.972455Z     info    ClientConn switching balancer to "pick_first"
    123 2020-09-11T12:59:38.983124Z     info    Adding Kubernetes registry adapter
    124 2020-09-11T12:59:38.983138Z     info    Primary Cluster name: Kubernetes
    125 2020-09-11T12:59:38.983143Z     info    Service controller watching Member Roll list default for services, endpoints, nodes and pods
    126 2020-09-11T12:59:38.990955Z     info    pickfirstBalancer: HandleSubConnStateChange: 0xc00060a040, CONNECTING
    127 2020-09-11T12:59:38.992438Z     info    ads     Starting ADS server with pushThrottle=100
    128 2020-09-11T12:59:39.006593Z     info    Setting up event handlers
    129 2020-09-11T12:59:39.006736Z     info    Starting Secrets controller
    130 2020-09-11T12:59:39.006777Z     info    Waiting for informer caches to sync
    131 2020-09-11T12:59:39.046108Z     info    ControlZ available at 127.0.0.1:9876
    132 2020-09-11T12:59:39.046136Z     warn    Run: this operation is not supported by mcp controller
    133 2020-09-11T12:59:39.046163Z     info    mcp     (re)trying to establish new MCP sink stream
    134 2020-09-11T12:59:39.052938Z     info    starting discovery service at http=[::]:8080 grpc=[::]:15010
    135 2020-09-11T12:59:39.246781Z     info    Handling event add for pod istio-egressgateway-79844b5bd8-ts4sk in namespace istio-system -> 10.130.0.8
    136 2020-09-11T12:59:39.246824Z     info    Handling event add for pod istio-policy-584dfd6ccc-rxdhh in namespace istio-system -> 10.130.0.19
    137 2020-09-11T12:59:39.246831Z     info    Handling event add for pod istio-telemetry-9cb9856dd-7vqtw in namespace istio-system -> 10.130.0.17
    138 2020-09-11T12:59:39.246837Z     info    Handling event add for pod prometheus-6b4b677d6c-hhrrq in namespace istio-system -> 10.130.0.14
    139 2020-09-11T12:59:39.246844Z     info    Handling event add for pod grafana-5b6ffc7867-vq7x7 in namespace istio-system -> 10.130.0.6
    140 2020-09-11T12:59:39.246849Z     info    Handling event add for pod istio-ingressgateway-74c55b479d-crn66 in namespace istio-system -> 10.130.0.3
    141 2020-09-11T12:59:39.246856Z     info    Handling event add for pod istio-pilot-7cb6c546d5-vw5zt in namespace istio-system -> 10.130.0.9
    142 2020-09-11T12:59:39.246862Z     info    Handling event add for pod kiali-6cc8488fb7-74kcn in namespace istio-system -> 10.130.0.2
    143 2020-09-11T12:59:39.246872Z     info    Handle EDS endpoint istio-citadel in namespace istio-system -> []
    144 2020-09-11T12:59:39.246883Z     info    Handle EDS endpoint istio-pilot in namespace istio-system -> []
    145 2020-09-11T12:59:39.246891Z     info    Handle EDS endpoint jaeger-agent in namespace istio-system -> []
    146 2020-09-11T12:59:39.246918Z     info    Handle EDS endpoint istio-policy in namespace istio-system -> [10.130.0.19 10.130.0.19 10.130.0.19]
    147 2020-09-11T12:59:39.246935Z     info    ads     Full push, new service istio-policy.istio-system.svc.cluster.local
    148 2020-09-11T12:59:39.246943Z     info    ads     Full push, service accounts changed, istio-policy.istio-system.svc.cluster.local
    149 2020-09-11T12:59:39.246953Z     info    Handle EDS endpoint prometheus in namespace istio-system -> []
    150 2020-09-11T12:59:39.246962Z     info    Handle EDS endpoint jaeger-collector-headless in namespace istio-system -> []
    151 2020-09-11T12:59:39.246973Z     info    Handle EDS endpoint jaeger-query in namespace istio-system -> []
    152 2020-09-11T12:59:39.246981Z     info    Handle EDS endpoint kiali in namespace istio-system -> []
    153 2020-09-11T12:59:39.246989Z     info    Handle EDS endpoint zipkin in namespace istio-system -> []
    154 2020-09-11T12:59:39.246999Z     info    Handle EDS endpoint istio-egressgateway in namespace istio-system -> []
```