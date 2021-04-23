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
# <a name="http-server-api-version-10-data-types"></a><span data-ttu-id="87971-107">Типы данных API сервера HTTP версии 1,0</span><span class="sxs-lookup"><span data-stu-id="87971-107">HTTP Server API Version 1.0 Data Types</span></span>

<span data-ttu-id="87971-108">API сервера HTTP использует различные типы идентификаторов специального назначения, объявленные в файле заголовка HTTP. h, как 64-разрядные целые числа без знака (**улонглонгс**):</span><span class="sxs-lookup"><span data-stu-id="87971-108">The HTTP Server API uses various special purpose identifier types declared in the Http.h header file as 64-bit unsigned integers (**ULONGLONGs**):</span></span>

-   <span data-ttu-id="87971-109">Идентификатор HTTP- \_ соединения \_</span><span class="sxs-lookup"><span data-stu-id="87971-109">HTTP\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="87971-110">Идентификатор HTTP- \_ подключения необработанного \_ соединения \_</span><span class="sxs-lookup"><span data-stu-id="87971-110">HTTP\_RAW\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="87971-111">Идентификатор HTTP- \_ запроса \_</span><span class="sxs-lookup"><span data-stu-id="87971-111">HTTP\_REQUEST\_ID</span></span>
-   <span data-ttu-id="87971-112">\_контекст URL-адреса HTTP \_</span><span class="sxs-lookup"><span data-stu-id="87971-112">HTTP\_URL\_CONTEXT</span></span>

<span data-ttu-id="87971-113">Приложение не должно пытаться создать или изменить идентификатор, принадлежащий одному из этих типов.</span><span class="sxs-lookup"><span data-stu-id="87971-113">An application should not attempt to generate or modify any identifier that belongs to one of these types.</span></span>

 

 




