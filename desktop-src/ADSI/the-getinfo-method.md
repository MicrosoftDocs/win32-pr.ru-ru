---
title: Метод info
description: Метод IADs info загружает все значения атрибутов объекта ADSI в локальный кэш из базовой службы каталогов.
ms.assetid: b29f1156-7c38-4f5a-a88c-578ae6167758
ms.tgt_platform: multiple
keywords:
- Info ADSI, использование команды IADs info
- ADSI ADSI с использованием с помощью метода IADs info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b374791e7fd7ff787c1b825827f410a9c15b551b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772908"
---
# <a name="the-getinfo-method"></a><span data-ttu-id="ee597-105">Метод info</span><span class="sxs-lookup"><span data-stu-id="ee597-105">The GetInfo Method</span></span>

<span data-ttu-id="ee597-106">Метод [**iAds:: info**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) загружает все значения АТРИБУТОВ объекта ADSI в локальный кэш из базовой службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="ee597-106">The [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method loads all of the attribute values for an ADSI object into the local cache from the underlying directory service.</span></span> <span data-ttu-id="ee597-107">Метод [**iAds:: жетинфоекс**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) используется для загрузки конкретных значений атрибутов в локальный кэш.</span><span class="sxs-lookup"><span data-stu-id="ee597-107">The [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method is used to load specific attribute values into the local cache.</span></span> <span data-ttu-id="ee597-108">Дополнительные сведения об использовании метода **iAds:: жетинфоекс** см. в разделе [Оптимизация с помощью жетинфоекс](optimization-using-getinfoex.md).</span><span class="sxs-lookup"><span data-stu-id="ee597-108">For more information about using the **IADs::GetInfoEx** method, see [Optimization Using GetInfoEx](optimization-using-getinfoex.md).</span></span>

<span data-ttu-id="ee597-109">ADSI сделает неявный вызов метода [**iAds::**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get) или [**iAds:: жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) для конкретного атрибута, и в локальном кэше значение не найдено.</span><span class="sxs-lookup"><span data-stu-id="ee597-109">ADSI will make an implicit [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) call when the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) or [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method is called for a specific attribute and no value is found in the local cache.</span></span> <span data-ttu-id="ee597-110">При вызове метода **iAds::-info** неявный вызов не повторяется.</span><span class="sxs-lookup"><span data-stu-id="ee597-110">When **IADs::GetInfo** has been called, an implicit call is not repeated.</span></span> <span data-ttu-id="ee597-111">Если значение уже существует в кэше свойств, то при вызове метода **iAds:: Get** или **iAds:: жетекс** без предварительного вызова функции **iAds::-info** будет получено кэшированное значение, а не самое последнее значение из базового каталога.</span><span class="sxs-lookup"><span data-stu-id="ee597-111">If a value already exists in the property cache, however, calling the **IADs::Get** or **IADs::GetEx** method without first calling **IADs::GetInfo** will retrieve the cached value rather than the most current value from the underlying directory.</span></span> <span data-ttu-id="ee597-112">Это может привести к перезаписанию обновленных значений атрибутов, если локальный кэш был изменен, но значения не были зафиксированы в базовой службе каталогов с помощью вызова метода [**iAds:: сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="ee597-112">This can cause updated attribute values to be overwritten if the local cache has been modified but the values have not been committed to the underlying directory service with a call to the [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span> <span data-ttu-id="ee597-113">Чтобы избежать проблем с кэшированием, следует зафиксировать изменения значений атрибутов, вызвав метод **iAds:: сетинфо** перед вызовом метода **iAds::** OutAttribute.</span><span class="sxs-lookup"><span data-stu-id="ee597-113">To avoid caching problems, commit attribute value changes by calling **IADs::SetInfo** before calling **IADs::GetInfo**.</span></span>


```VB
Dim usr As IADs

' Bind to a specific user object.
Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' This code example assumes that the property description has a single value in the directory.
' Be aware that this will IMPLICITLY call GetInfo because at this point GetInfo
' has not yet been called (implicitly or explicitly) on the usr object.
Debug.Print "User's title is " + usr.Get("title")

' Change the attribute value in the local cache.
usr.Put "title", "Vice President"
Debug.Print "User's title is " + usr.Get("title")

' Call GetInfo, which will overwrite the updated value because SetInfo has not 
' been called.
usr.GetInfo
Debug.Print "User's title is " + usr.Get("title")
```



<span data-ttu-id="ee597-114">Некоторые службы каталогов не возвращают значения атрибутов объекта в ответ на вызов метода [**iAds::**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) GetResponse.</span><span class="sxs-lookup"><span data-stu-id="ee597-114">Some directory services do not return all attribute values for an object in response to a [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) call.</span></span> <span data-ttu-id="ee597-115">В этих случаях для загрузки этих значений в локальный кэш используйте метод [**iAds:: жетинфоекс**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) .</span><span class="sxs-lookup"><span data-stu-id="ee597-115">In these cases, use the [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method to load these values into the local cache.</span></span>

 

 




