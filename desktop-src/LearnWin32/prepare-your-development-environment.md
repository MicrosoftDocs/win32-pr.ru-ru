---
title: Подготовка среды разработки
description: Подготовка среды разработки
ms.assetid: 5a3fd27e-ec8f-41eb-9d31-86d6d9f70862
ms.topic: article
ms.date: 10/03/2019
ms.openlocfilehash: 8245326ba0d7862836336cf050eb3abf1873139873bde8b9bab238ff5a738942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896974"
---
# <a name="prepare-your-development-environment"></a>Подготовка среды разработки

чтобы написать Windows программу на C или C++, необходимо установить пакет средств разработки Microsoft Windows Software Development Kit (SDK) или Microsoft Visual Studio. Windows SDK содержит заголовки и библиотеки, необходимые для компиляции и связывания приложения. Windows SDK также содержит программы командной строки для создания Windows приложений, включая компилятор Visual C++ и компоновщик. хотя вы можете компилировать и создавать Windows программы с помощью программ командной строки, рекомендуется использовать Microsoft Visual Studio. вы можете скачать бесплатную версию Visual Studio Community или бесплатные пробные версии Visual Studio [здесь](https://visualstudio.microsoft.com/downloads/).

каждый выпуск Windows SDK предназначен для последней версии Windows, а также для нескольких предыдущих версий. в заметках о выпуске перечислены поддерживаемые платформы, но если вы не обслуживаете приложение для очень старой версии Windows, следует установить последнюю версию Windows SDK. последнюю Windows SDK можно скачать [здесь](https://developer.microsoft.com/windows/downloads/windows-10-sdk).

Windows SDK поддерживает разработку как 32-разрядных, так и 64-разрядных приложений. api-интерфейсы Windows разработаны таким образом, чтобы один и тот же код можно было компилировать для 32-или 64-бит без изменений.

> [!Note]  
> Windows SDK не поддерживает разработку драйверов оборудования, и эта серия не будет обсуждать разработку драйверов. сведения о создании драйвера оборудования см. в разделе [начало работы с драйверами Windows](/windows-hardware/drivers/gettingstarted/).

## <a name="next"></a>Следующая

[Windows Соглашения о написании кода](windows-coding-conventions.md)

## <a name="related-topics"></a>Связанные темы

* [Скачать Visual Studio](https://visualstudio.microsoft.com/downloads/)
* [скачать Windows SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)