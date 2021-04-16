---
description: Пустой список DACL предоставляет полный доступ любому пользователю, который его запрашивает. Пустой DACL — это правильно выделенный и инициализированный DACL, который не содержит записей контроля доступа. Пустой DACL не предоставляет доступа к объекту, которому он назначен.
ms.assetid: 26e5c98d-bbdc-4f9f-96e0-18d1c429f1e6
title: Списки DACL NULL и пустые списки DACL (авторизация)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c06942d7b2d188a74b7e3e307cf60d6740a4251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664299"
---
# <a name="null-dacls-and-empty-dacls-authorization"></a><span data-ttu-id="6054f-105">Списки DACL NULL и пустые списки DACL (авторизация)</span><span class="sxs-lookup"><span data-stu-id="6054f-105">Null DACLs and Empty DACLs (Authorization)</span></span>

<span data-ttu-id="6054f-106">Если [*избирательный список управления доступом*](/windows/desktop/SecGloss/d-gly) (DACL), принадлежащий [*дескриптору безопасности*](/windows/desktop/SecGloss/s-gly) объекта, имеет значение **null**, создается пустой список DACL.</span><span class="sxs-lookup"><span data-stu-id="6054f-106">If the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) that belongs to an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly) is set to **NULL**, a null DACL is created.</span></span> <span data-ttu-id="6054f-107">Пустой список DACL предоставляет полный доступ любому пользователю, который запрашивает его; Обычная проверка безопасности не выполняется в отношении объекта.</span><span class="sxs-lookup"><span data-stu-id="6054f-107">A null DACL grants full access to any user that requests it; normal security checking is not performed with respect to the object.</span></span> <span data-ttu-id="6054f-108">Пустой список DACL не следует путать с пустым списком DACL.</span><span class="sxs-lookup"><span data-stu-id="6054f-108">A null DACL should not be confused with an empty DACL.</span></span> <span data-ttu-id="6054f-109">Пустой DACL — это правильно выделенный и инициализированный DACL, который не содержит [*записей контроля доступа*](/windows/desktop/SecGloss/a-gly) (ACE).</span><span class="sxs-lookup"><span data-stu-id="6054f-109">An empty DACL is a properly allocated and initialized DACL that contains no [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs).</span></span> <span data-ttu-id="6054f-110">Пустой DACL не предоставляет доступа к объекту, которому он назначен.</span><span class="sxs-lookup"><span data-stu-id="6054f-110">An empty DACL grants no access to the object it is assigned to.</span></span>

<span data-ttu-id="6054f-111">Пример создания списка DACL см. в разделе [Создание списка DACL](/windows/desktop/SecBP/creating-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="6054f-111">For an example of how to create a DACL, see [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span></span>

 

 
