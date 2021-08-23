---
description: Содержит указатель Имффиелдофусемфтунлокк, который можно использовать для разблокировки преобразования Media Foundation (MFT). Интерфейс Имффиелдофусемфтунлокк используется для разблокировки MFT с ограничениями на использование полей.
ms.assetid: 7f48967e-375a-4019-b14f-2f457b616cc0
title: Атрибут MFT_FIELDOFUSE_UNLOCK_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476ae7ffdc6de506b4dbc2f49ec7a6b19b01affafd53f0c9495f9f5c396c5caf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973073"
---
# <a name="mft_fieldofuse_unlock_attribute-attribute"></a>\_Атрибут фиелдофусе \_ Unlock атрибута MFT \_

Содержит указатель [**имффиелдофусемфтунлокк**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , который можно использовать для разблокировки преобразования Media Foundation (MFT). Интерфейс **имффиелдофусемфтунлокк** используется для разблокировки MFT с ограничениями на использование полей.

## <a name="data-type"></a>Тип данных

**[**Имффиелдофусемфтунлокк**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) \* *_ хранится как _* IUnknown\***

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Remarks

Дополнительные сведения об этом атрибуте см. в разделе [ограничения использования](field-of-use-restrictions.md).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для настольных приложений Server 2008 R2 \|\]<br/>                           |
| Заголовок<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Поле ограничений использования](field-of-use-restrictions.md)
</dt> <dt>

[**мфкреатетрансформактивате**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> </dl>

 

 




