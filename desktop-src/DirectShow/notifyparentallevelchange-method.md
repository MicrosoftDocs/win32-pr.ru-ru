---
description: Метод Нотифипаренталлевелчанже включает или отключает обработку событий для временных команд родительского уровня управления.
ms.assetid: c8252cc6-a83f-4cce-ba3e-7db669eeb465
title: Метод Нотифипаренталлевелчанже (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc47b7d78af8cfdd32aa63361411e769c375ddf1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688831"
---
# <a name="notifyparentallevelchange-method"></a><span data-ttu-id="8ff78-103">Метод Нотифипаренталлевелчанже</span><span class="sxs-lookup"><span data-stu-id="8ff78-103">NotifyParentalLevelChange Method</span></span>

> [!Note]  
> <span data-ttu-id="8ff78-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8ff78-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="8ff78-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="8ff78-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="8ff78-106">`NotifyParentalLevelChange`Метод включает или отключает обработку событий для временных команд родительского уровня управления.</span><span class="sxs-lookup"><span data-stu-id="8ff78-106">The `NotifyParentalLevelChange` method enables or disables the event handling for temporary parental management level commands.</span></span>

``` syntax
MSWebDVD.NotifyParentalLevelChange(bNotify)
```

## <a name="parameters"></a><span data-ttu-id="8ff78-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ff78-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ff78-108"><span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*бнотифи*</span><span class="sxs-lookup"><span data-stu-id="8ff78-108"><span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bNotify*</span></span>
</dt> <dd>

<span data-ttu-id="8ff78-109">Указывает логическое значение, указывающее, будет ли приложение уведомлено, когда объект Мсвебдвд встречает сегменты видео с более полной оценкой, чем общая оценка для диска.</span><span class="sxs-lookup"><span data-stu-id="8ff78-109">Specifies a Boolean value indicating whether or not the application is notified when the MSWebDVD object encounters video segments with a rating more restrictive than the overall rating for the disc.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ff78-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ff78-110">Return Value</span></span>

<span data-ttu-id="8ff78-111">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="8ff78-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ff78-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ff78-112">Remarks</span></span>

<span data-ttu-id="8ff78-113">По умолчанию уведомления родительского управления отключены.</span><span class="sxs-lookup"><span data-stu-id="8ff78-113">Parental management notifications are disabled by default.</span></span> <span data-ttu-id="8ff78-114">Это означает, что временные родительские команды с диска разрешены, но не учитываются, и диск будет воспроизводиться без прерывания.</span><span class="sxs-lookup"><span data-stu-id="8ff78-114">This means that temporary parental commands from the disc are allowed but ignored and disc will play without interruption.</span></span> <span data-ttu-id="8ff78-115">Вызывайте этот метод во время инициализации приложения, если необходимо управлять временными командами родительского уровня управления с диска. Чтобы отключить функцию родительского управления после ее включения, вызовите этот метод с аргументом false.</span><span class="sxs-lookup"><span data-stu-id="8ff78-115">Call this method during initialization of your application if you need to handle temporary parental management level commands from the disc. To disable parental management after it is enabled, call this method with an argument of false.</span></span> <span data-ttu-id="8ff78-116">Дополнительные сведения о службе родительского управления см. в разделе [**акцептпаренталлевелчанже**](acceptparentallevelchange-method.md).</span><span class="sxs-lookup"><span data-stu-id="8ff78-116">For more details on parental management, see [**AcceptParentalLevelChange**](acceptparentallevelchange-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ff78-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8ff78-117">Requirements</span></span>



| <span data-ttu-id="8ff78-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8ff78-118">Requirement</span></span> | <span data-ttu-id="8ff78-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8ff78-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8ff78-120">Header</span><span class="sxs-lookup"><span data-stu-id="8ff78-120">Header</span></span><br/> | <dl> <span data-ttu-id="8ff78-121"><dt>Сегмент. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ff78-121"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ff78-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ff78-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ff78-123">**селектпаренталлевел**</span><span class="sxs-lookup"><span data-stu-id="8ff78-123">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="8ff78-124">**жеттитлепаренталлевелс**</span><span class="sxs-lookup"><span data-stu-id="8ff78-124">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="8ff78-125">**жетплайерпаренталкаунтри**</span><span class="sxs-lookup"><span data-stu-id="8ff78-125">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="8ff78-126">**жетплайерпаренталлевел**</span><span class="sxs-lookup"><span data-stu-id="8ff78-126">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="8ff78-127">**селектпаренталкаунтри**</span><span class="sxs-lookup"><span data-stu-id="8ff78-127">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> </dl>

 

 




