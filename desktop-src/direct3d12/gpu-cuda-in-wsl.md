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
# <a name="enable-nvidia-cuda-in-wsl-2"></a>Включение NVIDIA CUDA в WSL 2

Пакет SDK для предварительной оценки Windows поддерживает запуск существующих средств машинного обучения, библиотек и популярных платформ, использующих NVIDIA CUDA для аппаратного ускорения GPU в экземпляре WSL 2. Сюда входят PyTorch и TensorFlow, а также все средства поддержки DOCKER и Toolkit для контейнера NVIDIA, доступные в собственной среде Linux. 

> [!NOTE]
> Следующие функции доступны в предварительных версиях Windows 10 и могут изменяться.

## <a name="install-the-latest-windows-insider-dev-channel-build"></a>Установите последнюю сборку канала разработки для программы предварительной оценки Windows 

Чтобы использовать эту предварительную версию, необходимо [зарегистрироваться для использования программы предварительной оценки Windows](https://insider.windows.com/getting-started/#register). После этого выполните следующие [инстуктионс](https://insider.windows.com/getting-started/#install) , чтобы установить последнюю сборку Insider Preview. При выборе параметров убедитесь, что выбран [канал разработки](/windows-insider/flight-hub/#active-development-builds-of-windows-10). 

Для этой предварительной версии требуется сборка 20150 или более поздняя версия. Номер версии сборки можно проверить, выполнив `winver` команду **Run** (клавиша Windows + R).

## <a name="install-the-preview-gpu-driver"></a>Установка драйвера GPU для предварительной версии 

Скачайте и установите [драйвер NVIDIA CUDA с поддержкой WSL](https://developer.nvidia.com/cuda/wsl) для использования с существующими рабочими ПРОЦЕССами ML в CUDA. 

## <a name="set-up-wsl-2-for-the-preview"></a>Настройка WSL 2 для предварительной версии 

Установив приведенный выше драйвер, убедитесь, что вы [включили WSL 2](/windows/wsl/install-win10) и [установите дистрибутив на основе glibc](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (например, Ubuntu или Debian). Убедитесь, что у вас установлена последняя версия ядра, выбрав пункт **проверить наличие обновлений** в разделе **Центр обновления Windows** приложения "Параметры". 

> [!NOTE]
> При обновлении Windows убедитесь, что вы **получили обновления для других продуктов Майкрософт** . Его можно найти в **дополнительных параметрах** в разделе **Центр обновления Windows** приложения "Параметры". 

Для этой предварительной версии необходима версия ядра 4.19.121 или более поздняя. Номер версии можно проверить, выполнив следующую команду в PowerShell. 

```powershell
wsl cat /proc/version
```

Теперь вы можете начать использовать существующие рабочие процессы Linux с помощью [NVIDIA DOCKER](https://github.com/NVIDIA/nvidia-docker)или установить [PyTorch](https://pytorch.org/get-started/locally/) или [TensorFlow](https://www.tensorflow.org/install/gpu) внутри WSL 2. Дополнительные сведения о настройке см. в разделе [руководства пользователя NVIDIA CUDA on WSL](https://docs.nvidia.com/cuda/wsl-user-guide/index.html).

Поделитесь отзывами о поддержке NVIDIA через [форум сообщества для CUDA на WSL](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303).
