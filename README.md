# Flow types for verdaccio

Flow definitions for verdaccio plugins and internal code.


## Usage

To set up the types we need to add them to the `.flowconfig` flow configuration file.

```
[libs]
node_modules/@verdaccio/types/lib/

[options]
suppress_comment= \\(.\\|\n\\)*\\$FlowFixMe
unsafe.enable_getters_and_setters=true

[version]
^0.52.0
```

### Imports

```
import type {ILocalData, LocalStorage, Logger, Config} from '@verdaccio/types';

 class LocalData implements ILocalData {

  path: string;
  logger: Logger;
  data: LocalStorage;
  config: Config;
  locked: boolean;
  ...  
}
```


