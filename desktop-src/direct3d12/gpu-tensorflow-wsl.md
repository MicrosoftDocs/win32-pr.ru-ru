---
title: Tensorflow с Директмл на WSL 2
description: Включение TensorFlow с Директмл в подсистеме Windows для Linux
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: bfd776013e417760d52134d697439be60c5a1ae8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "105719162"
---
# <a name="enable-tensorflow-with-directml-in-wsl-2"></a>Включение TensorFlow с DirectML в WSL 2

Эта предварительная версия предоставляет учащимся и начинающим пользователям способ начать создание знаний в пространстве машинного обучения на имеющемся оборудовании с помощью пакета TensorFlow с Директмл. После настройки пользователи могут начать с [моделей учебников по TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) или наших [примеров директмл](https://github.com/microsoft/DirectML). 

> [!NOTE]
> Следующие функции доступны в предварительных версиях Windows 10 и могут изменяться.

## <a name="install-the-latest-windows-insider-dev-channel-build"></a>Установите последнюю сборку канала разработки для программы предварительной оценки Windows 

Чтобы использовать эту предварительную версию, необходимо [зарегистрироваться для использования программы предварительной оценки Windows](https://insider.windows.com/getting-started/#register). После этого выполните следующие [инстуктионс](https://insider.windows.com/getting-started/#install) , чтобы установить последнюю сборку Insider Preview. При выборе параметров убедитесь, что выбран [канал разработки](/windows-insider/flight-hub/#active-development-builds-of-windows-10). 

Для этой предварительной версии требуется сборка 20150 или более поздняя версия. Номер версии сборки можно проверить, выполнив `winver` команду **Run** (клавиша Windows + R).

## <a name="install-the-preview-gpu-driver"></a>Установка драйвера GPU для предварительной версии 

Перед установкой TensorFlow с пакетом Директмл в WSL 2 необходимо установить драйверы от поставщика оборудования GPU. Эти драйверы позволяют графическому процессору Windows работать с WSL 2.

### <a name="amd"></a>AMD 

[Скачайте и установите драйвер предварительной версии AMD](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support) с веб-сайта. Этот предварительный драйвер поддерживает следующее оборудование: 

* AMD Radeon™ серии RX и Radeon™ вии Graphics. 
* Графика AMD Radeon™ Pro. 
* Процессоры AMD ризен™ и ризен™ PRO с Radeon™ Вега Graphics. 
* Процессоры AMD ризен™ и ризен™ PRO для мобильных устройств с Radeon™ Вега Graphics. 

Полный список совместимых продуктов AMD см. в заметках о выпуске AMD. 

### <a name="intel"></a>Intel 

[Скачайте и установите драйвер Intel Preview](https://downloadcenter.intel.com/download/29526) для использования с директмл на своем веб-сайте. 

### <a name="nvidia"></a>NVIDIA 

[Скачайте и установите драйвер для предварительной версии NVIDIA](https://developer.nvidia.com/cuda/wsl/download) для использования с директмл на своем веб-сайте. Дополнительные сведения см. на странице о [GPU NVIDIA в подсистеме Windows для Linux (WSL)](https://developer.nvidia.com/cuda/wsl) .

## <a name="set-up-the-tensorflow-with-directml-preview"></a>Настройка TensorFlow с помощью предварительной версии Директмл 

### <a name="install-wsl-2"></a>Установка WSL 2 

Установив приведенный выше драйвер, убедитесь, что вы [включили WSL 2](/windows/wsl/install-win10) и [установите дистрибутив на основе glibc](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (например, Ubuntu или Debian). Для нашего тестирования мы использовали Ubuntu. Убедитесь, что у вас установлена последняя версия ядра, выбрав пункт **проверить наличие обновлений** в разделе **Центр обновления Windows** приложения "Параметры". 

> [!NOTE]
> При обновлении Windows убедитесь, что у вас есть **обновления для получения других продуктов Майкрософт** . Его можно найти в **дополнительных параметрах** в разделе **Центр обновления Windows** приложения "Параметры". 

Для этой предварительной версии необходима версия ядра 4.19.121 или более поздняя. Номер версии можно проверить, выполнив следующую команду в PowerShell. 

```
wsl cat /proc/version
```

### <a name="set-up-python-environment"></a>Настройка среды Python 

Рекомендуется настроить виртуальную среду Python в экземпляре WSL 2. Существует множество средств, которые можно использовать для настройки виртуальной среды Python. для получения этих инструкций мы будем использовать [Miniconda Anaconda](https://docs.conda.io/en/latest/miniconda.html). В оставшейся части этой программы установки предполагается, что вы используете среду miniconda. 

Установите Miniconda, следуя [указаниям на сайте Anaconda](https://conda.io/projects/conda/en/latest/user-guide/install/index.html), или выполнив следующие команды в WSL. 

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh 
bash Miniconda3-latest-Linux-x86_64.sh 
```

После установки Miniconda в WSL Создайте среду с помощью Python с именем "директмл" и активируйте ее с помощью следующих команд. 

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

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library libdirectml.so.ba106a7c621ea741d21598708ee581c11918380 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a>Tensorflow с примерами Директмл и отзывами 

Теперь вы готовы начать обучение в МАШИНном обучении. Ознакомьтесь с [учебниками по TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) или [примерами](https://github.com/microsoft/DirectML). Мы использовали это содержимое как проверку для этого первоначального предварительного пакета TensorFlow с Директмл. 

Если у вас возникли проблемы или вы получили отзыв о TensorFlow с пакетом Директмл, обратитесь [к нашей группе](https://github.com/microsoft/DirectML/issues).
