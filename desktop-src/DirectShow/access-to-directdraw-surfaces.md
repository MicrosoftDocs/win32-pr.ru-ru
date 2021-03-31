---
description: Доступ к областям DirectDraw
ms.assetid: 21002c9f-8b8b-49f3-9ea3-3703780e3412
title: Доступ к областям DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac1acdd122fa7d21fd49868c45f065f59b06ad8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103895097"
---
# <a name="access-to-directdraw-surfaces"></a><span data-ttu-id="bef72-103">Доступ к областям DirectDraw</span><span class="sxs-lookup"><span data-stu-id="bef72-103">Access to DirectDraw Surfaces</span></span>

<span data-ttu-id="bef72-104">Образцы объектов мультимедиа, предоставляемые VMR для вышестоящего фильтра, поддерживают интерфейс [**ивмрсурфаце**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) .</span><span class="sxs-lookup"><span data-stu-id="bef72-104">The Media Sample objects provided by the VMR to upstream filters support the [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) interface.</span></span> <span data-ttu-id="bef72-105">Чтобы получить интерфейс, вызовите QueryInterface в интерфейсе [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) и укажите IID \_ ивмрсурфаце.</span><span class="sxs-lookup"><span data-stu-id="bef72-105">To obtain the interface, call QueryInterface on the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface and specify IID\_IVMRSurface.</span></span> <span data-ttu-id="bef72-106">Вышестоящий фильтр может использовать методы Ивмрсурфаце для доступа к поверхности, созданной с помощью VMR, и управления ей.</span><span class="sxs-lookup"><span data-stu-id="bef72-106">Upstream filters can then use the IVMRSurface methods to access and manipulate the surface that has been created by the VMR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bef72-107">См. также</span><span class="sxs-lookup"><span data-stu-id="bef72-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bef72-108">Использование VMR для разработчиков фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="bef72-108">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



