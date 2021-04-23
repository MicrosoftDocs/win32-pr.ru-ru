---
description: Метод Акцептпаренталлевелчанже принимает или отклоняет новый временный родительский уровень управления.
ms.assetid: b3d58069-16dc-4598-90ea-6136c2f62ac7
title: Метод Акцептпаренталлевелчанже
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b2e81d1d82c4ede14580ed65d88566738dac1b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682322"
---
# <a name="acceptparentallevelchange-method"></a><span data-ttu-id="15f9b-103">Метод Акцептпаренталлевелчанже</span><span class="sxs-lookup"><span data-stu-id="15f9b-103">AcceptParentalLevelChange Method</span></span>

> [!Note]  
> <span data-ttu-id="15f9b-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="15f9b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="15f9b-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="15f9b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="15f9b-106">Метод Акцептпаренталлевелчанже принимает или отклоняет новый временный родительский уровень управления.</span><span class="sxs-lookup"><span data-stu-id="15f9b-106">The AcceptParentalLevelChange method accepts or rejects the new temporary parental management level.</span></span>

``` syntax
        MSWebDVD.AcceptParentalLevelChange(bAccept)
```

## <a name="parameters"></a><span data-ttu-id="15f9b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="15f9b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15f9b-108"><span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*бакцепт*</span><span class="sxs-lookup"><span data-stu-id="15f9b-108"><span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*bAccept*</span></span>
</dt> <dd>

<span data-ttu-id="15f9b-109">Указывает новый родительский уровень в качестве логического значения.</span><span class="sxs-lookup"><span data-stu-id="15f9b-109">Specifies the new parental level as a Boolean value.</span></span>



| <span data-ttu-id="15f9b-110">Значение</span><span class="sxs-lookup"><span data-stu-id="15f9b-110">Value</span></span> | <span data-ttu-id="15f9b-111">Описание</span><span class="sxs-lookup"><span data-stu-id="15f9b-111">Description</span></span>                               |
|-------|-------------------------------------------|
| <span data-ttu-id="15f9b-112">true</span><span class="sxs-lookup"><span data-stu-id="15f9b-112">true</span></span>  | <span data-ttu-id="15f9b-113">Примите новый уровень родительского управления.</span><span class="sxs-lookup"><span data-stu-id="15f9b-113">Accept the new parental management level.</span></span> |
| <span data-ttu-id="15f9b-114">false</span><span class="sxs-lookup"><span data-stu-id="15f9b-114">false</span></span> | <span data-ttu-id="15f9b-115">Отклонить новый уровень родительского управления.</span><span class="sxs-lookup"><span data-stu-id="15f9b-115">Reject the new parental management level.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15f9b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15f9b-116">Return Value</span></span>

<span data-ttu-id="15f9b-117">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="15f9b-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15f9b-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15f9b-118">Remarks</span></span>

<span data-ttu-id="15f9b-119">Вызовите этот метод в ответ на \_ \_ \_ \_ уведомление о событии изменения родительского уровня EC, чтобы указать, должен ли навигатор DVD воспроизводить содержимое с новым родительским уровнем, или ветвь, где диск указывает, отклоняется ли новый уровень.</span><span class="sxs-lookup"><span data-stu-id="15f9b-119">Call this method in response to an EC\_DVD\_PARENTAL\_LEVEL\_CHANGE event notification to specify whether the DVD Navigator should play the content with the new parental level, or branch to where the disc specifies if the new level is rejected.</span></span>

## <a name="see-also"></a><span data-ttu-id="15f9b-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15f9b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15f9b-121">Применение уровней родительского управления</span><span class="sxs-lookup"><span data-stu-id="15f9b-121">Enforcing Parental Management Levels</span></span>](enforcing-parental-management-levels.md)
</dt> <dt>

[<span data-ttu-id="15f9b-122">**жетплайерпаренталкаунтри**</span><span class="sxs-lookup"><span data-stu-id="15f9b-122">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="15f9b-123">**жетплайерпаренталлевел**</span><span class="sxs-lookup"><span data-stu-id="15f9b-123">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="15f9b-124">**жеттитлепаренталлевелс**</span><span class="sxs-lookup"><span data-stu-id="15f9b-124">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="15f9b-125">**нотифипаренталлевелчанже**</span><span class="sxs-lookup"><span data-stu-id="15f9b-125">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="15f9b-126">**селектпаренталкаунтри**</span><span class="sxs-lookup"><span data-stu-id="15f9b-126">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="15f9b-127">**селектпаренталлевел**</span><span class="sxs-lookup"><span data-stu-id="15f9b-127">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> </dl>

 

 



