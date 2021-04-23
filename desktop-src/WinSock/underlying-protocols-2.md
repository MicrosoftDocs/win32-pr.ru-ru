---
description: Некоторые протоколы, от которых зависит ваше приложение, для некоторых служб, таких как удаленный вызов процедур (RPC), могут иметь зависимые от IP-версии функции и структуры, требующие изменения приложения с точки зрения их использования.
ms.assetid: b1eac461-10c9-4077-b531-28b7c65a2e31
title: Базовые протоколы для IPv6-приложений Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88789a5f4cd557111c6e1aee8c51ba00eed25e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263064"
---
# <a name="underlying-protocols-for-ipv6-winsock-applications"></a><span data-ttu-id="a04e2-103">Базовые протоколы для IPv6-приложений Winsock</span><span class="sxs-lookup"><span data-stu-id="a04e2-103">Underlying Protocols for IPv6 Winsock Applications</span></span>

<span data-ttu-id="a04e2-104">Некоторые протоколы, от которых зависит ваше приложение, для некоторых служб, таких как удаленный вызов процедур (RPC), могут иметь зависимые от IP-версии функции и структуры, требующие изменения приложения с точки зрения их использования.</span><span class="sxs-lookup"><span data-stu-id="a04e2-104">Some protocols that your application depends on for certain services, such as Remote Procedure Call (RPC), may have IP-version dependent functions and structures that require you to modify your application in terms of their usage.</span></span>

<span data-ttu-id="a04e2-105">Часть процесса изменения кода для поддержки IPv6 должна включать определение того, используются ли базовые протоколы (с точки зрения стека, эти протоколы считаются протоколами более высокого уровня), для правильного использования протокола IPv6 требуется изменение.</span><span class="sxs-lookup"><span data-stu-id="a04e2-105">Part of the process to modify your code to support IPv6 should include determining whether the use of the underlying protocols (from the perspective of the stack, these protocols are considered higher-layer protocols) require modification in order to properly make use of IPv6.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a04e2-106">См. также</span><span class="sxs-lookup"><span data-stu-id="a04e2-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a04e2-107">Рекомендации по IPv6 для приложений Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="a04e2-107">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="a04e2-108">Изменение структур данных для IPv6 Winsock Аппикатионс</span><span class="sxs-lookup"><span data-stu-id="a04e2-108">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="a04e2-109">Сокеты с двумя стеками для IPv6-приложений Winsock</span><span class="sxs-lookup"><span data-stu-id="a04e2-109">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="a04e2-110">Вызовы функций для IPv6-приложений Winsock</span><span class="sxs-lookup"><span data-stu-id="a04e2-110">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
</dt> <dt>

[<span data-ttu-id="a04e2-111">Использование жестко закодированных IPv4-адресов</span><span class="sxs-lookup"><span data-stu-id="a04e2-111">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="a04e2-112">Проблемы с пользовательским интерфейсом для IPv6-приложений Winsock</span><span class="sxs-lookup"><span data-stu-id="a04e2-112">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> </dl>

 

 



