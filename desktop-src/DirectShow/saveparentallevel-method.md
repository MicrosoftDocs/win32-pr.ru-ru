---
description: Метод Двдадм. Савепаренталлевел сохраняет новый родительский уровень по умолчанию в реестре.
ms.assetid: 8ad22098-acbd-41fd-9224-829b3cc5f8ae
title: Метод Савепаренталлевел (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d30d26264dff077de391b6b513f7e9ab5048c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675613"
---
# <a name="saveparentallevel-method"></a><span data-ttu-id="be65c-103">Метод Савепаренталлевел</span><span class="sxs-lookup"><span data-stu-id="be65c-103">SaveParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="be65c-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="be65c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="be65c-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="be65c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="be65c-106">Метод **двдадм. савепаренталлевел** сохраняет новый родительский уровень по умолчанию в реестре.</span><span class="sxs-lookup"><span data-stu-id="be65c-106">The **DVDAdm.SaveParentalLevel** method saves a new default parental level to the registry.</span></span>

``` syntax
DVD.DVDAdm.SaveParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="be65c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="be65c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be65c-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*илевел*</span><span class="sxs-lookup"><span data-stu-id="be65c-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span></span>
</dt> <dd>

<span data-ttu-id="be65c-109">Задает родительский уровень в качестве значения anInteger от 1 до 8.</span><span class="sxs-lookup"><span data-stu-id="be65c-109">Specifies the parental level as anInteger value from 1 through 8.</span></span>

</dd> <dt>

<span data-ttu-id="be65c-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*сусернаме*</span><span class="sxs-lookup"><span data-stu-id="be65c-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="be65c-111">Указывает имя пользователя в виде строки.</span><span class="sxs-lookup"><span data-stu-id="be65c-111">Specifies the user name as a String.</span></span> <span data-ttu-id="be65c-112">(В настоящий момент игнорируется.)</span><span class="sxs-lookup"><span data-stu-id="be65c-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="be65c-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*спассворд*</span><span class="sxs-lookup"><span data-stu-id="be65c-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="be65c-114">Указывает пароль в виде строки.</span><span class="sxs-lookup"><span data-stu-id="be65c-114">Specifies the password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be65c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be65c-115">Return Value</span></span>

<span data-ttu-id="be65c-116">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="be65c-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be65c-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be65c-117">Remarks</span></span>

<span data-ttu-id="be65c-118">Этот метод позволяет пользователю, знающему текущий пароль, сохранить новый параметр родительского уровня в реестре.</span><span class="sxs-lookup"><span data-stu-id="be65c-118">This method enables a user who knows the current password to save a new parental level setting to the registry.</span></span> <span data-ttu-id="be65c-119">Как и для всех методов **мсдвдадм**, этот метод не влияет на текущий уровень проигрывателя. Он изменяет только параметр реестра, чтобы при следующем запуске объекта Мсвебдвд он открывался с новым уровнем.</span><span class="sxs-lookup"><span data-stu-id="be65c-119">As with all the methods of **MSDVDAdm**, this method does not affect the current level in the player; it changes only the registry setting, so that the next time the MSWebDVD object is started, it will open with the new level.</span></span> <span data-ttu-id="be65c-120">Укажите значение-1, чтобы отключить функцию родительского управления.</span><span class="sxs-lookup"><span data-stu-id="be65c-120">Specify -1 to disable parental management.</span></span> <span data-ttu-id="be65c-121">Чтобы изменить родительский уровень в проигрывателе, вызовите [**селектпаренталлевел**](selectparentallevel-method.md), который не изменяет параметр реестра.</span><span class="sxs-lookup"><span data-stu-id="be65c-121">To change the parental level in the player, call [**SelectParentalLevel**](selectparentallevel-method.md), which does not change the registry setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="be65c-122">Требования</span><span class="sxs-lookup"><span data-stu-id="be65c-122">Requirements</span></span>



| <span data-ttu-id="be65c-123">Требование</span><span class="sxs-lookup"><span data-stu-id="be65c-123">Requirement</span></span> | <span data-ttu-id="be65c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="be65c-124">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="be65c-125">Header</span><span class="sxs-lookup"><span data-stu-id="be65c-125">Header</span></span><br/> | <dl> <span data-ttu-id="be65c-126"><dt>Сегмент. h</dt></span><span class="sxs-lookup"><span data-stu-id="be65c-126"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be65c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be65c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be65c-128">Объект Мсдвдадм</span><span class="sxs-lookup"><span data-stu-id="be65c-128">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




