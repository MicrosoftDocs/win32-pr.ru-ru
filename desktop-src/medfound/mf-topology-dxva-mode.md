---
description: Указывает, включает ли загрузчик топологии ускорение видео Microsoft DirectX (ДКСВА) в топологии.
ms.assetid: 03783ef3-f957-41e3-9734-94cb34ecc088
title: Атрибут MF_TOPOLOGY_DXVA_MODE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5462ccf575f94935d100eb70a6d806e139f09762151c2dad8d4e155ca5d1d17e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875741"
---
# <a name="mf_topology_dxva_mode-attribute"></a>\_ \_ Атрибут режима ДКСВА топологии MF \_

Указывает, включает ли загрузчик топологии ускорение видео Microsoft DirectX (ДКСВА) в топологии.

## <a name="data-type"></a>Тип данных

**[**Мфтопологи \_ \_Режим дксва**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** , хранящийся как **UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфтопологи**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Remarks

Значением этого атрибута является константа перечисления [**мфтопологи \_ дксва \_ mode**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) . Значение по умолчанию — **мфтопологи \_ дксва \_ по умолчанию**.

Этот атрибут определяет, какой МФТС получает указатель на диспетчер устройств Direct3D. Чтобы включить полное ускорение видео, присвойте параметру значение **мфтопологи \_ дксва \_ Full**. Значение **мфтопологи \_ дксва \_ по умолчанию** определено для обеспечения обратной совместимости. оно соответствует поведению всех более ранних версий Microsoft Media Foundation.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                            |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[диспетчер устройств Direct3D](direct3d-device-manager.md)
</dt> <dt>

[Атрибуты топологии](topology-attributes.md)
</dt> </dl>

 

 




