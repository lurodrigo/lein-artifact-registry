# lein-artifact-registry

Deploy and consume artifacts to/from Google Artifact Registry
[Leiningen](https://github.com/technomancy/leiningen) projects.

This is minimal wrapper around [artifact-registry-maven-wagon](https://github.com/GoogleCloudPlatform/artifact-registry-maven-tools).

## Usage

The plugin uses Google [Application Default Credentials](https://cloud.google.com/docs/authentication/production) for
authentication. Add this to your `project.clj`:

```clojure
:repositories [["snapshots" {:url           "artifact-registry://..."}]
               ["releases" {:url           "artifact-registry://..."}]]
:plugins [[polvotech/lein-artifact-registry "0.1.0"]]
```

See [Leiningen documentation](https://github.com/technomancy/leiningen/blob/master/doc/DEPLOY.md) for more information
about repository configuration.

## License

Distributed under the MIT License.
