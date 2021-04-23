---
description: Терминал потоковой передачи мультимедиа (MST) — это динамический терминал, основанный на использовании фильтров DirectShow. Запись MSP, написанная с помощью базовых классов MSP TAPI 3, будет включать MST, но авторы MSP могут реализовать его без использования базовых классов.
ms.assetid: 21015c33-2ad1-4472-b346-167953d06a21
title: Терминал потоковой передачи мультимедиа (MST)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afb9bb4b97d0e741aec96454b187beefe2d21eb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999916"
---
# <a name="media-streaming-terminal-mst"></a><span data-ttu-id="afd1e-104">Терминал потоковой передачи мультимедиа (MST)</span><span class="sxs-lookup"><span data-stu-id="afd1e-104">Media Streaming Terminal (MST)</span></span>

<span data-ttu-id="afd1e-105">Терминал потоковой передачи мультимедиа (MST) — это динамический терминал, основанный на использовании фильтров DirectShow.</span><span class="sxs-lookup"><span data-stu-id="afd1e-105">The Media Streaming Terminal (MST) is a dynamic terminal based on use of DirectShow filters.</span></span> <span data-ttu-id="afd1e-106">Запись MSP, написанная с помощью [базовых классов MSP TAPI 3](tapi-3-msp-base-classes.md) , будет включать MST, но авторы MSP могут реализовать его без использования базовых классов.</span><span class="sxs-lookup"><span data-stu-id="afd1e-106">An MSP written using the [TAPI 3 MSP Base Classes](tapi-3-msp-base-classes.md) will incorporate an MST, but MSP authors may choose to implement it without using the base classes.</span></span>

<span data-ttu-id="afd1e-107">Чтобы вызвать создание MST, приложение выполняет вызов [**иттерминалсуппорт:: креатетерминал**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) , используя *птерминалкласс* , для которого задано значение CLSID \_ медиастреамтерминал.</span><span class="sxs-lookup"><span data-stu-id="afd1e-107">To invoke MST creation, an application makes a call to [**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) using *pTerminalClass* set to CLSID\_MediaStreamTerminal.</span></span>

<span data-ttu-id="afd1e-108">Затем интерфейсы [**итаммедиаформат**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) и [**италлокаторпропертиес**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) предоставляются в терминале, что позволяет приложению настраивать производительность потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="afd1e-108">The [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) and [**ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) interfaces are then exposed on the terminal, allowing an application to tune streaming performance.</span></span> <span data-ttu-id="afd1e-109">Эти интерфейсы объявляются в Tapi3. h.</span><span class="sxs-lookup"><span data-stu-id="afd1e-109">These interfaces are declared in Tapi3.h.</span></span>

<span data-ttu-id="afd1e-110">Для реализации и использования MST требуется знание фильтров DirectShow и управления графами фильтров.</span><span class="sxs-lookup"><span data-stu-id="afd1e-110">Implementation and use of an MST requires familiarity with DirectShow filters and filter graph management.</span></span> <span data-ttu-id="afd1e-111">Ознакомьтесь с материалами DirectShow в узле "графические и мультимедийные службы" пакета средств разработки программного обеспечения (SDK) платформы.</span><span class="sxs-lookup"><span data-stu-id="afd1e-111">Please refer to the DirectShow material under the Graphic and Multimedia Services node of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="afd1e-112">Ссылка на потоковую передачу мультимедиа будет особенно полезна для авторов MSP.</span><span class="sxs-lookup"><span data-stu-id="afd1e-112">The Multimedia Streaming Reference will be particularly useful to MSP authors.</span></span>

 

 
