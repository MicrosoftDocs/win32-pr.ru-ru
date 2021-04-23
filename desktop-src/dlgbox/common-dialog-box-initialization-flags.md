---
title: Флаги общего диалогового окна
description: Флаги используются для изменения поведения и внешнего вида общего диалогового окна.
ms.assetid: 072cdcab-00d1-4a09-97fb-a6de2d51392e
keywords:
- Библиотека общих диалоговых окон, инициализация
- Общие диалоговые окна, инициализация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0c994e743178e3b6a17129275affed099d3004
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/19/2020
ms.locfileid: "104488622"
---
# <a name="common-dialog-box-initialization-flags"></a><span data-ttu-id="73215-105">Флаги общего диалогового окна</span><span class="sxs-lookup"><span data-stu-id="73215-105">Common Dialog Box Initialization Flags</span></span>

<span data-ttu-id="73215-106">Флаги используются для изменения поведения и внешнего вида общего диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="73215-106">Flags are used to modify the behavior and appearance of a common dialog box.</span></span> <span data-ttu-id="73215-107">Флаги инициализации — это значения, заданные в элементе **flags** структуры, которая используется для создания диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="73215-107">Initialization flags are the values that you set in the **Flags** member of the structure that is used to create the dialog box.</span></span> <span data-ttu-id="73215-108">С помощью флагов можно указать, какие элементы управления в диалоговом окне получают начальные значения, отключать выбранные элементы управления и изменять диапазон значений, которые пользователь может задавать с помощью элементов управления.</span><span class="sxs-lookup"><span data-stu-id="73215-108">You use the flags to specify which controls in a dialog box receive initial values, to disable selected controls, and to modify the range of values that the user can set with the controls.</span></span> <span data-ttu-id="73215-109">Кроме того, с помощью флагов можно включить процедуры-обработчики и пользовательские шаблоны для диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="73215-109">You also use the flags to enable hook procedures and custom templates for the dialog boxes.</span></span>

<span data-ttu-id="73215-110">Например, можно задать значение **\_ эффектов CF** в элементе **flags** структуры [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) , чтобы направлять диалоговое окно **Шрифт** для отображения элементов управления эффектами.</span><span class="sxs-lookup"><span data-stu-id="73215-110">For example, you can set the **CF\_EFFECTS** value in the **Flags** member of the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to direct the **Font** dialog box to display the effects controls.</span></span> <span data-ttu-id="73215-111">Эти элементы управления позволяют пользователю выбрать цвет шрифта, а также эффект перечеркивания и подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="73215-111">These controls let the user choose a font color as well as strikethrough and underline effects.</span></span>

<span data-ttu-id="73215-112">Значения флагов инициализации уникальны для каждого общего диалогового окна и подробно описаны элементами **флагов** следующих структур, которые соответствуют им:</span><span class="sxs-lookup"><span data-stu-id="73215-112">The initialization flag values are unique to each common dialog box and are described in detail by the **Flags** members of the following structures that correspond to them:</span></span>

-   [<span data-ttu-id="73215-113">**чусеколор**</span><span class="sxs-lookup"><span data-stu-id="73215-113">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
-   [<span data-ttu-id="73215-114">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="73215-114">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
-   [<span data-ttu-id="73215-115">**финдреплаце**</span><span class="sxs-lookup"><span data-stu-id="73215-115">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
-   [<span data-ttu-id="73215-116">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="73215-116">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
-   [<span data-ttu-id="73215-117">**пажесетупдлг**</span><span class="sxs-lookup"><span data-stu-id="73215-117">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
-   [<span data-ttu-id="73215-118">**принтдлг**</span><span class="sxs-lookup"><span data-stu-id="73215-118">**PRINTDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlga)
-   [<span data-ttu-id="73215-119">**принтдлжекс**</span><span class="sxs-lookup"><span data-stu-id="73215-119">**PRINTDLGEX**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

 

 




