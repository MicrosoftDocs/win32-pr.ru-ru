---
title: Событие закладки
description: Событие закладки
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0695ccd04f93eae46eaae66955c84fefb9e0c963
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253111"
---
# <a name="bookmark-event"></a><span data-ttu-id="78d70-103">Событие закладки</span><span class="sxs-lookup"><span data-stu-id="78d70-103">Bookmark Event</span></span>

<span data-ttu-id="78d70-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="78d70-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="78d70-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="78d70-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="78d70-106">Возникает при активации закладки в текстовой строке в речевом коде, заданной приложением.</span><span class="sxs-lookup"><span data-stu-id="78d70-106">Occurs when a bookmark in a speech text string that your application defined is activated.</span></span>

</dd> <dt>

<span data-ttu-id="78d70-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="78d70-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="78d70-108"> Закладка подпрограммы- *агента* \_  **(ByVal** *букмаркид\ * *)**</span><span class="sxs-lookup"><span data-stu-id="78d70-108">**Sub** *agent*\_**Bookmark** **(ByVal** *BookmarkID\*\*\*)*\*</span></span>



| <span data-ttu-id="78d70-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="78d70-109">Part</span></span>         | <span data-ttu-id="78d70-110">Описание</span><span class="sxs-lookup"><span data-stu-id="78d70-110">Description</span></span>                                     |
|--------------|-------------------------------------------------|
| <span data-ttu-id="78d70-111">*BookmarkID*</span><span class="sxs-lookup"><span data-stu-id="78d70-111">*BookmarkID*</span></span> | <span data-ttu-id="78d70-112">Длинное целое число, определяющее номер закладки.</span><span class="sxs-lookup"><span data-stu-id="78d70-112">A Long integer identifying the bookmark number.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="78d70-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78d70-113">Remarks</span></span>

<span data-ttu-id="78d70-114">Чтобы указать событие закладки, используйте метод [**говорите**](speak-method.md) с тегом **МРК** в заданном тексте.</span><span class="sxs-lookup"><span data-stu-id="78d70-114">To specify a bookmark event, use the [**Speak**](speak-method.md) method with a **Mrk** tag in your supplied text.</span></span> <span data-ttu-id="78d70-115">Дополнительные сведения о тегах см. в разделе Теги вывода речи.</span><span class="sxs-lookup"><span data-stu-id="78d70-115">For more information about tags, see Speech Output Tags.</span></span>

 

 




