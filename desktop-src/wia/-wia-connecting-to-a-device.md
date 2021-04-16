---
description: Дополнительные сведения о подключении к устройству
ms.assetid: 16ff280d-818b-4a4e-b5a6-16e81f5b35c6
title: Подключение к устройству
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fc7d8c78f77854a9adbedad7c0870721b3b037ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693084"
---
# <a name="connecting-to-a-device"></a>Подключение к устройству

> [!Note]  
> Эта система сценариев была заменена на уровень автоматизации службы "получение образа Windows" (WIA). См. раздел [уровень службы "получение образа Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)".

 

Первым шагом в любом приложении или скрипте, использующем модель сценариев получения изображений Windows (WIA), является создание объекта [**WIA**](-wia-wia.md) . Этот объект предоставляет методы для получения коллекции объектов [**DeviceInfo**](-wia-deviceinfo.md) и подключения этих объектов к устройствам. Он также обеспечивает возможность прослушивания аппаратных событий WIA.

В следующей строке кода Microsoft Visual Basic Scripting Edition (VBScript) создается объект [**WIA**](-wia-wia.md) :


```
objWia = CreateObject("Wia.Script")
```



После создания объекта [**WIA**](-wia-wia.md) используйте его метод [**CREATE**](-wia-iwia-create.md) для подключения к аппаратному устройству WIA.

Для получения коллекции объектов [**DeviceInfo**](-wia-deviceinfo.md) можно также использовать свойство [**Devices**](-wia-iwia-devices.md) объекта [**WIA**](-wia-wia.md) . Перечисление этой коллекции и использование метода [**CREATE**](-wia-iwiadeviceinfo-create.md) для подключения к устройству.

 

 
