---
title: Часто задаваемые вопросы об ускорении с помощью GPU в WSL
description: Вопросы и ответы по ускорению GPU в подсистеме Windows для Linux
ms.topic: article
ms.date: 09/28/2020
ms.openlocfilehash: 7c55a8c06bd2b62c670cbf532bc3aa65ddd919d7
ms.sourcegitcommit: f58718691e8b989650108b8c70aaa471d17bf3aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "105719164"
---
# <a name="faq"></a>Вопросы и ответы

### <a name="how-do-i-enable-directml-acceleration"></a>Разделы справки включить ускорение Директмл? 

 
Устройство Директмл включено по умолчанию, предполагая, что доступен соответствующий GPU DirectX 12. Операции TensorFlow будут автоматически назначены устройству Директмл, если это возможно. 

Если у вас возникли проблемы с определением того, работает ли ваша модель с помощью ускорения Директмл или нет, можно вставить `tf.debugging.set_log_device_placement(True)` как первый оператор программы, а TensorFlow будет печатать сведения о размещении устройства в консоли.

### <a name="how-do-i-control-device-placement-of-specific-operations"></a>Разделы справки управлять размещением устройств конкретных операций? 
 

Как и для любого другого устройства (см. [руководство по TensorFlow: использование графического процессора](https://www.tensorflow.org/guide/gpu)), можно использовать `tf.device()` для управления устройством, на котором будет выполняться. 
 

Строка устройства Директмл имеет значение `'DML'` . 


```python 

import tensorflow as tf 

tf.debugging.set_log_device_placement(True) 

tf.enable_eager_execution() 

 

# Explicitly place tensors on the DirectML device 

with tf.device('/DML:0'): 

  a = tf.constant([1.0, 2.0, 3.0]) 

  b = tf.constant([4.0, 5.0, 6.0]) 

 

c = tf.add(a, b) 

print(c) 

``` 


``` 

Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([5. 7. 9.], shape=(3,), dtype=float32) 

```

### <a name="i-have-multiple-gpus-how-do-i-select-which-one-is-used-by-directml"></a>У меня несколько GPU. Разделы справки выбрать, какой из них используется в Директмл?

Это можно сделать несколькими способами, в зависимости от того, требуется ли управлять его масштабом обработки или сеансами (или обоими).

Если вы хотите контролировать, какие устройства видимы для TensorFlow всего процесса, используйте `DML_VISIBLE_DEVICES` переменную среды. Если вы хотите контролировать его отдельно для каждого сеанса, используйте `tf.GPUOptions.visible_device_list` .

### <a name="how-do-i-use-the-dml_visible_devices-environment-variable-to-control-which-gpus-get-used-by-directml"></a>Разделы справки использовать `DML_VISIBLE_DEVICES` переменную среды для управления тем, какие GPU используются в директмл?

TensorFlow с Директмл поддерживает `DML_VISIBLE_DEVICES` переменную среды, которая принимает форму списка идентификаторов устройств с разделителями-запятыми (также называемых «индексами адаптера»). Если задано значение, только идентификаторы устройств в этом списке будут видимы для TensorFlow всего процесса. Устройства, исключенные с помощью `DML_VISIBLE_DEVICES` , не отображаются в списке физических устройств, доступных для TensorFlow.

```python
import tensorflow as tf
tf.debugging.set_log_device_placement(True)
tf.enable_eager_execution()

a = tf.constant([1.])
b = tf.constant([2.])
c = tf.add(a, b)
print(c)
```

Ниже приведен пример выходных данных **без** `DML_VISIBLE_DEVICES` Set:

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (NVIDIA TITAN V)
DirectML: creating device on adapter 1 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

С `DML_VISIBLE_DEVICES="1"`:

```
DirectML device enumeration: found 1 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

Обратите внимание, что при ограничении видимых устройств только индексом 1 (AMD Radeon RX 5700 XT) TensorFlow теперь присваивает этому устройству идентификатор 0 и делает его значением по умолчанию.

Вы также можете изменить порядок устройств с помощью этой переменной среды. Например, параметр `DML_VISIBLE_DEVICES="1,0"` :

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
DirectML: creating device on adapter 1 (NVIDIA TITAN V)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

Обратите внимание, что два графических процессора (NVIDIA TITAN V и AMD Radeon RX 5700 XT) теперь имеют переключенные места.

Чтобы предотвратить отображение конкретных устройств, можно указать недопустимый идентификатор (например, `-1` ) в списке с разделителями-запятыми. Все идентификаторы устройств после неправильной записи игнорируются. Это также можно использовать для полного отключения ускорения Директмл.

`DML_VISIBLE_DEVICES="-1"`:

```
DirectML device enumeration: found 0 compatible adapters.
Executing op Add in device /job:localhost/replica:0/task:0/device:CPU:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

### <a name="how-do-i-use-the-visible_device_list-session-option-to-control-which-gpus-directml-uses-to-run-the-session"></a>Разделы справки использовать `visible_device_list` Параметр сеанса для управления тем, какие GPU директмл использует для запуска сеанса?

Аналогично `DML_VISIBLE_DEVICES` , можно также задать аналогичную строку для управления видимыми устройствами на уровне сеанса. `visible_device_list`Атрибут доступен в `GPUOptions` классе при создании сеанса TensorFlow.

```python
import tensorflow as tf

a = tf.constant([1.])
b = tf.constant([2.])
c = tf.add(a, b)

gpu_config = tf.GPUOptions()
gpu_config.visible_device_list = "1"

session = tf.Session(config=tf.ConfigProto(gpu_options=gpu_config))
print(session.run(c))
```

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 1 (AMD Radeon RX 5700 XT)
[3.]
```

Дополнительные сведения см. в [справочнике по API TensorFlow гпуоптионс](https://www.tensorflow.org/versions/r1.15/api_docs/python/tf/GPUOptions#visible_device_list) .