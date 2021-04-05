---
description: Сервер TAPI (ТАПИСРВ) является центральным репозиторием данных телефонии на компьютере пользователя.
ms.assetid: 794d230c-abe8-429d-bbf5-91ba364b16ab
title: Сервер TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a6886a5d8e56519f10fc370ed15adc3b1af7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911531"
---
# <a name="tapi-server"></a><span data-ttu-id="6ce99-103">Сервер TAPI</span><span class="sxs-lookup"><span data-stu-id="6ce99-103">TAPI Server</span></span>

<span data-ttu-id="6ce99-104">Сервер TAPI (ТАПИСРВ) является центральным репозиторием данных телефонии на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="6ce99-104">The TAPI server (TAPISRV) is the central repository of telephony data on a user computer.</span></span> <span data-ttu-id="6ce99-105">Этот процесс службы отслеживает локальные и удаленные ресурсы телефонии, приложения, зарегистрированные для обработки обращений в службу поддержки, и ожидающие асинхронные функции, а также обеспечивает единообразный интерфейс с поставщиками услуг телефонии (специалистами).</span><span class="sxs-lookup"><span data-stu-id="6ce99-105">This service process tracks local and remote telephony resources, applications registered to handle Assisted Telephony requests, and pending asynchronous functions, and it also enables a consistent interface with telephony service providers (TSPs).</span></span> <span data-ttu-id="6ce99-106">Дополнительные сведения и схема, иллюстрирующие связь между сервером TAPI и другими компонентами, а также обзор их ролей см. в [статье модель программирования телефонии (Майкрософт](microsoft-telephony-programming-model.md)).</span><span class="sxs-lookup"><span data-stu-id="6ce99-106">For more information and a diagram that illustrates the relationship of the TAPI Server to other components and an overview of their roles, see [Microsoft Telephony Programming Model](microsoft-telephony-programming-model.md).</span></span>

<span data-ttu-id="6ce99-107">Для компьютеров, работающих под управлением операционных систем Windows Server 2003, Windows XP и Windows 2000, ТАПИСРВ выполняется в контексте Svchost.exe.</span><span class="sxs-lookup"><span data-stu-id="6ce99-107">For computers running on Windows Server 2003 operating systems, Windows XP, and Windows 2000, TAPISRV runs within the context of Svchost.exe.</span></span> <span data-ttu-id="6ce99-108">Для компьютеров под управлением Windows NT он выполняется как отдельный процесс службы.</span><span class="sxs-lookup"><span data-stu-id="6ce99-108">For computers running on Windows NT, it runs as a separate service process.</span></span> <span data-ttu-id="6ce99-109">Когда приложение загружает библиотеку DLL TAPI в пространство процесса и выполняет операцию инициализации, Библиотека DLL устанавливает ссылку RPC на сервер TAPI.</span><span class="sxs-lookup"><span data-stu-id="6ce99-109">When an application loads a TAPI DLL into its process space and performs an initialization operation, the DLL establishes an RPC link to the TAPI Server.</span></span> <span data-ttu-id="6ce99-110">Сервер TAPI загружает поставщиков телефонных услуг (специалистами) в пространство процесса.</span><span class="sxs-lookup"><span data-stu-id="6ce99-110">The TAPI Server loads telephone service providers (TSPs) into its process space.</span></span> <span data-ttu-id="6ce99-111">Независимо от количества приложений, обращающихся к определенным устройствам поставщика, будет существовать только один экземпляр данного TSP.</span><span class="sxs-lookup"><span data-stu-id="6ce99-111">Regardless of how many applications access a given provider's devices, only one instance of a given TSP will exist.</span></span>

 

 



