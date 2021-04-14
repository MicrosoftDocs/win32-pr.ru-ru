---
description: Интерфейс Ивбемклассобжект предоставляет следующие методы.
ms.assetid: 20BF7775-89D9-4851-8561-EEBA398A0584
ms.tgt_platform: multiple
title: Методы Ивбемклассобжект
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825b3f15f17dca6dd0871bbcae3f531a90c90f1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350085"
---
# <a name="iwbemclassobject-methods"></a><span data-ttu-id="2cc2d-103">Методы Ивбемклассобжект</span><span class="sxs-lookup"><span data-stu-id="2cc2d-103">IWbemClassObject Methods</span></span>

<span data-ttu-id="2cc2d-104">Интерфейс [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2cc2d-104">The [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2cc2d-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="2cc2d-105">In this section</span></span>

-   [<span data-ttu-id="2cc2d-106">**Метод BeginEnumeration**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-106">**BeginEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration)
-   [<span data-ttu-id="2cc2d-107">**Метод Бегинмесоденумератион**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-107">**BeginMethodEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginmethodenumeration)
-   [<span data-ttu-id="2cc2d-108">**Clone, метод**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-108">**Clone method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone)
-   [<span data-ttu-id="2cc2d-109">**CompareTo - метод**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-109">**CompareTo method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-compareto)
-   [<span data-ttu-id="2cc2d-110">**Метод Delete**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-110">**Delete method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete)
-   [<span data-ttu-id="2cc2d-111">**Метод DeleteMethod**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-111">**DeleteMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-deletemethod)
-   [<span data-ttu-id="2cc2d-112">**Метод EndEnumeration**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-112">**EndEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration)
-   [<span data-ttu-id="2cc2d-113">**Метод Ендмесоденумератион**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-113">**EndMethodEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endmethodenumeration)
-   [<span data-ttu-id="2cc2d-114">**Метод Get**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-114">**Get method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)
-   [<span data-ttu-id="2cc2d-115">**Метод метода WebMethod**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-115">**GetMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod)
-   [<span data-ttu-id="2cc2d-116">**Метод Жетмесодоригин**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-116">**GetMethodOrigin method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodorigin)
-   [<span data-ttu-id="2cc2d-117">**Метод Жетмесодкуалифиерсет**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-117">**GetMethodQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset)
-   [<span data-ttu-id="2cc2d-118">**Метод Names**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-118">**GetNames method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getnames)
-   [<span data-ttu-id="2cc2d-119">**Метод Жетобжекттекст**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-119">**GetObjectText method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext)
-   [<span data-ttu-id="2cc2d-120">**Метод Жетпропертйоригин**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-120">**GetPropertyOrigin method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyorigin)
-   [<span data-ttu-id="2cc2d-121">**Метод Жетпропертикуалифиерсет**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-121">**GetPropertyQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset)
-   [<span data-ttu-id="2cc2d-122">**Метод Жеткуалифиерсет**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-122">**GetQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset)
-   [<span data-ttu-id="2cc2d-123">**Метод раскрывшемся**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-123">**InheritsFrom method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-inheritsfrom)
-   [<span data-ttu-id="2cc2d-124">**Метод Next**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-124">**Next method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-next)
-   [<span data-ttu-id="2cc2d-125">**Метод Некстмесод**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-125">**NextMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-nextmethod)
-   [<span data-ttu-id="2cc2d-126">**Метод размещения**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-126">**Put method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)
-   [<span data-ttu-id="2cc2d-127">**Метод Путмесод**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-127">**PutMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)
-   [<span data-ttu-id="2cc2d-128">**Метод Спавндериведкласс**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-128">**SpawnDerivedClass method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass)
-   [<span data-ttu-id="2cc2d-129">**Метод Спавнинстанце**</span><span class="sxs-lookup"><span data-stu-id="2cc2d-129">**SpawnInstance method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)

 

 



