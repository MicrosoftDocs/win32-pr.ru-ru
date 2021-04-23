---
title: Свойство страницы
description: Свойство страницы
ms.assetid: c3cf07e9-a324-443b-a0c0-2fb80463548f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c51f55e4d1e9c7d2d23713810412060d915c7af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410932"
---
# <a name="page-property"></a><span data-ttu-id="061d2-103">Свойство страницы</span><span class="sxs-lookup"><span data-stu-id="061d2-103">Page Property</span></span>

<span data-ttu-id="061d2-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="061d2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="061d2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="061d2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="061d2-106">Возвращает или задает страницу, отображаемую в окне страницы свойств агента Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="061d2-106">Returns or sets the page displayed in the Microsoft Agent property sheet window.</span></span>

</dd> <dt>

<span data-ttu-id="061d2-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="061d2-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="061d2-108">\*агент \* \* *.* \*  \[  =  *Строка* PropertySheet.Page\]</span><span class="sxs-lookup"><span data-stu-id="061d2-108">*agent\*\*\*.PropertySheet.Page*\* \[ = *string*\]</span></span>



| <span data-ttu-id="061d2-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="061d2-109">Part</span></span>     | <span data-ttu-id="061d2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="061d2-110">Description</span></span>                                                                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="061d2-111">*string*</span><span class="sxs-lookup"><span data-stu-id="061d2-111">*string*</span></span> | <span data-ttu-id="061d2-112">Строковое выражение с одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="061d2-112">A string expression with one of the following values.</span></span> <span data-ttu-id="061d2-113">**"Речь"** Отображает страницу речевого ввода.</span><span class="sxs-lookup"><span data-stu-id="061d2-113">**"Speech"** Displays the Speech Input page.</span></span><br/> <span data-ttu-id="061d2-114">**"Output"** Отображает страницу выходных данных.</span><span class="sxs-lookup"><span data-stu-id="061d2-114">**"Output"** Displays the Output page.</span></span><br/> <span data-ttu-id="061d2-115">**"Авторские права"** Отображает страницу авторских прав.</span><span class="sxs-lookup"><span data-stu-id="061d2-115">**"Copyright"** Displays the Copyright page.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="061d2-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="061d2-116">Remarks</span></span>

<span data-ttu-id="061d2-117">Если модуль распознавания речи не установлен, задание для **страницы** значения **"речь"** не оказывает никакого воздействия.</span><span class="sxs-lookup"><span data-stu-id="061d2-117">If no speech engine is installed, setting **Page** to **"Speech"** has no effect.</span></span> <span data-ttu-id="061d2-118">Кроме того, свойство **Visible** окна должно иметь значение **true** , чтобы пользователь отображал страницу.</span><span class="sxs-lookup"><span data-stu-id="061d2-118">Also, the window's **Visible** property must be set to **True** for the user to see the page.</span></span>

> [!Note]  
> <span data-ttu-id="061d2-119">Пользователь может переопределить это свойство.</span><span class="sxs-lookup"><span data-stu-id="061d2-119">The user can override this property.</span></span>

 

 

 





