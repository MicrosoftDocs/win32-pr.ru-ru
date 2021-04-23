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
# <a name="enable-tensorflow-with-directml-on-windows"></a><span data-ttu-id="349d4-103">Включение TensorFlow с помощью DirectML в Windows</span><span class="sxs-lookup"><span data-stu-id="349d4-103">Enable TensorFlow with DirectML on Windows</span></span>

<span data-ttu-id="349d4-104">Эта предварительная версия предоставляет учащимся и начинающим пользователям способ приступить к созданию знаний в пространстве машинного обучения на имеющемся оборудовании с помощью пакета TensorFlow с Директмл.</span><span class="sxs-lookup"><span data-stu-id="349d4-104">This preview provides students and beginners a way to start building their knowledge in the ML space on their existing hardware by using the the TensorFlow with DirectML package.</span></span> <span data-ttu-id="349d4-105">После настройки пользователи могут начать с [моделей учебников по TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) или [наших примеров директмл](https://github.com/microsoft/DirectML).</span><span class="sxs-lookup"><span data-stu-id="349d4-105">Once set up, users can start with the [TensorFlow tutorial models](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our DirectML samples](https://github.com/microsoft/DirectML).</span></span> 

> [!NOTE]
> <span data-ttu-id="349d4-106">Приведенная ниже функция доступна в предварительной версии и может изменяться.</span><span class="sxs-lookup"><span data-stu-id="349d4-106">The following feature is in preview, and are subject to change.</span></span>

## <a name="check-your-version-of-windows"></a><span data-ttu-id="349d4-107">Проверка версии Windows</span><span class="sxs-lookup"><span data-stu-id="349d4-107">Check your version of Windows</span></span> 

<span data-ttu-id="349d4-108">TensorFlow с пакетом Директмл в собственном Windows работает начиная с Windows 10 версии 1709 (сборка 16299 или более поздняя версия).</span><span class="sxs-lookup"><span data-stu-id="349d4-108">The TensorFlow with DirectML package on native Windows works starting with Windows 10 Version 1709 (Build 16299 or higher).</span></span> <span data-ttu-id="349d4-109">Номер версии сборки можно проверить, выполнив `winver` команду **Run** (клавиша Windows + R).</span><span class="sxs-lookup"><span data-stu-id="349d4-109">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="check-for-gpu-driver-updates"></a><span data-ttu-id="349d4-110">Проверить наличие обновлений драйвера GPU</span><span class="sxs-lookup"><span data-stu-id="349d4-110">Check for GPU driver updates</span></span> 

<span data-ttu-id="349d4-111">Убедитесь, что установлен последний драйвер GPU.</span><span class="sxs-lookup"><span data-stu-id="349d4-111">Ensure you have the latest GPU driver installed.</span></span> <span data-ttu-id="349d4-112">Выберите **Проверка обновлений** в разделе **Центр обновления Windows** приложения "Параметры".</span><span class="sxs-lookup"><span data-stu-id="349d4-112">Select **Check for updates** in the **Windows Update** section of the Settings app.</span></span>

## <a name="set-up-the-tensorflow-with-directml-preview"></a><span data-ttu-id="349d4-113">Настройка TensorFlow с помощью предварительной версии Директмл</span><span class="sxs-lookup"><span data-stu-id="349d4-113">Set up the TensorFlow with DirectML preview</span></span> 

<span data-ttu-id="349d4-114">Рекомендуется настроить виртуальную среду Python в Windows.</span><span class="sxs-lookup"><span data-stu-id="349d4-114">We recommend setting up a virtual Python environment inside Windows.</span></span> <span data-ttu-id="349d4-115">Существует множество средств, которые можно использовать для настройки виртуальной среды Python. для получения этих инструкций мы будем использовать [Miniconda Anaconda](https://docs.conda.io/en/latest/miniconda.html).</span><span class="sxs-lookup"><span data-stu-id="349d4-115">There are many tools you can use to setup a virtual Python environment — for these instructions, we'll use [Anaconda’s Miniconda](https://docs.conda.io/en/latest/miniconda.html).</span></span> <span data-ttu-id="349d4-116">В оставшейся части этой программы установки предполагается, что вы используете среду miniconda.</span><span class="sxs-lookup"><span data-stu-id="349d4-116">The rest of this setup assumes you use a miniconda environment.</span></span> 

### <a name="set-up-python-environment"></a><span data-ttu-id="349d4-117">Настройка среды Python</span><span class="sxs-lookup"><span data-stu-id="349d4-117">Set up Python environment</span></span> 

<span data-ttu-id="349d4-118">Скачайте и установите [установщик Windows Miniconda](https://docs.conda.io/en/latest/miniconda.html#windows-installers) в системе.</span><span class="sxs-lookup"><span data-stu-id="349d4-118">Download and install the [Miniconda Windows installer](https://docs.conda.io/en/latest/miniconda.html#windows-installers) on your system.</span></span> <span data-ttu-id="349d4-119">Для установки на сайте Anaconda есть [Дополнительные рекомендации](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html) .</span><span class="sxs-lookup"><span data-stu-id="349d4-119">There is [additional guidance for setup](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html) on Anaconda’s site.</span></span> <span data-ttu-id="349d4-120">После установки Miniconda Создайте среду с помощью Python с именем **директмл** и активируйте ее с помощью следующих команд.</span><span class="sxs-lookup"><span data-stu-id="349d4-120">Once Miniconda is installed, create an environment using Python named **directml** and activate it through the following commands.</span></span> 

> [!NOTE]
> <span data-ttu-id="349d4-121">В приведенных ниже командах мы используем Python 3,6.</span><span class="sxs-lookup"><span data-stu-id="349d4-121">In the commands below, we use Python 3.6.</span></span> <span data-ttu-id="349d4-122">Однако пакет tensorflow-директмл работает в среде Python 3,5, 3,6 или 3,7.</span><span class="sxs-lookup"><span data-stu-id="349d4-122">However, the tensorflow-directml package works in a Python 3.5, 3.6 or 3.7 environment.</span></span> 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a><span data-ttu-id="349d4-123">Установка Tensorflow с помощью пакета Директмл</span><span class="sxs-lookup"><span data-stu-id="349d4-123">Install the Tensorflow with DirectML package</span></span> 

<span data-ttu-id="349d4-124">Установите пакет TensorFlow с серверной частью Директмл в PIP, выполнив следующую команду.</span><span class="sxs-lookup"><span data-stu-id="349d4-124">Install the package of TensorFlow with a DirectML backend through pip by running the following command.</span></span>

> [!NOTE]
> <span data-ttu-id="349d4-125">Пакет tensorflow-директмл поддерживает только TensorFlow 1,15.</span><span class="sxs-lookup"><span data-stu-id="349d4-125">The tensorflow-directml package only supports TensorFlow 1.15.</span></span> 

```
pip install tensorflow-directml
```

<span data-ttu-id="349d4-126">После установки пакета tensorflow-директмл можно убедиться, что он работает правильно, добавив два десятка.</span><span class="sxs-lookup"><span data-stu-id="349d4-126">Once you’ve installed the tensorflow-directml package, you can verify that it runs correctly by adding two tensors.</span></span> <span data-ttu-id="349d4-127">Скопируйте следующие строки в интерактивный сеанс Python.</span><span class="sxs-lookup"><span data-stu-id="349d4-127">Copy the following lines into an interactive Python session.</span></span> 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

<span data-ttu-id="349d4-128">Вы должны увидеть результат, аналогичный приведенному ниже, с оператором Add, размещенным на устройстве DML.</span><span class="sxs-lookup"><span data-stu-id="349d4-128">You should see output similar to the following, with the add operator placed on the DML device.</span></span> 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library DirectMLba106a7c621ea741d2159d8708ee581c11918380.dll 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a><span data-ttu-id="349d4-129">Tensorflow с примерами Директмл и отзывами</span><span class="sxs-lookup"><span data-stu-id="349d4-129">Tensorflow with DirectML samples and feedback</span></span> 

<span data-ttu-id="349d4-130">Теперь вы готовы начать обучение в МАШИНном обучении.</span><span class="sxs-lookup"><span data-stu-id="349d4-130">Now you’re ready to start learning more about ML training.</span></span> <span data-ttu-id="349d4-131">Ознакомьтесь с [учебниками по TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) или [примерами](https://github.com/microsoft/DirectML).</span><span class="sxs-lookup"><span data-stu-id="349d4-131">Check out the [TensorFlow tutorials](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our samples](https://github.com/microsoft/DirectML).</span></span> <span data-ttu-id="349d4-132">Мы использовали это содержимое как проверку для этого начального предварительного пакета TensorFlow с серверной частью Директмл.</span><span class="sxs-lookup"><span data-stu-id="349d4-132">We used this content as validation for this initial preview package of TensorFlow with a DirectML backend.</span></span> 

<span data-ttu-id="349d4-133">Если у вас возникли проблемы или вы получили отзыв о TensorFlow с пакетом Директмл, обратитесь [к нашей группе](https://github.com/microsoft/DirectML/issues).</span><span class="sxs-lookup"><span data-stu-id="349d4-133">If you run into issues or have feedback on the TensorFlow with DirectML package, please [connect with our team here](https://github.com/microsoft/DirectML/issues).</span></span> 
