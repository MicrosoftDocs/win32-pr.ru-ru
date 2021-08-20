---
description: Состояние транспорта устройства
ms.assetid: 15edded0-207c-41e8-81fe-deb6335045eb
title: Состояние транспорта устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99ea7c3d6cba8363826c0fdab3cf411f0d68d6e284832a75c02cac3b1eefa770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952953"
---
# <a name="device-transport-state"></a>Состояние транспорта устройства

Чтобы получить текущее состояние устройства, например воспроизведение, пауза или остановка, вызовите метод [**иамексттранспорт:: Get \_**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) . Метод получает константу, которая указывает состояние устройства:



| Значение                    | Состояние устройства |
|--------------------------|--------------|
| \_Воспроизведение в режиме ED \_           | Воспроизведение         |
| \_точка в режиме ED \_           | Stop         |
| \_заморозить режим ED \_         | Пауза        |
| ED, \_ режим \_ FF             | Перемотка вперед |
| ED \_ Mode \_ выгру            | Rewind       |
| \_запись в режиме ED \_         | Record       |
| \_закрепление записи в режиме ED \_ \_ | Запись — приостановка |



 

Следующий код проверяет состояние устройства:


```C++
LONG State;
hr = MyDevCap.pTransport->get_Mode(&State);
if (SUCCEEDED(hr))
{
    switch (State)
    {
        case ED_MODE_PLAY:
        // ... 
    }
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Управление видеокамерой](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



