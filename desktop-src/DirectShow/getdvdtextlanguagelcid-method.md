---
description: Метод ЖетдвдтекстлангуажелЦид извлекает код локали (LCID) для указанного блока текстовой строки.
ms.assetid: feaa1db8-2d33-4c32-8491-f3aa5555e3d3
title: Метод ЖетдвдтекстлангуажелЦид
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66d21b9870982b605d9deeb1e22882a525c5616
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536626"
---
# <a name="getdvdtextlanguagelcid-method"></a><span data-ttu-id="60f97-103">Метод ЖетдвдтекстлангуажелЦид</span><span class="sxs-lookup"><span data-stu-id="60f97-103">GetDVDTextLanguageLCID Method</span></span>

> [!Note]  
> <span data-ttu-id="60f97-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="60f97-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="60f97-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="60f97-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="60f97-106">`GetDVDTextLanguageLCID`Метод получает код локали (LCID) для указанного блока текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="60f97-106">The `GetDVDTextLanguageLCID` method retrieves the locale identifier (LCID) for the specified text string block.</span></span>

``` syntax
[ iLCID = ] MSWebDVD.GetDVDTextLanguageLCID(iLangIndex)
```

## <a name="parameters"></a><span data-ttu-id="60f97-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="60f97-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60f97-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*илангиндекс*</span><span class="sxs-lookup"><span data-stu-id="60f97-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span></span>
</dt> <dd>

<span data-ttu-id="60f97-109">Задает языковой блок текста на диске в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="60f97-109">Specifies the text language block on the disc as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60f97-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60f97-110">Return Value</span></span>

<span data-ttu-id="60f97-111">Возвращает значение LCID, содержащее сведения, указывающие язык, на котором написаны строки.</span><span class="sxs-lookup"><span data-stu-id="60f97-111">Returns an LCID value that contains information specifying the language the strings are written in.</span></span>

## <a name="remarks"></a><span data-ttu-id="60f97-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="60f97-112">Remarks</span></span>

<span data-ttu-id="60f97-113">Дополнительные текстовые строки хранятся в смежных блоках на диске. Каждый язык имеет один блок строк.</span><span class="sxs-lookup"><span data-stu-id="60f97-113">Supplemental text strings are stored in contiguous blocks on the disc. Each language has one block of strings.</span></span> <span data-ttu-id="60f97-114">Приложение задает эти блоки по индексу, который должен быть меньше значения, возвращаемого функцией [**жетдвдтекстнумберофлангуажес**](getdvdtextnumberoflanguages-method.md).</span><span class="sxs-lookup"><span data-stu-id="60f97-114">An application specifies these blocks by an index, which must be less than the value returned by [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="60f97-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60f97-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60f97-116">Объект Мсвебдвд</span><span class="sxs-lookup"><span data-stu-id="60f97-116">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> <dt>

[<span data-ttu-id="60f97-117">**жетлангфромлангид**</span><span class="sxs-lookup"><span data-stu-id="60f97-117">**GetLangFromLangID**</span></span>](getlangfromlangid-method.md)
</dt> </dl>

 

 



