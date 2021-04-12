---
description: Содержит указатель на прокси-объект для дескриптора представления приложений.
ms.assetid: 0cd83204-0d32-417c-8911-1d3358eb0802
title: Атрибут MF_PD_PMPHOST_CONTEXT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e8903e438a4649ae43d7aa2072e5a5146e3126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423973"
---
# <a name="mf_pd_pmphost_context-attribute"></a>\_ \_ Атрибут контекста MF PD пмфост \_

Содержит указатель на прокси-объект для дескриптора представления приложения.

## <a name="data-type"></a>Тип данных

**IUnknown \** _

## <a name="remarks"></a>Комментарии

Узел защищенного пути к носителю (PMP) использует этот атрибут для хранения дескриптора представления приложения в дескрипторе удаленной презентации. Значение атрибута является указателем на интерфейс [_ *имфремотепрокси* *](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy) .

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

[**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Атрибуты дескриптора представления](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




