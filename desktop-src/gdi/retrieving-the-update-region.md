---
description: Функции Жетупдатерект и Жетупдатергн извлекают текущий регион обновления для окна.
ms.assetid: c0729c4f-3b00-4ab9-91b2-4a2fecee8727
title: Получение региона обновления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8115f47a6c585d5b660d73bbf4fb3de21334b6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263651"
---
# <a name="retrieving-the-update-region"></a><span data-ttu-id="2962b-103">Получение региона обновления</span><span class="sxs-lookup"><span data-stu-id="2962b-103">Retrieving the Update Region</span></span>

<span data-ttu-id="2962b-104">Функции [**жетупдатерект**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) и [**жетупдатергн**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) извлекают текущий регион обновления для окна.</span><span class="sxs-lookup"><span data-stu-id="2962b-104">The [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) and [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) functions retrieve the current update region for the window.</span></span> <span data-ttu-id="2962b-105">Жетупдатерект извлекает наименьший прямоугольник (в логических координатах), охватывающий всю область обновления.</span><span class="sxs-lookup"><span data-stu-id="2962b-105">GetUpdateRect retrieves the smallest rectangle (in logical coordinates) that encloses the entire update region.</span></span> <span data-ttu-id="2962b-106">Жетупдатергн извлекает сам регион обновления.</span><span class="sxs-lookup"><span data-stu-id="2962b-106">GetUpdateRgn retrieves the update region itself.</span></span> <span data-ttu-id="2962b-107">Эти функции можно использовать для вычисления текущего размера области обновления, чтобы определить, где нужно выполнить операцию рисования.</span><span class="sxs-lookup"><span data-stu-id="2962b-107">These functions can be used to calculate the current size of the update region to determine where to carry out a drawing operation.</span></span>

<span data-ttu-id="2962b-108">[**Бегинпаинт**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) также получает размеры самого маленького прямоугольника, охватывающего текущую область обновления, копируя измерения в элемент **члене rcpaint структуры** в структуре [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) .</span><span class="sxs-lookup"><span data-stu-id="2962b-108">[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) also retrieves the dimensions of the smallest rectangle enclosing the current update region, copying the dimensions to the **rcPaint** member in the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="2962b-109">Так как **бегинпаинт** проверяет регион обновления, любой вызов [**жетупдатерект**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) и [**жетупдатергн**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) сразу после вызова **бегинпаинт** возвращает пустой регион обновления.</span><span class="sxs-lookup"><span data-stu-id="2962b-109">Because **BeginPaint** validates the update region, any call to [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) and [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) immediately after a call to **BeginPaint** returns an empty update region.</span></span>

 

 



