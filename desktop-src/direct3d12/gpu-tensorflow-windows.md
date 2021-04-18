---
title: Tensorflow с Директмл в Windows
description: Включение TensorFlow с Директмл непосредственно в Windows
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: 665ba456d59f09f27a435135468cf71cb6f6f014
ms.sourcegitcommit: 8f3fb56ebad4615389dec5c74d965dec84ad4123
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/22/2020
ms.locfileid: "105719118"
---
# <a name="enable-tensorflow-with-directml-on-windows"></a>Включение TensorFlow с помощью DirectML в Windows

Эта предварительная версия предоставляет учащимся и начинающим пользователям способ приступить к созданию знаний в пространстве машинного обучения на имеющемся оборудовании с помощью пакета TensorFlow с Директмл. После настройки пользователи могут начать с [моделей учебников по TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) или [наших примеров директмл](https://github.com/microsoft/DirectML). 

> [!NOTE]
> Приведенная ниже функция доступна в предварительной версии и может изменяться.

## <a name="check-your-version-of-windows"></a>Проверка версии Windows 

TensorFlow с пакетом Директмл в собственном Windows работает начиная с Windows 10 версии 1709 (сборка 16299 или более поздняя версия). Номер версии сборки можно проверить, выполнив `winver` команду **Run** (клавиша Windows + R).

## <a name="check-for-gpu-driver-updates"></a>Проверить наличие обновлений драйвера GPU 

Убедитесь, что установлен последний драйвер GPU. Выберите **Проверка обновлений** в разделе **Центр обновления Windows** приложения "Параметры".

## <a name="set-up-the-tensorflow-with-directml-preview"></a>Настройка TensorFlow с помощью предварительной версии Директмл 

Рекомендуется настроить виртуальную среду Python в Windows. Существует множество средств, которые можно использовать для настройки виртуальной среды Python. для получения этих инструкций мы будем использовать [Miniconda Anaconda](https://docs.conda.io/en/latest/miniconda.html). В оставшейся части этой программы установки предполагается, что вы используете среду miniconda. 

### <a name="set-up-python-environment"></a>Настройка среды Python 

Скачайте и установите [установщик Windows Miniconda](https://docs.conda.io/en/latest/miniconda.html#windows-installers) в системе. Для установки на сайте Anaconda есть [Дополнительные рекомендации](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html) . После установки Miniconda Создайте среду с помощью Python с именем **директмл** и активируйте ее с помощью следующих команд. 

> [!NOTE]
> В приведенных ниже командах мы используем Python 3,6. Однако пакет tensorflow-директмл работает в среде Python 3,5, 3,6 или 3,7. 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a>Установка Tensorflow с помощью пакета Директмл 

Установите пакет TensorFlow с серверной частью Директмл в PIP, выполнив следующую команду.

> [!NOTE]
> Пакет tensorflow-директмл поддерживает только TensorFlow 1,15. 

```
pip install tensorflow-directml
```

После установки пакета tensorflow-директмл можно убедиться, что он работает правильно, добавив два десятка. Скопируйте следующие строки в интерактивный сеанс Python. 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

Вы должны увидеть результат, аналогичный приведенному ниже, с оператором Add, размещенным на устройстве DML. 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library DirectMLba106a7c621ea741d2159d8708ee581c11918380.dll 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a>Tensorflow с примерами Директмл и отзывами 

Теперь вы готовы начать обучение в МАШИНном обучении. Ознакомьтесь с [учебниками по TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) или [примерами](https://github.com/microsoft/DirectML). Мы использовали это содержимое как проверку для этого начального предварительного пакета TensorFlow с серверной частью Директмл. 

Если у вас возникли проблемы или вы получили отзыв о TensorFlow с пакетом Директмл, обратитесь [к нашей группе](https://github.com/microsoft/DirectML/issues). 
