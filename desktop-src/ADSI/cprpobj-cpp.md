---
title: КПРПОБЖ. CPP
description: В примере компонента поставщика методы объекта свойства в кпрпобж. cpp перечислены в следующей таблице.
ms.assetid: 88628b9b-12e6-4d64-9a21-b30f7392a5f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 948409cc135daaffa249f8aa0b3729b34799957c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252762"
---
# <a name="cprpobjcpp"></a><span data-ttu-id="16cf4-103">КПРПОБЖ. CPP</span><span class="sxs-lookup"><span data-stu-id="16cf4-103">CPRPOBJ.CPP</span></span>

<span data-ttu-id="16cf4-104">В примере компонента поставщика методы объекта свойства в кпрпобж. cpp перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="16cf4-104">In the example provider component, property object methods, in cprpobj.cpp, are listed in the following table.</span></span>



| <span data-ttu-id="16cf4-105">Метод</span><span class="sxs-lookup"><span data-stu-id="16cf4-105">Method</span></span>                                                 | <span data-ttu-id="16cf4-106">Описание</span><span class="sxs-lookup"><span data-stu-id="16cf4-106">Description</span></span>                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16cf4-107">**Ксампледспроперти:: Ксампледспроперти**</span><span class="sxs-lookup"><span data-stu-id="16cf4-107">**CSampleDSProperty::CSampleDSProperty**</span></span>               | <span data-ttu-id="16cf4-108">Стандартный конструктор.</span><span class="sxs-lookup"><span data-stu-id="16cf4-108">Standard constructor.</span></span>                                                                                                                          |
| <span data-ttu-id="16cf4-109">**Ксампледспроперти:: ~ Ксампледспроперти**</span><span class="sxs-lookup"><span data-stu-id="16cf4-109">**CSampleDSProperty::~CSampleDSProperty**</span></span>              | <span data-ttu-id="16cf4-110">Стандартный деструктор.</span><span class="sxs-lookup"><span data-stu-id="16cf4-110">Standard destructor.</span></span>                                                                                                                           |
| <span data-ttu-id="16cf4-111">**Ксампледспроперти:: CreateProperty**</span><span class="sxs-lookup"><span data-stu-id="16cf4-111">**CSampleDSProperty::CreateProperty**</span></span>                  | <span data-ttu-id="16cf4-112">Создайте объект свойства ADS, выполнив поиск определений атрибутов, вызвав **сампледсжетпропертидефинитион**.</span><span class="sxs-lookup"><span data-stu-id="16cf4-112">Create an ADS Property object, looking up the attribute definitions by calling **SampleDSGetPropertyDefinition**.</span></span>                              |
| <span data-ttu-id="16cf4-113">**Ксампледспроперти:: CreateProperty**</span><span class="sxs-lookup"><span data-stu-id="16cf4-113">**CSampleDSProperty::CreateProperty**</span></span>                  | <span data-ttu-id="16cf4-114">При наличии определения атрибута создайте объект Property, установив соответствие между поддерживаемыми синтаксисами объявлений и синтаксисом поставщика.</span><span class="sxs-lookup"><span data-stu-id="16cf4-114">Given the attribute definition, create a property object, setting the correspondence between supported ADS syntaxes and the provider syntaxes.</span></span> |
| <span data-ttu-id="16cf4-115">**Ксампледспроперти:: Аллокатепропертйобжект**</span><span class="sxs-lookup"><span data-stu-id="16cf4-115">**CSampleDSProperty::AllocatePropertyObject**</span></span>          | <span data-ttu-id="16cf4-116">Создайте объект Property и загрузите его данные типа.</span><span class="sxs-lookup"><span data-stu-id="16cf4-116">Create a property object and load its type data.</span></span>                                                                                               |
| <span data-ttu-id="16cf4-117">**Ксампледспроперти:: QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="16cf4-117">**CSampleDSProperty::QueryInterface**</span></span>                  | <span data-ttu-id="16cf4-118">Возвращает запрошенный указатель интерфейса, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="16cf4-118">Return the requested interface pointer, if available.</span></span>                                                                                          |
| <span data-ttu-id="16cf4-119">Стандартные методы [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="16cf4-119">Standard [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) methods.</span></span>                 |                                                                                                                                                |
| <span data-ttu-id="16cf4-120">Стандартные методы [**иадспроперти**](/windows/desktop/api/Iads/nn-iads-iadsproperty) .</span><span class="sxs-lookup"><span data-stu-id="16cf4-120">Standard [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) methods.</span></span> |                                                                                                                                                |
| <span data-ttu-id="16cf4-121">**мапсинтаксидтоадссинтакс**</span><span class="sxs-lookup"><span data-stu-id="16cf4-121">**MapSyntaxIdtoADsSyntax**</span></span>                             | <span data-ttu-id="16cf4-122">Установите соответствие между ИДЕНТИФИКАТОРом синтаксиса и синтаксисом объявлений.</span><span class="sxs-lookup"><span data-stu-id="16cf4-122">Set the correspondence between the syntax ID and the ADS syntax.</span></span>                                                                               |
| <span data-ttu-id="16cf4-123">**мапсинтаксидтосампледссинтакс**</span><span class="sxs-lookup"><span data-stu-id="16cf4-123">**MapSyntaxIdtoSampleDSSyntax**</span></span>                        | <span data-ttu-id="16cf4-124">Установите соответствие между ИДЕНТИФИКАТОРом синтаксиса и синтаксисом поставщика.</span><span class="sxs-lookup"><span data-stu-id="16cf4-124">Set the correspondence between the syntax ID and the provider syntax.</span></span>                                                                          |



 

 

 




