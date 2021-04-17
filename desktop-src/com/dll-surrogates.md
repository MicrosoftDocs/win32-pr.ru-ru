---
title: Суррогаты библиотеки DLL
description: Суррогаты библиотеки DLL
ms.assetid: fe30c0ae-1d19-4a5f-8ee3-8a5337c79c44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c3fcbd07b4c6317dfb6ac8ede772fc62035f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710164"
---
# <a name="dll-surrogates"></a><span data-ttu-id="241be-103">Суррогаты библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="241be-103">DLL Surrogates</span></span>

<span data-ttu-id="241be-104">COM позволяет создавать серверы DLL, которые могут быть загружены в процесс суррогатного EXE-файла.</span><span class="sxs-lookup"><span data-stu-id="241be-104">COM makes it possible to create DLL servers that can be loaded into a surrogate EXE process.</span></span> <span data-ttu-id="241be-105">Это сочетает простоту написания серверов DLL с учетом реализации исполняемых файлов.</span><span class="sxs-lookup"><span data-stu-id="241be-105">This combines the ease of writing DLL servers with the benefits of executable implementation.</span></span> <span data-ttu-id="241be-106">Средства разработки, такие как Microsoft Visual Studio упрощают написание серверов DLL, но сам сервер DLL имеет ограничения.</span><span class="sxs-lookup"><span data-stu-id="241be-106">Development tools like Microsoft Visual Studio facilitate the writing of DLL servers, but a DLL server in itself has limits.</span></span> <span data-ttu-id="241be-107">Запуск сервера DLL в суррогатном процессе предлагает несколько возможных преимуществ.</span><span class="sxs-lookup"><span data-stu-id="241be-107">Running the DLL server in a surrogate process offers several possible benefits:</span></span>

-   <span data-ttu-id="241be-108">Изоляция сбоев и возможность обслуживания нескольких клиентов одновременно.</span><span class="sxs-lookup"><span data-stu-id="241be-108">Fault isolation and the ability to service multiple clients simultaneously.</span></span>
-   <span data-ttu-id="241be-109">В распределенной среде реализация сервера DLL может использоваться для обслуживания удаленных клиентов.</span><span class="sxs-lookup"><span data-stu-id="241be-109">In a distributed environment, a DLL server implementation could be used to service remote clients.</span></span>
-   <span data-ttu-id="241be-110">Он может позволить клиентам защищать себя от ненадежного серверного кода, разрешая им доступ к службам, предоставляемым сервером DLL.</span><span class="sxs-lookup"><span data-stu-id="241be-110">It could permit clients to help protect themselves from untrusted server code while allowing them access to the services the DLL server provides.</span></span>
-   <span data-ttu-id="241be-111">Запуск сервера DLL в суррогате предоставляет библиотеку DLL с защитой суррогатов.</span><span class="sxs-lookup"><span data-stu-id="241be-111">Running a DLL server in a surrogate provides the DLL with the surrogate's security.</span></span>

<span data-ttu-id="241be-112">COM предоставляет суррогатный процесс по умолчанию, или вы можете написать пользовательский суррогат, если у вас есть особые потребности.</span><span class="sxs-lookup"><span data-stu-id="241be-112">COM provides a default surrogate process, or you can write a custom surrogate if you have special needs.</span></span>

<span data-ttu-id="241be-113">В следующих разделах содержатся дополнительные сведения о суррогатах DLL:</span><span class="sxs-lookup"><span data-stu-id="241be-113">The following topics provide more information on DLL surrogates:</span></span>

-   [<span data-ttu-id="241be-114">Требования к серверу DLL</span><span class="sxs-lookup"><span data-stu-id="241be-114">DLL Server Requirements</span></span>](dll-server-requirements.md)
-   [<span data-ttu-id="241be-115">Использование суррогата System-Supplied</span><span class="sxs-lookup"><span data-stu-id="241be-115">Using the System-Supplied Surrogate</span></span>](using-the-system-supplied-surrogate.md)
-   [<span data-ttu-id="241be-116">Написание пользовательского суррогата</span><span class="sxs-lookup"><span data-stu-id="241be-116">Writing a Custom Surrogate</span></span>](writing-a-custom-surrogate.md)

 

 




