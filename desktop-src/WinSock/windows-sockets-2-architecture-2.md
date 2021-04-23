---
description: Архитектура Windows Sockets 2 (Winsock) совместима с архитектурой Windows Open System (ВОСА).
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Архитектура Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae85ad58a4206d75144e47662bd563fb3235eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155262"
---
# <a name="windows-sockets-2-architecture"></a><span data-ttu-id="545ec-103">Архитектура Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="545ec-103">Windows Sockets 2 Architecture</span></span>

<span data-ttu-id="545ec-104">Архитектура Windows Sockets 2 совместима с архитектурой Windows Open System (ВОСА), как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="545ec-104">The Windows Sockets 2 architecture is compliant with the Windows Open System Architecture (WOSA), as illustrated below:</span></span>

![Архитектура Windows Sockets 2](images/ovrvw2-1.png)

<span data-ttu-id="545ec-106">Winsock определяет стандартный интерфейс поставщика услуг (SPI) между прикладным программным интерфейсом (API) и его функциями, экспортированными из WS2 \_32.dll и стеками протоколов.</span><span class="sxs-lookup"><span data-stu-id="545ec-106">Winsock defines a standard service provider interface (SPI) between the application programming interface (API), with its functions exported from WS2\_32.dll and the protocol stacks.</span></span> <span data-ttu-id="545ec-107">Следовательно, поддержка Winsock не ограничена протоколами TCP/IP, как в случае с сокетами Windows 1,1.</span><span class="sxs-lookup"><span data-stu-id="545ec-107">Consequently, Winsock support is not limited to TCP/IP protocol stacks as is the case for Windows Sockets 1.1.</span></span>

<span data-ttu-id="545ec-108">Архитектура Windows Sockets 2 не является обязательной или желательной, чтобы поставщики стеков предWS2и собственную реализацию \_32.dll, поскольку один WS2 \_32.dll должен работать во всех стеках.</span><span class="sxs-lookup"><span data-stu-id="545ec-108">With the Windows Sockets 2 architecture, it is not necessary or desirable, for stack vendors to supply their own implementation of WS2\_32.dll, since a single WS2\_32.dll must work across all stacks.</span></span> <span data-ttu-id="545ec-109">WS2 \_32.dll и оболочки совместимости должны быть просмотрены так же, как компонент операционной системы.</span><span class="sxs-lookup"><span data-stu-id="545ec-109">The WS2\_32.dll and compatibility shims should be viewed in the same way as an operating system component.</span></span>

 

 



