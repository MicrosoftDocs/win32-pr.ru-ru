---
description: .
ms.assetid: f91c4604-b2d6-41e5-be66-bbc8a4f0e28e
title: Подмножество .NET 2,0 теперь в Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e0f836ca7afaef920429df17ef8be845ce92e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104273087"
---
# <a name="subset-of-net-20-now-on-server-core"></a><span data-ttu-id="6abed-103">Подмножество .NET 2,0 теперь в Server Core</span><span class="sxs-lookup"><span data-stu-id="6abed-103">Subset of .NET 2.0 Now on Server Core</span></span>

## <a name="platform"></a><span data-ttu-id="6abed-104">Платформа</span><span class="sxs-lookup"><span data-stu-id="6abed-104">Platform</span></span>

<span data-ttu-id="6abed-105">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6abed-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="6abed-106">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="6abed-106">Feature Impact</span></span>

 <span data-ttu-id="6abed-107">**Серьезность** — низкая</span><span class="sxs-lookup"><span data-stu-id="6abed-107">**Severity** - Low</span></span>  
<span data-ttu-id="6abed-108">**Частота** -низкая</span><span class="sxs-lookup"><span data-stu-id="6abed-108">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="6abed-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6abed-109">Description</span></span>

<span data-ttu-id="6abed-110">Вариант установки Server Core для Windows Server 2008 R2 теперь включает подмножество платформа .NET Framework 2,0.</span><span class="sxs-lookup"><span data-stu-id="6abed-110">The Server Core installation option for Windows Server 2008 R2 now includes a subset of the .NET Framework 2.0.</span></span> <span data-ttu-id="6abed-111">Подмножество — это функциональность в .NET 2,0, которая соответствует функциональным возможностям в Server Core; в базу Server Core не были добавлены двоичные файлы, чтобы разрешить функционирование любой части .NET 2,0.</span><span class="sxs-lookup"><span data-stu-id="6abed-111">The subset is the functionality in .NET 2.0 that aligns with the functionality in Server Core; no binaries were added to the Server Core base to allow any portion of .NET 2.0 to function.</span></span>

<span data-ttu-id="6abed-112">В варианте установки Server Core для Windows Server 2008 не поддерживалась поддержка .NET.</span><span class="sxs-lookup"><span data-stu-id="6abed-112">There was no .NET support in the Server Core installation option for Windows Server 2008.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="6abed-113">Влияние на манифесты</span><span class="sxs-lookup"><span data-stu-id="6abed-113">Manifestation of Impact</span></span>

<span data-ttu-id="6abed-114">Это позволяет запускать в Windows Server 2008 R2 некоторые приложения на основе .NET 2,0.</span><span class="sxs-lookup"><span data-stu-id="6abed-114">This allows some .NET 2.0 based-applications to run on Server Core in Windows Server 2008 R2.</span></span>

## <a name="testing"></a><span data-ttu-id="6abed-115">Тестирование</span><span class="sxs-lookup"><span data-stu-id="6abed-115">Testing</span></span>

<span data-ttu-id="6abed-116">Убедитесь, что используемые в коде классы .NET входят в ядро сервера.</span><span class="sxs-lookup"><span data-stu-id="6abed-116">Verify that the .NET classes your code uses is included in Server Core.</span></span> <span data-ttu-id="6abed-117">Также протестируйте все приложения, которые запускают этот код в Server Core.</span><span class="sxs-lookup"><span data-stu-id="6abed-117">Also test any applications that run this code on Server Core.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="6abed-118">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="6abed-118">Links to Other Resources</span></span>

-   <span data-ttu-id="6abed-119">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6abed-119">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span></span>
-   [<span data-ttu-id="6abed-120">Блог Server Core</span><span class="sxs-lookup"><span data-stu-id="6abed-120">Server Core Blog</span></span>](https://blogs.technet.com/server_core/archive/2008/11/25/net-2-0-and-server-core-in-windows-server-2008-r2.aspx)
-   <span data-ttu-id="6abed-121">*См. также* раздел Server Core *пакета SDK для Windows Server 2008 R2* , когда он станет доступен</span><span class="sxs-lookup"><span data-stu-id="6abed-121">*See also* the Server Core section of the *Windows Server 2008 R2 SDK* when it becomes available</span></span>

> [!Note]  
> <span data-ttu-id="6abed-122">Эти ресурсы могут быть недоступны в некоторых языках и странах или регионах.</span><span class="sxs-lookup"><span data-stu-id="6abed-122">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
