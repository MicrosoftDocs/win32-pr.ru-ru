---
description: Класс Чстрингаррай предоставляет следующие методы.
ms.assetid: AFE4306E-6BB1-4F1D-A301-CD5F05385466
ms.tgt_platform: multiple
title: Методы Чстрингаррай
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bfbe2afa9948e14362d05f5f90a2e375a9cffab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712672"
---
# <a name="chstringarray-methods"></a><span data-ttu-id="1fef0-103">Методы Чстрингаррай</span><span class="sxs-lookup"><span data-stu-id="1fef0-103">CHStringArray Methods</span></span>

<span data-ttu-id="1fef0-104">\[Класс [**чстрингаррай**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="1fef0-104">\[The [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="1fef0-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="1fef0-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="1fef0-106">Класс [**чстрингаррай**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1fef0-106">The [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1fef0-107">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="1fef0-107">In this section</span></span>

-   [<span data-ttu-id="1fef0-108">**Добавить метод**</span><span class="sxs-lookup"><span data-stu-id="1fef0-108">**Add method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-add)
-   [<span data-ttu-id="1fef0-109">**Append - метод**</span><span class="sxs-lookup"><span data-stu-id="1fef0-109">**Append method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-append)
-   [<span data-ttu-id="1fef0-110">**Метод Чстрингаррай**</span><span class="sxs-lookup"><span data-stu-id="1fef0-110">**CHStringArray method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-chstringarray)
-   [<span data-ttu-id="1fef0-111">**Метод Copy**</span><span class="sxs-lookup"><span data-stu-id="1fef0-111">**Copy method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-copy)
-   <span data-ttu-id="1fef0-112">[**Метод ElementAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-elementat(int))</span><span class="sxs-lookup"><span data-stu-id="1fef0-112">[**ElementAt method**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-elementat(int))</span></span>
-   [<span data-ttu-id="1fef0-113">**Метод Фриекстра**</span><span class="sxs-lookup"><span data-stu-id="1fef0-113">**FreeExtra method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-freeextra)
-   <span data-ttu-id="1fef0-114">[**Метод GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))</span><span class="sxs-lookup"><span data-stu-id="1fef0-114">[**GetAt method**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))</span></span>
-   [<span data-ttu-id="1fef0-115">**Метод GetData**</span><span class="sxs-lookup"><span data-stu-id="1fef0-115">**GetData method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getdata)
-   [<span data-ttu-id="1fef0-116">**Метод метода Resize**</span><span class="sxs-lookup"><span data-stu-id="1fef0-116">**GetSize method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getsize)
-   [<span data-ttu-id="1fef0-117">**Метод GetUpperBound**</span><span class="sxs-lookup"><span data-stu-id="1fef0-117">**GetUpperBound method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)
-   <span data-ttu-id="1fef0-118">[**Методы Инсертат**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-insertat(int_chstringarray))</span><span class="sxs-lookup"><span data-stu-id="1fef0-118">[**InsertAt methods**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-insertat(int_chstringarray))</span></span>
-   <span data-ttu-id="1fef0-119">[**Чстрингаррай:: operator \[\]**](chstringarray--operator-brackets.md)</span><span class="sxs-lookup"><span data-stu-id="1fef0-119">[**CHStringArray::operator \[ \]**](chstringarray--operator-brackets.md)</span></span>
-   [<span data-ttu-id="1fef0-120">**RemoveAll, метод**</span><span class="sxs-lookup"><span data-stu-id="1fef0-120">**RemoveAll method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-removeall)
-   [<span data-ttu-id="1fef0-121">**RemoveAt, метод**</span><span class="sxs-lookup"><span data-stu-id="1fef0-121">**RemoveAt method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-removeat)
-   <span data-ttu-id="1fef0-122">[**Метод SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="1fef0-122">[**SetAt method**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))</span></span>
-   [<span data-ttu-id="1fef0-123">**Метод Сетатгров**</span><span class="sxs-lookup"><span data-stu-id="1fef0-123">**SetAtGrow method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setatgrow)
-   [<span data-ttu-id="1fef0-124">**Метод SetSize**</span><span class="sxs-lookup"><span data-stu-id="1fef0-124">**SetSize method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setsize)

 

 
