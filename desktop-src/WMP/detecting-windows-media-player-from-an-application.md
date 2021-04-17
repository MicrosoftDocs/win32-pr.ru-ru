---
title: Обнаружение проигрывателя Windows Media из приложения
description: Обнаружение проигрывателя Windows Media из приложения
ms.assetid: 3cf8a619-3b7e-45af-af6b-4711a45c7e07
keywords:
- Проигрыватель Windows Media, обнаружение из приложений
- обнаружение проигрывателя Windows Media из приложений
- реестр, обнаружение проигрывателя Windows Media из приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ae0c7d30b71749a22ecef10806817cd4182224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691356"
---
# <a name="detecting-windows-media-player-from-an-application"></a>Обнаружение проигрывателя Windows Media из приложения

Чтобы определить, какая версия проигрывателя Windows Media установлена, проверьте следующий раздел реестра:

**HKEY \_ по для локального \_ компьютера \\ программное обеспечение \\ Microsoft \\ Active Setup \\ установленные компоненты**

Для проигрывателя Windows Media 6,4 просмотрите раздел **{22d6f312-b0f6-11D0-94ab-0080c74c7e95}**.

Для проигрывателя Windows Media 7 или более поздней версии ознакомьтесь с разделом **{6BF52A52-394A-11D3-B153-00C04F79FAA6}**.

В любом из этих ключей, если **установлен**<dl> <dt>

Тип данных
</dt> <dd>DWORD</dd> </dl> DWORD value is set to 0x1, you can safely use the **Version**<dl> <dt>

Тип данных
</dt> <dd>строка</dd> </dl> string value as the version of Windows Media Player that is installed.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Распространение программного обеспечения проигрывателя Windows Media**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




