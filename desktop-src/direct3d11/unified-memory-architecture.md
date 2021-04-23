---
title: Архитектура единой памяти
description: Запрос на то, поддерживает ли архитектура унифицированной памяти (верхнюю память), может помочь определить способ обработки некоторых ресурсов.
ms.assetid: E43892F9-E7CD-4D18-BDDE-3C4F03F8F4EA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99baeab51838b9b3382884a681ec9b579fa700a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986227"
---
# <a name="unified-memory-architecture"></a><span data-ttu-id="b83ac-103">Архитектура единой памяти</span><span class="sxs-lookup"><span data-stu-id="b83ac-103">Unified Memory Architecture</span></span>

<span data-ttu-id="b83ac-104">Запрос на то, поддерживает ли архитектура унифицированной памяти (верхнюю память), может помочь определить способ обработки некоторых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b83ac-104">Querying for whether Unified Memory Architecture (UMA) is supported can help determine how to handle some resources.</span></span>

<span data-ttu-id="b83ac-105">Логическое значение, заданное драйвером, может быть считано из структуры [**D3D11 \_ \_ Data \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) , чтобы определить, поддерживает ли оборудование верхнюю область.</span><span class="sxs-lookup"><span data-stu-id="b83ac-105">A boolean, set by the driver, can be read from the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) structure to determine if the hardware supports UMA.</span></span>

<span data-ttu-id="b83ac-106">В приложениях, работающих в самой операционной системе, может потребоваться больше ресурсов с включенным доступом к ЦП, чем если он недоступен.</span><span class="sxs-lookup"><span data-stu-id="b83ac-106">Applications running on UMA may want to have more resources with CPU access enabled than if it is not available.</span></span> <span data-ttu-id="b83ac-107">Область памяти позволяет приложениям избегать копирования данных ресурсов, а не только эффективно для графических адаптеров, не использующих верхнюю часть.</span><span class="sxs-lookup"><span data-stu-id="b83ac-107">UMA enables applications to avoiding copying resource data around, instead of staying efficient solely for non-UMA graphics adapters.</span></span> [<span data-ttu-id="b83ac-108">Функции Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="b83ac-108">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)

## <a name="related-topics"></a><span data-ttu-id="b83ac-109">См. также</span><span class="sxs-lookup"><span data-stu-id="b83ac-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b83ac-110">Функции Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="b83ac-110">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> </dl>

 

 




