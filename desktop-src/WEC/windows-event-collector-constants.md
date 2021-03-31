---
title: Константы сборщика событий Windows (Евколл. h)
description: Пакет SDK сборщика событий Windows содержит следующие константы.
ms.assetid: 2ba862f9-6849-43b3-8914-e18ede1d63c0
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- EC_VARIANT_TYPE_MASK
- EC_VARIANT_TYPE_ARRAY
- EC_READ_ACCESS
- EC_WRITE_ACCESS
- EC_OPEN_ALWAYS
- EC_CREATE_NEW
- EC_OPEN_EXISTING
api_location:
- Evcoll.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6e7e99186e2148bf6ec3400aadf760a79a2331
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800958"
---
# <a name="windows-event-collector-constants"></a>Константы сборщика событий Windows

Пакет SDK сборщика событий Windows содержит следующие константы.

<dl> <dt>

<span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**EC \_ вариантный \_ тип \_ маски**
</dt> <dd> <dl> <dt>

0x7F
</dt> <dt>



Используется для маскирования бита массива из свойства **Type** [**\_ варианта EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) , чтобы извлечь тип значения типа Variant.


</dt> </dl> </dd> <dt>

<span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**EC \_ \_ тип Variant \_ массива**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Если этот бит задан в свойстве **Type** [**\_ варианта EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant), то объект Variant содержит указатель на массив значений, а не само значение.


</dt> </dl> </dd> <dt>

<span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**EC \_ доступ на чтение \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Разрешение на управление доступом на чтение, позволяющее считывать данные из сборщика событий.


</dt> </dl> </dd> <dt>

<span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**\_доступ для записи EC \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Разрешение на запись контроля доступа, позволяющее записывать данные в сборщик событий.


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC \_ открыть \_ всегда**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Открывает существующую подписку или создает подписку, если она не существует. Используется методом [**екопенсубскриптион**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .


</dt> </dl> </dd> <dt>

<span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**EC \_ Создание \_ нового**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Флаг, передаваемый функции [**екопенсубскриптион**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) , указывающий, что должна быть создана новая подписка.


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC \_ открыть \_ существующий**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Флаг, передаваемый функции [**екопенсубскриптион**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) , указывающий, что должна быть открыта существующая подписка.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                      |
| Header<br/>                   | <dl> <dt>Евколл. h</dt> </dl> |



 

 





