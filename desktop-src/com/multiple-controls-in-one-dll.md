---
title: Несколько элементов управления в одной библиотеке DLL
description: Несколько элементов управления в одной библиотеке DLL
ms.assetid: 76c1c0ef-af24-43e8-b3a7-337841c338ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e11c91faa26420f37df330ad7f1d9eff4587f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067406"
---
# <a name="multiple-controls-in-one-dll"></a><span data-ttu-id="10899-103">Несколько элементов управления в одной библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="10899-103">Multiple Controls in One DLL</span></span>

<span data-ttu-id="10899-104">Одна DLL-библиотека. ocx может быть контейнером любого количества элементов управления ActiveX, что упрощает распространение и использование набора связанных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="10899-104">A single .ocx DLL can container any number of ActiveX controls, thus simplifying the distribution and use of a set of related controls.</span></span>

<span data-ttu-id="10899-105">При отправке нескольких элементов управления в одной библиотеке DLL обязательно включите имя поставщика в каждое имя элемента управления в пакете.</span><span class="sxs-lookup"><span data-stu-id="10899-105">If you ship multiple controls in a single DLL, be sure to include the vendor name in each control name in the package.</span></span> <span data-ttu-id="10899-106">Включение имен поставщиков в каждое имя элемента управления позволит пользователям легко находить элементы управления внутри пакета.</span><span class="sxs-lookup"><span data-stu-id="10899-106">Including the vendors' names in each control name will enable users to easily identify controls within a package.</span></span> <span data-ttu-id="10899-107">Например, при отправке библиотеки DLL, реализующей три элемента управления, Con1, Con2 и Con3, имена элементов управления должны быть:</span><span class="sxs-lookup"><span data-stu-id="10899-107">For example, if you ship a DLL that implements three controls, Con1, Con2, and Con3, then the control names should be:</span></span>

-   <span data-ttu-id="10899-108">*Название вашей компании* Элемент управления Con1</span><span class="sxs-lookup"><span data-stu-id="10899-108">*Your company name* Con1 Control</span></span>

-   <span data-ttu-id="10899-109">*Название вашей компании* Элемент управления Con2</span><span class="sxs-lookup"><span data-stu-id="10899-109">*Your company name* Con2 Control</span></span>

-   <span data-ttu-id="10899-110">*Название вашей компании* Элемент управления Con3</span><span class="sxs-lookup"><span data-stu-id="10899-110">*Your company name* Con3 Control</span></span>

 

 




