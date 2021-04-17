---
description: Метод Жетдвдтекстнумберофстрингс извлекает количество текстовых строк, доступных для указанного языка.
ms.assetid: 84d2b5b7-b474-48a4-9058-ea9da8109398
title: Метод Жетдвдтекстнумберофстрингс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18c9c4fadfd28d6cddc8b9013a6e426aebe9f816
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673079"
---
# <a name="getdvdtextnumberofstrings-method"></a><span data-ttu-id="21ee5-103">Метод Жетдвдтекстнумберофстрингс</span><span class="sxs-lookup"><span data-stu-id="21ee5-103">GetDVDTextNumberOfStrings Method</span></span>

> [!Note]  
> <span data-ttu-id="21ee5-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="21ee5-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="21ee5-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="21ee5-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="21ee5-106">`GetDVDTextNumberOfStrings`Метод получает количество текстовых строк, доступных для указанного языка.</span><span class="sxs-lookup"><span data-stu-id="21ee5-106">The `GetDVDTextNumberOfStrings` method retrieves the number of text strings available for the specified language.</span></span>

``` syntax
[ iStrings = ] MSWebDVD.GetDVDTextNumberOfStrings(iLangIndex)
```

## <a name="parameters"></a><span data-ttu-id="21ee5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="21ee5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21ee5-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*илангиндекс*</span><span class="sxs-lookup"><span data-stu-id="21ee5-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span></span>
</dt> <dd>

<span data-ttu-id="21ee5-109">Задает язык в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="21ee5-109">Specifies the language as an Integer.</span></span> <span data-ttu-id="21ee5-110">Значение должно находиться в диапазоне от нуля до значения, возвращенного [**жетдвдтекстнумберофлангуажес**](getdvdtextnumberoflanguages-method.md).</span><span class="sxs-lookup"><span data-stu-id="21ee5-110">The value must range from zero through one less than the value returned by [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21ee5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="21ee5-111">Return Value</span></span>

<span data-ttu-id="21ee5-112">Возвращает целочисленное значение, указывающее, сколько строк содержит диск на указанном языке.</span><span class="sxs-lookup"><span data-stu-id="21ee5-112">Returns an integer value specifying how many strings the disc contains in the specified language.</span></span>

## <a name="see-also"></a><span data-ttu-id="21ee5-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21ee5-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21ee5-114">Объект Мсвебдвд</span><span class="sxs-lookup"><span data-stu-id="21ee5-114">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> </dl>

 

 



