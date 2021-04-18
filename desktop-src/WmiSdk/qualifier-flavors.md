---
description: Разновидности квалификаторов предоставляют дополнительные сведения об квалификаторе, например, может ли производный класс или экземпляр переопределять исходное значение квалификаторов.
ms.assetid: 6a0769ac-e16c-45e1-92b6-26e4969bf23d
ms.tgt_platform: multiple
title: Разновидности квалификаторов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8ddf6c2daea59931e533174c532e3d07b147a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703187"
---
# <a name="qualifier-flavors"></a><span data-ttu-id="f4ec9-103">Разновидности квалификаторов</span><span class="sxs-lookup"><span data-stu-id="f4ec9-103">Qualifier Flavors</span></span>

<span data-ttu-id="f4ec9-104">Разновидности квалификаторов предоставляют дополнительные сведения об квалификаторе, например, может ли производный класс или экземпляр переопределять исходное значение квалификатора.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-104">Qualifier flavors provide more information about a qualifier, such as whether a derived class or instance can override the qualifier's original value.</span></span>

<span data-ttu-id="f4ec9-105">Флаги квалификатора можно добавить в начало MOF-файла с помощью следующего синтаксиса, что приводит к их применению во всем определении.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-105">Qualifier flavors may be added to the top of the MOF file, using the following syntax, causing them to be applied throughout the definition.</span></span> <span data-ttu-id="f4ec9-106">Пример:</span><span class="sxs-lookup"><span data-stu-id="f4ec9-106">For example:</span></span>

``` syntax
Qualifier Description : ToSubClass Amended;
```

<span data-ttu-id="f4ec9-107">**ToSubClass** и **измененные** флаги применяются ко всем квалификаторам **описания** в MOF.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-107">The **ToSubClass** and **Amended** flavors applies to all the **Description** qualifiers in the MOF.</span></span>

<span data-ttu-id="f4ec9-108">В следующей таблице перечислены разновидности квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-108">The following table lists the qualifier flavors.</span></span>



| <span data-ttu-id="f4ec9-109">Разновидность квалификатора</span><span class="sxs-lookup"><span data-stu-id="f4ec9-109">Qualifier Flavor</span></span>    | <span data-ttu-id="f4ec9-110">Значение</span><span class="sxs-lookup"><span data-stu-id="f4ec9-110">Meaning</span></span>                                                                                                                                                                                                                                         |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4ec9-111">**Измененная**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-111">**Amended**</span></span>         | <span data-ttu-id="f4ec9-112">Квалификатор не требуется в определении базового класса. Поэтому его можно переместить в изменение, которое необходимо локализовать.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-112">The qualifier is not required in the basic class definition and can be moved to the amendment to be localized.</span></span>                                                                                                                                  |
| <span data-ttu-id="f4ec9-113">**DisableOverride**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-113">**DisableOverride**</span></span> | <span data-ttu-id="f4ec9-114">Квалификатор невозможно переопределить в производном классе или экземпляре.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-114">The qualifier cannot be overridden in a derived class or instance.</span></span> <span data-ttu-id="f4ec9-115">Обратите внимание, что возможность переопределения распространенного квалификатора предоставляется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-115">Note that being able to override a propagated qualifier is the default.</span></span>                                                                                                      |
| <span data-ttu-id="f4ec9-116">**енаблеоверриде**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-116">**EnableOverride**</span></span>  | <span data-ttu-id="f4ec9-117">При распространении на производный класс или экземпляр значение квалификатора может быть переопределено.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-117">When propagated to a derived class or instance, the value of the qualifier can be overridden.</span></span> <span data-ttu-id="f4ec9-118">Установка **енаблеоверриде** необязательна, так как возможность переопределения значения квалификатора является функцией по умолчанию для распространяемых квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-118">Setting **EnableOverride** is optional because being able to override the qualifier value is the default functionality for propagated qualifiers.</span></span> |
| <span data-ttu-id="f4ec9-119">**ноттоинстанце**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-119">**NotToInstance**</span></span>   | <span data-ttu-id="f4ec9-120">Квалификатор не распространяется на экземпляры класса.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-120">The qualifier is not propagated to class instances.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="f4ec9-121">**ноттосубкласс**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-121">**NotToSubClass**</span></span>   | <span data-ttu-id="f4ec9-122">Квалификатор не распространяется в производные классы.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-122">The qualifier is not propagated to derived classes.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="f4ec9-123">**Ограниченный**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-123">**Restricted**</span></span>      | <span data-ttu-id="f4ec9-124">Квалификатор не распространяется на экземпляры или производные классы.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-124">The qualifier is not propagated to instances or derived classes.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="f4ec9-125">**тоинстанце**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-125">**ToInstance**</span></span>      | <span data-ttu-id="f4ec9-126">Квалификатор распространяется в экземпляры.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-126">The qualifier is propagated to instances.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="f4ec9-127">**ToSubClass**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-127">**ToSubClass**</span></span>      | <span data-ttu-id="f4ec9-128">Квалификатор распространяется на производные классы.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-128">The qualifier is propagated to derived classes.</span></span> <span data-ttu-id="f4ec9-129">Эта разновидность подходит только для квалификаторов, определенных для класса, и не может быть присоединена к квалификатору, описывающему экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-129">This flavor is only appropriate for qualifiers defined for a class and cannot be attached to a qualifier describing a class instance.</span></span>                                                           |



 

 

 



