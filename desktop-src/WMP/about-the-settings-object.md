---
title: Сведения об объекте Settings
description: Сведения об объекте Settings
ms.assetid: 941463e6-7928-438e-824e-e5e281421a4a
keywords:
- Проигрыватель Windows Media, объект параметров
- Объектная модель проигрывателя Windows Media, объект параметров
- Объектная модель, объект Settings
- Элемент управления ActiveX проигрывателя Windows Media, объект Settings
- Элемент управления ActiveX, объект Settings
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, объект Settings
- Проигрыватель Windows Media Mobile, объект параметров
- Объект параметров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20dae51d42e6c67a59ddc23dca19bc7f4180001
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887804"
---
# <a name="about-the-settings-object"></a>Сведения об объекте Settings

Объект **параметров** управляет параметрами таких элементов управления, как громкость, число воспроизведения, звук и т. д. Доступ к нему осуществляется только через свойство **Settings** объекта **Player** . Свойство **Settings** возвращает объект **Settings** . Доступ к свойствам объекта **параметров** можно получить только после его создания. Например, чтобы получить значение свойства **Volume** , необходимо использовать следующий код:


```C++
myvolume = player.settings.volume;

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Объектная модель проигрывателя для языков сценариев**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Объект параметров**](settings-object.md)
</dt> </dl>

 

 




