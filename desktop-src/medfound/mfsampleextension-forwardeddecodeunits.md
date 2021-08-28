---
description: Возвращает объект типа Имфколлектион, содержащий объекты Имфсампле, которые содержат единицы уровня абстракции сети (Налус) и дополнительные модули сведений об улучшении (SEI), перенаправляемые декодером.
ms.assetid: F9FD7959-A78A-4C72-8326-EE8FF9066E6C
title: Атрибут MFSampleExtension_ForwardedDecodeUnits (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2298a29d722c118fb79d5f0b49aa9d3d94fd735150a65772eb15e6da7638445
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713734"
---
# <a name="mfsampleextension_forwardeddecodeunits-attribute"></a>Мфсампликстенсион \_ форвардеддекодеунитс, атрибут

Возвращает объект типа [**имфколлектион**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) , содержащий объекты [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , которые содержат единицы уровня абстракции сети (налус) и дополнительные модули сведений об улучшении (SEI), перенаправляемые декодером.

## <a name="data-type"></a>Тип данных

**IUnknown**

## <a name="remarks"></a>Remarks

Коллекция содержит все пользовательские единицы налу/SEI, начиная с предыдущего кадра с удаленными байтами защиты эмуляции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>                          |
| Минимальная версия сервера<br/> | Windows Server 2016 \[ только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



 

 




