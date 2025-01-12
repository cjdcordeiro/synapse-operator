<!-- markdownlint-disable -->

<a href="../src/pebble.py#L0"><img align="right" style="float:right;" src="https://img.shields.io/badge/-source-cccccc?style=flat-square"></a>

# <kbd>module</kbd> `pebble.py`
Class to interact with pebble. 

**Global Variables**
---------------
- **STATS_EXPORTER_SERVICE_NAME**

---

<a href="../src/pebble.py#L41"><img align="right" style="float:right;" src="https://img.shields.io/badge/-source-cccccc?style=flat-square"></a>

## <kbd>function</kbd> `check_synapse_ready`

```python
check_synapse_ready() → CheckDict
```

Return the Synapse container ready check. 



**Returns:**
 
 - <b>`Dict`</b>:  check object converted to its dict representation. 


---

<a href="../src/pebble.py#L54"><img align="right" style="float:right;" src="https://img.shields.io/badge/-source-cccccc?style=flat-square"></a>

## <kbd>function</kbd> `check_synapse_alive`

```python
check_synapse_alive() → CheckDict
```

Return the Synapse container alive check. 



**Returns:**
 
 - <b>`Dict`</b>:  check object converted to its dict representation. 


---

<a href="../src/pebble.py#L67"><img align="right" style="float:right;" src="https://img.shields.io/badge/-source-cccccc?style=flat-square"></a>

## <kbd>function</kbd> `restart_synapse`

```python
restart_synapse(
    charm_state: CharmState,
    container: Container,
    is_main: bool = True
) → None
```

Restart Synapse service. 

This will force a restart even if its plan hasn't changed. 



**Args:**
 
 - <b>`charm_state`</b>:  Instance of CharmState 
 - <b>`container`</b>:  Synapse container. 
 - <b>`is_main`</b>:  if unit is main. 


---

<a href="../src/pebble.py#L89"><img align="right" style="float:right;" src="https://img.shields.io/badge/-source-cccccc?style=flat-square"></a>

## <kbd>function</kbd> `check_nginx_ready`

```python
check_nginx_ready() → CheckDict
```

Return the Synapse NGINX container check. 



**Returns:**
 
 - <b>`Dict`</b>:  check object converted to its dict representation. 


---

<a href="../src/pebble.py#L102"><img align="right" style="float:right;" src="https://img.shields.io/badge/-source-cccccc?style=flat-square"></a>

## <kbd>function</kbd> `check_mjolnir_ready`

```python
check_mjolnir_ready() → CheckDict
```

Return the Synapse Mjolnir service check. 



**Returns:**
 
 - <b>`Dict`</b>:  check object converted to its dict representation. 


---

<a href="../src/pebble.py#L115"><img align="right" style="float:right;" src="https://img.shields.io/badge/-source-cccccc?style=flat-square"></a>

## <kbd>function</kbd> `check_irc_bridge_ready`

```python
check_irc_bridge_ready() → CheckDict
```

Return the Synapse IRC bridge service check. 



**Returns:**
 
 - <b>`Dict`</b>:  check object converted to its dict representation. 


---

<a href="../src/pebble.py#L128"><img align="right" style="float:right;" src="https://img.shields.io/badge/-source-cccccc?style=flat-square"></a>

## <kbd>function</kbd> `replan_nginx`

```python
replan_nginx(container: Container, main_unit_address: str) → None
```

Replan Synapse NGINX service and regenerate configuration. 



**Args:**
 
 - <b>`container`</b>:  Charm container. 
 - <b>`main_unit_address`</b>:  Main unit address to be used in configuration. 


---

<a href="../src/pebble.py#L140"><img align="right" style="float:right;" src="https://img.shields.io/badge/-source-cccccc?style=flat-square"></a>

## <kbd>function</kbd> `replan_mjolnir`

```python
replan_mjolnir(container: Container) → None
```

Replan Synapse Mjolnir service. 



**Args:**
 
 - <b>`container`</b>:  Charm container. 


---

<a href="../src/pebble.py#L150"><img align="right" style="float:right;" src="https://img.shields.io/badge/-source-cccccc?style=flat-square"></a>

## <kbd>function</kbd> `replan_irc_bridge`

```python
replan_irc_bridge(container: Container) → None
```

Replan Synapse IRC bridge service. 



**Args:**
 
 - <b>`container`</b>:  Charm container. 


---

<a href="../src/pebble.py#L160"><img align="right" style="float:right;" src="https://img.shields.io/badge/-source-cccccc?style=flat-square"></a>

## <kbd>function</kbd> `replan_stats_exporter`

```python
replan_stats_exporter(container: Container, charm_state: CharmState) → None
```

Replan Synapse StatsExporter service. 



**Args:**
 
 - <b>`container`</b>:  Charm container. 
 - <b>`charm_state`</b>:  Instance of CharmState. 


---

<a href="../src/pebble.py#L228"><img align="right" style="float:right;" src="https://img.shields.io/badge/-source-cccccc?style=flat-square"></a>

## <kbd>function</kbd> `get_worker_config`

```python
get_worker_config(unit_number: str) → dict
```

Get worker configuration. 



**Args:**
 
 - <b>`unit_number`</b>:  Unit number to be used in the worker_name field. 



**Returns:**
 Worker configuration. 


---

<a href="../src/pebble.py#L261"><img align="right" style="float:right;" src="https://img.shields.io/badge/-source-cccccc?style=flat-square"></a>

## <kbd>function</kbd> `change_config`

```python
change_config(
    charm_state: CharmState,
    container: Container,
    is_main: bool = True,
    unit_number: str = ''
) → None
```

Change the configuration (main and worker). 



**Args:**
 
 - <b>`charm_state`</b>:  Instance of CharmState 
 - <b>`container`</b>:  Charm container. 
 - <b>`is_main`</b>:  if unit is main. 
 - <b>`unit_number`</b>:  unit number id to set the worker name. 



**Raises:**
 
 - <b>`PebbleServiceError`</b>:  if something goes wrong while interacting with Pebble. 


---

<a href="../src/pebble.py#L356"><img align="right" style="float:right;" src="https://img.shields.io/badge/-source-cccccc?style=flat-square"></a>

## <kbd>function</kbd> `enable_redis`

```python
enable_redis(charm_state: CharmState, container: Container) → None
```

Enable Redis while receiving on_redis_relation_updated event. 



**Args:**
 
 - <b>`container`</b>:  Charm container. 
 - <b>`charm_state`</b>:  Instance of CharmState. 



**Raises:**
 
 - <b>`PebbleServiceError`</b>:  if something goes wrong while interacting with Pebble. 


---

<a href="../src/pebble.py#L376"><img align="right" style="float:right;" src="https://img.shields.io/badge/-source-cccccc?style=flat-square"></a>

## <kbd>function</kbd> `enable_saml`

```python
enable_saml(charm_state: CharmState, container: Container) → None
```

Enable SAML while receiving on_saml_data_available event. 



**Args:**
 
 - <b>`charm_state`</b>:  Instance of CharmState 
 - <b>`container`</b>:  Charm container. 



**Raises:**
 
 - <b>`PebbleServiceError`</b>:  if something goes wrong while interacting with Pebble. 


---

<a href="../src/pebble.py#L396"><img align="right" style="float:right;" src="https://img.shields.io/badge/-source-cccccc?style=flat-square"></a>

## <kbd>function</kbd> `enable_smtp`

```python
enable_smtp(charm_state: CharmState, container: Container) → None
```

Enable SMTP while receiving on_smtp_data_available event. 



**Args:**
 
 - <b>`charm_state`</b>:  Instance of CharmState 
 - <b>`container`</b>:  Charm container. 



**Raises:**
 
 - <b>`PebbleServiceError`</b>:  if something goes wrong while interacting with Pebble. 


---

<a href="../src/pebble.py#L416"><img align="right" style="float:right;" src="https://img.shields.io/badge/-source-cccccc?style=flat-square"></a>

## <kbd>function</kbd> `enable_media`

```python
enable_media(charm_state: CharmState, container: Container) → None
```

Enable S3 Media while receiving on_media_data_available event. 



**Args:**
 
 - <b>`charm_state`</b>:  Instance of CharmState 
 - <b>`container`</b>:  Charm container. 



**Raises:**
 
 - <b>`PebbleServiceError`</b>:  if something goes wrong while interacting with Pebble. 


---

<a href="../src/pebble.py#L436"><img align="right" style="float:right;" src="https://img.shields.io/badge/-source-cccccc?style=flat-square"></a>

## <kbd>function</kbd> `reset_instance`

```python
reset_instance(charm_state: CharmState, container: Container) → None
```

Reset instance. 



**Args:**
 
 - <b>`charm_state`</b>:  Instance of CharmState 
 - <b>`container`</b>:  Charm container. 



**Raises:**
 
 - <b>`PebbleServiceError`</b>:  if something goes wrong while interacting with Pebble. 


---

## <kbd>class</kbd> `PebbleServiceError`
Exception raised when something fails while interacting with Pebble. 

Attrs:  msg (str): Explanation of the error. 

<a href="../src/pebble.py#L32"><img align="right" style="float:right;" src="https://img.shields.io/badge/-source-cccccc?style=flat-square"></a>

### <kbd>function</kbd> `__init__`

```python
__init__(msg: str)
```

Initialize a new instance of the PebbleServiceError exception. 



**Args:**
 
 - <b>`msg`</b> (str):  Explanation of the error. 





