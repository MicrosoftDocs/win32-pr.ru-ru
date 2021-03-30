---
description: Содержит указатель на дескриптор представления из защищенного пути к носителю (PMP).
ms.assetid: cf12552e-0963-46fa-9a26-44dd601ab68c
title: Атрибут MF_PD_APP_CONTEXT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8971ead121407ff1a7793c16b14f6b02d3dd102e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266020"
---
# <a name="mf_pd_app_context-attribute"></a>\_ \_ Атрибут контекста приложения MF PD \_

Содержит указатель на дескриптор представления из защищенного пути к носителю (PMP).

## <a name="data-type"></a>Тип данных

**IUnknown \** _

## <a name="remarks"></a>Комментарии

Прокси-сервер источника мультимедиа, созданный в процессе PMP, использует этот атрибут для хранения дескриптора удаленной презентации в дескрипторе представления приложения.

Значение этого атрибута является указателем на интерфейс [_ *имфпресентатиондескриптор* *](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .

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

[**Имфаттрибутес:: неизвестный**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**Имфаттрибутес:: Сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[Атрибуты дескриптора представления](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




