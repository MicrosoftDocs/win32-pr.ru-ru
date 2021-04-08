---
title: Настройка поставщика службы имен
description: Если распределенное приложение регистрирует свой интерфейс в службе имен, клиент и сервер должны использовать одну и ту же службу имен.
ms.assetid: a3f201e1-1a01-4794-9026-05e51a96afc0
keywords:
- Удаленный вызов процедур RPC, задачи, Настройка поставщика службы имен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b7a44ec9a1c83eb7c37f10caae6ca3870679bde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067954"
---
# <a name="configuring-the-name-service-provider"></a><span data-ttu-id="1df4a-104">Настройка поставщика службы имен</span><span class="sxs-lookup"><span data-stu-id="1df4a-104">Configuring the Name Service Provider</span></span>

<span data-ttu-id="1df4a-105">Если распределенное приложение регистрирует свой интерфейс в службе имен, клиент и сервер должны использовать одну и ту же службу имен.</span><span class="sxs-lookup"><span data-stu-id="1df4a-105">If your distributed application registers its interface with a name service, both the client and server must be using the same name service.</span></span> <span data-ttu-id="1df4a-106">Microsoft RPC взаимодействует с локатором Майкрософт и любым поставщиком службы имен (NSP), который соответствует интерфейсу службы имен Microsoft RPC (NSI), например к службе каталогов ячеек DCE, доступ к которой осуществляется с помощью управляющей программы-службы имени корпорации Digital Equipment (НСИД).</span><span class="sxs-lookup"><span data-stu-id="1df4a-106">Microsoft RPC interoperates with Microsoft Locator and any name service provider (NSP) that adheres to the Microsoft RPC name service interface (NSI)—for example, the DCE Cell Directory Service accessed through Digital Equipment Corporation's name service daemon (NSID).</span></span> <span data-ttu-id="1df4a-107">Служба локатора Майкрософт, предназначенная для использования в средах Windows, является поставщиком службы имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1df4a-107">Microsoft Locator, which is designed for use in Windows environments, is the default name service provider.</span></span>

<span data-ttu-id="1df4a-108">В этом разделе представлено обсуждение установки и настройки поставщиков услуг имен.</span><span class="sxs-lookup"><span data-stu-id="1df4a-108">This section presents a discussion of installing and configuring name service providers:</span></span>

-   [<span data-ttu-id="1df4a-109">Настройка службы имен</span><span class="sxs-lookup"><span data-stu-id="1df4a-109">Configuring the Name Service</span></span>](configuring-the-name-service-for-windows-xp-windows-2000-or-windows-nt.md)
-   [<span data-ttu-id="1df4a-110">Настройка службы имен для Windows 95</span><span class="sxs-lookup"><span data-stu-id="1df4a-110">Configuring the Name Service for Windows 95</span></span>](configuring-the-name-service-for-windows-95.md)
-   [<span data-ttu-id="1df4a-111">Настройка службы имен для Windows 3. x или MS-DOS</span><span class="sxs-lookup"><span data-stu-id="1df4a-111">Configuring the Name Service for Windows 3.x or MS-DOS</span></span>](configuring-the-name-service-for-windows-3-x-or-ms-dos.md)
-   [<span data-ttu-id="1df4a-112">Запуск и остановка локатора Майкрософт</span><span class="sxs-lookup"><span data-stu-id="1df4a-112">Starting and Stopping Microsoft Locator</span></span>](starting-and-stopping-microsoft-locator.md)

 

 




