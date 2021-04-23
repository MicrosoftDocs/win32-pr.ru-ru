---
description: Библиотеки DLL TAPI, а также сервер TAPI (Tapisvr.exe) являются важнейшими абстракциями, разделяющими приложения конечных пользователей или серверов от поставщиков услуг. Библиотека DLL TAPI в сочетании с сервером TAPI обеспечивает согласованный интерфейс между этими двумя уровнями.
ms.assetid: 17937bf1-e0bd-4845-9484-d23190807642
title: БИБЛИОТЕКА DLL TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8482045ec16a999957121aff669e93b34b605069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563439"
---
# <a name="tapi-dll"></a><span data-ttu-id="71e41-104">БИБЛИОТЕКА DLL TAPI</span><span class="sxs-lookup"><span data-stu-id="71e41-104">TAPI DLL</span></span>

<span data-ttu-id="71e41-105">Библиотеки DLL TAPI, а также сервер TAPI (Tapisvr.exe) являются важнейшими абстракциями, разделяющими приложения конечных пользователей или серверов от поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="71e41-105">The TAPI DLLs, along with the TAPI Server (Tapisvr.exe), are crucial abstractions separating end-user or server applications from service providers.</span></span> <span data-ttu-id="71e41-106">Библиотека DLL TAPI в сочетании с сервером TAPI обеспечивает согласованный интерфейс между этими двумя уровнями.</span><span class="sxs-lookup"><span data-stu-id="71e41-106">A TAPI DLL in conjunction with the TAPI Server provides a consistent interface between these two layers.</span></span>

<span data-ttu-id="71e41-107">Приложение TAPI загружает соответствующую библиотеку DLL в пространство процесса.</span><span class="sxs-lookup"><span data-stu-id="71e41-107">A TAPI application loads the appropriate DLL into its process space.</span></span> <span data-ttu-id="71e41-108">Во время инициализации TAPI устанавливает связь RPC с Tapisvr.exe.</span><span class="sxs-lookup"><span data-stu-id="71e41-108">During initialization, TAPI establishes an RPC link with Tapisvr.exe.</span></span> <span data-ttu-id="71e41-109">Сервер TAPI работает в контексте SVCHOST.</span><span class="sxs-lookup"><span data-stu-id="71e41-109">The TAPI Server runs in the context of SVCHOST.</span></span>

<span data-ttu-id="71e41-110">Существует три библиотеки DLL, связанные с TAPI: Tapi.dll, Tapi32.dll и Tapi3.dll.</span><span class="sxs-lookup"><span data-stu-id="71e41-110">There are three DLLs associated with TAPI: Tapi.dll, Tapi32.dll, and Tapi3.dll.</span></span> <span data-ttu-id="71e41-111">Эти библиотеки DLL расположены в папке% SystemRoot% \\ System32.</span><span class="sxs-lookup"><span data-stu-id="71e41-111">These DLLs are located in %SystemRoot%\\system32.</span></span> <span data-ttu-id="71e41-112">На следующем рисунке показаны роли соответствующих ролей в телефонии Microsoft:</span><span class="sxs-lookup"><span data-stu-id="71e41-112">The following figure illustrates the roles of their respective roles in Microsoft Telephony:</span></span>

![роли трех библиотек DLL TAPI](images/dllserv.png)

<span data-ttu-id="71e41-114">Существующие 16-разрядные приложения имеют ссылку на Tapi.dll.</span><span class="sxs-lookup"><span data-stu-id="71e41-114">Existing 16-bit applications link to Tapi.dll.</span></span> <span data-ttu-id="71e41-115">Tapi.dll — это просто слой преобразователя, который сопоставляет 16-битные адреса с 32-битными адресами и передает запросы Tapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="71e41-115">Tapi.dll is simply a thunk layer that maps 16-bit addresses to 32-bit addresses and pass requests to Tapi32.dll.</span></span>

<span data-ttu-id="71e41-116">Существующие 32-разрядные приложения TAPI 2. x, связанные с Tapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="71e41-116">Existing 32-bit TAPI 2.x applications link to Tapi32.dll.</span></span> <span data-ttu-id="71e41-117">Tapi32.dll является тонким слоем маршалинга, который передает запросы функций на сервер TAPI (ТАПИСРВ) и при необходимости загружает и вызывает библиотеки DLL поставщика службы мультимедиа в процессе приложения.</span><span class="sxs-lookup"><span data-stu-id="71e41-117">Tapi32.dll is a thin marshalling layer that transfers function requests to the TAPI Server (TAPISRV) and, when needed, loads and invokes media service provider DLLs in the application's process.</span></span>

<span data-ttu-id="71e41-118">Приложения TAPI 3. x связаны с Tapi3.dll.</span><span class="sxs-lookup"><span data-stu-id="71e41-118">TAPI 3.x applications link to Tapi3.dll.</span></span>

 

 



