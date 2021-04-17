---
description: Класс Вбемтимеспан предоставляет следующие методы.
ms.assetid: 7D450EE2-C52F-4B78-B6B1-9FD74394C3DE
ms.tgt_platform: multiple
title: Методы WBEMTimeSpan
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d516f22a7ecd5468d53bda44ce47edbe4504d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713021"
---
# <a name="wbemtimespan-methods"></a><span data-ttu-id="ff6b6-103">Методы WBEMTimeSpan</span><span class="sxs-lookup"><span data-stu-id="ff6b6-103">WBEMTimeSpan Methods</span></span>

<span data-ttu-id="ff6b6-104">\[Класс [**вбемтимеспан**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="ff6b6-104">\[The [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="ff6b6-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="ff6b6-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="ff6b6-106">Класс [**вбемтимеспан**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ff6b6-106">The [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ff6b6-107">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="ff6b6-107">In this section</span></span>

-   <span data-ttu-id="ff6b6-108">[**Конструкторы Вбемтимеспан**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span><span class="sxs-lookup"><span data-stu-id="ff6b6-108">[**WbemTimeSpan constructors**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span></span>
-   [<span data-ttu-id="ff6b6-109">**Метод Clear**</span><span class="sxs-lookup"><span data-stu-id="ff6b6-109">**Clear method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-clear)
-   [<span data-ttu-id="ff6b6-110">**GetBSTR - метод**</span><span class="sxs-lookup"><span data-stu-id="ff6b6-110">**GetBSTR method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-getbstr)
-   [<span data-ttu-id="ff6b6-111">**Метод метода Time**</span><span class="sxs-lookup"><span data-stu-id="ff6b6-111">**GetTime method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-gettime)
-   [<span data-ttu-id="ff6b6-112">**Метод исок**</span><span class="sxs-lookup"><span data-stu-id="ff6b6-112">**IsOk method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-isok)
-   <span data-ttu-id="ff6b6-113">[**operator= - метод**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span><span class="sxs-lookup"><span data-stu-id="ff6b6-113">[**operator= method**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span></span>
-   [<span data-ttu-id="ff6b6-114">**operator +, метод**</span><span class="sxs-lookup"><span data-stu-id="ff6b6-114">**operator+ method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-add)
-   [<span data-ttu-id="ff6b6-115">**operator + =, метод**</span><span class="sxs-lookup"><span data-stu-id="ff6b6-115">**operator+= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-add-assign)
-   [<span data-ttu-id="ff6b6-116">**operator-метод**</span><span class="sxs-lookup"><span data-stu-id="ff6b6-116">**operator- method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-sub)
-   [<span data-ttu-id="ff6b6-117">**operator-= метод**</span><span class="sxs-lookup"><span data-stu-id="ff6b6-117">**operator-= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-sub-assign)
-   [<span data-ttu-id="ff6b6-118">**operator = = метод**</span><span class="sxs-lookup"><span data-stu-id="ff6b6-118">**operator == method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-equal-equal-to)
-   [<span data-ttu-id="ff6b6-119">**operator! = метод**</span><span class="sxs-lookup"><span data-stu-id="ff6b6-119">**operator != method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-not-equal-to)
-   [<span data-ttu-id="ff6b6-120">**метод > оператора**</span><span class="sxs-lookup"><span data-stu-id="ff6b6-120">**operator > method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than)
-   [<span data-ttu-id="ff6b6-121">**Оператор >= Method**</span><span class="sxs-lookup"><span data-stu-id="ff6b6-121">**operator >= method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than-equal-to)
-   [<span data-ttu-id="ff6b6-122">**метод < оператора**</span><span class="sxs-lookup"><span data-stu-id="ff6b6-122">**operator < method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-less-than)
-   [<span data-ttu-id="ff6b6-123">**Оператор <= Method**</span><span class="sxs-lookup"><span data-stu-id="ff6b6-123">**operator <= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-less-than-equal-to)

 

 
