---
description: Представляет тип источника кадра.
ms.assetid: 4A2B427E-E654-48BA-8BF4-16F1B1F8D266
title: Атрибут MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8823a828a81290fe3b039c8959d694c62331622f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692665"
---
# <a name="mf_devicestream_attribute_framesource_types-attribute"></a>\_ \_ \_ \_ Атрибут фрамесаурце Types для атрибута MF девицестреам

Представляет тип источника кадра.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Это значение этого атрибута должно быть битовой маской одного или нескольких значений из перечисления [**мффрамесаурцетипес**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) . Для поддержки обратной совместимости, если этот атрибут не определен для типа мультимедиа, предполагается, что оно имеет значение **мффрамесаурцетипес:: Color**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1607\]<br/>                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



 

 




