---
description: Возвращает объект типа Имфколлектион, содержащий объекты Имфсампле, которые содержат единицы уровня абстракции сети (Налус) и дополнительные модули сведений об улучшении (SEI), перенаправляемые декодером.
ms.assetid: F9FD7959-A78A-4C72-8326-EE8FF9066E6C
title: Атрибут MFSampleExtension_ForwardedDecodeUnits (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ab5c10a4a7fb4dfd201f9c494c1bc65e14c162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719474"
---
# <a name="mfsampleextension_forwardeddecodeunits-attribute"></a>Мфсампликстенсион \_ форвардеддекодеунитс, атрибут

Возвращает объект типа [**имфколлектион**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) , содержащий объекты [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , которые содержат единицы уровня абстракции сети (налус) и дополнительные модули сведений об улучшении (SEI), перенаправляемые декодером.

## <a name="data-type"></a>Тип данных

**IUnknown**

## <a name="remarks"></a>Комментарии

Коллекция содержит все пользовательские единицы налу/SEI, начиная с предыдущего кадра с удаленными байтами защиты эмуляции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



 

 




