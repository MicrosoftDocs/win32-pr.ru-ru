---
title: Распространенные ошибки (AD DS)
description: В следующей таблице содержится список распространенных ошибок, которые могут возникать в зависимости от области вложенности группы.
ms.assetid: 844d4280-a943-4906-b0c6-0c650ef9c114
ms.tgt_platform: multiple
keywords:
- Распространенные ошибки AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c719aad39690932de51c58d0f8081a8c855980bd
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2019
ms.locfileid: "104487252"
---
# <a name="common-errors-ad-ds"></a><span data-ttu-id="7a740-104">Распространенные ошибки (AD DS)</span><span class="sxs-lookup"><span data-stu-id="7a740-104">Common Errors (AD DS)</span></span>

<span data-ttu-id="7a740-105">В следующей таблице содержится список распространенных ошибок, которые могут возникать в зависимости от области вложенности группы.</span><span class="sxs-lookup"><span data-stu-id="7a740-105">The following table contains a list of common errors that can occur based on the scope of the group being nested.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a740-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7a740-106">HRESULT</span></span></th>
<th><span data-ttu-id="7a740-107">Описание</span><span class="sxs-lookup"><span data-stu-id="7a740-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7a740-108">0x8007001F</span><span class="sxs-lookup"><span data-stu-id="7a740-108">0x8007001F</span></span></td>
<td><span data-ttu-id="7a740-109">Общая ошибка.</span><span class="sxs-lookup"><span data-stu-id="7a740-109">General failure.</span></span> <span data-ttu-id="7a740-110">Эта ошибка возникает при попытке выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7a740-110">This error occurs if you attempt to:</span></span>
<ul>
<li><span data-ttu-id="7a740-111">Добавьте локальную группу домена в глобальную или универсальную группу или локальную группу домена в другом домене.</span><span class="sxs-lookup"><span data-stu-id="7a740-111">Add a domain local group to a global or universal group or a domain local group in another domain.</span></span> <span data-ttu-id="7a740-112">Локальные группы домена могут добавляться только в качестве членов других локальных групп домена в том же домене.</span><span class="sxs-lookup"><span data-stu-id="7a740-112">Domain local groups can only be added as members to other domain local groups in the same domain.</span></span></li>
<li><span data-ttu-id="7a740-113">Добавьте универсальную группу в глобальную группу.</span><span class="sxs-lookup"><span data-stu-id="7a740-113">Add a universal group to a global group.</span></span> <span data-ttu-id="7a740-114">Универсальные группы можно добавлять в универсальные и доменные локальные группы, но не глобальные группы.</span><span class="sxs-lookup"><span data-stu-id="7a740-114">Universal groups can be added to universal and domain local groups, but not global groups.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a740-115">0x8007202F</span><span class="sxs-lookup"><span data-stu-id="7a740-115">0x8007202F</span></span></td>
<td><span data-ttu-id="7a740-116"><strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>.</span><span class="sxs-lookup"><span data-stu-id="7a740-116"><strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>.</span></span> <span data-ttu-id="7a740-117">Эта ошибка возникает при попытке добавить группу безопасности в другую группу в домене, работающем в смешанном режиме.</span><span class="sxs-lookup"><span data-stu-id="7a740-117">This error occurs if you attempt to add a security group to another group in a domain running in mixed mode.</span></span> <span data-ttu-id="7a740-118">Группы безопасности не могут быть вложенными в смешанный режим. группы безопасности могут быть вложены только в собственном режиме.</span><span class="sxs-lookup"><span data-stu-id="7a740-118">Security groups cannot be nested in mixed mode; security groups can only be nested in native mode.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




