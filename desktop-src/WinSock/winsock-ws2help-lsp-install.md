---
description: Событие изменения каталога Winsock для операции установки поставщика многоуровневой службы (LSP).
ms.assetid: 76A3D175-8CDC-486C-8341-D6314BCEC113
title: WINSOCK_WS2HELP_LSP_INSTALL событие
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_INSTALL
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2d95a77f68bafd29fde3bbf34336d9b31d2a412e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999064"
---
# <a name="winsock_ws2help_lsp_install-event"></a>\_ \_ Событие установки LSP Winsock WS2HELP \_

> [!Note]  
> Многоуровневые поставщики служб являются устаревшими. Начиная с Windows 8 и Windows Server 2012, используйте [платформу фильтрации Windows](../fwp/windows-filtering-platform-start-page.md).

 

Событие **\_ \_ \_ установки LSP Winsock WS2HELP** — это событие изменения каталога Winsock для операции установки поставщика многоуровневой службы (LSP).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_INSTALL = {0x1, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя LSP* 
</dt> <dd>

Имя LSP, полученное из элемента **сзпротокол** структуры [**\_ сведений о ВСАПРОТОКОЛ**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для устанавливаемого LSP.

</dd> <dt>

*Каталог* 
</dt> <dd>

Каталог Winsock (32-разрядный или 64-bit), где устанавливается LSP. Это целочисленное значение, равное 32 или 64.

</dd> <dt>

*Установщик* 
</dt> <dd>

Имя файла модуля приложения, выполняющего вызов установки LSP.

</dd> <dt>

*GUID* 
</dt> <dd>

Значение идентификатора GUID поставщика транспорта Winsock, в котором устанавливается LSP.

</dd> <dt>

*Категория* 
</dt> <dd>

Элемент **двкаталожентрид** структуры сведений о [**всапротокол \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для устанавливаемого LSP.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Событие **\_ \_ \_ установки LSP Winsock WS2HELP** будет отслеживаться для операции установки LSP при установке записи протокола в каталог Winsock.

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

 

 
