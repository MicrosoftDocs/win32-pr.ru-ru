---
title: Метод Жетекс
description: Некоторые атрибуты могут хранить одно или несколько значений.
ms.assetid: aaa5fa90-7e60-4668-bd23-1475c2e4d184
ms.tgt_platform: multiple
keywords:
- Жетекс ADSI, использование функции IADs Жетекс
- ADSI ADSI с использованием с помощью метода IADs Жетекс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a909b33664ad805b0bf483ee9f0c2b40316ec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654095"
---
# <a name="the-getex-method"></a><span data-ttu-id="9f005-105">Метод Жетекс</span><span class="sxs-lookup"><span data-stu-id="9f005-105">The GetEx Method</span></span>

<span data-ttu-id="9f005-106">Некоторые атрибуты могут хранить одно или несколько значений.</span><span class="sxs-lookup"><span data-stu-id="9f005-106">Some attributes can store one or more values.</span></span> <span data-ttu-id="9f005-107">Например, атрибут **осертелефоне** объекта пользователя в Active Directory является свойством, которое может иметь ноль, одно или несколько значений.</span><span class="sxs-lookup"><span data-stu-id="9f005-107">For example, the **otherTelephone** attribute of a user object in Active Directory is a property that can have zero, one, or many values.</span></span> <span data-ttu-id="9f005-108">Атрибуты, имеющие несколько значений, называются атрибутами с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="9f005-108">Attributes that have multiple values are known as "multi-valued attributes".</span></span> <span data-ttu-id="9f005-109">Если метод [**iAds:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) используется для получения атрибута с несколькими значениями, результаты должны обрабатываться иначе, чем если бы атрибут состоять из одного значения.</span><span class="sxs-lookup"><span data-stu-id="9f005-109">If the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method is used to retrieve a multi-valued attribute, the results must be processed differently than if the attribute has a single value.</span></span> <span data-ttu-id="9f005-110">Однако результаты, предоставляемые методом [**iAds:: жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) , обрабатываются одинаковым образом независимо от того, имеет ли атрибут одно или несколько значений.</span><span class="sxs-lookup"><span data-stu-id="9f005-110">The results provided by the [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method, however, are processed in the same manner, regardless if the attribute has a single or multiple values.</span></span> <span data-ttu-id="9f005-111">В обоих случаях метод **iAds:: жетекс** возвращает значения в массиве.</span><span class="sxs-lookup"><span data-stu-id="9f005-111">In both cases, the **IADs::GetEx** method returns the values in an array.</span></span>

<span data-ttu-id="9f005-112">Метод [**iAds:: жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) извлекает свойства из кэша свойств.</span><span class="sxs-lookup"><span data-stu-id="9f005-112">The [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method retrieves properties from the property cache.</span></span> <span data-ttu-id="9f005-113">Если указанное свойство не найдено в кэше, метод **iAds:: жетекс** выполняет неявный вызов метода [**iAds::-info**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) .</span><span class="sxs-lookup"><span data-stu-id="9f005-113">If the specified property is not found in the cache, **IADs::GetEx** performs an implicit [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) call.</span></span>

<span data-ttu-id="9f005-114">Метод [**iAds:: жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) возвращает массив вариантов типа Variant, независимо от числа возвращаемых сервером значений.</span><span class="sxs-lookup"><span data-stu-id="9f005-114">The [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method returns a variant array of variants regardless of the number of values returned from the server.</span></span> <span data-ttu-id="9f005-115">Это справедливо, даже если атрибут содержит только одно значение.</span><span class="sxs-lookup"><span data-stu-id="9f005-115">This is true even if the attribute only contains one value.</span></span>


```VB
Dim usr As IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
homePhones = usr.GetEx("otherHomePhone")
For each phone in homePhones
    Debug.Print phone
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



<span data-ttu-id="9f005-116">Метод [**iAds:: жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) можно также использовать для атрибутов с одним значением.</span><span class="sxs-lookup"><span data-stu-id="9f005-116">The [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method can also be used for single-valued attributes.</span></span> <span data-ttu-id="9f005-117">Результаты атрибута с одним значением обрабатываются так же, как и результаты для атрибута с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="9f005-117">The results of a single-valued attribute are processed the same as the results for a multi-valued attribute.</span></span>


```VB
Dim usr as IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
sds = usr.GetEx("ntSecurityDescriptor")
For each sd in sds
    Set acl = sd.DiscretionaryACL
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



<span data-ttu-id="9f005-118">Если для атрибута не задано значение, функция [**iAds:: жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) возвращает ошибку "свойство не найдено в кэше".</span><span class="sxs-lookup"><span data-stu-id="9f005-118">If no value is set for the attribute, [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) returns the error "Property not found in cache".</span></span>

 

 




