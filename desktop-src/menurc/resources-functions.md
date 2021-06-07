---
title: Функции ресурсов (меню и другие ресурсы)
description: Функции ресурсов (меню и другие ресурсы)
ms.assetid: dfeaaf01-f947-453e-946e-65ad9ec40958
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee066a6a111c911dd704997eeb7ed1c89ae1f417
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/06/2021
ms.locfileid: "111550006"
---
# <a name="resource-functions-menus-and-other-resources"></a><span data-ttu-id="84667-103">Функции ресурсов (меню и другие ресурсы)</span><span class="sxs-lookup"><span data-stu-id="84667-103">Resource Functions (Menus and Other Resources)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="84667-104">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="84667-104">In This Section</span></span>

-   [<span data-ttu-id="84667-105">**бегинупдатересаурце**</span><span class="sxs-lookup"><span data-stu-id="84667-105">**BeginUpdateResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea)
-   [<span data-ttu-id="84667-106">**CopyImage**</span><span class="sxs-lookup"><span data-stu-id="84667-106">**CopyImage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-copyimage)
-   [<span data-ttu-id="84667-107">**ендупдатересаурце**</span><span class="sxs-lookup"><span data-stu-id="84667-107">**EndUpdateResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea)
-   <span data-ttu-id="84667-108">[*енумреслангпрок*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="84667-108">[*EnumResLangProc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85))</span></span>
-   [<span data-ttu-id="84667-109">*енумреснамепрок*</span><span class="sxs-lookup"><span data-stu-id="84667-109">*EnumResNameProc*</span></span>](/windows/win32/api/libloaderapi/nc-libloaderapi-enumresnameproca)
-   [<span data-ttu-id="84667-110">**енумресаурцелангуажес**</span><span class="sxs-lookup"><span data-stu-id="84667-110">**EnumResourceLanguages**</span></span>](/windows/desktop/api/Winbase/nf-winbase-enumresourcelanguagesa)
-   [<span data-ttu-id="84667-111">**енумресаурцелангуажесекс**</span><span class="sxs-lookup"><span data-stu-id="84667-111">**EnumResourceLanguagesEx**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexa)
-   [<span data-ttu-id="84667-112">**енумресаурценамес**</span><span class="sxs-lookup"><span data-stu-id="84667-112">**EnumResourceNames**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-enumresourcenamesa)
-   [<span data-ttu-id="84667-113">**енумресаурценамесекс**</span><span class="sxs-lookup"><span data-stu-id="84667-113">**EnumResourceNamesEx**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexa)
-   [<span data-ttu-id="84667-114">**енумресаурцетипес**</span><span class="sxs-lookup"><span data-stu-id="84667-114">**EnumResourceTypes**</span></span>](/windows/desktop/api/Winbase/nf-winbase-enumresourcetypesa)
-   [<span data-ttu-id="84667-115">**енумресаурцетипесекс**</span><span class="sxs-lookup"><span data-stu-id="84667-115">**EnumResourceTypesEx**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexa)
-   [<span data-ttu-id="84667-116">*енумрестипепрок*</span><span class="sxs-lookup"><span data-stu-id="84667-116">*EnumResTypeProc*</span></span>](/windows/win32/api/libloaderapi/nc-libloaderapi-enumrestypeproca)
-   [<span data-ttu-id="84667-117">**FindResource**</span><span class="sxs-lookup"><span data-stu-id="84667-117">**FindResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-findresourcea)
-   [<span data-ttu-id="84667-118">**финдресаурцеекс**</span><span class="sxs-lookup"><span data-stu-id="84667-118">**FindResourceEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-findresourceexa)
-   [<span data-ttu-id="84667-119">**фриресаурце**</span><span class="sxs-lookup"><span data-stu-id="84667-119">**FreeResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freeresource)
-   [<span data-ttu-id="84667-120">**лоадимаже**</span><span class="sxs-lookup"><span data-stu-id="84667-120">**LoadImage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
-   [<span data-ttu-id="84667-121">**лоадресаурце**</span><span class="sxs-lookup"><span data-stu-id="84667-121">**LoadResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
-   [<span data-ttu-id="84667-122">**локкресаурце**</span><span class="sxs-lookup"><span data-stu-id="84667-122">**LockResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-lockresource)
-   [<span data-ttu-id="84667-123">**сизеофресаурце**</span><span class="sxs-lookup"><span data-stu-id="84667-123">**SizeofResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-sizeofresource)
-   [<span data-ttu-id="84667-124">**—**</span><span class="sxs-lookup"><span data-stu-id="84667-124">**UpdateResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-updateresourcea)

 

 
