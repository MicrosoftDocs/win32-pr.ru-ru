---
title: Что должна делать установка
description: На новые атрибуты, на которые ссылается шаг 3, должен быть указан идентификатор OID, так как в этом месте в кэше схемы отсутствует новое имя атрибута.
ms.assetid: 57da8740-7646-4ca9-ba8d-832e4f520b13
ms.tgt_platform: multiple
keywords:
- Что должна делать установка AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5724a7acbb4d0bf8ef3008fa48e2f10fcc04a324
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986131"
---
# <a name="what-the-installation-must-do"></a><span data-ttu-id="348e0-104">Что должна делать установка</span><span class="sxs-lookup"><span data-stu-id="348e0-104">What the Installation Must Do</span></span>

<span data-ttu-id="348e0-105">Приложения, расширяющие схему, должны применять обновления, как описано в следующей процедуре.</span><span class="sxs-lookup"><span data-stu-id="348e0-105">Applications that extend the schema, must apply updates as described in the following procedure.</span></span>

<span data-ttu-id="348e0-106">**Применение обновлений при расширении схемы**</span><span class="sxs-lookup"><span data-stu-id="348e0-106">**To apply updates when extending the schema**</span></span>

1.  <span data-ttu-id="348e0-107">Добавьте новые атрибуты.</span><span class="sxs-lookup"><span data-stu-id="348e0-107">Add the new attributes.</span></span>
2.  <span data-ttu-id="348e0-108">Добавьте новые классы.</span><span class="sxs-lookup"><span data-stu-id="348e0-108">Add the new classes.</span></span>
3.  <span data-ttu-id="348e0-109">Добавьте новые атрибуты в классы.</span><span class="sxs-lookup"><span data-stu-id="348e0-109">Add the new attributes to classes.</span></span>
4.  <span data-ttu-id="348e0-110">Активация перезагрузки кэша.</span><span class="sxs-lookup"><span data-stu-id="348e0-110">Trigger a cache reload.</span></span>

<span data-ttu-id="348e0-111">На новые атрибуты, на которые ссылается шаг 3, должен быть указан идентификатор OID, так как в этом месте в кэше схемы отсутствует новое имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="348e0-111">New attributes referenced in Step 3 must be referred to by its OID because the new attribute name is not present in the schema cache at this point.</span></span>

<span data-ttu-id="348e0-112">Шаг 4 не нужен, если расширения не будут использоваться немедленно. расширения будут отображаться в кэше схемы примерно через 5 минут в зависимости от нагрузки на систему.</span><span class="sxs-lookup"><span data-stu-id="348e0-112">Step 4 is unnecessary if the extensions will not be used immediately; the extensions will appear in the schema cache in approximately 5 minutes, depending on system load.</span></span> <span data-ttu-id="348e0-113">Дополнительные сведения о кэше схем и о том, как активировать перезагрузку кэша, см. в разделе [Обновление кэша схемы](updating-the-schema-cache.md).</span><span class="sxs-lookup"><span data-stu-id="348e0-113">For more information about the schema cache and how to trigger a cache reload, see [Updating the Schema Cache](updating-the-schema-cache.md).</span></span>

 

 




