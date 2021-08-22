---
description: Событие изменения каталога Winsock для операции сброса каталога Winsock.
ms.assetid: BE8DC0DB-0F96-4015-87F5-ECF25AE164AA
title: WINSOCK_WS2HELP_LSP_RESET событие
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_RESET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3c9a638d962db908b24387d7baeb2f34d4e09ece561fdd1796a8a44930a5dfb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051292"
---
# <a name="winsock_ws2help_lsp_reset-event"></a>\_ \_ Событие сброса LSP Winsock WS2HELP \_

> [!Note]  
> Многоуровневые поставщики служб являются устаревшими. начиная с Windows 8 и Windows Server 2012 используйте [платформу фильтрации Windows](../fwp/windows-filtering-platform-start-page.md).

 

Событием **\_ \_ \_ сброса LSP Winsock WS2HELP** является событием изменения каталога Winsock для операции сброса каталога Winsock.


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_RESET = {0x4, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Каталог* 
</dt> <dd>

Каталог Winsock (32-разрядный или 64-разрядный), который сбрасывается. Это целочисленное значение, равное 32 или 64.

</dd> </dl>

## <a name="remarks"></a>Remarks

Событие **" \_ \_ \_ Сброс LSP" для Winsock WS2HELP** отслеживается для операции поставщика многоуровневых служб Winsock (LSP) при сбросе каталога Winsock.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Управление трассировкой Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Трассировка Winsock](winsock-tracing.md)
</dt> <dt>

[Уровни трассировки Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Сведения о трассировке изменений каталога Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
