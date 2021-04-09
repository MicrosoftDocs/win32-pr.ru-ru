---
title: Дескрипторы возобновления перечисления
description: Дескрипторы возобновления перечисления — это идентификаторы фактического ключа возобновления, содержащегося в данных экземпляра для функции. Это необходимо для обеспечения безопасности, взаимодействия и упрощения кода вызывающей стороны для функции.
ms.assetid: 6734e99b-7f8c-43c9-96e3-44c9783960dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f20e7a7d5e1f9afb15e6adad4c0d7643bf841d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986505"
---
# <a name="enumeration-resume-handles"></a><span data-ttu-id="dea49-104">Дескрипторы возобновления перечисления</span><span class="sxs-lookup"><span data-stu-id="dea49-104">Enumeration Resume Handles</span></span>

<span data-ttu-id="dea49-105">Дескрипторы возобновления перечисления — это идентификаторы фактического ключа возобновления, содержащегося в данных экземпляра для функции.</span><span class="sxs-lookup"><span data-stu-id="dea49-105">Enumeration resume handles are identifiers for the actual resume key contained in the instance data for the function.</span></span> <span data-ttu-id="dea49-106">Это необходимо для обеспечения безопасности, взаимодействия и упрощения кода вызывающей стороны для функции.</span><span class="sxs-lookup"><span data-stu-id="dea49-106">This is required for security, interoperability, and to simplify the caller code for the function.</span></span>

<span data-ttu-id="dea49-107">Если для указателя на обработчик возобновления передается **значение NULL** , то обработчик не сохраняется и поиск перечисления не может быть продолжен.</span><span class="sxs-lookup"><span data-stu-id="dea49-107">If a **NULL** is passed for the pointer to the resume handle, no handle is stored and the enumeration search cannot be continued.</span></span> <span data-ttu-id="dea49-108">Это полезно в тех случаях, когда приложению не требуется перечислять все элементы.</span><span class="sxs-lookup"><span data-stu-id="dea49-108">This is useful in cases where the application does not want to enumerate all the items.</span></span>

<span data-ttu-id="dea49-109">Если при вызове перечисления возвращается ошибка, то обработчик возобновления должен рассматриваться как недопустимый и не используется для последующих вызовов перечисления.</span><span class="sxs-lookup"><span data-stu-id="dea49-109">If an error is returned from an enumeration call, the resume handle must be treated as invalid and not used for any subsequent enumeration calls.</span></span> <span data-ttu-id="dea49-110">В этом случае необходимо перезапустить перечисление с начала.</span><span class="sxs-lookup"><span data-stu-id="dea49-110">When this occurs you must restart the enumeration from the beginning.</span></span>

 

 




