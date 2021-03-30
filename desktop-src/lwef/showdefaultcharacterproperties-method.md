---
title: Метод Шовдефаултчарактерпропертиес
description: Метод Шовдефаултчарактерпропертиес
ms.assetid: a3b109c0-5701-4a72-baae-bcbb97b025a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f055b2ca0f00e0a13c24ec95dc82509ae9c45b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775449"
---
# <a name="showdefaultcharacterproperties-method"></a><span data-ttu-id="9137d-103">Метод Шовдефаултчарактерпропертиес</span><span class="sxs-lookup"><span data-stu-id="9137d-103">ShowDefaultCharacterProperties Method</span></span>

<span data-ttu-id="9137d-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9137d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9137d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="9137d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9137d-106">Отображает свойства символа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9137d-106">Displays the default character's properties.</span></span>

</dd> <dt>

<span data-ttu-id="9137d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="9137d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9137d-108">\*агент \* \* *. Шовдефаултчарактерпропертиес* \*  \[ *X* , *Y*\]</span><span class="sxs-lookup"><span data-stu-id="9137d-108">*agent\*\*\*.ShowDefaultCharacterProperties*\* \[ *X* , *Y* \]</span></span>



| <span data-ttu-id="9137d-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="9137d-109">Part</span></span> | <span data-ttu-id="9137d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9137d-110">Description</span></span>                                                                                                                                                |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9137d-111">*X*</span><span class="sxs-lookup"><span data-stu-id="9137d-111">*X*</span></span>  | <span data-ttu-id="9137d-112">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="9137d-112">Optional.</span></span> <span data-ttu-id="9137d-113">Короткое целое значение, указывающее координату горизонтального (*X* ) экрана для отображения окна.</span><span class="sxs-lookup"><span data-stu-id="9137d-113">A short integer value that indicates the horizontal (*X* ) screen coordinate to display the window.</span></span> <span data-ttu-id="9137d-114">Эта координата должна быть указана в пикселях.</span><span class="sxs-lookup"><span data-stu-id="9137d-114">This coordinate must be specified in pixels.</span></span> |
| <span data-ttu-id="9137d-115">*да*</span><span class="sxs-lookup"><span data-stu-id="9137d-115">*Y*</span></span>  | <span data-ttu-id="9137d-116">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="9137d-116">Optional.</span></span> <span data-ttu-id="9137d-117">Короткое целое значение, указывающее координату вертикального экрана (*Y*) для отображения окна.</span><span class="sxs-lookup"><span data-stu-id="9137d-117">A short integer value that indicates the vertical (*Y*) screen coordinate to display the window.</span></span> <span data-ttu-id="9137d-118">Эта координата должна быть указана в пикселях.</span><span class="sxs-lookup"><span data-stu-id="9137d-118">This coordinate must be specified in pixels.</span></span>    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9137d-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9137d-119">Remarks</span></span>

<span data-ttu-id="9137d-120">При вызове этого метода отображается окно «Свойства символа по умолчанию» (не вкладка свойств Microsoft Agent).</span><span class="sxs-lookup"><span data-stu-id="9137d-120">Calling this method displays the default character properties window (not the Microsoft Agent property sheet).</span></span> <span data-ttu-id="9137d-121">Если не указать координаты X и Y, окно будет отображаться в последнем расположении.</span><span class="sxs-lookup"><span data-stu-id="9137d-121">If you do not specify the X and Y coordinates, the window appears at the last location it was displayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="9137d-122">См. также:</span><span class="sxs-lookup"><span data-stu-id="9137d-122">See Also</span></span>

[<span data-ttu-id="9137d-123">**Событие Дефаултчарактерчанже**</span><span class="sxs-lookup"><span data-stu-id="9137d-123">**DefaultCharacterChange event**</span></span>](defaultcharacterchange-event.md)


 

 




