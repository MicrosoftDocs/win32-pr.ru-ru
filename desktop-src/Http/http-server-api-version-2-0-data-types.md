---
title: Типы данных API сервера HTTP версии 2,0
description: Типы данных API сервера HTTP версии 2,0
ms.assetid: 13a0cac9-9e75-4350-a523-5ad9a57caad7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670099f3303682f52fdc78397dc7f229577b94d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661613"
---
# <a name="http-server-api-version-20-data-types"></a><span data-ttu-id="440bc-103">Типы данных API сервера HTTP версии 2,0</span><span class="sxs-lookup"><span data-stu-id="440bc-103">HTTP Server API Version 2.0 Data Types</span></span>

<span data-ttu-id="440bc-104">API сервера HTTP использует различные специальные типы идентификаторов назначения, объявленные в заголовке HTTP. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="440bc-104">The HTTP Server API uses various special purpose identifier types declared in the Http.h header as follows:</span></span>

-   <span data-ttu-id="440bc-105">**UShort** \_ \_ \_ параметр времени ожидания конфигурации службы HTTP \_ , \* \_ \_ \_ параметр времени ожидания конфигурации службы \_ ФТТП</span><span class="sxs-lookup"><span data-stu-id="440bc-105">**USHORT** HTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM, \*PHTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM</span></span>
-   <span data-ttu-id="440bc-106">**Улонглонг** непрозрачный идентификатор HTTP \_ \_ , \* \_ непрозрачный \_ идентификатор ФТТП</span><span class="sxs-lookup"><span data-stu-id="440bc-106">**ULONGLONG** HTTP\_OPAQUE\_ID, \*PHTTP\_OPAQUE\_ID</span></span>
-   <span data-ttu-id="440bc-107">**Протокол HTTP \_ Идентификатор запроса HTTP непрозрачного \_ идентификатора** \_ \_ , \* \_ идентификатор запроса ФТТП \_</span><span class="sxs-lookup"><span data-stu-id="440bc-107">**HTTP\_OPAQUE\_ID** HTTP\_REQUEST\_ID, \*PHTTP\_REQUEST\_ID</span></span>
-   <span data-ttu-id="440bc-108">**Протокол HTTP \_ Идентификатор HTTP-подключения непрозрачного \_ идентификатора** \_ \_ , \* \_ идентификатор подключения ФТТП \_</span><span class="sxs-lookup"><span data-stu-id="440bc-108">**HTTP\_OPAQUE\_ID** HTTP\_CONNECTION\_ID, \*PHTTP\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="440bc-109">**Протокол HTTP \_ Идентификатор \_** необработанного подключения HTTP непрозрачного идентификатора \_ \_ \_ , \* \_ идентификатор необработанного \_ подключения ФТТП \_</span><span class="sxs-lookup"><span data-stu-id="440bc-109">**HTTP\_OPAQUE\_ID** HTTP\_RAW\_CONNECTION\_ID, \*PHTTP\_RAW\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="440bc-110">**UShort** \_ \_ \_ параметр времени ожидания конфигурации службы HTTP \_ , \* \_ \_ \_ параметр времени ожидания конфигурации службы \_ ФТТП</span><span class="sxs-lookup"><span data-stu-id="440bc-110">**USHORT** HTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM, \*PHTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM</span></span>

<span data-ttu-id="440bc-111">Приложение не должно пытаться создать или изменить идентификатор, принадлежащий одному из этих типов.</span><span class="sxs-lookup"><span data-stu-id="440bc-111">An application should not attempt to generate or modify any identifier that belongs to one of these types.</span></span>

 

 




