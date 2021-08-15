---
title: Константы HTTP_RESPONSE_FLAG_ (HTTP. h)
description: Определите параметры для настройки ответов в API HTTP-сервера.
ms.assetid: bcb59457-fd22-4166-8a72-ba85209ec8c7
topic_type:
- apiref
api_name:
- HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3099012df5be9ed4a53d3072319be6dc47ede32b71567749c4668cd7870fee29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394412"
---
# <a name="http_response_flag_-constants"></a>\_ \_ Константы флага HTTP-ответа \_

Константы **\_ \_ флага \_ http-ответа** определяют параметры для настройки ответов в API-интерфейсе сервера HTTP.

Эти константы используются в элементе **flags** структуры [**HTTP \_ Response \_ v1**](/windows/desktop/api/Http/ns-http-http_response_v1) .

<dl> <dt>

<span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**\_флаг ответа \_ HTTP \_ \_ доступно несколько кодировок \_**
</dt> <dd> <dl> <dt>



Для этого ресурса доступны кодировки, отличные от формы Identity. Этот флаг пропускается, если приложение не запросило кэширование ответа. Он используется как подсказка к API HTTP-сервера для согласования содержимого при обслуживании из кэша ответов ядра.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                           |
| Header<br/>                   | <dl> <dt>HTTP. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы API сервера HTTP версии 2,0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**HTTP- \_ ответ \_ v1**](/windows/desktop/api/Http/ns-http-http_response_v1)
</dt> </dl>

 

 





