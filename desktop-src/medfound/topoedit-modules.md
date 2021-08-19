---
description: Модули Топоедит
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: Модули Топоедит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc95848a533ba67599c114917ebe502f42a4fe859df9c1ac6bf5acfc40bb393c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118057719"
---
# <a name="topoedit-modules"></a>Модули Топоедит

средство топоедит предоставляется с Windows SDK для Windows Server 2008 и более поздних версий. для этого средства требуется Windows Vista или более поздней версии.

Модули Топоедит находятся в папке bin пакета SDK. Эти модули:

-   TopoEdit.exe — исполняемый файл приложения
-   TEDUTIL.dll — библиотека DLL расширения

Установка пакета SDK регистрирует библиотеку DLL. Однако в случае сбоя в командной строке выполните следующую команду.


```C++
Regsvr32 <Install path>\Microsoft SDKs\Windows\v6.0\Bin\TEDUTIL.dll
```



исходный код для топоедит также предоставляется в виде образца в Windows SDK. Он находится в следующем каталоге:

<samples root>\\Мультимедиа \\ Media Foundation \\ топоедит

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Введение в Топоедит](introduction-to-topoedit.md)
</dt> <dt>

[топоедит](topoedit.md)
</dt> </dl>

 

 



