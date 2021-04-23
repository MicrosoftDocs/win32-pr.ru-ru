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
# <a name="faq"></a><span data-ttu-id="988e4-103">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="988e4-103">FAQ</span></span>

### <a name="how-do-i-enable-directml-acceleration"></a><span data-ttu-id="988e4-104">Разделы справки включить ускорение Директмл?</span><span class="sxs-lookup"><span data-stu-id="988e4-104">How do I enable DirectML acceleration?</span></span> 

 
<span data-ttu-id="988e4-105">Устройство Директмл включено по умолчанию, предполагая, что доступен соответствующий GPU DirectX 12.</span><span class="sxs-lookup"><span data-stu-id="988e4-105">The DirectML device is enabled by default, assuming you have an appropriate DirectX 12 GPU available.</span></span> <span data-ttu-id="988e4-106">Операции TensorFlow будут автоматически назначены устройству Директмл, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="988e4-106">TensorFlow operations will automatically be assigned to the DirectML device if possible.</span></span> 

<span data-ttu-id="988e4-107">Если у вас возникли проблемы с определением того, работает ли ваша модель с помощью ускорения Директмл или нет, можно вставить `tf.debugging.set_log_device_placement(True)` как первый оператор программы, а TensorFlow будет печатать сведения о размещении устройства в консоли.</span><span class="sxs-lookup"><span data-stu-id="988e4-107">If you're having trouble determining whether your model is running using DirectML acceleration or not, you can put `tf.debugging.set_log_device_placement(True)` as the first statement of your program and TensorFlow will print device placement information to the console.</span></span>

### <a name="how-do-i-control-device-placement-of-specific-operations"></a><span data-ttu-id="988e4-108">Разделы справки управлять размещением устройств конкретных операций?</span><span class="sxs-lookup"><span data-stu-id="988e4-108">How do I control device placement of specific operations?</span></span> 
 

<span data-ttu-id="988e4-109">Как и для любого другого устройства (см. [руководство по TensorFlow: использование графического процессора](https://www.tensorflow.org/guide/gpu)), можно использовать `tf.device()` для управления устройством, на котором будет выполняться.</span><span class="sxs-lookup"><span data-stu-id="988e4-109">As with any other device (see [TensorFlow Guide: Use a GPU](https://www.tensorflow.org/guide/gpu)), you can use `tf.device()` to control which device to run on.</span></span> 
 

<span data-ttu-id="988e4-110">Строка устройства Директмл имеет значение `'DML'` .</span><span class="sxs-lookup"><span data-stu-id="988e4-110">The DirectML device string is `'DML'`.</span></span> 


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

### <a name="i-have-multiple-gpus-how-do-i-select-which-one-is-used-by-directml"></a><span data-ttu-id="988e4-111">У меня несколько GPU.</span><span class="sxs-lookup"><span data-stu-id="988e4-111">I have multiple GPUs.</span></span> <span data-ttu-id="988e4-112">Разделы справки выбрать, какой из них используется в Директмл?</span><span class="sxs-lookup"><span data-stu-id="988e4-112">How do I select which one is used by DirectML?</span></span>

<span data-ttu-id="988e4-113">Это можно сделать несколькими способами, в зависимости от того, требуется ли управлять его масштабом обработки или сеансами (или обоими).</span><span class="sxs-lookup"><span data-stu-id="988e4-113">There are a couple of different ways to do this, depending on whether you want to control it process-wide or per-session (or both).</span></span>

<span data-ttu-id="988e4-114">Если вы хотите контролировать, какие устройства видимы для TensorFlow всего процесса, используйте `DML_VISIBLE_DEVICES` переменную среды.</span><span class="sxs-lookup"><span data-stu-id="988e4-114">If you want to control which devices are visible to TensorFlow process-wide, use the `DML_VISIBLE_DEVICES` environment variable.</span></span> <span data-ttu-id="988e4-115">Если вы хотите контролировать его отдельно для каждого сеанса, используйте `tf.GPUOptions.visible_device_list` .</span><span class="sxs-lookup"><span data-stu-id="988e4-115">If you want to control it on a per-session basis, use `tf.GPUOptions.visible_device_list`.</span></span>

### <a name="how-do-i-use-the-dml_visible_devices-environment-variable-to-control-which-gpus-get-used-by-directml"></a><span data-ttu-id="988e4-116">Разделы справки использовать `DML_VISIBLE_DEVICES` переменную среды для управления тем, какие GPU используются в директмл?</span><span class="sxs-lookup"><span data-stu-id="988e4-116">How do I use the `DML_VISIBLE_DEVICES` environment variable to control which GPU(s) get used by DirectML?</span></span>

<span data-ttu-id="988e4-117">TensorFlow с Директмл поддерживает `DML_VISIBLE_DEVICES` переменную среды, которая принимает форму списка идентификаторов устройств с разделителями-запятыми (также называемых «индексами адаптера»). Если задано значение, только идентификаторы устройств в этом списке будут видимы для TensorFlow всего процесса.</span><span class="sxs-lookup"><span data-stu-id="988e4-117">TensorFlow with DirectML supports a `DML_VISIBLE_DEVICES` environment variable, which takes the form of a comma-separated list of device IDs (also known as "adapter indices".) When set, only the device IDs in that list will be visible to TensorFlow process-wide.</span></span> <span data-ttu-id="988e4-118">Устройства, исключенные с помощью `DML_VISIBLE_DEVICES` , не отображаются в списке физических устройств, доступных для TensorFlow.</span><span class="sxs-lookup"><span data-stu-id="988e4-118">Devices excluded using `DML_VISIBLE_DEVICES` will not appear in the list of physical devices available to TensorFlow.</span></span>

```python
import tensorflow as tf
tf.debugging.set_log_device_placement(True)
tf.enable_eager_execution()

a = tf.constant([1.])
b = tf.constant([2.])
c = tf.add(a, b)
print(c)
```

<span data-ttu-id="988e4-119">Ниже приведен пример выходных данных **без** `DML_VISIBLE_DEVICES` Set:</span><span class="sxs-lookup"><span data-stu-id="988e4-119">Here is example output **without** `DML_VISIBLE_DEVICES` set:</span></span>

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (NVIDIA TITAN V)
DirectML: creating device on adapter 1 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="988e4-120">С `DML_VISIBLE_DEVICES="1"`:</span><span class="sxs-lookup"><span data-stu-id="988e4-120">With `DML_VISIBLE_DEVICES="1"`:</span></span>

```
DirectML device enumeration: found 1 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="988e4-121">Обратите внимание, что при ограничении видимых устройств только индексом 1 (AMD Radeon RX 5700 XT) TensorFlow теперь присваивает этому устройству идентификатор 0 и делает его значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="988e4-121">Note that by restricting the visible devices to only index 1 (AMD Radeon RX 5700 XT), TensorFlow now assigns an ID of 0 to this device, and makes it the default.</span></span>

<span data-ttu-id="988e4-122">Вы также можете изменить порядок устройств с помощью этой переменной среды.</span><span class="sxs-lookup"><span data-stu-id="988e4-122">You may also re-order devices using this environment variable.</span></span> <span data-ttu-id="988e4-123">Например, параметр `DML_VISIBLE_DEVICES="1,0"` :</span><span class="sxs-lookup"><span data-stu-id="988e4-123">For example, setting `DML_VISIBLE_DEVICES="1,0"`:</span></span>

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
DirectML: creating device on adapter 1 (NVIDIA TITAN V)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="988e4-124">Обратите внимание, что два графических процессора (NVIDIA TITAN V и AMD Radeon RX 5700 XT) теперь имеют переключенные места.</span><span class="sxs-lookup"><span data-stu-id="988e4-124">Notice that the two GPUs (NVIDIA TITAN V and AMD Radeon RX 5700 XT) have now switched places.</span></span>

<span data-ttu-id="988e4-125">Чтобы предотвратить отображение конкретных устройств, можно указать недопустимый идентификатор (например, `-1` ) в списке с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="988e4-125">To prevent specific devices from being visible, you can supply an invalid ID (e.g. `-1`) in the comma-separated list.</span></span> <span data-ttu-id="988e4-126">Все идентификаторы устройств после неправильной записи игнорируются.</span><span class="sxs-lookup"><span data-stu-id="988e4-126">All device IDs after the invalid entry are ignored.</span></span> <span data-ttu-id="988e4-127">Это также можно использовать для полного отключения ускорения Директмл.</span><span class="sxs-lookup"><span data-stu-id="988e4-127">You can also use this to disable DirectML acceleration altogether.</span></span>

<span data-ttu-id="988e4-128">`DML_VISIBLE_DEVICES="-1"`:</span><span class="sxs-lookup"><span data-stu-id="988e4-128">`DML_VISIBLE_DEVICES="-1"`:</span></span>

```
DirectML device enumeration: found 0 compatible adapters.
Executing op Add in device /job:localhost/replica:0/task:0/device:CPU:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

### <a name="how-do-i-use-the-visible_device_list-session-option-to-control-which-gpus-directml-uses-to-run-the-session"></a><span data-ttu-id="988e4-129">Разделы справки использовать `visible_device_list` Параметр сеанса для управления тем, какие GPU директмл использует для запуска сеанса?</span><span class="sxs-lookup"><span data-stu-id="988e4-129">How do I use the `visible_device_list` session option to control which GPU(s) DirectML uses to run the session?</span></span>

<span data-ttu-id="988e4-130">Аналогично `DML_VISIBLE_DEVICES` , можно также задать аналогичную строку для управления видимыми устройствами на уровне сеанса.</span><span class="sxs-lookup"><span data-stu-id="988e4-130">Similar to `DML_VISIBLE_DEVICES`, you can also set a similar string to control visible devices at a session level.</span></span> <span data-ttu-id="988e4-131">`visible_device_list`Атрибут доступен в `GPUOptions` классе при создании сеанса TensorFlow.</span><span class="sxs-lookup"><span data-stu-id="988e4-131">The `visible_device_list` attribute is available on the `GPUOptions` class when creating your TensorFlow session.</span></span>

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

<span data-ttu-id="988e4-132">Дополнительные сведения см. в [справочнике по API TensorFlow гпуоптионс](https://www.tensorflow.org/versions/r1.15/api_docs/python/tf/GPUOptions#visible_device_list) .</span><span class="sxs-lookup"><span data-stu-id="988e4-132">You can read the [TensorFlow GPUOptions API reference](https://www.tensorflow.org/versions/r1.15/api_docs/python/tf/GPUOptions#visible_device_list) for more details.</span></span>