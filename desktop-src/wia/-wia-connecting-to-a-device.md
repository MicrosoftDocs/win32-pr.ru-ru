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
ms.openlocfilehash: bf98c11b285d4c7aa4705095af99f35c129e27311dbe19ff42e4b0d288c45efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451224"
---
# <a name="connecting-to-a-device"></a>Подключение к устройству

> [!Note]  
> эта система сценариев была заменена на уровень автоматизации службы Windowsного получения изображений (WIA). см. раздел [уровень автоматизации получения образа Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

первым шагом в любом приложении или скрипте, использующем модель сценариев Windowsного получения изображений (wia), является создание объекта [**WIA**](-wia-wia.md) . Этот объект предоставляет методы для получения коллекции объектов [**DeviceInfo**](-wia-deviceinfo.md) и подключения этих объектов к устройствам. Он также обеспечивает возможность прослушивания аппаратных событий WIA.

в следующей строке кода Microsoft Visual Basic scripting Edition (VBScript) создается объект [**Wia**](-wia-wia.md) :


```
objWia = CreateObject("Wia.Script")
```



После создания объекта [**WIA**](-wia-wia.md) используйте его метод [**CREATE**](-wia-iwia-create.md) для подключения к аппаратному устройству WIA.

Для получения коллекции объектов [**DeviceInfo**](-wia-deviceinfo.md) можно также использовать свойство [**Devices**](-wia-iwia-devices.md) объекта [**WIA**](-wia-wia.md) . Перечисление этой коллекции и использование метода [**CREATE**](-wia-iwiadeviceinfo-create.md) для подключения к устройству.

 

 
