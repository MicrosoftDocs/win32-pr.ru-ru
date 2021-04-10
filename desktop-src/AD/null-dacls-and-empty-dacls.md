---
title: Списки DACL NULL и пустые списки DACL (AD DS)
description: Наличие списка управления доступом (DACL) со значением NULL в атрибуте Нтсекуритидескриптор любого объекта может привести к серьезным угрозам безопасности.
ms.assetid: 32b786d2-e676-4402-ad22-550de9289494
ms.tgt_platform: multiple
keywords:
- Списки DACL со значением NULL и пустые DACL
- DACL Active Directory, NULL и Empty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b841bb0253547fea291232fb4c9e6e0f3377d18
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103987318"
---
# <a name="null-dacls-and-empty-dacls-ad-ds"></a><span data-ttu-id="63084-105">Списки DACL NULL и пустые списки DACL (AD DS)</span><span class="sxs-lookup"><span data-stu-id="63084-105">Null DACLs and Empty DACLs (AD DS)</span></span>

<span data-ttu-id="63084-106">Наличие списка управления доступом (DACL) со значением NULL в атрибуте [**нтсекуритидескриптор**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) любого объекта может привести к серьезным угрозам безопасности.</span><span class="sxs-lookup"><span data-stu-id="63084-106">The presence of a null discretionary access-control list (DACL) in the [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) attribute of any object can create a serious security risk.</span></span> <span data-ttu-id="63084-107">Пустой список DACL предоставляет полный доступ любому пользователю, который запрашивает его; Обычная проверка безопасности не выполняется в отношении объекта.</span><span class="sxs-lookup"><span data-stu-id="63084-107">A null DACL grants full access to any user that requests it; normal security checking is not performed with respect to the object.</span></span> <span data-ttu-id="63084-108">Пустой список DACL не следует путать с пустым списком DACL.</span><span class="sxs-lookup"><span data-stu-id="63084-108">A null DACL should not be confused with an empty DACL.</span></span> <span data-ttu-id="63084-109">Пустой DACL — это правильно выделенный и инициализированный DACL, который не содержит записей контроля доступа (ACE).</span><span class="sxs-lookup"><span data-stu-id="63084-109">An empty DACL is a properly allocated and initialized DACL containing no access-control entries (ACEs).</span></span> <span data-ttu-id="63084-110">Пустой DACL не предоставляет доступа к объекту, которому он назначен.</span><span class="sxs-lookup"><span data-stu-id="63084-110">An empty DACL grants no access to the object it is assigned to.</span></span>

<span data-ttu-id="63084-111">Дополнительные сведения см. в статьях [DACL NULL и пустые списки DACL](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls).</span><span class="sxs-lookup"><span data-stu-id="63084-111">For more information, see [Null DACLs and Empty DACLs](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls).</span></span>

 

 