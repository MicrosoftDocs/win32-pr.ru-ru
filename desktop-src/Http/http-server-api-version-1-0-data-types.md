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
ms.openlocfilehash: 151ef975470ca21c6e82e5bc7bd7bd8b99a70573385375e8552b6660ce78f631
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950803"
---
# <a name="http-server-api-version-10-data-types"></a>Типы данных API сервера HTTP версии 1,0

API сервера HTTP использует различные типы идентификаторов специального назначения, объявленные в файле заголовка HTTP. h, как 64-разрядные целые числа без знака (**улонглонгс**):

-   Идентификатор HTTP- \_ соединения \_
-   Идентификатор HTTP- \_ подключения необработанного \_ соединения \_
-   Идентификатор HTTP- \_ запроса \_
-   \_контекст URL-адреса HTTP \_

Приложение не должно пытаться создать или изменить идентификатор, принадлежащий одному из этих типов.

 

 




