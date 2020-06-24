# lein-artifact-registry
[![Clojars Project](https://img.shields.io/clojars/v/lurodrigo/lein-artifact-registry.svg)](https://clojars.org/lurodrigo/lein-artifact-registry)

Allows using Google Artifact Registry repositories [Leiningen](https://github.com/technomancy/leiningen) projects.
This is a minimal wrapper around [artifact-registry-maven-wagon](https://github.com/GoogleCloudPlatform/artifact-registry-maven-tools).
[Really](https://github.com/lurodrigo/lein-artifact-registry/blob/master/src/leiningen/wagons.clj).

## Usage

The plugin uses Google [Application Default Credentials](https://cloud.google.com/sdk/gcloud/reference/auth/application-default/login) for
authentication. Add this to your `project.clj`:

```clojure
:plugins [[lurodrigo/lein-artifact-registry "0.1.0"]]
:repositories [["snapshots" {:url "artifact-registry://..."}]
               ["releases"  {:url "artifact-registry://..."}]]
```

[Leiningen documentation](https://github.com/technomancy/leiningen/blob/master/doc/DEPLOY.md) might be useful
if you need more configuration info.

## License

Distributed under the MIT License.
