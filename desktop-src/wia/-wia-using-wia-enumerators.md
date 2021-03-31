---
description: WIA предоставляет несколько интерфейсов для перечисления различных возможностей, свойств и информации.
ms.assetid: d46d4c18-79cc-4f3c-9745-522ab2635068
title: Использование перечислителей WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ee42f99718cb36071b828e87e3a71de6d70ab5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263124"
---
# <a name="using-wia-enumerators"></a>Использование перечислителей WIA

WIA предоставляет несколько интерфейсов для перечисления различных возможностей, свойств и информации. Интерфейсы перечисления для получения образа Windows (WIA) — это все определенные реализации интерфейса перечисления (COM) стандартного компонента. Дополнительные сведения см. в разделе [иенумкскскскс](/previous-versions//ms680089(v=vs.85)).

В следующей таблице приведены сведения о интерфейсах перечисления WIA. 

| Интерфейс                                                   | Получение указателя                                                                                                                                                                                    | Область использования                                                                                                                             |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**Иенумвиа \_ dev \_ Cap**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)       | Вызовите метод [**ивиаитем:: енумдевицекапабилитиес**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) или [**IWiaItem2:: енумдевицекапабилитиес**](-wia-iwiaitem2-enumdevicecapabilities.md) для корневого элемента WIA. | Перечисляет возможности аппаратного устройства WIA, такие как команды и события устройства.                                            |
| [**\_ \_ Сведения о иенумвиа dev**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)       | Вызовите метод [**ивиадевмгр:: енумдевицеинфо**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) или [**IWiaDevMgr2:: енумдевицеинфо**](-wia-iwiadevmgr2-enumdeviceinfo.md) .                                            | Перечисляет доступные устройства WIA и предоставляет указатели на их интерфейсы [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) . |
| [**\_ \_ Сведения о формате иенумвиа**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) | Вызовите метод [**\_ \_ сведений о формате Ивиадататрансфер:: идтенумвиа**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtenumwia_format_info) элемента.                                                                              | Перечисляет все сведения о формате изображения, предоставляемые элементом WIA.                                                                    |
| [**иенумвиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem)                   | Вызовите метод [**ивиаитем:: енумчилдитемс**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) или [**IWiaItem2:: енумчилдитемс**](-wia-iwiaitem2-enumchilditems.md) элемента WIA.                                          | Перечисляет дочерние элементы элемента WIA, представляющего либо устройство, либо папку.                                                |



 

 

 
