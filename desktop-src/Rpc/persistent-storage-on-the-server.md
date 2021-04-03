---
title: Постоянное хранилище на сервере
description: Вы можете оптимизировать приложение, чтобы заглушка сервера не вымогла освободить память на сервере при завершении удаленного вызова процедуры.
ms.assetid: 340334e2-94ac-4be2-a16d-38bc4c64e7db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7237fe6136918e5495ee1f22bac0991d71c5dbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986657"
---
# <a name="persistent-storage-on-the-server"></a><span data-ttu-id="546ea-103">Постоянное хранилище на сервере</span><span class="sxs-lookup"><span data-stu-id="546ea-103">Persistent Storage on the Server</span></span>

<span data-ttu-id="546ea-104">Вы можете оптимизировать приложение, чтобы заглушка сервера не вымогла освободить память на сервере при завершении удаленного вызова процедуры.</span><span class="sxs-lookup"><span data-stu-id="546ea-104">You can optimize your application so the server stub does not free memory on the server at the conclusion of a remote procedure call.</span></span> <span data-ttu-id="546ea-105">Например, если обработчик контекста будет управляться несколькими удаленными процедурами, можно использовать атрибут ACF, **\[ выделяющий (не \_ освобождая) \]** , чтобы хранить выделенную память на сервере.</span><span class="sxs-lookup"><span data-stu-id="546ea-105">For example, when a context handle will be manipulated by several remote procedures, you can use the ACF attribute **\[allocate(dont\_free)\]** to retain the allocated memory on the server.</span></span>

<span data-ttu-id="546ea-106">Атрибут **\[ выделения (не \_ Free) \]** добавляется в объявление **typedef** ACF в ACF.</span><span class="sxs-lookup"><span data-stu-id="546ea-106">The **\[allocate(dont\_free)\]** attribute is added to the ACF **typedef** declaration in the ACF.</span></span> <span data-ttu-id="546ea-107">Пример:</span><span class="sxs-lookup"><span data-stu-id="546ea-107">For example:</span></span>

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes, dont_free)] P_TREE_TYPE;
```

<span data-ttu-id="546ea-108">Если задан атрибут **\[ выделения (не \_ свободен) \]** , то в качестве серверной заглушки выделяется структура данных дерева, но не освобождается.</span><span class="sxs-lookup"><span data-stu-id="546ea-108">When the **\[allocate(dont\_free)\]** attribute is specified, the tree data structure is allocated, but not freed, by the server stub.</span></span> <span data-ttu-id="546ea-109">При внесении указателей на такие постоянные области данных, которые доступны для других подпрограмм, например путем копирования указателей на глобальные переменные, сохраненные данные доступны другим серверным функциям.</span><span class="sxs-lookup"><span data-stu-id="546ea-109">When you make the pointers to such persistent data areas available to other routines—for example, by copying the pointers to global variables—the retained data is accessible to other server functions.</span></span> <span data-ttu-id="546ea-110">Атрибут **\[ выделения (не \_ Free) \]** особенно полезен для поддержания постоянных структур указателей в составе сведений о состоянии сервера, связанных с типом обработчика контекста.</span><span class="sxs-lookup"><span data-stu-id="546ea-110">The **\[allocate(dont\_free)\]** attribute is particularly useful for maintaining persistent pointer structures as part of the server state information associated with a context-handle type.</span></span>

 

 




