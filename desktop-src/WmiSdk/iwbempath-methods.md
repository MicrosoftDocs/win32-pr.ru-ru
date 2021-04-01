---
description: Интерфейс Ивбемпас предоставляет следующие методы.
ms.assetid: 36EC7EF6-5CCA-4D18-AB09-9EE41D1B9524
ms.tgt_platform: multiple
title: Методы Ивбемпас
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f1ae802fd7741e5b1317160991a50bd2a535a9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263928"
---
# <a name="iwbempath-methods"></a><span data-ttu-id="58ba3-103">Методы Ивбемпас</span><span class="sxs-lookup"><span data-stu-id="58ba3-103">IWbemPath Methods</span></span>

<span data-ttu-id="58ba3-104">Интерфейс [**ивбемпас**](/windows/desktop/api/Wmiutils/nn-wmiutils-iwbempath) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="58ba3-104">The [**IWbemPath**](/windows/desktop/api/Wmiutils/nn-wmiutils-iwbempath) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="58ba3-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="58ba3-105">In this section</span></span>

-   [<span data-ttu-id="58ba3-106">**Метод Креатекласспарт**</span><span class="sxs-lookup"><span data-stu-id="58ba3-106">**CreateClassPart method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-createclasspart)
-   [<span data-ttu-id="58ba3-107">**Метод Делетекласспарт**</span><span class="sxs-lookup"><span data-stu-id="58ba3-107">**DeleteClassPart method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-deleteclasspart)
-   [<span data-ttu-id="58ba3-108">**Метод ClassName**</span><span class="sxs-lookup"><span data-stu-id="58ba3-108">**GetClassName method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getclassname)
-   [<span data-ttu-id="58ba3-109">**Метод получения сведений**</span><span class="sxs-lookup"><span data-stu-id="58ba3-109">**GetInfo method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getinfo)
-   [<span data-ttu-id="58ba3-110">**Метод Жеткэйлист**</span><span class="sxs-lookup"><span data-stu-id="58ba3-110">**GetKeyList method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getkeylist)
-   [<span data-ttu-id="58ba3-111">**Метод Жетнамеспацеат**</span><span class="sxs-lookup"><span data-stu-id="58ba3-111">**GetNamespaceAt method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getnamespaceat)
-   [<span data-ttu-id="58ba3-112">**Метод Жетнамеспацекаунт**</span><span class="sxs-lookup"><span data-stu-id="58ba3-112">**GetNamespaceCount method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getnamespacecount)
-   [<span data-ttu-id="58ba3-113">**Метод superscope**</span><span class="sxs-lookup"><span data-stu-id="58ba3-113">**GetScope method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getscope)
-   [<span data-ttu-id="58ba3-114">**Метод Жетскопеастекст**</span><span class="sxs-lookup"><span data-stu-id="58ba3-114">**GetScopeAsText method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getscopeastext)
-   [<span data-ttu-id="58ba3-115">**Метод Жетскопекаунт**</span><span class="sxs-lookup"><span data-stu-id="58ba3-115">**GetScopeCount method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getscopecount)
-   [<span data-ttu-id="58ba3-116">**Метод метода onserver**</span><span class="sxs-lookup"><span data-stu-id="58ba3-116">**GetServer method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getserver)
-   [<span data-ttu-id="58ba3-117">**GetText - метод**</span><span class="sxs-lookup"><span data-stu-id="58ba3-117">**GetText method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-gettext)
-   [<span data-ttu-id="58ba3-118">**Метод onlocal**</span><span class="sxs-lookup"><span data-stu-id="58ba3-118">**IsLocal method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-islocal)
-   [<span data-ttu-id="58ba3-119">**Метод "методом"**</span><span class="sxs-lookup"><span data-stu-id="58ba3-119">**IsRelative method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-isrelative)
-   [<span data-ttu-id="58ba3-120">**Метод Исрелативеорчилд**</span><span class="sxs-lookup"><span data-stu-id="58ba3-120">**IsRelativeOrChild method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-isrelativeorchild)
-   [<span data-ttu-id="58ba3-121">**Метод Иссамекласснаме**</span><span class="sxs-lookup"><span data-stu-id="58ba3-121">**IsSameClassName method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-issameclassname)
-   [<span data-ttu-id="58ba3-122">**Метод Ремовеаллнамеспацес**</span><span class="sxs-lookup"><span data-stu-id="58ba3-122">**RemoveAllNamespaces method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removeallnamespaces)
-   [<span data-ttu-id="58ba3-123">**Метод Ремовеаллскопес**</span><span class="sxs-lookup"><span data-stu-id="58ba3-123">**RemoveAllScopes method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removeallscopes)
-   [<span data-ttu-id="58ba3-124">**Метод Ремовенамеспацеат**</span><span class="sxs-lookup"><span data-stu-id="58ba3-124">**RemoveNamespaceAt method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removenamespaceat)
-   [<span data-ttu-id="58ba3-125">**Метод RemoveScope**</span><span class="sxs-lookup"><span data-stu-id="58ba3-125">**RemoveScope method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removescope)
-   [<span data-ttu-id="58ba3-126">**Метод Сеткласснаме**</span><span class="sxs-lookup"><span data-stu-id="58ba3-126">**SetClassName method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setclassname)
-   [<span data-ttu-id="58ba3-127">**Метод Сетнамеспацеат**</span><span class="sxs-lookup"><span data-stu-id="58ba3-127">**SetNamespaceAt method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setnamespaceat)
-   [<span data-ttu-id="58ba3-128">**Метод Сетскопе**</span><span class="sxs-lookup"><span data-stu-id="58ba3-128">**SetScope method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setscope)
-   [<span data-ttu-id="58ba3-129">**Метод Сетсервер**</span><span class="sxs-lookup"><span data-stu-id="58ba3-129">**SetServer method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setserver)
-   [<span data-ttu-id="58ba3-130">**SetText - метод**</span><span class="sxs-lookup"><span data-stu-id="58ba3-130">**SetText method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-settext)

 

 



