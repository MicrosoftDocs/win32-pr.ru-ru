---
title: Типы данных API сервера HTTP версии 1,0
description: API сервера HTTP использует различные специальные типы идентификаторов, объявленные в файле заголовка HTTP. h как 64-разрядные целые числа без знака.
ms.assetid: bec1d41e-0c80-49bc-84e1-b16c409cd0f3
keywords:
- Тип HTTP_CONNECTION_ID HTTP
- Тип HTTP_RAW_CONNECTION_ID HTTP
- Тип HTTP_REQUEST_ID HTTP
- Тип HTTP_URL_CONTEXT HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681e24c06334a9010287e2084d9d6a04428ca6a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681522"
---
# <a name="http-server-api-version-10-data-types"></a>Типы данных API сервера HTTP версии 1,0

API сервера HTTP использует различные типы идентификаторов специального назначения, объявленные в файле заголовка HTTP. h, как 64-разрядные целые числа без знака (**улонглонгс**):

-   Идентификатор HTTP- \_ соединения \_
-   Идентификатор HTTP- \_ подключения необработанного \_ соединения \_
-   Идентификатор HTTP- \_ запроса \_
-   \_контекст URL-адреса HTTP \_

Приложение не должно пытаться создать или изменить идентификатор, принадлежащий одному из этих типов.

 

 




