---
description: Метод Жеттитлепаренталлевелс извлекает уровни родительского управления для указанного заголовка.
ms.assetid: 076808d7-6cb6-4d81-b26d-c7945db298f2
title: Метод Жеттитлепаренталлевелс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6db82ca21c2fdd023aa472e4c3428260464a8612
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416705"
---
# <a name="gettitleparentallevels-method"></a><span data-ttu-id="8bea5-103">Метод Жеттитлепаренталлевелс</span><span class="sxs-lookup"><span data-stu-id="8bea5-103">GetTitleParentalLevels Method</span></span>

> [!Note]  
> <span data-ttu-id="8bea5-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8bea5-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="8bea5-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="8bea5-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="8bea5-106">`GetTitleParentalLevels`Метод получает уровни родительского управления для указанного заголовка.</span><span class="sxs-lookup"><span data-stu-id="8bea5-106">The `GetTitleParentalLevels` method retrieves the parental management levels for the specified title.</span></span>

``` syntax
[ iLevels = ] MSWebDVD.GetTitleParentalLevels(iTitle)
```

## <a name="parameters"></a><span data-ttu-id="8bea5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8bea5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bea5-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*ититле*</span><span class="sxs-lookup"><span data-stu-id="8bea5-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="8bea5-109">Задает заголовок в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="8bea5-109">Specifies the title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bea5-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8bea5-110">Return Value</span></span>

<span data-ttu-id="8bea5-111">Возвращает целочисленное значение, отдельные биты которого указывают, какие уровни родительского управления (ПМЛ) установлены в указанном заголовке.</span><span class="sxs-lookup"><span data-stu-id="8bea5-111">Returns an integer value whose individual bits indicate which parental management levels (PML) are set in the specified title.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bea5-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8bea5-112">Remarks</span></span>

<span data-ttu-id="8bea5-113">Заголовок может содержать главы или даже короткие сегменты, имеющие ПМЛ, отличающиеся от общего ПМЛ для заголовка.</span><span class="sxs-lookup"><span data-stu-id="8bea5-113">A title may have chapters or even short segments that have a PML different from the overall PML for the title.</span></span> <span data-ttu-id="8bea5-114">Используйте этот метод, чтобы определить все Пмлс, которые будут обнаружены при воспроизведении указанного заголовка.</span><span class="sxs-lookup"><span data-stu-id="8bea5-114">Use this method to determine all the PMLs that will be encountered when playing a specified title.</span></span> <span data-ttu-id="8bea5-115">Возвращаемое целое число — это набор битовых флагов, которые определены, как показано в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="8bea5-115">The returned integer is a set of bit flags that are defined as shown in the table below.</span></span> <span data-ttu-id="8bea5-116">Выполните побитовую операцию и для *илевелс* и каждого возможного значения.</span><span class="sxs-lookup"><span data-stu-id="8bea5-116">Perform a bitwise AND operation on *iLevels* and each possible value.</span></span> <span data-ttu-id="8bea5-117">Если операция возвращает **значение true**, это означает, что в этом заголовке будет обнаружено ПМЛ.</span><span class="sxs-lookup"><span data-stu-id="8bea5-117">If the operation returns **true**, it means that PML will be encountered at some point in this title.</span></span>



| <span data-ttu-id="8bea5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8bea5-118">Value</span></span>  | <span data-ttu-id="8bea5-119">Описание</span><span class="sxs-lookup"><span data-stu-id="8bea5-119">Description</span></span>          |
|--------|----------------------|
| <span data-ttu-id="8bea5-120">0x100</span><span class="sxs-lookup"><span data-stu-id="8bea5-120">0x100</span></span>  | <span data-ttu-id="8bea5-121">Родительский уровень 1 DVD</span><span class="sxs-lookup"><span data-stu-id="8bea5-121">DVD Parental Level 1</span></span> |
| <span data-ttu-id="8bea5-122">0x200</span><span class="sxs-lookup"><span data-stu-id="8bea5-122">0x200</span></span>  | <span data-ttu-id="8bea5-123">Родительский уровень DVD 2</span><span class="sxs-lookup"><span data-stu-id="8bea5-123">DVD Parental Level 2</span></span> |
| <span data-ttu-id="8bea5-124">0x400</span><span class="sxs-lookup"><span data-stu-id="8bea5-124">0x400</span></span>  | <span data-ttu-id="8bea5-125">Родительский уровень DVD 3</span><span class="sxs-lookup"><span data-stu-id="8bea5-125">DVD Parental Level 3</span></span> |
| <span data-ttu-id="8bea5-126">0x800</span><span class="sxs-lookup"><span data-stu-id="8bea5-126">0x800</span></span>  | <span data-ttu-id="8bea5-127">Родительский уровень DVD 4</span><span class="sxs-lookup"><span data-stu-id="8bea5-127">DVD Parental Level 4</span></span> |
| <span data-ttu-id="8bea5-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="8bea5-128">0x1000</span></span> | <span data-ttu-id="8bea5-129">Родительский уровень диска DVD 5</span><span class="sxs-lookup"><span data-stu-id="8bea5-129">DVD Parental Level 5</span></span> |
| <span data-ttu-id="8bea5-130">0x2000</span><span class="sxs-lookup"><span data-stu-id="8bea5-130">0x2000</span></span> | <span data-ttu-id="8bea5-131">Родительский уровень DVD 6</span><span class="sxs-lookup"><span data-stu-id="8bea5-131">DVD Parental Level 6</span></span> |
| <span data-ttu-id="8bea5-132">0x4000</span><span class="sxs-lookup"><span data-stu-id="8bea5-132">0x4000</span></span> | <span data-ttu-id="8bea5-133">Родительский уровень DVD 7</span><span class="sxs-lookup"><span data-stu-id="8bea5-133">DVD Parental Level 7</span></span> |
| <span data-ttu-id="8bea5-134">0x8000</span><span class="sxs-lookup"><span data-stu-id="8bea5-134">0x8000</span></span> | <span data-ttu-id="8bea5-135">Родительский уровень DVD 8</span><span class="sxs-lookup"><span data-stu-id="8bea5-135">DVD Parental Level 8</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="8bea5-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8bea5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bea5-137">**селектпаренталлевел**</span><span class="sxs-lookup"><span data-stu-id="8bea5-137">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="8bea5-138">**жетплайерпаренталкаунтри**</span><span class="sxs-lookup"><span data-stu-id="8bea5-138">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="8bea5-139">**жетплайерпаренталлевел**</span><span class="sxs-lookup"><span data-stu-id="8bea5-139">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="8bea5-140">**селектпаренталкаунтри**</span><span class="sxs-lookup"><span data-stu-id="8bea5-140">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> </dl>

 

 



