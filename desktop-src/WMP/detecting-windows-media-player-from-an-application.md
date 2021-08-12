---
title: обнаружение проигрыватель Windows Media из приложения
description: обнаружение проигрыватель Windows Media из приложения
ms.assetid: 3cf8a619-3b7e-45af-af6b-4711a45c7e07
keywords:
- проигрыватель Windows Media, обнаружение из приложений
- обнаружение проигрыватель Windows Media из приложений
- реестр, обнаружение проигрыватель Windows Media из приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5267dc6c3202d9ecf894377899dfb34cf02ad42dfee05f8d42896c39ae48fc24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579490"
---
# <a name="detecting-windows-media-player-from-an-application"></a>обнаружение проигрыватель Windows Media из приложения

чтобы определить, какая версия проигрыватель Windows Media установлена, проверьте следующий раздел реестра:

**HKEY \_ по для локального \_ компьютера \\ программное обеспечение \\ Microsoft \\ Active Setup \\ установленные компоненты**

для проигрыватель Windows Media 6,4 просмотрите раздел **{22d6f312-b0f6-11d0-94ab-0080c74c7e95}**.

для проигрыватель Windows Media 7 или более поздней версии просмотрите раздел **{6BF52A52-394A-11d3-B153-00C04F79FAA6}**.

В любом из этих ключей, если **установлен**<dl> <dt>

Тип данных
</dt> <dd>DWORD</dd> </dl> DWORD value is set to 0x1, you can safely use the **Version**<dl> <dt>

Тип данных
</dt> <dd>строка</dd> </dl> string value as the version of Windows Media Player that is installed.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**распространение проигрыватель Windows Media программного обеспечения**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




