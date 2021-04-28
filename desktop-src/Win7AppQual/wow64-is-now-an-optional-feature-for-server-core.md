---
description: Подсистема WoW64 теперь является дополнительным компонентом для Server Core
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: Состояние WoW64 в Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fad947dac85707d3c9c89a2cffea38c4a4850a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084052"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a><span data-ttu-id="2304e-103">Подсистема WoW64 теперь является дополнительным компонентом для Server Core</span><span class="sxs-lookup"><span data-stu-id="2304e-103">WoW64 Is Now an Optional Feature for Server Core</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="2304e-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="2304e-104">Affected Platforms</span></span>

<span data-ttu-id="2304e-105">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2304e-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="2304e-106">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="2304e-106">Feature Impact</span></span>

 <span data-ttu-id="2304e-107">**Серьезность** — низкая</span><span class="sxs-lookup"><span data-stu-id="2304e-107">**Severity** - Low</span></span>  
<span data-ttu-id="2304e-108">**Частота** -низкая</span><span class="sxs-lookup"><span data-stu-id="2304e-108">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="2304e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="2304e-109">Description</span></span>

<span data-ttu-id="2304e-110">Вариант установки Server Core для Windows Server 2008 R2 позволяет удалить WoW64.</span><span class="sxs-lookup"><span data-stu-id="2304e-110">The Server Core installation option for Windows Server 2008 R2 allows you to uninstall WoW64.</span></span> <span data-ttu-id="2304e-111">WoW64 теперь является необязательным компонентом, который можно удалить, если не требуется выполнять 32-разрядный код.</span><span class="sxs-lookup"><span data-stu-id="2304e-111">WoW64 is now an optional feature that you can uninstall if it is not necessary to run 32-bit code.</span></span>

<span data-ttu-id="2304e-112">Кроме того, для работы в Windows Server 2008 R2 роли Active Directory и службы Active Directory облегченного доступа к каталогам нуждаются в эмуляторе WoW64.</span><span class="sxs-lookup"><span data-stu-id="2304e-112">In addition, the Active Directory and Active Directory Lightweight Directory Services roles require WoW64 in order to run in Windows Server 2008 R2.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="2304e-113">Влияние на манифесты</span><span class="sxs-lookup"><span data-stu-id="2304e-113">Manifestation of Impact</span></span>

<span data-ttu-id="2304e-114">При удалении WoW64 администраторы, выполняющие 32-разрядный код в Server Core, получат сообщение об ошибке, которое не может быть выполнено.</span><span class="sxs-lookup"><span data-stu-id="2304e-114">If you uninstall WoW64, Administrators running 32-bit code on Server Core will receive an error message that the application cannot be executed.</span></span> <span data-ttu-id="2304e-115">Если администраторы пытаются запустить Active Directory и службы Active Directory облегченного доступа к каталогам, они получат сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="2304e-115">If Administrators attempt to run Active Directory and Active Directory Lightweight Directory Services, they will receive an error message.</span></span>

## <a name="mitigation"></a><span data-ttu-id="2304e-116">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="2304e-116">Mitigation</span></span>

<span data-ttu-id="2304e-117">Установите WoW64.</span><span class="sxs-lookup"><span data-stu-id="2304e-117">Install WoW64.</span></span>

## <a name="solution"></a><span data-ttu-id="2304e-118">Решение</span><span class="sxs-lookup"><span data-stu-id="2304e-118">Solution</span></span>

<span data-ttu-id="2304e-119">Предпочтительное решение — предоставить 64-разрядную версию кода, чтобы ее можно было использовать в Server Core без необходимости WoW64.</span><span class="sxs-lookup"><span data-stu-id="2304e-119">The preferred solution is to provide a 64-bit version of the code to enable it to run on Server Core without needing WoW64.</span></span>

<span data-ttu-id="2304e-120">Как минимум, предоставьте документацию пользователя, указывая, что для запуска 32-разрядного кода они должны установить WoW64.</span><span class="sxs-lookup"><span data-stu-id="2304e-120">At a minimum, provide user documentation noting that to run 32-bit code they must install WoW64.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="2304e-121">Совместимость, производительность, надежность и тестирование на удобство использования</span><span class="sxs-lookup"><span data-stu-id="2304e-121">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="2304e-122">Убедитесь, что весь используемый код является 64-битным.</span><span class="sxs-lookup"><span data-stu-id="2304e-122">Verify that all code used is 64-bit.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="2304e-123">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="2304e-123">Links to Other Resources</span></span>

-   [<span data-ttu-id="2304e-124">Сведения о реализации WOW64</span><span class="sxs-lookup"><span data-stu-id="2304e-124">WOW64 Implementation Details</span></span>](../winprog64/wow64-implementation-details.md)
-   [<span data-ttu-id="2304e-125">Отладка WOW64</span><span class="sxs-lookup"><span data-stu-id="2304e-125">Debugging WOW64</span></span>](../winprog64/debugging-wow64.md)
-   <span data-ttu-id="2304e-126">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2304e-126">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span></span>

 

 
