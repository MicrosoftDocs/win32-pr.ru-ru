---
description: Модули Топоедит
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: Модули Топоедит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728f39edace5974d390746173308361b595c3b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080571"
---
# <a name="topoedit-modules"></a>Модули Топоедит

Средство Топоедит предоставляется с Windows SDK для Windows Server 2008 и более поздних версий. Для этого средства требуется Windows Vista или более поздняя версия.

Модули Топоедит находятся в папке bin пакета SDK. Эти модули:

-   TopoEdit.exe — исполняемый файл приложения
-   TEDUTIL.dll — библиотека DLL расширения

Установка пакета SDK регистрирует библиотеку DLL. Однако в случае сбоя в командной строке выполните следующую команду.


```C++
Regsvr32 <Install path>\Microsoft SDKs\Windows\v6.0\Bin\TEDUTIL.dll
```



Исходный код для Топоедит также предоставляется в виде образца в Windows SDK. Он находится в следующем каталоге:

<samples root>\\Мультимедиа \\ Media Foundation \\ топоедит

## <a name="related-topics"></a>См. также

<dl> <dt>

[Введение в Топоедит](introduction-to-topoedit.md)
</dt> <dt>

[топоедит](topoedit.md)
</dt> </dl>

 

 



