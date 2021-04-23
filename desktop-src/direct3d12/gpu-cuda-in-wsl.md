---
title: Включение NVIDIA CUDA в WSL 2
description: Включение предварительной версии NVIDIA CUDA в подсистеме Windows для Linux
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: ea5b460d4b4c71417f8ac9969f58bcebf6d10af9
ms.sourcegitcommit: 85acfd5afdcd30c81e3d2b375e813957f9830e9f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/03/2020
ms.locfileid: "105719158"
---
# <a name="enable-nvidia-cuda-in-wsl-2"></a><span data-ttu-id="01ec7-103">Включение NVIDIA CUDA в WSL 2</span><span class="sxs-lookup"><span data-stu-id="01ec7-103">Enable NVIDIA CUDA in WSL 2</span></span>

<span data-ttu-id="01ec7-104">Пакет SDK для предварительной оценки Windows поддерживает запуск существующих средств машинного обучения, библиотек и популярных платформ, использующих NVIDIA CUDA для аппаратного ускорения GPU в экземпляре WSL 2.</span><span class="sxs-lookup"><span data-stu-id="01ec7-104">The Windows Insider SDK supports running existing ML tools, libraries, and popular frameworks that use NVIDIA CUDA for GPU hardware acceleration inside a WSL 2 instance.</span></span> <span data-ttu-id="01ec7-105">Сюда входят PyTorch и TensorFlow, а также все средства поддержки DOCKER и Toolkit для контейнера NVIDIA, доступные в собственной среде Linux.</span><span class="sxs-lookup"><span data-stu-id="01ec7-105">This includes PyTorch and TensorFlow as well as all the Docker and NVIDIA Container Toolkit support available in a native Linux environment.</span></span> 

> [!NOTE]
> <span data-ttu-id="01ec7-106">Следующие функции доступны в предварительных версиях Windows 10 и могут изменяться.</span><span class="sxs-lookup"><span data-stu-id="01ec7-106">The following features are available in prerelease versions of Windows 10, and are subject to change.</span></span>

## <a name="install-the-latest-windows-insider-dev-channel-build"></a><span data-ttu-id="01ec7-107">Установите последнюю сборку канала разработки для программы предварительной оценки Windows</span><span class="sxs-lookup"><span data-stu-id="01ec7-107">Install the latest Windows Insider Dev Channel build</span></span> 

<span data-ttu-id="01ec7-108">Чтобы использовать эту предварительную версию, необходимо [зарегистрироваться для использования программы предварительной оценки Windows](https://insider.windows.com/getting-started/#register).</span><span class="sxs-lookup"><span data-stu-id="01ec7-108">To use this preview, you'll need to [register for the Windows Insider Program](https://insider.windows.com/getting-started/#register).</span></span> <span data-ttu-id="01ec7-109">После этого выполните следующие [инстуктионс](https://insider.windows.com/getting-started/#install) , чтобы установить последнюю сборку Insider Preview.</span><span class="sxs-lookup"><span data-stu-id="01ec7-109">Once you do, follow [these instuctions](https://insider.windows.com/getting-started/#install) to install the latest Insider build.</span></span> <span data-ttu-id="01ec7-110">При выборе параметров убедитесь, что выбран [канал разработки](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span><span class="sxs-lookup"><span data-stu-id="01ec7-110">When choosing your settings, ensure you're selecting the [Dev Channel](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span></span> 

<span data-ttu-id="01ec7-111">Для этой предварительной версии требуется сборка 20150 или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="01ec7-111">For this preview, you need Build 20150 or higher.</span></span> <span data-ttu-id="01ec7-112">Номер версии сборки можно проверить, выполнив `winver` команду **Run** (клавиша Windows + R).</span><span class="sxs-lookup"><span data-stu-id="01ec7-112">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="install-the-preview-gpu-driver"></a><span data-ttu-id="01ec7-113">Установка драйвера GPU для предварительной версии</span><span class="sxs-lookup"><span data-stu-id="01ec7-113">Install the preview GPU driver</span></span> 

<span data-ttu-id="01ec7-114">Скачайте и установите [драйвер NVIDIA CUDA с поддержкой WSL](https://developer.nvidia.com/cuda/wsl) для использования с существующими рабочими ПРОЦЕССами ML в CUDA.</span><span class="sxs-lookup"><span data-stu-id="01ec7-114">Download and install the [NVIDIA CUDA-enabled driver for WSL](https://developer.nvidia.com/cuda/wsl) to use with your existing CUDA ML workflows.</span></span> 

## <a name="set-up-wsl-2-for-the-preview"></a><span data-ttu-id="01ec7-115">Настройка WSL 2 для предварительной версии</span><span class="sxs-lookup"><span data-stu-id="01ec7-115">Set up WSL 2 for the preview</span></span> 

<span data-ttu-id="01ec7-116">Установив приведенный выше драйвер, убедитесь, что вы [включили WSL 2](/windows/wsl/install-win10) и [установите дистрибутив на основе glibc](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (например, Ubuntu или Debian).</span><span class="sxs-lookup"><span data-stu-id="01ec7-116">Once you've installed the above driver, ensure you [enable WSL 2](/windows/wsl/install-win10) and [install a glibc-based distribution](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (such as Ubuntu or Debian).</span></span> <span data-ttu-id="01ec7-117">Убедитесь, что у вас установлена последняя версия ядра, выбрав пункт **проверить наличие обновлений** в разделе **Центр обновления Windows** приложения "Параметры".</span><span class="sxs-lookup"><span data-stu-id="01ec7-117">Ensure you have the latest kernel by selecting **Check for updates** in the **Windows Update** section of the Settings app.</span></span> 

> [!NOTE]
> <span data-ttu-id="01ec7-118">При обновлении Windows убедитесь, что вы **получили обновления для других продуктов Майкрософт** .</span><span class="sxs-lookup"><span data-stu-id="01ec7-118">Ensure you have **Receive updates for other Microsoft products when you update Windows** enabled.</span></span> <span data-ttu-id="01ec7-119">Его можно найти в **дополнительных параметрах** в разделе **Центр обновления Windows** приложения "Параметры".</span><span class="sxs-lookup"><span data-stu-id="01ec7-119">You can find it in **Advanced options** within the **Windows Update** section of the Settings app.</span></span> 

<span data-ttu-id="01ec7-120">Для этой предварительной версии необходима версия ядра 4.19.121 или более поздняя.</span><span class="sxs-lookup"><span data-stu-id="01ec7-120">For this preview, you need a kernel version of 4.19.121 or higher.</span></span> <span data-ttu-id="01ec7-121">Номер версии можно проверить, выполнив следующую команду в PowerShell.</span><span class="sxs-lookup"><span data-stu-id="01ec7-121">You can check the version number by running the following command in PowerShell.</span></span> 

```powershell
wsl cat /proc/version
```

<span data-ttu-id="01ec7-122">Теперь вы можете начать использовать существующие рабочие процессы Linux с помощью [NVIDIA DOCKER](https://github.com/NVIDIA/nvidia-docker)или установить [PyTorch](https://pytorch.org/get-started/locally/) или [TensorFlow](https://www.tensorflow.org/install/gpu) внутри WSL 2.</span><span class="sxs-lookup"><span data-stu-id="01ec7-122">Now you can start using your exisiting Linux workflows through [NVIDIA Docker](https://github.com/NVIDIA/nvidia-docker), or by installing [PyTorch](https://pytorch.org/get-started/locally/) or [TensorFlow](https://www.tensorflow.org/install/gpu) inside WSL 2.</span></span> <span data-ttu-id="01ec7-123">Дополнительные сведения о настройке см. в разделе [руководства пользователя NVIDIA CUDA on WSL](https://docs.nvidia.com/cuda/wsl-user-guide/index.html).</span><span class="sxs-lookup"><span data-stu-id="01ec7-123">More information on getting set up is captured in [NVIDIA's CUDA on WSL User Guide](https://docs.nvidia.com/cuda/wsl-user-guide/index.html).</span></span>

<span data-ttu-id="01ec7-124">Поделитесь отзывами о поддержке NVIDIA через [форум сообщества для CUDA на WSL](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303).</span><span class="sxs-lookup"><span data-stu-id="01ec7-124">Share feedback on NVIDIA's support via their [Community forum for CUDA on WSL](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303).</span></span>
