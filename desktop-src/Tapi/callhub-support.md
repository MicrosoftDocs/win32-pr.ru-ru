---
description: Отслеживание Каллхуб — это новая функция в интерфейсе TAPI версии 3,0.
ms.assetid: 29b6e585-6da8-46a2-a612-f42d0f65f68e
title: Поддержка Каллхуб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efe6891cfdad956a87745f8e4b35dd117fe775e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674025"
---
# <a name="callhub-support"></a><span data-ttu-id="4c0ee-103">Поддержка Каллхуб</span><span class="sxs-lookup"><span data-stu-id="4c0ee-103">CallHub Support</span></span>

<span data-ttu-id="4c0ee-104">Отслеживание Каллхуб — это новая функция в интерфейсе TAPI версии 3,0.</span><span class="sxs-lookup"><span data-stu-id="4c0ee-104">CallHub tracking is a new feature in TAPI version 3.0.</span></span> <span data-ttu-id="4c0ee-105">Функции Каллхуб были добавлены в элементы программирования TAPI 2,1 с доставкой Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4c0ee-105">CallHub functionality was added to the TAPI 2.1 programming elements with the delivery of Windows 2000.</span></span> <span data-ttu-id="4c0ee-106">*Каллхуб* представляет собой стороннее представление вызова, а дескрипторы вызовов TAPI представляют первое представление вызова.</span><span class="sxs-lookup"><span data-stu-id="4c0ee-106">A *CallHub* represents a third-party view of a call, and TAPI's call handles represent the first-party view of a call.</span></span> <span data-ttu-id="4c0ee-107">С помощью отслеживания Каллхуб поставщик услуг должен следовать за Каллхубс и предоставлять сведения о вызове в течение времени существования Каллхуб.</span><span class="sxs-lookup"><span data-stu-id="4c0ee-107">With CallHub tracking, the service provider is requested to follow CallHubs and give information about the call during the lifetime of a CallHub.</span></span> <span data-ttu-id="4c0ee-108">По мере того, как новые стороны присоединяются и оставляют Каллхуб, поставщик услуг должен сообщить о TAPI.</span><span class="sxs-lookup"><span data-stu-id="4c0ee-108">As new parties join and leave the CallHub, the service provider should inform TAPI.</span></span>

<span data-ttu-id="4c0ee-109">Поставщику услуг не требуется реализовывать новые функции для поддержки Каллхуб.</span><span class="sxs-lookup"><span data-stu-id="4c0ee-109">A service provider does not need to implement any new functions in order to support CallHub.</span></span> <span data-ttu-id="4c0ee-110">Он просто должен заполнить элемент **двкаллид** структуры [**линекаллинфо**](/windows/win32/api/tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="4c0ee-110">It simply needs to fill in the **dwCallID** member of the [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="4c0ee-111">В TAPI 3 TAPI собирает все вызовы с одним и тем же **двкаллид** и создает обработчик каллхуб, который приложение может использовать для наблюдения за вызовом.</span><span class="sxs-lookup"><span data-stu-id="4c0ee-111">In TAPI 3, TAPI collects all calls with the same **dwCallID** and creates a CallHub handle that the application can use to track the call.</span></span>

 

 
