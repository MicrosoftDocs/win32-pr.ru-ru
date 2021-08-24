---
description: Указывает, поддерживает ли преобразование, связанное с узлом топологии, поддержку ускорения видео DirectX (ДКСВА).
ms.assetid: b9e393be-0bc0-4cf6-be44-e9e95339c434
title: Атрибут MF_TOPONODE_D3DAWARE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e49735a1178cc521efd152f4fa11ab7c84069b07d0e5001f0f0e8e38bec940ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607154"
---
# <a name="mf_toponode_d3daware-attribute"></a>\_Атрибут MF топоноде \_ D3DAWARE

Указывает, поддерживает ли преобразование, связанное с узлом топологии, поддержку ускорения видео DirectX (ДКСВА).

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Remarks

Этот атрибут применяется к узлам преобразования (**\_ \_ \_ узел преобразования топологии MF**).

Обычно приложения не используют этот атрибут напрямую. Сеанс мультимедиа задает этот атрибут на узле преобразования, если в базовом преобразовании Media Foundation имеется атрибут [**MF \_ SA с \_ \_ поддержкой D3D**](mf-sa-d3d-aware-attribute.md) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

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

 

 




