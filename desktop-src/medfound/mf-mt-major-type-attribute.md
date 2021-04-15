---
description: Основной тип GUID для типа мультимедиа.
ms.assetid: b88b5fcf-8025-4638-930d-9fc5cf0ec8a3
title: Атрибут MF_MT_MAJOR_TYPE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c4cc02df4f89e261605c91b71ac1c80ba38b9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701615"
---
# <a name="mf_mt_major_type-attribute"></a>\_ \_ Атрибут основного типа MF MT \_

Основной тип GUID для типа мультимедиа.

## <a name="data-type"></a>Тип данных

**GUID**

## <a name="remarks"></a>Комментарии

Основной тип определяет общую категорию данных мультимедиа. К основным типам относятся видео, звук, сценарий и т. д. Список возможных значений см. в разделе [основные типы носителей](media-type-guids.md).

Альтернативным способом получения этого атрибута является вызов [**имфмедиатипе:: жетмажортипе**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: a GUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**Имфаттрибутес:: Сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 




