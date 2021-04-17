---
description: Использование платформа .NET Framework 4 с приложениями, созданными на основе более ранних версий
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: Использование платформа .NET Framework 4 с приложениями, созданными на основе более ранних версий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ef252d128ae5d3c8f5b85ef486828fb82e152d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703401"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a><span data-ttu-id="ac3b0-103">Использование платформа .NET Framework 4 с приложениями, созданными на основе более ранних версий</span><span class="sxs-lookup"><span data-stu-id="ac3b0-103">Using .NET Framework 4 with Applications Built on Earlier Versions</span></span>

## <a name="platform"></a><span data-ttu-id="ac3b0-104">Платформа</span><span class="sxs-lookup"><span data-stu-id="ac3b0-104">Platform</span></span>

 <span data-ttu-id="ac3b0-105">**Клиенты** — Windows XP Windows Vista, Windows \| \| 7</span><span class="sxs-lookup"><span data-stu-id="ac3b0-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="ac3b0-106">**Серверы** — windows Server 2003 windows \| Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ac3b0-106">**Servers** - Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="ac3b0-107">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="ac3b0-107">Feature Impact</span></span>

 <span data-ttu-id="ac3b0-108">**Серьезность** — низкая</span><span class="sxs-lookup"><span data-stu-id="ac3b0-108">**Severity** - Low</span></span>  
<span data-ttu-id="ac3b0-109">**Частота** — высокая</span><span class="sxs-lookup"><span data-stu-id="ac3b0-109">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="ac3b0-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ac3b0-110">Description</span></span>

<span data-ttu-id="ac3b0-111">Платформа .NET Framework 4 обеспечивает высокую совместимость с приложениями, созданными с помощью более ранних версий платформа .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ac3b0-111">The .NET Framework 4 is highly compatible with applications that are built by using earlier .NET Framework versions.</span></span> <span data-ttu-id="ac3b0-112">Основные изменения в платформа .NET Framework 4 предназначены для повышения безопасности, соответствия стандартам, правильности, надежности и производительности.</span><span class="sxs-lookup"><span data-stu-id="ac3b0-112">The primary changes in .NET Framework 4 are to improve security, standards compliance, correctness, reliability, and performance.</span></span>

<span data-ttu-id="ac3b0-113">Однако платформа .NET Framework 4 не будет автоматически использовать свою версию среды CLR для запуска приложений, созданных с помощью более ранних версий платформа .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ac3b0-113">However, .NET Framework 4 does not automatically use its version of the common language runtime (CLR) to run applications that are built by using earlier versions of the .NET Framework.</span></span>

## <a name="manifestation"></a><span data-ttu-id="ac3b0-114">Проявление</span><span class="sxs-lookup"><span data-stu-id="ac3b0-114">Manifestation</span></span>

<span data-ttu-id="ac3b0-115">Если приложение создано с помощью более ранней платформа .NET Framework и пользователь открывает это приложение на компьютере, где установлены платформа .NET Framework 4 и более ранняя версия платформа .NET Framework, то приложение использует предыдущую версию среды CLR.</span><span class="sxs-lookup"><span data-stu-id="ac3b0-115">If you built an application by using an earlier .NET Framework and a user opens that application on a computer that has both .NET Framework 4 and the earlier version of the .NET Framework installed, the application uses the earlier CLR version.</span></span>

<span data-ttu-id="ac3b0-116">Однако если платформа .NET Framework 4 является единственной версией среды выполнения, установленной на компьютере, приложение создает исключение и предлагает пользователю установить версию среды выполнения, для которой было создано приложение.</span><span class="sxs-lookup"><span data-stu-id="ac3b0-116">However, if the .NET Framework 4 is the only runtime version that is installed on the computer, the application throws an exception and asks the user to install the runtime version that you built the application against.</span></span>

## <a name="solution"></a><span data-ttu-id="ac3b0-117">Решение</span><span class="sxs-lookup"><span data-stu-id="ac3b0-117">Solution</span></span>

<span data-ttu-id="ac3b0-118">Для запуска приложений, созданных с помощью более ранних версий платформа .NET Framework с платформа .NET Framework 4, необходимо скомпилировать приложение для целевой версии платформа .NET Framework 4, указав его в свойствах проекта в Microsoft Visual Studio, или можно указать платформа .NET Framework 4 в [**<supportedRuntime> элементе**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) в файле конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="ac3b0-118">To run applications that are built with earlier .NET Framework versions with .NET Framework 4, you must compile your application to target the .NET Framework 4 version by specifying it in the properties for your project in Microsoft Visual Studio, or you can specify .NET Framework 4 in the [**<supportedRuntime> element**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) in an application configuration file.</span></span>

<span data-ttu-id="ac3b0-119">Дополнительные сведения о переходе на платформа .NET Framework 4 см. в разделе [руководство по миграции по платформа .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) и [совместимости версий в платформа .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="ac3b0-119">For more information about how to migrate to the .NET Framework 4, see [Migration Guide to the .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) and [Version Compatibility in the .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).</span></span>

## <a name="compatibility-tests"></a><span data-ttu-id="ac3b0-120">Тесты на совместимость</span><span class="sxs-lookup"><span data-stu-id="ac3b0-120">Compatibility Tests</span></span>

<span data-ttu-id="ac3b0-121">После внесения изменений проверьте приложение, чтобы убедиться, что оно выполняется правильно.</span><span class="sxs-lookup"><span data-stu-id="ac3b0-121">After you make the changes, test your application to make sure that it runs correctly.</span></span> <span data-ttu-id="ac3b0-122">Совместимость можно проверить, как описано в разделе о [совместимости приложений платформа .NET Framework 4](/previous-versions/dd889541(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="ac3b0-122">You can test compatibility as described in the [.NET Framework 4 Application Compatibility](/previous-versions/dd889541(v=msdn.10)) topic.</span></span>

<span data-ttu-id="ac3b0-123">Если приложение или компонент не работает после установки платформа .NET Framework 4, отправьте сообщение об ошибке через веб-сайт [Microsoft Connect](https://connect.microsoft.com/visualstudio) .</span><span class="sxs-lookup"><span data-stu-id="ac3b0-123">If your application or component does not work after .NET Framework 4 is installed, submit a bug through the [Microsoft Connect](https://connect.microsoft.com/visualstudio) website.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="ac3b0-124">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="ac3b0-124">Links to Other Resources</span></span>

-   <span data-ttu-id="ac3b0-125">[**<supportedRuntime> дерев**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="ac3b0-125">[**<supportedRuntime> element**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))</span></span>
-   <span data-ttu-id="ac3b0-126">[Руководство. Миграция в .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="ac3b0-126">[Migration Guide to the .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))</span></span>
-   <span data-ttu-id="ac3b0-127">[Совместимость версий в .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="ac3b0-127">[Version Compatibility in the .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))</span></span>
-   <span data-ttu-id="ac3b0-128">**Пошаговое руководство по совместимости приложений платформа .NET Framework 4 RTM:**<https://msdn.microsoft.com/library/dd889541.aspx></span><span class="sxs-lookup"><span data-stu-id="ac3b0-128">**.NET Framework 4 RTM Application Compatibility Walkthrough:**<https://msdn.microsoft.com/library/dd889541.aspx></span></span>
-   [<span data-ttu-id="ac3b0-129">Microsoft Connect</span><span class="sxs-lookup"><span data-stu-id="ac3b0-129">Microsoft Connect</span></span>](https://connect.microsoft.com/)

 

 
