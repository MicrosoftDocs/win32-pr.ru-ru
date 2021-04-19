---
description: Событие изменения каталога Winsock для операции удаления поставщика многоуровневой службы (LSP).
ms.assetid: 86FF17F7-8CCF-4A03-899F-42BFACDF3F54
title: WINSOCK_WS2HELP_LSP_REMOVE событие
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_REMOVE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 597cd2f8cfc3bb7727301e64af53671bafbd9469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693382"
---
# <a name="winsock_ws2help_lsp_remove-event"></a>\_ \_ Событие удаления LSP Winsock WS2HELP \_

> [!Note]  
> Многоуровневые поставщики служб являются устаревшими. Начиная с Windows 8 и Windows Server 2012, используйте [платформу фильтрации Windows](../fwp/windows-filtering-platform-start-page.md).

 

Событие **\_ \_ \_ удаления LSP Winsock WS2HELP** является событием изменения каталога Winsock для операции удаления поставщика многоуровневой службы (LSP).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_REMOVE = {0x2, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя LSP* 
</dt> <dd>

Имя LSP, полученное из элемента **сзпротокол** структуры [**\_ сведений о ВСАПРОТОКОЛ**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для удаляемого LSP.

</dd> <dt>

*Каталог* 
</dt> <dd>

Каталог Winsock (32-разрядный или 64-бит), в который удаляется LSP. Это целочисленное значение, равное 32 или 64.

</dd> <dt>

*Установщик* 
</dt> <dd>

Имя файла модуля приложения, вызывающего удаление LSP.

</dd> <dt>

*GUID* 
</dt> <dd>

Значение идентификатора GUID поставщика транспорта Winsock, из которого удаляется LSP.

</dd> <dt>

*Категория* 
</dt> <dd>

Элемент **двкаталожентрид** структуры сведений о [**всапротокол \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для удаляемого LSP.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Событие **\_ \_ \_ удаления LSP Winsock WS2HELP** будет отслеживаться для операции удаления LSP при удалении записи протокола из каталога Winsock.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Управление трассировкой Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Трассировка Winsock](winsock-tracing.md)
</dt> <dt>

[Уровни трассировки Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Сведения о трассировке изменений каталога Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
