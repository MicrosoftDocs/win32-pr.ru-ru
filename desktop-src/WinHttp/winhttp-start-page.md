---
description: Службы Microsoft Windows HTTP Services (WinHTTP) предоставляют разработчикам интерфейс прикладного программирования (API) HTTP для отправки запросов через протокол HTTP к другим серверам HTTP.
ms.assetid: 354ab65d-5e46-451d-b36b-2f8166a1a048
title: Службы HTTP Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f03a3204257410e4db0182724ab63743116f021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692322"
---
# <a name="windows-http-services"></a><span data-ttu-id="c5f07-103">Службы HTTP Windows</span><span class="sxs-lookup"><span data-stu-id="c5f07-103">Windows HTTP Services</span></span>

## <a name="purpose"></a><span data-ttu-id="c5f07-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="c5f07-104">Purpose</span></span>

<span data-ttu-id="c5f07-105">Службы Microsoft Windows HTTP Services (WinHTTP) предоставляют разработчикам интерфейс прикладного программирования (API) HTTP для отправки запросов через протокол HTTP к другим серверам HTTP.</span><span class="sxs-lookup"><span data-stu-id="c5f07-105">Microsoft Windows HTTP Services (WinHTTP) provides developers with an HTTP client application programming interface (API) to send requests through the HTTP protocol to other HTTP servers.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="c5f07-106">Где применимо</span><span class="sxs-lookup"><span data-stu-id="c5f07-106">Where applicable</span></span>

<span data-ttu-id="c5f07-107">WinHTTP поддерживает Настольные клиентские приложения, службы Windows и приложения на основе Windows Server.</span><span class="sxs-lookup"><span data-stu-id="c5f07-107">WinHTTP supports desktop client applications, Windows services, and Windows server-based applications.</span></span>

<span data-ttu-id="c5f07-108">Дополнительные сведения об использовании WinHTTP для приложений, построенных на платформе Microsoft .NET Framework, см. в разделе [API винхттфандлер](/dotnet/api/system.net.http?view=netframework-4.8) .</span><span class="sxs-lookup"><span data-stu-id="c5f07-108">For more information on how to use WinHTTP for applications built on the Microsoft .NET Framework, see the [WinHttpHandler API](/dotnet/api/system.net.http?view=netframework-4.8)</span></span>

## <a name="developer-audience"></a><span data-ttu-id="c5f07-109">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="c5f07-109">Developer audience</span></span>

<span data-ttu-id="c5f07-110">WinHTTP предлагает как интерфейс прикладного программирования (API) C/C++, так и компонент автоматизации модели COM, который подходит для использования в приложениях на основе Active Server страниц (ASP).</span><span class="sxs-lookup"><span data-stu-id="c5f07-110">WinHTTP offers both a C/C++ application programming interface (API) and a Component Object Model (COM) automation component suitable for use in Active Server Pages (ASP) based applications.</span></span>

<span data-ttu-id="c5f07-111">Основное понимание протокола HTTP важно для использования любого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c5f07-111">A basic understanding of the HTTP protocol is important to use either interface.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c5f07-112">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="c5f07-112">Run-time requirements</span></span>

<span data-ttu-id="c5f07-113">WinHTTP 5,1 предлагает улучшения по сравнению с версией 5,0.</span><span class="sxs-lookup"><span data-stu-id="c5f07-113">WinHTTP 5.1 offers improvements over version 5.0.</span></span> <span data-ttu-id="c5f07-114">Он включен в операционную систему.</span><span class="sxs-lookup"><span data-stu-id="c5f07-114">It is included in the operating system.</span></span> <span data-ttu-id="c5f07-115">Дополнительные сведения о новых возможностях см. в статьях [что нового в WinHTTP 5,1](what-s-new-in-winhttp-5-1.md) и [что нового в Windows Server 2008 и Windows Vista](what-s-new-in-windows-longhorn.md).</span><span class="sxs-lookup"><span data-stu-id="c5f07-115">For more information about new features, see [What's New in WinHTTP 5.1](what-s-new-in-winhttp-5-1.md) and [What's New in Windows Server 2008 and Windows Vista](what-s-new-in-windows-longhorn.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5f07-116">Скачивание WinHTTP 5,0 больше не доступно.</span><span class="sxs-lookup"><span data-stu-id="c5f07-116">The WinHTTP 5.0 download is no longer available.</span></span> <span data-ttu-id="c5f07-117">Начиная с 1 октября 2004 г. Корпорация Майкрософт удалила пакет SDK для WinHTTP 5,0 с сайта MSDN и прекратил поддержку продукта для версии 5,0.</span><span class="sxs-lookup"><span data-stu-id="c5f07-117">As of October 1, 2004, Microsoft removed the WinHTTP 5.0 SDK download from MSDN and terminated product support for version 5.0.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="c5f07-118">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="c5f07-118">In this section</span></span>

-   [<span data-ttu-id="c5f07-119">Сведения о WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c5f07-119">About WinHTTP</span></span>](about-winhttp.md)
-   [<span data-ttu-id="c5f07-120">Использование WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c5f07-120">Using WinHTTP</span></span>](using-winhttp.md)
-   [<span data-ttu-id="c5f07-121">Справочник по WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c5f07-121">WinHTTP Reference</span></span>](winhttp-reference.md)

 

 
