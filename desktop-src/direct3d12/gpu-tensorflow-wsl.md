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
# <a name="enable-tensorflow-with-directml-in-wsl-2"></a><span data-ttu-id="c3c3d-103">Включение TensorFlow с DirectML в WSL 2</span><span class="sxs-lookup"><span data-stu-id="c3c3d-103">Enable TensorFlow with DirectML in WSL 2</span></span>

<span data-ttu-id="c3c3d-104">Эта предварительная версия предоставляет учащимся и начинающим пользователям способ начать создание знаний в пространстве машинного обучения на имеющемся оборудовании с помощью пакета TensorFlow с Директмл.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-104">This preview provides students and beginners a way to start building knowledge in the ML space on their existing hardware by using the TensorFlow with DirectML package.</span></span> <span data-ttu-id="c3c3d-105">После настройки пользователи могут начать с [моделей учебников по TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) или наших [примеров директмл](https://github.com/microsoft/DirectML).</span><span class="sxs-lookup"><span data-stu-id="c3c3d-105">Once set up, users can start with the [TensorFlow tutorial models](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or our [DirectML samples](https://github.com/microsoft/DirectML).</span></span> 

> [!NOTE]
> <span data-ttu-id="c3c3d-106">Следующие функции доступны в предварительных версиях Windows 10 и могут изменяться.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-106">The following features are available in prerelease versions of Windows 10, and are subject to change.</span></span>

## <a name="install-the-latest-windows-insider-dev-channel-build"></a><span data-ttu-id="c3c3d-107">Установите последнюю сборку канала разработки для программы предварительной оценки Windows</span><span class="sxs-lookup"><span data-stu-id="c3c3d-107">Install the latest Windows Insider Dev Channel build</span></span> 

<span data-ttu-id="c3c3d-108">Чтобы использовать эту предварительную версию, необходимо [зарегистрироваться для использования программы предварительной оценки Windows](https://insider.windows.com/getting-started/#register).</span><span class="sxs-lookup"><span data-stu-id="c3c3d-108">To use this preview, you'll need to [register for the Windows Insider Program](https://insider.windows.com/getting-started/#register).</span></span> <span data-ttu-id="c3c3d-109">После этого выполните следующие [инстуктионс](https://insider.windows.com/getting-started/#install) , чтобы установить последнюю сборку Insider Preview.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-109">Once you do, follow [these instuctions](https://insider.windows.com/getting-started/#install) to install the latest insider build.</span></span> <span data-ttu-id="c3c3d-110">При выборе параметров убедитесь, что выбран [канал разработки](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span><span class="sxs-lookup"><span data-stu-id="c3c3d-110">When choosing your settings, ensure you're selecting the [Dev Channel](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span></span> 

<span data-ttu-id="c3c3d-111">Для этой предварительной версии требуется сборка 20150 или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-111">For this preview, you need Build 20150 or higher.</span></span> <span data-ttu-id="c3c3d-112">Номер версии сборки можно проверить, выполнив `winver` команду **Run** (клавиша Windows + R).</span><span class="sxs-lookup"><span data-stu-id="c3c3d-112">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="install-the-preview-gpu-driver"></a><span data-ttu-id="c3c3d-113">Установка драйвера GPU для предварительной версии</span><span class="sxs-lookup"><span data-stu-id="c3c3d-113">Install the preview GPU driver</span></span> 

<span data-ttu-id="c3c3d-114">Перед установкой TensorFlow с пакетом Директмл в WSL 2 необходимо установить драйверы от поставщика оборудования GPU.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-114">Before installing the TensorFlow with DirectML package inside WSL 2, you need to install drivers from your GPU hardware vendor.</span></span> <span data-ttu-id="c3c3d-115">Эти драйверы позволяют графическому процессору Windows работать с WSL 2.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-115">These drivers enable the Windows GPU to work with WSL 2.</span></span>

### <a name="amd"></a><span data-ttu-id="c3c3d-116">AMD</span><span class="sxs-lookup"><span data-stu-id="c3c3d-116">AMD</span></span> 

<span data-ttu-id="c3c3d-117">[Скачайте и установите драйвер предварительной версии AMD](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support) с веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-117">[Download and install AMD’s preview driver](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support) from their website.</span></span> <span data-ttu-id="c3c3d-118">Этот предварительный драйвер поддерживает следующее оборудование:</span><span class="sxs-lookup"><span data-stu-id="c3c3d-118">This preview driver supports the following hardware:</span></span> 

* <span data-ttu-id="c3c3d-119">AMD Radeon™ серии RX и Radeon™ вии Graphics.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-119">AMD Radeon™ RX series and Radeon™ VII graphics.</span></span> 
* <span data-ttu-id="c3c3d-120">Графика AMD Radeon™ Pro.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-120">AMD Radeon™ Pro series graphics.</span></span> 
* <span data-ttu-id="c3c3d-121">Процессоры AMD ризен™ и ризен™ PRO с Radeon™ Вега Graphics.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-121">AMD Ryzen™ and Ryzen™ PRO Processors with Radeon™ Vega graphics.</span></span> 
* <span data-ttu-id="c3c3d-122">Процессоры AMD ризен™ и ризен™ PRO для мобильных устройств с Radeon™ Вега Graphics.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-122">AMD Ryzen™ and Ryzen™ PRO Mobile Processors with Radeon™ Vega graphics.</span></span> 

<span data-ttu-id="c3c3d-123">Полный список совместимых продуктов AMD см. в заметках о выпуске AMD.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-123">For a complete list of compatible AMD products, please refer to the AMD Release Notes.</span></span> 

### <a name="intel"></a><span data-ttu-id="c3c3d-124">Intel</span><span class="sxs-lookup"><span data-stu-id="c3c3d-124">Intel</span></span> 

<span data-ttu-id="c3c3d-125">[Скачайте и установите драйвер Intel Preview](https://downloadcenter.intel.com/download/29526) для использования с директмл на своем веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-125">[Download and install Intel’s preview driver](https://downloadcenter.intel.com/download/29526) to use with DirectML from their website.</span></span> 

### <a name="nvidia"></a><span data-ttu-id="c3c3d-126">NVIDIA</span><span class="sxs-lookup"><span data-stu-id="c3c3d-126">NVIDIA</span></span> 

<span data-ttu-id="c3c3d-127">[Скачайте и установите драйвер для предварительной версии NVIDIA](https://developer.nvidia.com/cuda/wsl/download) для использования с директмл на своем веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-127">[Download and install NVIDIA's preview driver](https://developer.nvidia.com/cuda/wsl/download) to use with DirectML from their website.</span></span> <span data-ttu-id="c3c3d-128">Дополнительные сведения см. на странице о [GPU NVIDIA в подсистеме Windows для Linux (WSL)](https://developer.nvidia.com/cuda/wsl) .</span><span class="sxs-lookup"><span data-stu-id="c3c3d-128">For more information, see [NVIDIA's GPU in Windows Subsystem for Linux (WSL)](https://developer.nvidia.com/cuda/wsl) page.</span></span>

## <a name="set-up-the-tensorflow-with-directml-preview"></a><span data-ttu-id="c3c3d-129">Настройка TensorFlow с помощью предварительной версии Директмл</span><span class="sxs-lookup"><span data-stu-id="c3c3d-129">Set up the TensorFlow with DirectML preview</span></span> 

### <a name="install-wsl-2"></a><span data-ttu-id="c3c3d-130">Установка WSL 2</span><span class="sxs-lookup"><span data-stu-id="c3c3d-130">Install WSL 2</span></span> 

<span data-ttu-id="c3c3d-131">Установив приведенный выше драйвер, убедитесь, что вы [включили WSL 2](/windows/wsl/install-win10) и [установите дистрибутив на основе glibc](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (например, Ubuntu или Debian).</span><span class="sxs-lookup"><span data-stu-id="c3c3d-131">Once you've installed the above driver, ensure you [enable WSL 2](/windows/wsl/install-win10) and [install a glibc-based distribution](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (like Ubuntu or Debian).</span></span> <span data-ttu-id="c3c3d-132">Для нашего тестирования мы использовали Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-132">For our testing, we used Ubuntu.</span></span> <span data-ttu-id="c3c3d-133">Убедитесь, что у вас установлена последняя версия ядра, выбрав пункт **проверить наличие обновлений** в разделе **Центр обновления Windows** приложения "Параметры".</span><span class="sxs-lookup"><span data-stu-id="c3c3d-133">Ensure you have the latest kernel by selecting **Check for updates** in the **Windows Update** section of the Settings app.</span></span> 

> [!NOTE]
> <span data-ttu-id="c3c3d-134">При обновлении Windows убедитесь, что у вас есть **обновления для получения других продуктов Майкрософт** .</span><span class="sxs-lookup"><span data-stu-id="c3c3d-134">Ensure you have the **Receive updates for other Microsoft products when you update Windows** enabled.</span></span> <span data-ttu-id="c3c3d-135">Его можно найти в **дополнительных параметрах** в разделе **Центр обновления Windows** приложения "Параметры".</span><span class="sxs-lookup"><span data-stu-id="c3c3d-135">You can find it in **Advanced options** within the **Windows Update** section of the Settings app.</span></span> 

<span data-ttu-id="c3c3d-136">Для этой предварительной версии необходима версия ядра 4.19.121 или более поздняя.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-136">For this preview, you need a kernel version of 4.19.121 or higher.</span></span> <span data-ttu-id="c3c3d-137">Номер версии можно проверить, выполнив следующую команду в PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-137">You can check the version number by running the following command in PowerShell.</span></span> 

```
wsl cat /proc/version
```

### <a name="set-up-python-environment"></a><span data-ttu-id="c3c3d-138">Настройка среды Python</span><span class="sxs-lookup"><span data-stu-id="c3c3d-138">Set up Python environment</span></span> 

<span data-ttu-id="c3c3d-139">Рекомендуется настроить виртуальную среду Python в экземпляре WSL 2.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-139">We recommend setting up a virtual Python environment inside your WSL 2 instance.</span></span> <span data-ttu-id="c3c3d-140">Существует множество средств, которые можно использовать для настройки виртуальной среды Python. для получения этих инструкций мы будем использовать [Miniconda Anaconda](https://docs.conda.io/en/latest/miniconda.html).</span><span class="sxs-lookup"><span data-stu-id="c3c3d-140">There are many tools you can use to setup a virtual Python environment — for these instructions, we'll use [Anaconda’s Miniconda](https://docs.conda.io/en/latest/miniconda.html).</span></span> <span data-ttu-id="c3c3d-141">В оставшейся части этой программы установки предполагается, что вы используете среду miniconda.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-141">The rest of this setup assumes you use a miniconda environment.</span></span> 

<span data-ttu-id="c3c3d-142">Установите Miniconda, следуя [указаниям на сайте Anaconda](https://conda.io/projects/conda/en/latest/user-guide/install/index.html), или выполнив следующие команды в WSL.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-142">Install Miniconda by following the [guidance on Anaconda’s site](https://conda.io/projects/conda/en/latest/user-guide/install/index.html), or by running the following commands in WSL.</span></span> 

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh 
bash Miniconda3-latest-Linux-x86_64.sh 
```

<span data-ttu-id="c3c3d-143">После установки Miniconda в WSL Создайте среду с помощью Python с именем "директмл" и активируйте ее с помощью следующих команд.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-143">Once Miniconda is installed in WSL, create an environment using Python named “directml” and activate it through the following commands.</span></span> 

> [!NOTE]
> <span data-ttu-id="c3c3d-144">В приведенных ниже командах мы используем Python 3,6.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-144">In the commands below, we use Python 3.6.</span></span> <span data-ttu-id="c3c3d-145">Однако пакет tensorflow-директмл работает в среде Python 3,5, 3,6 или 3,7.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-145">However, the tensorflow-directml package works in a Python 3.5, 3.6 or 3.7 environment.</span></span> 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a><span data-ttu-id="c3c3d-146">Установка Tensorflow с помощью пакета Директмл</span><span class="sxs-lookup"><span data-stu-id="c3c3d-146">Install the Tensorflow with DirectML package</span></span> 

<span data-ttu-id="c3c3d-147">Установите пакет TensorFlow с серверной частью Директмл в PIP, выполнив следующую команду.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-147">Install the package of TensorFlow with a DirectML backend through pip by running the following command.</span></span>

> [!NOTE]
> <span data-ttu-id="c3c3d-148">Пакет tensorflow-директмл поддерживает только TensorFlow 1,15.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-148">The tensorflow-directml package only supports TensorFlow 1.15.</span></span> 

```
pip install tensorflow-directml
```

<span data-ttu-id="c3c3d-149">После установки пакета tensorflow-директмл можно убедиться, что он работает правильно, добавив два десятка.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-149">Once you’ve installed the tensorflow-directml package, you can verify that it runs correctly by adding two tensors.</span></span> <span data-ttu-id="c3c3d-150">Скопируйте следующие строки в интерактивный сеанс Python.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-150">Copy the following lines into an interactive Python session.</span></span> 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

<span data-ttu-id="c3c3d-151">Вы должны увидеть результат, аналогичный приведенному ниже, с оператором Add, размещенным на устройстве DML.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-151">You should see output similar to the following, with the add operator placed on the DML device.</span></span> 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library libdirectml.so.ba106a7c621ea741d21598708ee581c11918380 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a><span data-ttu-id="c3c3d-152">Tensorflow с примерами Директмл и отзывами</span><span class="sxs-lookup"><span data-stu-id="c3c3d-152">Tensorflow with DirectML samples and feedback</span></span> 

<span data-ttu-id="c3c3d-153">Теперь вы готовы начать обучение в МАШИНном обучении.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-153">Now you’re ready to start learning more about ML training.</span></span> <span data-ttu-id="c3c3d-154">Ознакомьтесь с [учебниками по TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) или [примерами](https://github.com/microsoft/DirectML).</span><span class="sxs-lookup"><span data-stu-id="c3c3d-154">Check out the [TensorFlow tutorials](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our samples](https://github.com/microsoft/DirectML).</span></span> <span data-ttu-id="c3c3d-155">Мы использовали это содержимое как проверку для этого первоначального предварительного пакета TensorFlow с Директмл.</span><span class="sxs-lookup"><span data-stu-id="c3c3d-155">We used this content as validation for this initial preview package of TensorFlow with DirectML.</span></span> 

<span data-ttu-id="c3c3d-156">Если у вас возникли проблемы или вы получили отзыв о TensorFlow с пакетом Директмл, обратитесь [к нашей группе](https://github.com/microsoft/DirectML/issues).</span><span class="sxs-lookup"><span data-stu-id="c3c3d-156">If you run into issues or have feedback on the TensorFlow with DirectML package, please [connect with our team here](https://github.com/microsoft/DirectML/issues).</span></span>
