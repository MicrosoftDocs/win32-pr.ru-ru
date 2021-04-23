---
description: Метод Селектпаренталлевел задает указанный родительский уровень для последующего воспроизведения.
ms.assetid: ffd1e204-6ed2-4190-8635-9f3866d38099
title: Метод Селектпаренталлевел
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb00172b8e61f353c45981af628eb396bca7a7df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537106"
---
# <a name="selectparentallevel-method"></a><span data-ttu-id="160e9-103">Метод Селектпаренталлевел</span><span class="sxs-lookup"><span data-stu-id="160e9-103">SelectParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="160e9-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="160e9-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="160e9-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="160e9-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="160e9-106">`SelectParentalLevel`Метод задает указанный родительский уровень для последующего воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="160e9-106">The `SelectParentalLevel` method sets the specified parental level for subsequent playback.</span></span>

``` syntax
MSWebDVD.SelectParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="160e9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="160e9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="160e9-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*илевел*</span><span class="sxs-lookup"><span data-stu-id="160e9-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span></span>
</dt> <dd>

<span data-ttu-id="160e9-109">Указывает уровень родительского управления в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="160e9-109">Specifies the parental management level as an Integer.</span></span> <span data-ttu-id="160e9-110">Чтобы включить функцию родительского управления, параметр *илевел* должен находиться в диапазоне от 1 до 8.</span><span class="sxs-lookup"><span data-stu-id="160e9-110">To enable the parental management, the *iLevel* parameter must range from 1 through 8.</span></span> <span data-ttu-id="160e9-111">Чтобы отключить функцию родительского управления, установите *илевел* в значение-1.</span><span class="sxs-lookup"><span data-stu-id="160e9-111">To disable the parental management, set *iLevel* to -1.</span></span>

</dd> <dt>

<span data-ttu-id="160e9-112"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*сусернаме*</span><span class="sxs-lookup"><span data-stu-id="160e9-112"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="160e9-113">Указывает текущего пользователя в виде строки.</span><span class="sxs-lookup"><span data-stu-id="160e9-113">Specifies the current user as a String.</span></span> <span data-ttu-id="160e9-114">(В настоящий момент игнорируется.)</span><span class="sxs-lookup"><span data-stu-id="160e9-114">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="160e9-115"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*спассворд*</span><span class="sxs-lookup"><span data-stu-id="160e9-115"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="160e9-116">Указывает пароль, который в настоящее время хранится в реестре в виде строки.</span><span class="sxs-lookup"><span data-stu-id="160e9-116">Specifies the password currently stored in the registry as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="160e9-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="160e9-117">Return Value</span></span>

<span data-ttu-id="160e9-118">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="160e9-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="160e9-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="160e9-119">Remarks</span></span>

<span data-ttu-id="160e9-120">Этот метод задает уровень доступа в объекте Мсвебдвд, который определяет, какое содержимое может воспроизводить пользователь.</span><span class="sxs-lookup"><span data-stu-id="160e9-120">This method sets the access level in the MSWebDVD object, which determines what content the user can play back.</span></span> <span data-ttu-id="160e9-121">Более высокие уровни могут воспроизводить содержимое нижнего уровня, но более низкие уровни не могут воспроизвести содержимое более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="160e9-121">Higher levels can play lower-level content but lower levels can't play higher-level content.</span></span> <span data-ttu-id="160e9-122">Точное значение восьми уровней родительского управления DVD зависит от страны или региона.</span><span class="sxs-lookup"><span data-stu-id="160e9-122">The exact meaning of the eight DVD parental management levels varies depending on the country/region.</span></span> <span data-ttu-id="160e9-123">В США и Канаде уровни сопоставлены с категориями рейтинга «Ассоциация движения» для «America» (МПАА).</span><span class="sxs-lookup"><span data-stu-id="160e9-123">In the United States and Canada, the levels are mapped to the Motion Picture Association of America (MPAA) rating categories.</span></span> <span data-ttu-id="160e9-124">По умолчанию функция родительского управления в навигаторе DVD отключена.</span><span class="sxs-lookup"><span data-stu-id="160e9-124">Parental management in the DVD Navigator is disabled by default.</span></span>

## <a name="see-also"></a><span data-ttu-id="160e9-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="160e9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="160e9-126">**селектпаренталкаунтри**</span><span class="sxs-lookup"><span data-stu-id="160e9-126">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="160e9-127">**нотифипаренталлевелчанже**</span><span class="sxs-lookup"><span data-stu-id="160e9-127">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="160e9-128">**жеттитлепаренталлевелс**</span><span class="sxs-lookup"><span data-stu-id="160e9-128">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="160e9-129">**жетплайерпаренталкаунтри**</span><span class="sxs-lookup"><span data-stu-id="160e9-129">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="160e9-130">**жетплайерпаренталлевел**</span><span class="sxs-lookup"><span data-stu-id="160e9-130">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="160e9-131">**акцептпаренталлевелчанже**</span><span class="sxs-lookup"><span data-stu-id="160e9-131">**AcceptParentalLevelChange**</span></span>](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



