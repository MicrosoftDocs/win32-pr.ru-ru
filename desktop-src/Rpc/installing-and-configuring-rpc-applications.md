---
title: Установка и настройка приложений RPC
description: При установке операционной системы Microsoft Windows на сервере или клиенте программа установки автоматически устанавливает файлы среды выполнения RPC.
ms.assetid: cfcada3d-cf7c-42a9-9ed4-0b1bba7a98cf
keywords:
- Удаленный вызов процедур RPC, задачи, установка и настройка приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90837261c571276a74bb3a5354c7b9a5db2da6cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487041"
---
# <a name="installing-and-configuring-rpc-applications"></a><span data-ttu-id="ba3ba-104">Установка и настройка приложений RPC</span><span class="sxs-lookup"><span data-stu-id="ba3ba-104">Installing and Configuring RPC Applications</span></span>

<span data-ttu-id="ba3ba-105">При установке операционной системы Microsoft Windows на сервере или клиенте программа установки автоматически устанавливает файлы среды выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="ba3ba-105">When the Microsoft Windows operating system is installed on a server or client, setup automatically installs the RPC run-time files.</span></span> <span data-ttu-id="ba3ba-106">Дальнейшая установка RPC не требуется.</span><span class="sxs-lookup"><span data-stu-id="ba3ba-106">No further RPC installation is required.</span></span> <span data-ttu-id="ba3ba-107">Однако необходимо убедиться, что устанавливаемая версия Windows поддерживает все функции, используемые в распределенном приложении.</span><span class="sxs-lookup"><span data-stu-id="ba3ba-107">You must ensure, however, that the version of Windows you install supports all the features used in your distributed application.</span></span>

<span data-ttu-id="ba3ba-108">При использовании приложения RPC в операционной системе Windows 3. x или Microsoft MS-DOS необходимо скопировать исполняемые файлы среды выполнения RPC на компьютеры Windows 3. x или MS-DOS, которые будут использовать приложение.</span><span class="sxs-lookup"><span data-stu-id="ba3ba-108">When you use an RPC application on a Windows 3.x or Microsoft MS-DOS operating system, you must copy the RPC run-time executable files to the Windows 3.x or MS-DOS computers that will be using the application.</span></span> <span data-ttu-id="ba3ba-109">Каталог \\ мстулс \\ RPC \_ rt16 на компакт-диске с пакетом программного обеспечения платформы (SDK) содержит образ этих файлов вместе с программой установки для установки файлов.</span><span class="sxs-lookup"><span data-stu-id="ba3ba-109">The directory \\mstools\\rpc\_rt16 on the Platform Software Development Kit (SDK) CD contains a disk image of these files along with a setup program to install the files.</span></span> <span data-ttu-id="ba3ba-110">Используйте этот образ диска, чтобы создать установочный диск для распространения с помощью приложения RPC.</span><span class="sxs-lookup"><span data-stu-id="ba3ba-110">Use this disk image to create an install disk for distribution with your RPC application.</span></span> <span data-ttu-id="ba3ba-111">Вы также можете использовать 16-разрядные клиентские приложения, предназначенные для MS-DOS или Windows, в 32-разрядной или 64-разрядной операционной системе Windows.</span><span class="sxs-lookup"><span data-stu-id="ba3ba-111">You can also use 16-bit client applications targeted toward MS-DOS or Windows on a 32-bit/64-bit Windows operating system.</span></span> <span data-ttu-id="ba3ba-112">Однако программа установки приложения должна установить исполняемые файлы, содержащиеся в этом образе диска.</span><span class="sxs-lookup"><span data-stu-id="ba3ba-112">However, your application's installation program must install the executable files contained in this disk image.</span></span>

<span data-ttu-id="ba3ba-113">При создании приложения RPC для клиента Macintosh необходимо связать необходимые файлы с приложением во время сборки.</span><span class="sxs-lookup"><span data-stu-id="ba3ba-113">When you build an RPC application for a Macintosh client, you must link the necessary files to the application at build time.</span></span> <span data-ttu-id="ba3ba-114">Дополнительные установки RPC не требуются.</span><span class="sxs-lookup"><span data-stu-id="ba3ba-114">No additional RPC installation is needed.</span></span>

<span data-ttu-id="ba3ba-115">Дополнительные сведения о распространяемых файлах и лицензионных соглашениях см \\ . в статье \\Redist.txt лицензий и \\ \\License.txt лицензий на компакт-диске Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="ba3ba-115">For more details about redistributable files and licensing agreements, see \\LICENSE\\Redist.txt and \\LICENSE\\License.txt on the Platform SDK CD.</span></span>

<span data-ttu-id="ba3ba-116">В этом разделе содержатся сведения о настройке приложений RPC на различных аппаратных и программных платформах.</span><span class="sxs-lookup"><span data-stu-id="ba3ba-116">This section contains information about setting up RPC applications on a variety of hardware and software platforms.</span></span> <span data-ttu-id="ba3ba-117">Он представляет обсуждение в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="ba3ba-117">It presents the discussion in the following sections:</span></span>

-   [<span data-ttu-id="ba3ba-118">Настройка поставщика службы имен</span><span class="sxs-lookup"><span data-stu-id="ba3ba-118">Configuring the Name Service Provider</span></span>](configuring-the-name-service-provider.md)
-   [<span data-ttu-id="ba3ba-119">Сведения о реестре</span><span class="sxs-lookup"><span data-stu-id="ba3ba-119">Registry Information</span></span>](registry-information.md)
-   [<span data-ttu-id="ba3ba-120">Использование RPC с прокси-сервером Winsock</span><span class="sxs-lookup"><span data-stu-id="ba3ba-120">Using RPC with Winsock Proxy</span></span>](using-rpc-with-winsock-proxy.md)
-   [<span data-ttu-id="ba3ba-121">Установка SPX/IPX</span><span class="sxs-lookup"><span data-stu-id="ba3ba-121">SPX/IPX Installation</span></span>](spx-ipx-installation.md)
-   [<span data-ttu-id="ba3ba-122">Настройка сервера безопасности</span><span class="sxs-lookup"><span data-stu-id="ba3ba-122">Configuring the Security Server</span></span>](configuring-the-security-server.md)

 

 




