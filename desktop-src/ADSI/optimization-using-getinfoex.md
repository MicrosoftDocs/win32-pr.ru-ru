---
title: Оптимизация с помощью Жетинфоекс
description: Используется для загрузки конкретных значений атрибутов в локальный кэш из базовой службы каталогов.
ms.assetid: e6111957-22cb-4473-9814-5bcbc79583b2
ms.tgt_platform: multiple
keywords:
- Оптимизация с помощью Жетинфоекс ADSI
- Жетинфоекс ADSI, оптимизация с помощью IADs Жетинфоекс
- ADSI ADSI, использование, оптимизация с помощью метода IADs Жетинфоекс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b522093fff00700cf35b864edde2a6ae7f8f9922
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339233"
---
# <a name="optimization-using-getinfoex"></a><span data-ttu-id="a0de3-106">Оптимизация с помощью Жетинфоекс</span><span class="sxs-lookup"><span data-stu-id="a0de3-106">Optimization Using GetInfoEx</span></span>

<span data-ttu-id="a0de3-107">Метод [**iAds. жетинфоекс**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) используется для загрузки конкретных значений атрибутов в локальный кэш из базовой службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="a0de3-107">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method is used to load specific attribute values into the local cache from the underlying directory service.</span></span> <span data-ttu-id="a0de3-108">Этот метод загружает указанные значения атрибутов в локальный кэш.</span><span class="sxs-lookup"><span data-stu-id="a0de3-108">This method only loads the specified attribute values into the local cache.</span></span> <span data-ttu-id="a0de3-109">Метод [**iAds.**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) OutAttribute используется для загрузки всех значений атрибутов в локальный кэш.</span><span class="sxs-lookup"><span data-stu-id="a0de3-109">The [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method is used to load all attribute values into the local cache.</span></span>

<span data-ttu-id="a0de3-110">Метод [**iAds. жетинфоекс**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) получает конкретные текущие значения свойств объекта Active Directory из базового хранилища каталога, обновляя кэшированные значения.</span><span class="sxs-lookup"><span data-stu-id="a0de3-110">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method gets specific current values for the properties of an Active Directory object from the underlying directory store, refreshing the cached values.</span></span>

<span data-ttu-id="a0de3-111">Если значение уже существует в кэше свойств, то при вызове метода [**iAds. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) или [**iAds. жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) без предварительного вызова функции [**iAds. жетинфоекс**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) для этого атрибута будет получено кэшированное значение, а не самое последнее значение из базового каталога.</span><span class="sxs-lookup"><span data-stu-id="a0de3-111">If a value already exists in the property cache, however, calling the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) or [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method without first calling [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) for that attribute will retrieve the cached value rather than the most current value from the underlying directory.</span></span> <span data-ttu-id="a0de3-112">Это может привести к перезаписанию обновленных значений атрибутов, если локальный кэш был изменен, но значения не были зафиксированы в базовой службе каталогов с помощью вызова метода [**iAds. сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="a0de3-112">This can cause updated attribute values to be overwritten if the local cache has been modified, but the values have not been committed to the underlying directory service with a call to the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span> <span data-ttu-id="a0de3-113">Предлагаемый метод предотвращения проблем с кэшированием заключается в том, чтобы всегда фиксировать изменения значений атрибутов путем вызова метода **iAds. сетинфо** перед вызовом метода [**iAds. info**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).</span><span class="sxs-lookup"><span data-stu-id="a0de3-113">The suggested method for avoiding caching problems is to always commit attribute value changes by calling **IADs.SetInfo** before calling [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).</span></span>


```VB
Dim usr As IADs
Dim PropArray As Variant

On Error GoTo Cleanup

' Bind to a specific user object.
Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' The code example assumes that the property description has a single value in the directory.
' Be aware that this will implicitly call GetInfo because, at this point, GetInfo
' has not yet been called (implicitly or explicitly) on the usr object.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Change two of the attribute values in the local cache.
usr.Put "cn", "Jeff Smith"
usr.Put "title", "Vice President"
usr.Put "department", "Head Office"
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Initialize the array of properties to pass to GetInfoEx.
PropArray = Array("department", "title")
 
' Get the specified attribute values.
usr.GetInfoEx PropArray, 0

' The specific attributes values were overwritten, but the attribute
' value not retrieved has not changed.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="retrieving-active-directory-constructed-attributes"></a><span data-ttu-id="a0de3-114">Получение Active Directory сконструированных атрибутов</span><span class="sxs-lookup"><span data-stu-id="a0de3-114">Retrieving Active Directory Constructed Attributes</span></span>

<span data-ttu-id="a0de3-115">В Active Directory большинство сконструированных атрибутов извлекается и кэшируется при вызове метода [**iAds. info**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) ([**iAds. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) выполняет неявный вызов **iAds.-info** , если кэш пуст).</span><span class="sxs-lookup"><span data-stu-id="a0de3-115">In Active Directory, most of the constructed attributes are retrieved and cached when the [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method is called ([**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) performs an implicit **IADs.GetInfo** call if the cache is empty).</span></span> <span data-ttu-id="a0de3-116">Однако некоторые сконструированные атрибуты не извлекаются автоматически и не кэшируются, поэтому для их извлечения требуется явно вызывать метод [**iAds. жетинфоекс**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) .</span><span class="sxs-lookup"><span data-stu-id="a0de3-116">Some constructed attributes, however, are not automatically retrieved and cached and, therefore, require that the [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method be called explicitly to retrieve them.</span></span> <span data-ttu-id="a0de3-117">Например, в Active Directory атрибут [**каноникалнаме**](/windows/desktop/ADSchema/a-canonicalname) не извлекается при вызове метода **iAds.** , а метод **iAds. Get** возвратит **\_ свойство E ADS \_ \_ не \_ Найдено**.</span><span class="sxs-lookup"><span data-stu-id="a0de3-117">For example, in Active Directory, the [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) attribute is not retrieved when the **IADs.GetInfo** method is called and **IADs.Get** will return **E\_ADS\_PROPERTY\_NOT\_FOUND**.</span></span> <span data-ttu-id="a0de3-118">Для получения атрибута **каноникалнаме** необходимо вызвать метод **iAds. жетинфоекс** .</span><span class="sxs-lookup"><span data-stu-id="a0de3-118">The **IADs.GetInfoEx** method must be called to retrieve the **canonicalName** attribute.</span></span> <span data-ttu-id="a0de3-119">Эти же сконструированные атрибуты также не будут извлекаться с помощью интерфейса [**иадспропертилист**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) для перечисления атрибутов.</span><span class="sxs-lookup"><span data-stu-id="a0de3-119">These same constructed attributes will also not be retrieved using the [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface to enumerate the attributes.</span></span>

<span data-ttu-id="a0de3-120">Дополнительные сведения и пример кода, демонстрирующий получение всех значений атрибутов, см. в разделе [пример кода для чтения сконструированного атрибута](example-code-for-reading-a-constructed-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="a0de3-120">For more information and a code example that shows how to retrieve all attribute values, see [Example Code for Reading a Constructed Attribute](example-code-for-reading-a-constructed-attribute.md).</span></span>

 

 