---
title: API подключаемого модуля WinRM
description: Интерфейс прикладного программирования (API) подключаемого модуля WinRM предоставляет функциональные возможности, позволяющие пользователю создавать подключаемые модули, реализуя определенные API для поддерживаемых URI и операций с ресурсами.
ms.assetid: d3e103c1-221b-441b-8bcb-883e3f2a4c1a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccc8920f7df788b4df355b0cbc23478e97111d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986633"
---
# <a name="winrm-plug-in-api"></a><span data-ttu-id="645de-103">API подключаемого модуля WinRM</span><span class="sxs-lookup"><span data-stu-id="645de-103">WinRM Plug-in API</span></span>

<span data-ttu-id="645de-104">Подключаемые модули служба удаленного управления Windows — это собственные библиотеки динамической компоновки (DLL), подключаемые к и расширяющие функциональность WinRM.</span><span class="sxs-lookup"><span data-stu-id="645de-104">Windows Remote Management plug-ins are native dynamic-link libraries (DLLs) that plug into and extend the functionality of WinRM.</span></span> <span data-ttu-id="645de-105">Интерфейс прикладного программирования (API) подключаемого модуля WinRM предоставляет функциональные возможности, позволяющие пользователю создавать подключаемые модули, реализуя определенные API для поддерживаемых URI и операций с [*ресурсами*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="645de-105">The WinRM Plug-in application programming interface (API) provides functionality that enables a user to write plug-ins by implementing certain APIs for supported [*resource URIs*](windows-remote-management-glossary.md) and operations.</span></span> <span data-ttu-id="645de-106">После того как подключаемые модули настроены для службы WinRM или службы IIS (IIS), они загружаются в узел WinRM или узел IIS соответственно.</span><span class="sxs-lookup"><span data-stu-id="645de-106">After the plug-ins are configured for either the WinRM service or Internet Information Services (IIS), they are loaded into the WinRM host or IIS host, respectively.</span></span> <span data-ttu-id="645de-107">Удаленные запросы направляются на эти точки входа подключаемых модулей для выполнения операций.</span><span class="sxs-lookup"><span data-stu-id="645de-107">Remote requests are routed to these plug-in entry points to carry out operations.</span></span>

<span data-ttu-id="645de-108">В разделе Справочник по интерфейсу API подключаемого модуля WinRM содержатся подробные сведения о следующих элементах API:</span><span class="sxs-lookup"><span data-stu-id="645de-108">The WinRM Plug-in API reference section contains detailed information about the following API elements:</span></span>

-   [<span data-ttu-id="645de-109">Точки входа подключаемого модуля авторизации</span><span class="sxs-lookup"><span data-stu-id="645de-109">Authorization Plug-in Entry Points</span></span>](authorization-plug-in-entry-points.md)
-   [<span data-ttu-id="645de-110">Методы подключаемого модуля авторизации</span><span class="sxs-lookup"><span data-stu-id="645de-110">Authorization Plug-in Methods</span></span>](authorization-plug-in-methods.md)
-   [<span data-ttu-id="645de-111">Точки входа подключаемых модулей операций</span><span class="sxs-lookup"><span data-stu-id="645de-111">Operations Plug-in Entry Points</span></span>](operations-plug-in-entry-points.md)
-   [<span data-ttu-id="645de-112">Методы подключаемых модулей операций</span><span class="sxs-lookup"><span data-stu-id="645de-112">Operations Plug-in Methods</span></span>](operations-plug-in-methods.md)
-   [<span data-ttu-id="645de-113">Структуры</span><span class="sxs-lookup"><span data-stu-id="645de-113">Structures</span></span>](winrm-plug-in-api-structures.md)

 

 




