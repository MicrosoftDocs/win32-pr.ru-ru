---
description: Свойство Дефаултсубпиктурелангуажеекст извлекает расширение языка по умолчанию для подаватара DVD.
ms.assetid: bd437844-6e5c-4237-a968-700a53e18635
title: Дефаултсубпиктурелангуажеекст, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37bba455a26df4eaa6676b77447c3faed408609
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536713"
---
# <a name="defaultsubpicturelanguageext-property"></a><span data-ttu-id="beb27-103">Дефаултсубпиктурелангуажеекст, свойство</span><span class="sxs-lookup"><span data-stu-id="beb27-103">DefaultSubpictureLanguageExt Property</span></span>

> [!Note]  
> <span data-ttu-id="beb27-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="beb27-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="beb27-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="beb27-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="beb27-106">`DefaultSubpictureLanguageExt`Свойство получает расширение языка по умолчанию для изображений DVD.</span><span class="sxs-lookup"><span data-stu-id="beb27-106">The `DefaultSubpictureLanguageExt` property retrieves the default DVD subpicture language extension.</span></span>

``` syntax
[ iLangExt = ] MSWebDVD.DefaultSubpictureLanguageExt
```

## <a name="return-value"></a><span data-ttu-id="beb27-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="beb27-107">Return Value</span></span>

<span data-ttu-id="beb27-108">Возвращает целочисленное значение, указывающее на расширение языка DVD с подизображением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="beb27-108">Returns an Integer value indicating the default DVD subpicture language extension.</span></span>

## <a name="remarks"></a><span data-ttu-id="beb27-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="beb27-109">Remarks</span></span>

<span data-ttu-id="beb27-110">Это свойство доступно только для чтения и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="beb27-110">This property is read-only with no default value.</span></span> <span data-ttu-id="beb27-111">В следующей таблице приводятся возможные значения.</span><span class="sxs-lookup"><span data-stu-id="beb27-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="beb27-112">Значение</span><span class="sxs-lookup"><span data-stu-id="beb27-112">Value</span></span> | <span data-ttu-id="beb27-113">Описание</span><span class="sxs-lookup"><span data-stu-id="beb27-113">Description</span></span>                    |
|-------|--------------------------------|
| <span data-ttu-id="beb27-114">0</span><span class="sxs-lookup"><span data-stu-id="beb27-114">0</span></span>     | <span data-ttu-id="beb27-115">Расширение не указано</span><span class="sxs-lookup"><span data-stu-id="beb27-115">Extension Not Specified</span></span>        |
| <span data-ttu-id="beb27-116">1</span><span class="sxs-lookup"><span data-stu-id="beb27-116">1</span></span>     | <span data-ttu-id="beb27-117">Обычные субтитры</span><span class="sxs-lookup"><span data-stu-id="beb27-117">Normal Captions</span></span>                |
| <span data-ttu-id="beb27-118">2</span><span class="sxs-lookup"><span data-stu-id="beb27-118">2</span></span>     | <span data-ttu-id="beb27-119">Крупные субтитры</span><span class="sxs-lookup"><span data-stu-id="beb27-119">Big Captions</span></span>                   |
| <span data-ttu-id="beb27-120">3</span><span class="sxs-lookup"><span data-stu-id="beb27-120">3</span></span>     | <span data-ttu-id="beb27-121">Субтитры детей</span><span class="sxs-lookup"><span data-stu-id="beb27-121">Children's Captions</span></span>            |
| <span data-ttu-id="beb27-122">5</span><span class="sxs-lookup"><span data-stu-id="beb27-122">5</span></span>     | <span data-ttu-id="beb27-123">Обычные закрытые субтитры</span><span class="sxs-lookup"><span data-stu-id="beb27-123">Normal Closed Captions</span></span>         |
| <span data-ttu-id="beb27-124">6</span><span class="sxs-lookup"><span data-stu-id="beb27-124">6</span></span>     | <span data-ttu-id="beb27-125">Большие закрытые субтитры</span><span class="sxs-lookup"><span data-stu-id="beb27-125">Big Closed Captions</span></span>            |
| <span data-ttu-id="beb27-126">7</span><span class="sxs-lookup"><span data-stu-id="beb27-126">7</span></span>     | <span data-ttu-id="beb27-127">Закрытые субтитры детей</span><span class="sxs-lookup"><span data-stu-id="beb27-127">Children's Closed Captions</span></span>     |
| <span data-ttu-id="beb27-128">9</span><span class="sxs-lookup"><span data-stu-id="beb27-128">9</span></span>     | <span data-ttu-id="beb27-129">Принудительно</span><span class="sxs-lookup"><span data-stu-id="beb27-129">Forced</span></span>                         |
| <span data-ttu-id="beb27-130">13</span><span class="sxs-lookup"><span data-stu-id="beb27-130">13</span></span>    | <span data-ttu-id="beb27-131">Обычные комментарии режиссера</span><span class="sxs-lookup"><span data-stu-id="beb27-131">Normal Director's Comments</span></span>     |
| <span data-ttu-id="beb27-132">14</span><span class="sxs-lookup"><span data-stu-id="beb27-132">14</span></span>    | <span data-ttu-id="beb27-133">Комментарии для крупного директора</span><span class="sxs-lookup"><span data-stu-id="beb27-133">Big Director's Comments</span></span>        |
| <span data-ttu-id="beb27-134">15</span><span class="sxs-lookup"><span data-stu-id="beb27-134">15</span></span>    | <span data-ttu-id="beb27-135">Комментарии Директор'с детей</span><span class="sxs-lookup"><span data-stu-id="beb27-135">Children's Director's Comments</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="beb27-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="beb27-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb27-137">**селектдефаултсубпиктурелангуаже**</span><span class="sxs-lookup"><span data-stu-id="beb27-137">**SelectDefaultSubpictureLanguage**</span></span>](selectdefaultsubpicturelanguage-method.md)
</dt> </dl>

 

 



