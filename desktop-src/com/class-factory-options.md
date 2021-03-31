---
title: Параметры фабрики класса
description: Параметры фабрики класса
ms.assetid: e9e33e07-7628-4c5e-965d-e12a9c1d69c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fab52ea11a0e7e20d10757eb8d6e86577afc35c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793974"
---
# <a name="class-factory-options"></a><span data-ttu-id="99a3a-103">Параметры фабрики класса</span><span class="sxs-lookup"><span data-stu-id="99a3a-103">Class Factory Options</span></span>

<span data-ttu-id="99a3a-104">Элемент управления ActiveX, который является COM-объектом, должен иметь связанный серверный код, поддерживающий создание элементов управления через [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) как минимум.</span><span class="sxs-lookup"><span data-stu-id="99a3a-104">An ActiveX Control, by virtue of being a COM object, must have associated server code that supports control creation through [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) as a minimum.</span></span>

<span data-ttu-id="99a3a-105">Это необязательно, а не обязательно, что этот объект класса также поддерживает [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) для управления лицензированием.</span><span class="sxs-lookup"><span data-stu-id="99a3a-105">It is optional, not required, that this class object also support [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) for licensing management.</span></span> <span data-ttu-id="99a3a-106">Только те поставщики, которые интересуются лицензией, должны поддерживать механизм лицензирования COM.</span><span class="sxs-lookup"><span data-stu-id="99a3a-106">Only those vendors that are concerned about licensing need to support COM's licensing mechanism.</span></span> <span data-ttu-id="99a3a-107">Иными словами, поскольку **IClassFactory2** является единственным способом обеспечения лицензирования на уровне com, этот интерфейс необходим для объекта класса для тех элементов управления, которые должны быть лицензированы.</span><span class="sxs-lookup"><span data-stu-id="99a3a-107">In other words, because **IClassFactory2** is the only way to achieve COM-level licensing, this interface is required on the class object for those controls that want to be licensed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99a3a-108">См. также</span><span class="sxs-lookup"><span data-stu-id="99a3a-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99a3a-109">Элементы управления</span><span class="sxs-lookup"><span data-stu-id="99a3a-109">Controls</span></span>](controls.md)
</dt> </dl>

 

 