---
description: Указывает время последнего изменения презентации.
ms.assetid: 12990de2-7656-4781-943b-c46f42a0e38d
title: Атрибут MF_PD_LAST_MODIFIED_TIME (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f97bf47cff32834b694f36cbd4c9062e06f2d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998851"
---
# <a name="mf_pd_last_modified_time-attribute"></a>\_ \_ \_ Атрибут времени последнего изменения MF PD \_

Указывает время последнего изменения презентации.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Комментарии

Источники мультимедиа могут задавать этот атрибут для дескриптора презентации. Значением атрибута является структура **fileTime** , которая описана в Windows SDK.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Атрибуты дескриптора представления](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




