---
title: Разработка приложений для Windows RPC
description: При установке пакета средств разработки программного обеспечения для платформы (SDK) автоматически устанавливаются следующие среды разработки RPC, библиотеки времени выполнения и средства.
ms.assetid: d5da3bca-5251-4ba4-b873-0817fe0f298d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b418358649d0cf7205b9a3bde236cf66d3ce81e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070511"
---
# <a name="developing-rpc-windows-applications"></a><span data-ttu-id="a5475-103">Разработка приложений для Windows RPC</span><span class="sxs-lookup"><span data-stu-id="a5475-103">Developing RPC Windows Applications</span></span>

<span data-ttu-id="a5475-104">При установке пакета средств разработки программного обеспечения для платформы (SDK) автоматически устанавливаются следующие среды разработки RPC, библиотеки времени выполнения и средства.</span><span class="sxs-lookup"><span data-stu-id="a5475-104">When you install the Platform Software Development Kit (SDK), the following RPC development environment, the run-time libraries, and tools are automatically installed:</span></span>

-   <span data-ttu-id="a5475-105">Заголовок языка C/C++ (. H) файлы</span><span class="sxs-lookup"><span data-stu-id="a5475-105">C/C++ language header (.H) files</span></span>
-   <span data-ttu-id="a5475-106">Файлы библиотек импорта RPC (lib)</span><span class="sxs-lookup"><span data-stu-id="a5475-106">RPC import libraries (.lib) files</span></span>
-   <span data-ttu-id="a5475-107">Примеры программ</span><span class="sxs-lookup"><span data-stu-id="a5475-107">Sample programs</span></span>
-   <span data-ttu-id="a5475-108">Справочные файлы по RPC</span><span class="sxs-lookup"><span data-stu-id="a5475-108">RPC reference Help files</span></span>
-   <span data-ttu-id="a5475-109">Служебная программа **uuidgen**</span><span class="sxs-lookup"><span data-stu-id="a5475-109">The **uuidgen** utility</span></span>

<span data-ttu-id="a5475-110">При установке Windows устанавливаются следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="a5475-110">When you install Windows, the following are installed:</span></span>

-   <span data-ttu-id="a5475-111">Библиотеки DLL времени выполнения RPC</span><span class="sxs-lookup"><span data-stu-id="a5475-111">RPC Run-time DLLs</span></span>
-   <span data-ttu-id="a5475-112">Локатор Майкрософт (не поддерживается в Windows Vista и более поздних версиях)</span><span class="sxs-lookup"><span data-stu-id="a5475-112">Microsoft Locator (not supported on Windows Vista and later)</span></span>
-   <span data-ttu-id="a5475-113">Конечная точка RPC — службы сопоставления</span><span class="sxs-lookup"><span data-stu-id="a5475-113">RPC Endpoint-mapping services</span></span>

<span data-ttu-id="a5475-114">Следующие библиотеки импорта RPC.</span><span class="sxs-lookup"><span data-stu-id="a5475-114">The following RPC import libraries.</span></span>



| <span data-ttu-id="a5475-115">Импорт библиотеки</span><span class="sxs-lookup"><span data-stu-id="a5475-115">Import library</span></span> | <span data-ttu-id="a5475-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a5475-116">Description</span></span>                |
|----------------|----------------------------|
| <span data-ttu-id="a5475-117">Rpcns4. lib</span><span class="sxs-lookup"><span data-stu-id="a5475-117">Rpcns4.lib</span></span>     | <span data-ttu-id="a5475-118">Функции Name-Service</span><span class="sxs-lookup"><span data-stu-id="a5475-118">Name-service functions</span></span>     |
| <span data-ttu-id="a5475-119">Rpcrt4. lib</span><span class="sxs-lookup"><span data-stu-id="a5475-119">Rpcrt4.lib</span></span>     | <span data-ttu-id="a5475-120">Функции времени выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="a5475-120">Windows run-time functions</span></span> |



 

> [!Note]  
> <span data-ttu-id="a5475-121">Rpcns4. lib устарела и больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a5475-121">Rpcns4.lib is obsolete and no longer supported.</span></span>

 

<span data-ttu-id="a5475-122">Для поддержки нижнего уровня включены следующие библиотеки RPC.</span><span class="sxs-lookup"><span data-stu-id="a5475-122">The following RPC libraries are included for down-level support.</span></span>



| <span data-ttu-id="a5475-123">Библиотека динамической компоновки</span><span class="sxs-lookup"><span data-stu-id="a5475-123">Dynamic-link library</span></span> | <span data-ttu-id="a5475-124">Описание:</span><span class="sxs-lookup"><span data-stu-id="a5475-124">Description</span></span>                 | <span data-ttu-id="a5475-125">Платформа</span><span class="sxs-lookup"><span data-stu-id="a5475-125">Platform</span></span>                           |
|----------------------|-----------------------------|------------------------------------|
| <span data-ttu-id="a5475-126">Rpcltc1.dll</span><span class="sxs-lookup"><span data-stu-id="a5475-126">Rpcltc1.dll</span></span>          | <span data-ttu-id="a5475-127">Транспорт клиента именованного канала</span><span class="sxs-lookup"><span data-stu-id="a5475-127">Client named-pipe transport</span></span> | <span data-ttu-id="a5475-128">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="a5475-128">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="a5475-129">Rpclts1.dll</span><span class="sxs-lookup"><span data-stu-id="a5475-129">Rpclts1.dll</span></span>          | <span data-ttu-id="a5475-130">Транспорт серверных именованных каналов</span><span class="sxs-lookup"><span data-stu-id="a5475-130">Server named-pipe transport</span></span> | <span data-ttu-id="a5475-131">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="a5475-131">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="a5475-132">Rpcltc3.dll</span><span class="sxs-lookup"><span data-stu-id="a5475-132">Rpcltc3.dll</span></span>          | <span data-ttu-id="a5475-133">Клиентский транспорт TCP/IP</span><span class="sxs-lookup"><span data-stu-id="a5475-133">Client TCP/IP transport</span></span>     | <span data-ttu-id="a5475-134">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="a5475-134">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="a5475-135">Rpclts3.dll</span><span class="sxs-lookup"><span data-stu-id="a5475-135">Rpclts3.dll</span></span>          | <span data-ttu-id="a5475-136">Транспорт TCP/IP сервера</span><span class="sxs-lookup"><span data-stu-id="a5475-136">Server TCP/IP transport</span></span>     | <span data-ttu-id="a5475-137">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="a5475-137">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="a5475-138">Rpcltc5.dll</span><span class="sxs-lookup"><span data-stu-id="a5475-138">Rpcltc5.dll</span></span>          | <span data-ttu-id="a5475-139">Клиентский транспорт NetBIOS</span><span class="sxs-lookup"><span data-stu-id="a5475-139">Client NetBIOS transport</span></span>    | <span data-ttu-id="a5475-140">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="a5475-140">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="a5475-141">Rpclts5.dll</span><span class="sxs-lookup"><span data-stu-id="a5475-141">Rpclts5.dll</span></span>          | <span data-ttu-id="a5475-142">Транспорт NetBIOS сервера</span><span class="sxs-lookup"><span data-stu-id="a5475-142">Server NetBIOS transport</span></span>    | <span data-ttu-id="a5475-143">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="a5475-143">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="a5475-144">Rpcltc6.dll</span><span class="sxs-lookup"><span data-stu-id="a5475-144">Rpcltc6.dll</span></span>          | <span data-ttu-id="a5475-145">Транспорт клиента SPX</span><span class="sxs-lookup"><span data-stu-id="a5475-145">Client SPX transport</span></span>        | <span data-ttu-id="a5475-146">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="a5475-146">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="a5475-147">Rpclts6.dll</span><span class="sxs-lookup"><span data-stu-id="a5475-147">Rpclts6.dll</span></span>          | <span data-ttu-id="a5475-148">Транспорт сервера SPX</span><span class="sxs-lookup"><span data-stu-id="a5475-148">Server SPX transport</span></span>        | <span data-ttu-id="a5475-149">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="a5475-149">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="a5475-150">Rpcdgc6.dll</span><span class="sxs-lookup"><span data-stu-id="a5475-150">Rpcdgc6.dll</span></span>          | <span data-ttu-id="a5475-151">Клиентский транспорт IPX</span><span class="sxs-lookup"><span data-stu-id="a5475-151">Client IPX transport</span></span>        | <span data-ttu-id="a5475-152">Windows NT</span><span class="sxs-lookup"><span data-stu-id="a5475-152">Windows NT</span></span>                         |
| <span data-ttu-id="a5475-153">Rpcdgs6.dll</span><span class="sxs-lookup"><span data-stu-id="a5475-153">Rpcdgs6.dll</span></span>          | <span data-ttu-id="a5475-154">Транспорт сервера IPX</span><span class="sxs-lookup"><span data-stu-id="a5475-154">Server IPX transport</span></span>        | <span data-ttu-id="a5475-155">Windows NT</span><span class="sxs-lookup"><span data-stu-id="a5475-155">Windows NT</span></span>                         |
| <span data-ttu-id="a5475-156">Rpcdgc3.dll</span><span class="sxs-lookup"><span data-stu-id="a5475-156">Rpcdgc3.dll</span></span>          | <span data-ttu-id="a5475-157">Клиентский транспорт UDP</span><span class="sxs-lookup"><span data-stu-id="a5475-157">Client UDP transport</span></span>        | <span data-ttu-id="a5475-158">Windows NT</span><span class="sxs-lookup"><span data-stu-id="a5475-158">Windows NT</span></span>                         |
| <span data-ttu-id="a5475-159">Rpcdgs3.dll</span><span class="sxs-lookup"><span data-stu-id="a5475-159">Rpcdgs3.dll</span></span>          | <span data-ttu-id="a5475-160">Транспорт UDP сервера</span><span class="sxs-lookup"><span data-stu-id="a5475-160">Server UDP transport</span></span>        | <span data-ttu-id="a5475-161">Windows NT</span><span class="sxs-lookup"><span data-stu-id="a5475-161">Windows NT</span></span>                         |



 

<span data-ttu-id="a5475-162">Также потребуется компилятор язык MIDL (MIDL).</span><span class="sxs-lookup"><span data-stu-id="a5475-162">You will also need the Microsoft Interface Definition Language (MIDL) compiler.</span></span> <span data-ttu-id="a5475-163">Дополнительные сведения см. [в разделе Использование КОМПИЛЯТОРА MIDL](/windows/desktop/Midl/using-the-midl-compiler-2).</span><span class="sxs-lookup"><span data-stu-id="a5475-163">For more information, see [Using The MIDL Compiler](/windows/desktop/Midl/using-the-midl-compiler-2).</span></span>

 

 