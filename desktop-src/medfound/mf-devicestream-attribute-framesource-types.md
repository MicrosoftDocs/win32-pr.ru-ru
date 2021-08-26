---
description: Представляет тип источника кадра.
ms.assetid: 4A2B427E-E654-48BA-8BF4-16F1B1F8D266
title: Атрибут MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce2e7f90f4e5f23e99bac8e532455fac1309cc0e20177c5800d85f4580e20a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013194"
---
# <a name="mf_devicestream_attribute_framesource_types-attribute"></a>\_ \_ \_ \_ Атрибут фрамесаурце Types для атрибута MF девицестреам

Представляет тип источника кадра.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Это значение этого атрибута должно быть битовой маской одного или нескольких значений из перечисления [**мффрамесаурцетипес**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) . Для поддержки обратной совместимости, если этот атрибут не определен для типа мультимедиа, предполагается, что оно имеет значение **мффрамесаурцетипес:: Color**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1607\]<br/>                          |
| Минимальная версия сервера<br/> | Windows Server 2016 \[ только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



 

 




