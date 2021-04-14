---
description: Указывает, использует ли сеанс мультимедиа преднакат приемника носителя, представленного этим узлом топологии.
ms.assetid: 1781f3a0-6baa-4e06-b2eb-9a8f572aa040
title: Атрибут MF_TOPONODE_DISABLE_PREROLL (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3d031a4ee50262e717731ae517d4441e9be9a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647673"
---
# <a name="mf_toponode_disable_preroll-attribute"></a>MF \_ топоноде \_ Отключить \_ атрибут onрулона

Указывает, использует ли сеанс мультимедиа преднакат приемника носителя, представленного этим узлом топологии.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к выходным узлам **( \_ \_ \_ узел выходных данных топологии MF**).

Если значение этого атрибута равно **true**, сеанс мультимедиа не выполняет промежуточную перегрузку данных в приемник мультимедиа, даже если приемник мультимедиа предоставляет интерфейс [**имфмедиасинкпреролл**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) . Если значение равно **false**, сеанс мультимедиа предмещает данные, если приемник мультимедиа реализует **имфмедиасинкпреролл**. Значение по умолчанию — **false**.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Атрибуты узла топологии](topology-node-attributes.md)
</dt> </dl>

 

 




