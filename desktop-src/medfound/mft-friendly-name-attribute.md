---
description: Содержит отображаемое имя для аппаратного преобразования Media Foundation (MFT).
ms.assetid: 8f2634e8-6bdd-463a-893a-6dc616c8333d
title: Атрибут MFT_FRIENDLY_NAME_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33417fd30f4d856ce7306fbbbd492fa29575f7ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647273"
---
# <a name="mft_friendly_name_attribute-attribute"></a>\_ \_ Атрибут атрибута понятного имени MFT \_

Содержит отображаемое имя для аппаратного преобразования Media Foundation (MFT).

## <a name="data-type"></a>Тип данных

**WCHAR \** _

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: GetString* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Комментарии

Этот атрибут поддерживается МФТС на основе оборудования. Он также задается для указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , выделенных функцией [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , если эти указатели представляют аппаратную МФТС.

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

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 




