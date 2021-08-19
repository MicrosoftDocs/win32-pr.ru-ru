---
description: Указывает, пытается ли сеанс мультимедиа изменить топологию при изменении формата потока.
ms.assetid: 8272ded7-9d27-4652-877b-40fc76426ffc
title: Атрибут MF_TOPOLOGY_DYNAMIC_CHANGE_NOT_ALLOWED (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2e984b45abc55246c9b1ae291c535c7fbb00f01f9405d827b7fe833b57a368
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875742"
---
# <a name="mf_topology_dynamic_change_not_allowed-attribute"></a>\_Атрибут " \_ Динамическое изменение топологии MF" \_ \_ не \_ разрешен

Указывает, пытается ли сеанс мультимедиа изменить топологию при изменении формата потока.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфтопологи**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Remarks

Этот атрибут управляет реакцией сеанса мультимедиа при изменении формата потока во время потоковой передачи.

Если в результате изменения формата и \_ атрибута " \_ Динамическое изменение топологии MF" \_ \_ \_ указано **значение false**, сеанс мультимедиа может вставить новые узлы в топологию в соответствии с новым форматом. Например, при изменении размера видео сеанс мультимедиа может добавить Media Foundation преобразование (MFT), которое изменяет размер видео. В противном случае, если атрибут имеет **значение true**, сеанс мультимедиа не изменит топологию.

Значение этого атрибута по умолчанию равно **false**. Рекомендуемое значение — **false**.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                            |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты топологии](topology-attributes.md)
</dt> </dl>

 

 




