---
title: Размер события
description: Размер события
ms.assetid: 06089f84-8e75-475f-a492-536c83fa6730
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9a896d2dcbf8b925c0ca13fa429f6dfd95bc21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888219"
---
# <a name="size-event"></a><span data-ttu-id="f7793-103">Размер события</span><span class="sxs-lookup"><span data-stu-id="f7793-103">Size Event</span></span>

<span data-ttu-id="f7793-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f7793-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f7793-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="f7793-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f7793-106">Происходит при изменении размера символа.</span><span class="sxs-lookup"><span data-stu-id="f7793-106">Occurs when a character's size changes.</span></span>

</dd> <dt>

<span data-ttu-id="f7793-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="f7793-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f7793-108"> *Размер подагента* \_ **(ByVal** *чарактерид*, **ByVal** *Width*, **ByVal** *Height*)</span><span class="sxs-lookup"><span data-stu-id="f7793-108">**Sub** *agent*\_**Size (ByVal** *CharacterID*, **ByVal** *Width*, **ByVal** *Height*)</span></span>



| <span data-ttu-id="f7793-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="f7793-109">Part</span></span>          | <span data-ttu-id="f7793-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f7793-110">Description</span></span>                                                         |
|---------------|---------------------------------------------------------------------|
| <span data-ttu-id="f7793-111">*чарактерид*</span><span class="sxs-lookup"><span data-stu-id="f7793-111">*CharacterID*</span></span> | <span data-ttu-id="f7793-112">Возвращает идентификатор перемещаемого символа.</span><span class="sxs-lookup"><span data-stu-id="f7793-112">Returns the ID of the character that moved.</span></span>                         |
| <span data-ttu-id="f7793-113">*Width*</span><span class="sxs-lookup"><span data-stu-id="f7793-113">*Width*</span></span>       | <span data-ttu-id="f7793-114">Возвращает новую ширину (в пикселях) символьного кадра в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="f7793-114">Returns the character frame's new width (in pixels) as an integer.</span></span>  |
| <span data-ttu-id="f7793-115">*Height*</span><span class="sxs-lookup"><span data-stu-id="f7793-115">*Height*</span></span>      | <span data-ttu-id="f7793-116">Возвращает новую высоту (в пикселях) символьного кадра в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="f7793-116">Returns the character frame's new height (in pixels) as an integer.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="f7793-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f7793-117">Remarks</span></span>

<span data-ttu-id="f7793-118">Это событие возникает, когда приложение изменяет размер символа.</span><span class="sxs-lookup"><span data-stu-id="f7793-118">This event occurs when an application changes the size of a character.</span></span> <span data-ttu-id="f7793-119">Это событие отправляется только клиентам символа (приложения, которые загрузили символ).</span><span class="sxs-lookup"><span data-stu-id="f7793-119">This event is sent only to the clients of the character (applications that have loaded the character).</span></span>

### <a name="see-also"></a><span data-ttu-id="f7793-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="f7793-120">See Also</span></span>

[<span data-ttu-id="f7793-121">**Переместить событие**</span><span class="sxs-lookup"><span data-stu-id="f7793-121">**Move event**</span></span>](move-event.md)


 

 




