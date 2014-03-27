### List of DNS Records and Zones that will need amending

| Zone          | DNS                         | Original     | New           | Notes                      |
| ------------- | ----------------------------| ------------ | --------------| ---------------------------|
| example.org   | ip-a.production.example.org | 192.0.2.1    | 198.51.100.1  | Production Jumpbox/Deploy  |
| example.org   | ip-b.production.example.org | 192.0.2.2    | 198.51.100.2  | Production Backend         |
| example.org   | ip-c.production.example.org | 192.0.2.3    | 198.51.100.3  | Production Bouncer         |
| example.org   | ip-d.production.example.org | 192.0.2.4    | 198.51.100.4  | Production Cache           |
| example.org   | ip-g.production.example.org | 192.0.2.5    | 198.51.100.5  | Production Logging         |
| example.org   | ip-h.production.example.org | 192.0.2.6    | 198.51.100.6  | Production EFG             |
| example.org   | ip-i.production.example.org | 192.0.2.7    | 198.51.100.7  | Production Redirector      |
| example.org   | ip-j.production.example.org | 192.0.2.8    | 198.51.100.8  | Production Licence Upload  |
| example.org   | ip-k.production.example.org | 192.0.2.9    | 198.51.100.9  | Production Frontend        |
| example.org   | ip-l.production.example.org | 192.0.2.10   | 198.51.100.10 | Production Monitoring      |
| example.org   | ip-m.production.example.org | 192.0.2.11   | 198.51.100.11 | Production Licensing Admin |
| example.org   | ip-n.production.example.org | 192.0.2.12   | 198.51.100.12 | Production Errbit          |
| example.org   | ip-a.staging.example.org    | 192.0.2.81   | 198.51.100.81 | Staging Jumpbox            |
| example.org   | ip-d.staging.example.org    | 192.0.2.84   | 198.51.100.84 | Staging Cache              |
| example.org   | ip-l.staging.example.org    | 192.0.2.90   | 198.51.100.90 | Staging Monitoring         |
