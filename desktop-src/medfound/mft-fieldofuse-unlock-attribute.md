---
description: Содержит указатель Имффиелдофусемфтунлокк, который можно использовать для разблокировки преобразования Media Foundation (MFT). Интерфейс Имффиелдофусемфтунлокк используется для разблокировки MFT с ограничениями на использование полей.
ms.assetid: 7f48967e-375a-4019-b14f-2f457b616cc0
title: Атрибут MFT_FIELDOFUSE_UNLOCK_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f02fbc032f16406a2b4407b197dc6140774001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812604"
---
# <a name="mft_fieldofuse_unlock_attribute-attribute"></a>\_Атрибут фиелдофусе \_ Unlock атрибута MFT \_

Содержит указатель [**имффиелдофусемфтунлокк**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , который можно использовать для разблокировки преобразования Media Foundation (MFT). Интерфейс **имффиелдофусемфтунлокк** используется для разблокировки MFT с ограничениями на использование полей.

## <a name="data-type"></a>Тип данных

**[](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) Имффиелдофусемфтунлокк \** _ хранится как _*IUnknown \**_

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: ununknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Комментарии

Дополнительные сведения об этом атрибуте см. в разделе [ограничения использования](field-of-use-restrictions.md).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Поле ограничений использования](field-of-use-restrictions.md)
</dt> <dt>

[**мфкреатетрансформактивате**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> </dl>

 

 




