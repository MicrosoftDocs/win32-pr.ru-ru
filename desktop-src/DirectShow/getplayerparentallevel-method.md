---
description: Жетплайерпаренталлевел извлекает уровень родительского управления, заданный в объекте Мсвебдвд.
ms.assetid: 451e0891-4e5d-4a01-94b8-290f5a804ff1
title: Метод Жетплайерпаренталлевел
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bac51e776a45e0d1fa748fc995240292474e902
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139318"
---
# <a name="getplayerparentallevel-method"></a><span data-ttu-id="3a17d-103">Метод Жетплайерпаренталлевел</span><span class="sxs-lookup"><span data-stu-id="3a17d-103">GetPlayerParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="3a17d-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3a17d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="3a17d-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="3a17d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="3a17d-106">`GetPlayerParentalLevel`Получает уровень родительского управления, заданный в объекте **мсвебдвд** .</span><span class="sxs-lookup"><span data-stu-id="3a17d-106">The `GetPlayerParentalLevel` retrieves the parental management level set in the **MSWebDVD** object.</span></span>

``` syntax
[ iLevel = ] MSWebDVD.GetPlayerParentalLevel()
```

## <a name="return-value"></a><span data-ttu-id="3a17d-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a17d-107">Return Value</span></span>

<span data-ttu-id="3a17d-108">Возвращает целочисленное значение, указывающее текущий родительский уровень в навигаторе DVD, или-1, если функция родительского управления отключена.</span><span class="sxs-lookup"><span data-stu-id="3a17d-108">Returns an integer value specifying the current parental level in the DVD Navigator, or -1 if parental management is disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a17d-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a17d-109">Remarks</span></span>

<span data-ttu-id="3a17d-110">Приложение проигрывателя отвечает за применение родительского контроля.</span><span class="sxs-lookup"><span data-stu-id="3a17d-110">A player application is responsible for enforcing parental controls.</span></span> <span data-ttu-id="3a17d-111">Родительский уровень игрока — это значение, установленное приложением, чем может быть использовано для указания самого высокого уровня родителей, который может просматривать текущий пользователь.</span><span class="sxs-lookup"><span data-stu-id="3a17d-111">The player parental level is a value set by an application than can be used to indicate the highest parental level the current user can view.</span></span> <span data-ttu-id="3a17d-112">Когда Навигатор DVD обнаруживает новый родительский уровень, используйте этот метод, чтобы определить, превышает ли новый уровень уровень, заданный приложением с помощью [**селектпаренталлевел**](selectparentallevel-method.md).</span><span class="sxs-lookup"><span data-stu-id="3a17d-112">When the DVD Navigator encounters a new parental level, use this method to determine whether the new level is greater than the level that was set by the application through [**SelectParentalLevel**](selectparentallevel-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3a17d-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a17d-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a17d-114">**жеттитлепаренталлевелс**</span><span class="sxs-lookup"><span data-stu-id="3a17d-114">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="3a17d-115">**жетплайерпаренталкаунтри**</span><span class="sxs-lookup"><span data-stu-id="3a17d-115">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="3a17d-116">**селектпаренталкаунтри**</span><span class="sxs-lookup"><span data-stu-id="3a17d-116">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="3a17d-117">**селектпаренталлевел**</span><span class="sxs-lookup"><span data-stu-id="3a17d-117">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> </dl>

 

 



