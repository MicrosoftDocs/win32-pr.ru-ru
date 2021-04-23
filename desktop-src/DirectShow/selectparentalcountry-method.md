---
description: Метод Селектпаренталкаунтри задает указанную локальную страну или регион для последующего воспроизведения.
ms.assetid: 70368351-c7b9-4640-a4f7-7d972b8e4628
title: Метод Селектпаренталкаунтри
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2216d2b2ed72436aca003b42cbf811c8a01bd8fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537787"
---
# <a name="selectparentalcountry-method"></a><span data-ttu-id="4eee6-103">Метод Селектпаренталкаунтри</span><span class="sxs-lookup"><span data-stu-id="4eee6-103">SelectParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="4eee6-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4eee6-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4eee6-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="4eee6-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4eee6-106">`SelectParentalCountry`Метод задает указанную родительским страну или регион для последующего воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="4eee6-106">The `SelectParentalCountry` method sets the specified parental country/region for subsequent playback.</span></span>

``` syntax
MSWebDVD.SelectParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="4eee6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4eee6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4eee6-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*икаунтри*</span><span class="sxs-lookup"><span data-stu-id="4eee6-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span></span>
</dt> <dd>

<span data-ttu-id="4eee6-109">Указывает страну или регион в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="4eee6-109">Specifies the country/region as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="4eee6-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*сусернаме*</span><span class="sxs-lookup"><span data-stu-id="4eee6-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="4eee6-111">Указывает текущего пользователя, выполнившего вход в систему, в виде строки.</span><span class="sxs-lookup"><span data-stu-id="4eee6-111">Specifies the current logged-on user as a String.</span></span> <span data-ttu-id="4eee6-112">(В настоящий момент игнорируется.)</span><span class="sxs-lookup"><span data-stu-id="4eee6-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="4eee6-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*спассворд*</span><span class="sxs-lookup"><span data-stu-id="4eee6-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="4eee6-114">Указывает строку пароля приложения.</span><span class="sxs-lookup"><span data-stu-id="4eee6-114">Specifies the application password String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4eee6-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4eee6-115">Return Value</span></span>

<span data-ttu-id="4eee6-116">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="4eee6-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4eee6-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4eee6-117">Remarks</span></span>

<span data-ttu-id="4eee6-118">Родительский регион определяет, как обрабатываются родительские уровни.</span><span class="sxs-lookup"><span data-stu-id="4eee6-118">The parental country/region determines how the parental levels are interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="4eee6-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4eee6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eee6-120">**селектпаренталлевел**</span><span class="sxs-lookup"><span data-stu-id="4eee6-120">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="4eee6-121">**нотифипаренталлевелчанже**</span><span class="sxs-lookup"><span data-stu-id="4eee6-121">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="4eee6-122">**жеттитлепаренталлевелс**</span><span class="sxs-lookup"><span data-stu-id="4eee6-122">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="4eee6-123">**жетплайерпаренталкаунтри**</span><span class="sxs-lookup"><span data-stu-id="4eee6-123">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="4eee6-124">**жетплайерпаренталлевел**</span><span class="sxs-lookup"><span data-stu-id="4eee6-124">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="4eee6-125">**акцептпаренталлевелчанже**</span><span class="sxs-lookup"><span data-stu-id="4eee6-125">**AcceptParentalLevelChange**</span></span>](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



