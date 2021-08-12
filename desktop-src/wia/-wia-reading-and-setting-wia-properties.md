---
description: интерфейс ивиапропертистораже предоставляет методы для чтения и записи свойств элемента Windowsного получения изображений (WIA). К свойствам элементов относятся команды устройств, сведения о формате элемента и сведения об устройстве.
ms.assetid: 268d2298-bc9c-479b-b078-a8180cd38bc3
title: Чтение и задание свойств WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607e319723023a00c4159687c3dff13fedab8275a0522fdb2254b36b8e62edb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439878"
---
# <a name="reading-and-setting-wia-properties"></a>Чтение и задание свойств WIA

интерфейс [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) предоставляет методы для чтения и записи свойств элемента Windowsного получения изображений (WIA). К свойствам элементов относятся команды устройств, сведения о формате элемента и сведения об устройстве.

Приложение может получить указатель на интерфейс [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) элемента, перечисляя сведения об устройстве или сведения о событии путем вызова [**Ивиаитем:: енумдевицекапабилитиес**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) или [**ивиаитем:: енумрегистеревентинфо**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) или путем запроса к интерфейсу [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) элемента. (В WIA 2,0 это можно сделать путем вызова [**IWiaItem2:: енумдевицекапабилитиес**](-wia-iwiaitem2-enumdevicecapabilities.md) или [**IWiaItem2:: енумрегистеревентинфо**](-wia-iwiaitem2-enumregistereventinfo.md) или путем запроса к интерфейсу [**IWiaItem2**](-wia-iwiaitem2.md) элемента.)

[**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) наследует от [ипропертистораже](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) , а унаследованные методы реализуются, как описано в разделе справки структурированных служба хранилища в Windowsном пакете средств разработки программного обеспечения (SDK).

> [!Note]
>
> Приложения WIA должны всегда считывать заголовки данных изображений для получения точных сведений об изображении. Драйвер WIA может изменять свойства WIA и заголовки данных изображения во время перемещения данных.
>
> Если отсутствует заголовок данных изображения в указанном формате, приложение WIA должно использовать свойства WIA в качестве источника информации о передаваемых данных. Приложение WIA должно повторно считывать необходимые свойства WIA после завершения сканирования или записи, чтобы получить обновленные параметры.

 

В следующих разделах описываются различные свойства WIA:

-   [Проверка свойства WIA](-wia-wia-property-validation.md)
-   [Свойства сведений об устройстве](-wia-device-information-properties-wia-dip-xxxx.md)
-   [Свойства устройства](-wia-device-properties.md)
-   [Свойства элемента](-wia-item-properties.md)
-   [Дополнительные свойства WIA](-wia-additional-wia-properties.md)
-   [Определение пользовательских свойств](-wia-defining-custom-properties.md)
-   [Использование пользовательских свойств](-wia-using-custom-properties.md)
-   [Схема профиля сканирования](-wia-scan-profile-schema.md)

 

 
