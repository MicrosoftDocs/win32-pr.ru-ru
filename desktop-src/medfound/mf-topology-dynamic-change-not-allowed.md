---
description: Указывает, пытается ли сеанс мультимедиа изменить топологию при изменении формата потока.
ms.assetid: 8272ded7-9d27-4652-877b-40fc76426ffc
title: Атрибут MF_TOPOLOGY_DYNAMIC_CHANGE_NOT_ALLOWED (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ade7308c4fadef315fae0828a5c2cb29575b03a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497355"
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

## <a name="remarks"></a>Комментарии

Этот атрибут управляет реакцией сеанса мультимедиа при изменении формата потока во время потоковой передачи.

Если в результате изменения формата и \_ атрибута " \_ Динамическое изменение топологии MF" \_ \_ \_ указано **значение false**, сеанс мультимедиа может вставить новые узлы в топологию в соответствии с новым форматом. Например, при изменении размера видео сеанс мультимедиа может добавить Media Foundation преобразование (MFT), которое изменяет размер видео. В противном случае, если атрибут имеет **значение true**, сеанс мультимедиа не изменит топологию.

Значение этого атрибута по умолчанию равно **false**. Рекомендуемое значение — **false**.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                         |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                            |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты топологии](topology-attributes.md)
</dt> </dl>

 

 




