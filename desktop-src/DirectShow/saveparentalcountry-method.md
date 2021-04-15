---
description: Метод Двдадм. Савепаренталкаунтри сохраняет в реестре новую страну или регион для приложения.
ms.assetid: 2185ad7d-c7c1-4d8b-82e7-5ed5fffaff26
title: Метод Савепаренталкаунтри (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ca47a6ca10f25298b4eb10fdcf532c8d764b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688903"
---
# <a name="saveparentalcountry-method"></a><span data-ttu-id="35a4b-103">Метод Савепаренталкаунтри</span><span class="sxs-lookup"><span data-stu-id="35a4b-103">SaveParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="35a4b-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="35a4b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="35a4b-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="35a4b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="35a4b-106">`DVDAdm.SaveParentalCountry`Метод сохраняет в реестре новую страну или регион для приложения.</span><span class="sxs-lookup"><span data-stu-id="35a4b-106">The `DVDAdm.SaveParentalCountry` method saves the application's new parental country/region to the registry.</span></span>

``` syntax
DVD.DVDAdm.SaveParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="35a4b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="35a4b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35a4b-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*икаунтри*</span><span class="sxs-lookup"><span data-stu-id="35a4b-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span></span>
</dt> <dd>

<span data-ttu-id="35a4b-109">Задает страну или регион в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="35a4b-109">Specifies the parental country/region as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="35a4b-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*сусернаме*</span><span class="sxs-lookup"><span data-stu-id="35a4b-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="35a4b-111">Указывает имя пользователя в виде строки.</span><span class="sxs-lookup"><span data-stu-id="35a4b-111">Specifies the user name as a String.</span></span> <span data-ttu-id="35a4b-112">(В настоящий момент игнорируется.)</span><span class="sxs-lookup"><span data-stu-id="35a4b-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="35a4b-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*спассворд*</span><span class="sxs-lookup"><span data-stu-id="35a4b-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="35a4b-114">Указывает пароль в виде строки.</span><span class="sxs-lookup"><span data-stu-id="35a4b-114">Specifies the password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35a4b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35a4b-115">Return value</span></span>

<span data-ttu-id="35a4b-116">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="35a4b-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="35a4b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35a4b-117">Remarks</span></span>

<span data-ttu-id="35a4b-118">Этот метод позволяет пользователю, знающему текущий пароль, сохранить в реестре новый родительский параметр страна или регион.</span><span class="sxs-lookup"><span data-stu-id="35a4b-118">This method enables a user who knows the current password to save a new parental country/region setting to the registry.</span></span> <span data-ttu-id="35a4b-119">Как и для всех методов **мсдвдадм**, этот метод не влияет на текущий уровень проигрывателя. Он изменяет только параметр реестра, чтобы при следующем создании объекта Мсвебдвд он открывался с новой страной или регионом.</span><span class="sxs-lookup"><span data-stu-id="35a4b-119">As with all the methods of **MSDVDAdm**, this method does not affect the current level in the player; it changes only the registry setting, so that the next time the MSWebDVD object is created, it will open with the new country/region.</span></span> <span data-ttu-id="35a4b-120">Чтобы изменить страну или регион в проигрывателе, вызовите [**селектпаренталкаунтри**](selectparentalcountry-method.md), который не изменяет параметр реестра.</span><span class="sxs-lookup"><span data-stu-id="35a4b-120">To change the parental country/region in the player, call [**SelectParentalCountry**](selectparentalcountry-method.md), which does not change the registry setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="35a4b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="35a4b-121">Requirements</span></span>



| <span data-ttu-id="35a4b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="35a4b-122">Requirement</span></span> | <span data-ttu-id="35a4b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="35a4b-123">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="35a4b-124">Header</span><span class="sxs-lookup"><span data-stu-id="35a4b-124">Header</span></span><br/> | <dl> <span data-ttu-id="35a4b-125"><dt>Сегмент. h</dt></span><span class="sxs-lookup"><span data-stu-id="35a4b-125"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35a4b-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35a4b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35a4b-127">**савепаренталлевел**</span><span class="sxs-lookup"><span data-stu-id="35a4b-127">**SaveParentalLevel**</span></span>](saveparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="35a4b-128">Объект Мсдвдадм</span><span class="sxs-lookup"><span data-stu-id="35a4b-128">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




