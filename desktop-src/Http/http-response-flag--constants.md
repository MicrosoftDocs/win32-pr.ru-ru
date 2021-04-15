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
ms.openlocfilehash: 96b7c34d453c1b9bbe45cf2c85ad268b414f3439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661865"
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
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                        |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                           |
| Header<br/>                   | <dl> <dt>HTTP. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы API сервера HTTP версии 2,0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**HTTP- \_ ответ \_ v1**](/windows/desktop/api/Http/ns-http-http_response_v1)
</dt> </dl>

 

 





