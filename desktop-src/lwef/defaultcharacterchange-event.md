---
title: Событие Дефаултчарактерчанже
description: Событие Дефаултчарактерчанже
ms.assetid: 14b86a44-8fd2-4719-b7b5-cdcc618d27cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab92fe04f9c42466d559e9b4610eafc8490556d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411144"
---
# <a name="defaultcharacterchange-event"></a><span data-ttu-id="879ed-103">Событие Дефаултчарактерчанже</span><span class="sxs-lookup"><span data-stu-id="879ed-103">DefaultCharacterChange Event</span></span>

<span data-ttu-id="879ed-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="879ed-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="879ed-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="879ed-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="879ed-106">Происходит, когда пользователь изменяет символ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="879ed-106">Occurs when the user changes the default character.</span></span>

</dd> <dt>

<span data-ttu-id="879ed-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="879ed-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="879ed-108"> *Подагент.\ *\ *\ * дефаултчарактерчанже*\ *  **(ByVal** *GUID\ *\ * *)**</span><span class="sxs-lookup"><span data-stu-id="879ed-108">**Sub** *agent.\*\*\*DefaultCharacterChange*\* **(ByVal** *GUID\*\*\*)*\*</span></span>



| <span data-ttu-id="879ed-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="879ed-109">Part</span></span>   | <span data-ttu-id="879ed-110">Описание</span><span class="sxs-lookup"><span data-stu-id="879ed-110">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="879ed-111">*GUID*</span><span class="sxs-lookup"><span data-stu-id="879ed-111">*GUID*</span></span> | <span data-ttu-id="879ed-112">Возвращает уникальный идентификатор для символа.</span><span class="sxs-lookup"><span data-stu-id="879ed-112">Returns the unique identifier for the character.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="879ed-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="879ed-113">Remarks</span></span>

<span data-ttu-id="879ed-114">Это событие указывает, что пользователь изменил символ, назначенный в качестве символа по умолчанию для пользователя.</span><span class="sxs-lookup"><span data-stu-id="879ed-114">This event indicates when the user has changed the character assigned as the user's default character.</span></span> <span data-ttu-id="879ed-115">Сервер отправляет его только клиентам, которые загрузили символ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="879ed-115">The server sends this only to clients that have loaded the default character.</span></span>

<span data-ttu-id="879ed-116">Когда появляется новый символ, он предполагает тот же размер, что и любой уже загруженный экземпляр символа или предыдущий символ по умолчанию (в указанном порядке).</span><span class="sxs-lookup"><span data-stu-id="879ed-116">When the new character appears, it assumes the same size as any already loaded instance of the character or the previous default character (in that order).</span></span>

### <a name="see-also"></a><span data-ttu-id="879ed-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="879ed-117">See Also</span></span>

<span data-ttu-id="879ed-118">[**Метод шовдефаултчарактерпропертиес**](showdefaultcharacterproperties-method.md), [ **метод Load**](load-method.md)</span><span class="sxs-lookup"><span data-stu-id="879ed-118">[**ShowDefaultCharacterProperties method**](showdefaultcharacterproperties-method.md), [**Load method**](load-method.md)</span></span>


 

 




