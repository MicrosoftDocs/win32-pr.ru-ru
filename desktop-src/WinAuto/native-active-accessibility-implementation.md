---
title: Реализация собственного Active Accessibility
description: Говорят, что элементы пользовательского интерфейса, реализующие интерфейс IAccessible, предоставляют собственную реализацию.
ms.assetid: 36a5c0cd-53f0-433e-8932-da7d1de177dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5f6e6b6152c2f5e5c41a6a2b7cd3f84a3fce373
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700569"
---
# <a name="native-active-accessibility-implementation"></a><span data-ttu-id="688a4-103">Реализация собственного Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="688a4-103">Native Active Accessibility Implementation</span></span>

<span data-ttu-id="688a4-104">Говорят, что элементы пользовательского интерфейса, реализующие интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , предоставляют *собственную реализацию*.</span><span class="sxs-lookup"><span data-stu-id="688a4-104">User interface elements that implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface are said to provide a *native implementation*.</span></span> <span data-ttu-id="688a4-105">Несмотря на то, что затраты на разработку для реализации **IAccessible** (или любого другого интерфейса COM) могут быть высокими, преимущество является исчерпывающим элементом управления информацией, предоставляемой клиентам.</span><span class="sxs-lookup"><span data-stu-id="688a4-105">Although the development cost for implementing **IAccessible** (or any other Component Object Model (COM) interface) can be high, the benefit is complete control over the information exposed to clients.</span></span>

<span data-ttu-id="688a4-106">Если приложение использует настраиваемые элементы управления или другие элементы управления, которые не могут быть переданы с помощью Oleacc.dll, необходимо предоставить собственную реализацию.</span><span class="sxs-lookup"><span data-stu-id="688a4-106">If your application uses custom controls or other controls that cannot be proxied by Oleacc.dll, you will need to provide a native implementation.</span></span>

 

 




