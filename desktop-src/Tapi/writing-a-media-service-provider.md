---
description: Поставщик службы мультимедиа должен реализовать минимальное подмножество МСПИ интерфейсов Итмспаддресс Иттерминалсуппорт Итстреамконтрол и Итстреам.
ms.assetid: 59560bdf-953e-48e8-b565-46c3e0123c7e
title: Создание поставщика службы мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782dddb9a87725bde7c104d459b71204a04de018
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351165"
---
# <a name="writing-a-media-service-provider"></a><span data-ttu-id="d7d0c-103">Создание поставщика службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d7d0c-103">Writing a Media Service Provider</span></span>

<span data-ttu-id="d7d0c-104">Поставщик службы мультимедиа должен реализовать минимальное подмножество интерфейсов МСПИ: [**итмспаддресс**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**иттерминалсуппорт**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**итстреамконтрол**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)и [**итстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span><span class="sxs-lookup"><span data-stu-id="d7d0c-104">A media service provider must implement a minimum subset of MSPI interfaces: [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol), and [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span></span> <span data-ttu-id="d7d0c-105">Поддержка подпотока является необязательной.</span><span class="sxs-lookup"><span data-stu-id="d7d0c-105">SubStream support is optional.</span></span> <span data-ttu-id="d7d0c-106">Кроме того, данный MSP может реализовывать дополнительные методы, например элементы управления, необходимые для специализированного оборудования.</span><span class="sxs-lookup"><span data-stu-id="d7d0c-106">In addition, a given MSP may implement additional methods, such as controls required for specialized hardware.</span></span>

<span data-ttu-id="d7d0c-107">Следующие материалные документы:</span><span class="sxs-lookup"><span data-stu-id="d7d0c-107">The following material documents:</span></span>

-   <span data-ttu-id="d7d0c-108">[Базовые классы MSP TAPI 3](tapi-3-msp-base-classes.md), которые представляют собой набор классов C++, предназначенных для упрощения задач создания MSP-файла на основе DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d7d0c-108">The [TAPI 3 MSP Base Classes](tapi-3-msp-base-classes.md), which are a set of C++ classes designed to simplify the task of building a DirectShow-based MSP.</span></span> <span data-ttu-id="d7d0c-109">Базовые классы реализуют все интерфейсы МСПИ обычным образом.</span><span class="sxs-lookup"><span data-stu-id="d7d0c-109">The base classes implement all the MSPI interfaces in a generic manner.</span></span> <span data-ttu-id="d7d0c-110">Различные MSP могут переопределять функции, относящиеся к MSP, и предоставлять собственные реализации.</span><span class="sxs-lookup"><span data-stu-id="d7d0c-110">Different MSPs can override MSP-specific functions and provide their own implementations.</span></span>
-   <span data-ttu-id="d7d0c-111">[Диспетчер терминалов TAPI 3](tapi-3-terminal-manager.md), предоставляющий интерфейсы и методы, используемые MSP для управления терминалами.</span><span class="sxs-lookup"><span data-stu-id="d7d0c-111">The [TAPI 3 Terminal Manager](tapi-3-terminal-manager.md), which provides interfaces and methods used by an MSP to control terminals.</span></span>
-   <span data-ttu-id="d7d0c-112">[Подключаемые терминалы](writing-a-pluggable-terminal.md), которые позволяют приложению вместо MSP создавать терминалы.</span><span class="sxs-lookup"><span data-stu-id="d7d0c-112">[Pluggable Terminals](writing-a-pluggable-terminal.md), which allow an application instead of an MSP to create terminals.</span></span> <span data-ttu-id="d7d0c-113">Разработчики, которые уже сталкивались с написанием поставщиков услуг, будут основными авторами подключаемых терминалов.</span><span class="sxs-lookup"><span data-stu-id="d7d0c-113">Developers who are already experienced at writing service providers will be the primary creators of pluggable terminals.</span></span> <span data-ttu-id="d7d0c-114">Первоначальная версия, реализованная для этого выпуска, предназначена для серверных приложений, которым необходимо добавить клиенты, не относящиеся к Windows 2000, или многоадресные, на многосторонние конференции, получающие многоадресную рассылку многофакторной IP-рассылки.</span><span class="sxs-lookup"><span data-stu-id="d7d0c-114">The initial version implemented for this release is aimed at conferencing server applications that need to add non-Windows 2000 or non-multicast clients to TAPI 3 multi-party SDP/IP multicast conferences.</span></span>

 

 
