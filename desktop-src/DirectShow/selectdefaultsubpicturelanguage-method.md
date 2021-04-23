---
description: Метод Селектдефаултсубпиктурелангуаже задает текущий язык подизображения по умолчанию в объекте Мсвебдвд.
ms.assetid: e83980d1-c7cd-4755-9a27-3b0c2548009e
title: Метод Селектдефаултсубпиктурелангуаже
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d7dd4d66ae9d0580bf863ede9fff1e51d373e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805836"
---
# <a name="selectdefaultsubpicturelanguage-method"></a><span data-ttu-id="50d7c-103">Метод Селектдефаултсубпиктурелангуаже</span><span class="sxs-lookup"><span data-stu-id="50d7c-103">SelectDefaultSubpictureLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="50d7c-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="50d7c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="50d7c-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="50d7c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="50d7c-106">`SelectDefaultSubpictureLanguage`Метод задает текущий язык подизображения по умолчанию в объекте **мсвебдвд** .</span><span class="sxs-lookup"><span data-stu-id="50d7c-106">The `SelectDefaultSubpictureLanguage` method sets the current default subpicture language in the **MSWebDVD** object.</span></span>

``` syntax
MSWebDVD.SelectDefaultSubpictureLanguage(iLang,iExt)
```

## <a name="parameters"></a><span data-ttu-id="50d7c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="50d7c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50d7c-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*иланг*</span><span class="sxs-lookup"><span data-stu-id="50d7c-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span></span>
</dt> <dd>

<span data-ttu-id="50d7c-109">Задает язык в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="50d7c-109">Specifies the language as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="50d7c-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*иекст*</span><span class="sxs-lookup"><span data-stu-id="50d7c-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span></span>
</dt> <dd>

<span data-ttu-id="50d7c-111">Задает расширение языка субтитров в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="50d7c-111">Specifies the subpicture language extension as an Integer.</span></span>



| <span data-ttu-id="50d7c-112">Значение</span><span class="sxs-lookup"><span data-stu-id="50d7c-112">Value</span></span> | <span data-ttu-id="50d7c-113">Описание</span><span class="sxs-lookup"><span data-stu-id="50d7c-113">Description</span></span>                    |
|-------|--------------------------------|
| <span data-ttu-id="50d7c-114">0</span><span class="sxs-lookup"><span data-stu-id="50d7c-114">0</span></span>     | <span data-ttu-id="50d7c-115">Расширение не указано</span><span class="sxs-lookup"><span data-stu-id="50d7c-115">Extension Not Specified</span></span>        |
| <span data-ttu-id="50d7c-116">1</span><span class="sxs-lookup"><span data-stu-id="50d7c-116">1</span></span>     | <span data-ttu-id="50d7c-117">Обычные субтитры</span><span class="sxs-lookup"><span data-stu-id="50d7c-117">Normal Captions</span></span>                |
| <span data-ttu-id="50d7c-118">2</span><span class="sxs-lookup"><span data-stu-id="50d7c-118">2</span></span>     | <span data-ttu-id="50d7c-119">Крупные субтитры</span><span class="sxs-lookup"><span data-stu-id="50d7c-119">Big Captions</span></span>                   |
| <span data-ttu-id="50d7c-120">3</span><span class="sxs-lookup"><span data-stu-id="50d7c-120">3</span></span>     | <span data-ttu-id="50d7c-121">Субтитры детей</span><span class="sxs-lookup"><span data-stu-id="50d7c-121">Children's Captions</span></span>            |
| <span data-ttu-id="50d7c-122">5</span><span class="sxs-lookup"><span data-stu-id="50d7c-122">5</span></span>     | <span data-ttu-id="50d7c-123">Обычные закрытые субтитры</span><span class="sxs-lookup"><span data-stu-id="50d7c-123">Normal Closed Captions</span></span>         |
| <span data-ttu-id="50d7c-124">6</span><span class="sxs-lookup"><span data-stu-id="50d7c-124">6</span></span>     | <span data-ttu-id="50d7c-125">Большие закрытые субтитры</span><span class="sxs-lookup"><span data-stu-id="50d7c-125">Big Closed Captions</span></span>            |
| <span data-ttu-id="50d7c-126">7</span><span class="sxs-lookup"><span data-stu-id="50d7c-126">7</span></span>     | <span data-ttu-id="50d7c-127">Закрытые субтитры детей</span><span class="sxs-lookup"><span data-stu-id="50d7c-127">Children's Closed Captions</span></span>     |
| <span data-ttu-id="50d7c-128">9</span><span class="sxs-lookup"><span data-stu-id="50d7c-128">9</span></span>     | <span data-ttu-id="50d7c-129">Принудительно</span><span class="sxs-lookup"><span data-stu-id="50d7c-129">Forced</span></span>                         |
| <span data-ttu-id="50d7c-130">13</span><span class="sxs-lookup"><span data-stu-id="50d7c-130">13</span></span>    | <span data-ttu-id="50d7c-131">Обычные комментарии режиссера</span><span class="sxs-lookup"><span data-stu-id="50d7c-131">Normal Director's Comments</span></span>     |
| <span data-ttu-id="50d7c-132">14</span><span class="sxs-lookup"><span data-stu-id="50d7c-132">14</span></span>    | <span data-ttu-id="50d7c-133">Комментарии для крупного директора</span><span class="sxs-lookup"><span data-stu-id="50d7c-133">Big Director's Comments</span></span>        |
| <span data-ttu-id="50d7c-134">15</span><span class="sxs-lookup"><span data-stu-id="50d7c-134">15</span></span>    | <span data-ttu-id="50d7c-135">Комментарии Директор'с детей</span><span class="sxs-lookup"><span data-stu-id="50d7c-135">Children's Director's Comments</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50d7c-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50d7c-136">Return Value</span></span>

<span data-ttu-id="50d7c-137">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="50d7c-137">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50d7c-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50d7c-138">Remarks</span></span>

<span data-ttu-id="50d7c-139">Расширение языка субтитров предоставляет дополнительные сведения о подизображении.</span><span class="sxs-lookup"><span data-stu-id="50d7c-139">The subpicture language extension provides further information about the subpicture.</span></span>

 

 



