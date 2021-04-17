---
description: Метод Двдадм. Жетпаренталкаунтри Извлекает родительский регион или страну, которая была сохранена в реестре в последний раз.
ms.assetid: 947c5e2a-dfd5-4900-87d4-0ec967b99a22
title: Метод Жетпаренталкаунтри (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fcee63fd3cad64498d95ca74e81a9f02804a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652109"
---
# <a name="getparentalcountry-method"></a><span data-ttu-id="cc571-103">Метод Жетпаренталкаунтри</span><span class="sxs-lookup"><span data-stu-id="cc571-103">GetParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="cc571-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cc571-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="cc571-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="cc571-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="cc571-106">`DVDAdm.GetParentalCountry`Метод извлекает страну или регион, которые были сохранены в реестре в последний раз.</span><span class="sxs-lookup"><span data-stu-id="cc571-106">The `DVDAdm.GetParentalCountry` method retrieves the parental country/region that was last saved to the registry.</span></span>

``` syntax
[ iParentalCountry = ] DVD.DVDAdm.GetParentalCountry()
```

## <a name="return-value"></a><span data-ttu-id="cc571-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc571-107">Return Value</span></span>

<span data-ttu-id="cc571-108">Возвращает целое число, указывающее код страны или региона по умолчанию, хранящийся в реестре.</span><span class="sxs-lookup"><span data-stu-id="cc571-108">Returns an Integer indicating the default country/region code stored in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc571-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc571-109">Remarks</span></span>

<span data-ttu-id="cc571-110">Родительский регион или страна, которую извлекает этот метод, не обязательно являются той же страной или регионом, которые в настоящее время хранятся в объекте Мсвебдвд.</span><span class="sxs-lookup"><span data-stu-id="cc571-110">The parental country/region this method retrieves is not necessarily the same country/region currently stored in the MSWebDVD object.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc571-111">Требования</span><span class="sxs-lookup"><span data-stu-id="cc571-111">Requirements</span></span>



| <span data-ttu-id="cc571-112">Требование</span><span class="sxs-lookup"><span data-stu-id="cc571-112">Requirement</span></span> | <span data-ttu-id="cc571-113">Значение</span><span class="sxs-lookup"><span data-stu-id="cc571-113">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cc571-114">Header</span><span class="sxs-lookup"><span data-stu-id="cc571-114">Header</span></span><br/> | <dl> <span data-ttu-id="cc571-115"><dt>Сегмент. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc571-115"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc571-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc571-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc571-117">Объект Мсдвдадм</span><span class="sxs-lookup"><span data-stu-id="cc571-117">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




