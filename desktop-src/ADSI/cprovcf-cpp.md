---
title: КПРОВКФ. CPP
description: В примере компонента поставщика код фабрики класса объекта поставщика ADs находится в кпровкф. cpp.
ms.assetid: 53a4da74-3f36-4e6d-ae93-8d595680bcf3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d086cd79086f40bab6d898b844ed52fc0161bc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486569"
---
# <a name="cprovcfcpp"></a><span data-ttu-id="005a8-103">КПРОВКФ. CPP</span><span class="sxs-lookup"><span data-stu-id="005a8-103">CPROVCF.CPP</span></span>

<span data-ttu-id="005a8-104">В примере компонента поставщика код фабрики класса объекта поставщика ADs находится в кпровкф. cpp.</span><span class="sxs-lookup"><span data-stu-id="005a8-104">In the example provider component, one code example of the ADs provider object class factory code is in cprovcf.cpp.</span></span> <span data-ttu-id="005a8-105">Компонент поставщика никогда не создает экземпляр этого объекта напрямую в любое время, Кроме того, когда объект создается автоматически во время операций привязки в [**адсжетобжект**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) или во внутренней функции в методе Visual Basic **GetObject**.</span><span class="sxs-lookup"><span data-stu-id="005a8-105">The provider component never directly creates an instance of this object at any time other than when the object is created automatically during the binding operations in [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) or the internal function in the Visual Basic method **GetObject**.</span></span> <span data-ttu-id="005a8-106">Поддерживаемый метод указан в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="005a8-106">The supported method is listed in the following table.</span></span>



| <span data-ttu-id="005a8-107">Метод</span><span class="sxs-lookup"><span data-stu-id="005a8-107">Method</span></span>                                  | <span data-ttu-id="005a8-108">Описание</span><span class="sxs-lookup"><span data-stu-id="005a8-108">Description</span></span>                                                           |
|-----------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="005a8-109">**Ксампледспровидеркф:: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="005a8-109">**CSampleDSProviderCF::CreateInstance**</span></span> | <span data-ttu-id="005a8-110">Создает экземпляр фабрики класса для объекта поставщика ADS.</span><span class="sxs-lookup"><span data-stu-id="005a8-110">Creates an instance of the class factory for the ADS provider object.</span></span> |



 

 

 




