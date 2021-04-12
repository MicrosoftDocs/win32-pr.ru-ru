---
title: Установка компрессоров и декомпрессоров
description: Установка компрессоров и декомпрессоров
ms.assetid: 8bcca000-c4c7-47e7-a4c0-5d0d1750176f
keywords:
- Диспетчер сжатия видео (ВКМ), установка компрессоров
- ВКМ (диспетчер сжатия видео), установка компрессоров
- Функция ИЦинсталл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8c3421b3d7f59e7f6b16150fcd0d641deaef17
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329275"
---
# <a name="installing-compressors-and-decompressors"></a>Установка компрессоров и декомпрессоров

В следующем примере показано, как приложение может установить функцию в виде программы сжатия или распаковки с помощью функции [**иЦинсталл**](/windows/desktop/api/Vfw/nf-vfw-icinstall) .


```C++
// This function looks like a DriverProc entry point. 

LRESULT MyCodecFunction(DWORD dwID, HDRVR hDriver, 
    UINT uiMessage, LPARAM lParam1, LPARAM lParam2); 
 
// This function installs the MyCodecFunction as a compressor. 

result = ICInstall ( ICTYPE_VIDEO, mmioFOURCC('s','a','m','p'), 
    (LPARAM)(FARPROC)&MyCodecFunction, NULL, ICINSTALL_FUNCTION); 
 
```



 

 




