---
description: Метод Селектдефаултаудиолангуаже задает текущий звуковой язык по умолчанию в объекте Мсвебдвд.
ms.assetid: 7d63b7ef-2b03-4929-822a-c4d11fb7a825
title: Метод Селектдефаултаудиолангуаже
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 126de6daf4f5e0337058495a3ee7898594bfd704
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537109"
---
# <a name="selectdefaultaudiolanguage-method"></a><span data-ttu-id="82d56-103">Метод Селектдефаултаудиолангуаже</span><span class="sxs-lookup"><span data-stu-id="82d56-103">SelectDefaultAudioLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="82d56-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="82d56-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="82d56-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="82d56-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="82d56-106">`SelectDefaultAudioLanguage`Метод задает текущий звуковой язык по умолчанию в объекте мсвебдвд.</span><span class="sxs-lookup"><span data-stu-id="82d56-106">The `SelectDefaultAudioLanguage` method sets the current default audio language in the MSWebDVD object.</span></span>

``` syntax
MSWebDVD.SelectDefaultAudioLanguage(iLang, iExt)
```

## <a name="parameters"></a><span data-ttu-id="82d56-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="82d56-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82d56-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*иланг*</span><span class="sxs-lookup"><span data-stu-id="82d56-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span></span>
</dt> <dd>

<span data-ttu-id="82d56-109">Задает язык в виде целочисленного значения LCID.</span><span class="sxs-lookup"><span data-stu-id="82d56-109">Specifies the language as an Integer LCID value.</span></span>

</dd> <dt>

<span data-ttu-id="82d56-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*иекст*</span><span class="sxs-lookup"><span data-stu-id="82d56-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span></span>
</dt> <dd>

<span data-ttu-id="82d56-111">Указывает расширение языка DVD-звука в виде целого значения.</span><span class="sxs-lookup"><span data-stu-id="82d56-111">Specifies the DVD audio language extension as an integer value.</span></span>



| <span data-ttu-id="82d56-112">Значение</span><span class="sxs-lookup"><span data-stu-id="82d56-112">Value</span></span> | <span data-ttu-id="82d56-113">Описание</span><span class="sxs-lookup"><span data-stu-id="82d56-113">Description</span></span>       |
|-------|-------------------|
| <span data-ttu-id="82d56-114">0</span><span class="sxs-lookup"><span data-stu-id="82d56-114">0</span></span>     | <span data-ttu-id="82d56-115">NotSpecified</span><span class="sxs-lookup"><span data-stu-id="82d56-115">NotSpecified</span></span>      |
| <span data-ttu-id="82d56-116">1</span><span class="sxs-lookup"><span data-stu-id="82d56-116">1</span></span>     | <span data-ttu-id="82d56-117">Субтитры</span><span class="sxs-lookup"><span data-stu-id="82d56-117">Captions</span></span>          |
| <span data-ttu-id="82d56-118">2</span><span class="sxs-lookup"><span data-stu-id="82d56-118">2</span></span>     | <span data-ttu-id="82d56-119">висуаллимпаиред</span><span class="sxs-lookup"><span data-stu-id="82d56-119">VisuallyImpaired</span></span>  |
| <span data-ttu-id="82d56-120">3</span><span class="sxs-lookup"><span data-stu-id="82d56-120">3</span></span>     | <span data-ttu-id="82d56-121">DirectorComments1</span><span class="sxs-lookup"><span data-stu-id="82d56-121">DirectorComments1</span></span> |
| <span data-ttu-id="82d56-122">4</span><span class="sxs-lookup"><span data-stu-id="82d56-122">4</span></span>     | <span data-ttu-id="82d56-123">DirectorComments2</span><span class="sxs-lookup"><span data-stu-id="82d56-123">DirectorComments2</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82d56-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82d56-124">Return Value</span></span>

<span data-ttu-id="82d56-125">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="82d56-125">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="82d56-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82d56-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d56-127">Объект Мсвебдвд</span><span class="sxs-lookup"><span data-stu-id="82d56-127">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> </dl>

 

 



