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
ms.openlocfilehash: 578479710856e149760202699be13d4b30b50709f6ea9b389e055793a8b0ca94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733134"
---
# <a name="winsock_ws2help_lsp_disable-event"></a>\_ \_ Событие отключения LSP Winsock WS2HELP \_

> [!Note]  
> Многоуровневые поставщики служб являются устаревшими. начиная с Windows 8 и Windows Server 2012 используйте [платформу фильтрации Windows](../fwp/windows-filtering-platform-start-page.md).

 

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

## <a name="remarks"></a>Remarks

Событие **Winsock \_ WS2HELP \_ LSP \_ Disable** ОТСЛЕЖИВАЕТся для операции отключения LSP, если запись протокола отключена в каталоге Winsock.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



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

 

 
