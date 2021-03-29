---
description: Событие изменения каталога Winsock для операции отключения поставщика многоуровневой службы (LSP).
ms.assetid: 6BCEECB1-92AD-47D8-952B-D0FD2A78EB45
title: WINSOCK_WS2HELP_LSP_DISABLE событие
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_DISABLE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6d785bfbd96d35717be7bbf76dab8f28f41c9fc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647529"
---
# <a name="winsock_ws2help_lsp_disable-event"></a>\_ \_ Событие отключения LSP Winsock WS2HELP \_

> [!Note]  
> Многоуровневые поставщики служб являются устаревшими. Начиная с Windows 8 и Windows Server 2012, используйте [платформу фильтрации Windows](../fwp/windows-filtering-platform-start-page.md).

 

Событие **Winsock \_ WS2HELP \_ LSP \_ Disable** — это событие изменения каталога Winsock для операции отключения поставщика многоуровневой службы (LSP).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_DISABLE = {0x3, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя LSP* 
</dt> <dd>

Имя LSP, полученное из элемента **сзпротокол** структуры [**\_ сведений о всапротокол**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для неактивного LSP.

</dd> <dt>

*Каталог* 
</dt> <dd>

Каталог Winsock (32-разрядный или 64-бит), в котором отключается LSP. Это целочисленное значение, равное 32 или 64.

</dd> <dt>

*Установщик* 
</dt> <dd>

Имя файла модуля приложения, которое делает вызов функции LSP отключить.

</dd> <dt>

*GUID* 
</dt> <dd>

Значение идентификатора GUID поставщика транспорта Winsock, для которого отключается LSP.

</dd> <dt>

*Категория* 
</dt> <dd>

Элемент **двкаталожентрид** структуры [**\_ сведений о всапротокол**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для LSP, который был отключен.

</dd> </dl>

У этого события нет параметров.

## <a name="remarks"></a>Комментарии

Событие **Winsock \_ WS2HELP \_ LSP \_ Disable** ОТСЛЕЖИВАЕТся для операции отключения LSP, если запись протокола отключена в каталоге Winsock.

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

 

 
