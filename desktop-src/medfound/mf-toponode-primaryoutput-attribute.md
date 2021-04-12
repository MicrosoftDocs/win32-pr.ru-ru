---
description: Указывает, какие выходные данные являются основными выходными данными на узле Tee.
ms.assetid: f7d98837-75da-48cc-8307-091be2d95392
title: Атрибут MF_TOPONODE_PRIMARYOUTPUT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4130f1df4789ad910ae013eab43168983b47c316
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344165"
---
# <a name="mf_toponode_primaryoutput-attribute"></a>\_Атрибут MF топоноде \_ PRIMARYOUTPUT

Указывает, какие выходные данные являются основными выходными данными на узле Tee.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к узлам tee (**\_ \_ \_ узел топологии MF tee**).

Значением этого атрибута является отсчитываемый от нуля индекс выходного соединения на этом tee узле. Это значение указывает, какие выходные данные являются основным выходным потоком. Конвейер ожидает запрос от основного выхода перед обработкой запросов из других выходных данных.

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

 

 




