---
title: Методы свойств Иадсконтаинер (iAds. h)
description: Методы свойств интерфейса Иадсконтаинер получают или задают свойства, описанные в следующей таблице. Дополнительные сведения и общее обсуждение методов свойств см. в разделе методы свойств интерфейса.
ms.assetid: 74d348bf-7b7f-4971-ba03-f77940600674
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсконтаинер ADSI
topic_type:
- apiref
api_name:
- IADsContainer Property Methods
- IADsContainer.Count
- IADsContainer.get_Count
- IADsContainer.Filter
- IADsContainer.get_Filter
- IADsContainer.put_Filter
- IADsContainer.Hints
- IADsContainer.get_Hints
- IADsContainer.put_Hints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5196addda0d9ff89f8a4976f3197bbeeae07044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136879"
---
# <a name="iadscontainer-property-methods"></a><span data-ttu-id="5690a-105">Методы свойств Иадсконтаинер</span><span class="sxs-lookup"><span data-stu-id="5690a-105">IADsContainer Property Methods</span></span>

<span data-ttu-id="5690a-106">Методы свойств интерфейса [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer) получают или задают свойства, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5690a-106">The property methods of the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="5690a-107">Дополнительные сведения и общее обсуждение методов свойств см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="5690a-107">For more information, and a general discussion about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="5690a-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="5690a-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="5690a-109">**Количество**</span><span class="sxs-lookup"><span data-stu-id="5690a-109">**Count**</span></span>
<span data-ttu-id="5690a-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5690a-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="5690a-111">Возвращает количество элементов в контейнере.</span><span class="sxs-lookup"><span data-stu-id="5690a-111">Retrieves the number of items in the container.</span></span> <span data-ttu-id="5690a-112">Если параметр **Filter** установлен, функция **Count** возвращает только число отфильтрованных элементов.</span><span class="sxs-lookup"><span data-stu-id="5690a-112">When **Filter** is set, **Count** returns only the number of filtered items.</span></span>

<dt>

<span data-ttu-id="5690a-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5690a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5690a-114">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="5690a-114">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="5690a-115">**Фильтр**</span><span class="sxs-lookup"><span data-stu-id="5690a-115">**Filter**</span></span>
<span data-ttu-id="5690a-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5690a-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="5690a-117">Возвращает или задает фильтр, используемый для выбора классов объектов в заданном перечислении.</span><span class="sxs-lookup"><span data-stu-id="5690a-117">Retrieves or sets the filter used to select object classes in a given enumeration.</span></span> <span data-ttu-id="5690a-118">Это массив вариантов, каждый элемент которого является именем класса схемы.</span><span class="sxs-lookup"><span data-stu-id="5690a-118">This is a variant array, each element of which is the name of a schema class.</span></span> <span data-ttu-id="5690a-119">Если параметр **Filter** не установлен или установлен в значение Empty, перечислитель получает все объекты всех классов.</span><span class="sxs-lookup"><span data-stu-id="5690a-119">If **Filter** is not set or set to empty, all objects of all classes are retrieved by the enumerator.</span></span>

<dt>

<span data-ttu-id="5690a-120">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5690a-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5690a-121">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="5690a-121">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Filter(
  [out] VARIANT* pvFilter
);
HRESULT put_Filter(
  [in] VARIANT vFilter
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="5690a-122">**Указания**</span><span class="sxs-lookup"><span data-stu-id="5690a-122">**Hints**</span></span>
<span data-ttu-id="5690a-123"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5690a-123"></dt> <dd> <dl></span></span>

<span data-ttu-id="5690a-124">Массив вариантов строк **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="5690a-124">A variant array of **BSTR** strings.</span></span> <span data-ttu-id="5690a-125">Каждый элемент определяет имя свойства, найденного в определении схемы.</span><span class="sxs-lookup"><span data-stu-id="5690a-125">Each element identifies the name of a property found in the schema definition.</span></span> <span data-ttu-id="5690a-126">Параметр *вхинтс* позволяет клиенту указать, какие атрибуты загружать для каждого перечислимого объекта.</span><span class="sxs-lookup"><span data-stu-id="5690a-126">The *vHints* parameter enables the client to indicate which attributes to load for each enumerated object.</span></span> <span data-ttu-id="5690a-127">Такие данные можно использовать для оптимизации сетевого доступа.</span><span class="sxs-lookup"><span data-stu-id="5690a-127">Such data may be used to optimize network access.</span></span> <span data-ttu-id="5690a-128">Однако конкретная реализация зависит от поставщика и сейчас не используется поставщиком WinNT.</span><span class="sxs-lookup"><span data-stu-id="5690a-128">The exact implementation, however, is provider-specific, and is currently not used by the WinNT provider.</span></span>

<dt>

<span data-ttu-id="5690a-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5690a-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5690a-130">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="5690a-130">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Hints(
  [out] VARIANT* pvHints
);
HRESULT put_Hints(
  [in] VARIANT vHints
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="5690a-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5690a-131">Remarks</span></span>

<span data-ttu-id="5690a-132">Процессы перечисления в разделе [**иадсконтаинер:: Get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) и **иадсконтаинер:: Get \_** выполняются для содержащихся в кэше объектов.</span><span class="sxs-lookup"><span data-stu-id="5690a-132">The enumeration processes under [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) and **IADsContainer::get\_Count** are performed against the contained objects in the cache.</span></span> <span data-ttu-id="5690a-133">Если контейнер содержит большое количество объектов, это может повлиять на производительность.</span><span class="sxs-lookup"><span data-stu-id="5690a-133">When a container contains a large number of objects, the performance may be affected.</span></span> <span data-ttu-id="5690a-134">Чтобы повысить производительность, отключите кэш, настройте соответствующий размер страницы и используйте интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="5690a-134">To enhance performance, turn off the cache, set up an appropriate page size, and use the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span> <span data-ttu-id="5690a-135">По этой причине свойство " **число получаемых \_ объектов** " не поддерживается поставщиком Microsoft LDAP.</span><span class="sxs-lookup"><span data-stu-id="5690a-135">For this reason, the **get\_Count** property is not supported in the Microsoft LDAP provider.</span></span>

## <a name="examples"></a><span data-ttu-id="5690a-136">Примеры</span><span class="sxs-lookup"><span data-stu-id="5690a-136">Examples</span></span>

<span data-ttu-id="5690a-137">В следующем Visual Basic примере кода показано, как можно использовать методы свойств [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="5690a-137">The following Visual Basic code example shows how property methods of [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) can be used.</span></span>


```VB
Dim cont As IADsContainer
Dim usr As IADsUser

On Error GoTo Cleanup
 
Set cont = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
cont.Hints = Array("adminDescription") ' Load this attribute. Optional.
Debug.Print cont.Get("adminDescription")

' Filter users.
cont.Filter = Array("user")

For Each usr In cont
  Debug.Print usr.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set usr = Nothing
```



<span data-ttu-id="5690a-138">В следующем примере кода C++ показано, как можно использовать методы свойств [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="5690a-138">The following C++ code example shows how the property methods of [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) can be used.</span></span> <span data-ttu-id="5690a-139">Для краткости проверка ошибок пропущена.</span><span class="sxs-lookup"><span data-stu-id="5690a-139">For brevity, error checking is omitted.</span></span>


```C++
IADsContainer *pCont;
IADs *pChild;
IADs *pADs;
 
HRESULT hr = ADsGetObject(L"LDAP://OU=Sales,DC=Fabrikam,DC=COM",
                          IID_IADsContainer, 
                          (void**)&pCont);

if(FAILED(hr)){goto Cleanup;}

LPWSTR pszArray[] = { L"adminDescription" };
DWORD dwNumber = sizeof(pszArray)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr( pszArray, dwNumber, &var);
if(FAILED(hr)){goto Cleanup;}

hr = pCont->put_Hints( var );
if(FAILED(hr)){goto Cleanup;}

VariantClear(&var);
 
hr = pCont->QueryInterface(IID_IADs, (void**)pADs);
if(FAILED(hr)){goto Cleanup;}
 
hr = pADs->Get(CComBSTR("adminDescription"), var);
 
LPWSTR pszUsers = {L"user"};
dwNumber = sizeof(pszUsers)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr(pszUsers, dwNumber, &var);
hr = pCont->put_Filter( var );
VariantClear(&var);
 
// Enumerate user objects in the container.
IEnumVARIANT *pEnum = NULL;
hr = ADsBuildEnumerator(pCont, &pEnum);
pCont->Release();    // Not required when users are enumerated.
 
ULONG lFetch;
VariantClear(&var);
while (SUCCEEDED(ADsEnumerateNext(pEnum, 1, &var, &lFetch)) && 
                      lFetch==1) {
    hr = V_DISPATCH(&var)->QueryInterface(IID_IADs, (void**)&pChild)
    if(SUCCEEDED(hr)) {
        BSTR bstrName;
        pChild->get_Name(&bstrName);
        printf("  %S\n", bstrName);
        SysFreeString(bstrName);
        pChild->Release();
    }
    VariantClear(&var);
}
Cleanup:
    if(pADs)
        pADs->Release();

    if(pCont)
        pCont->Release();

    if(pChild)
        pChild->Release();

    VariantClear(&var);
```



## <a name="requirements"></a><span data-ttu-id="5690a-140">Требования</span><span class="sxs-lookup"><span data-stu-id="5690a-140">Requirements</span></span>



| <span data-ttu-id="5690a-141">Требование</span><span class="sxs-lookup"><span data-stu-id="5690a-141">Requirement</span></span> | <span data-ttu-id="5690a-142">Значение</span><span class="sxs-lookup"><span data-stu-id="5690a-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5690a-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5690a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="5690a-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5690a-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5690a-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5690a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="5690a-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5690a-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5690a-147">Header</span><span class="sxs-lookup"><span data-stu-id="5690a-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="5690a-148"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="5690a-148"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="5690a-149">DLL</span><span class="sxs-lookup"><span data-stu-id="5690a-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5690a-150"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5690a-150"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="5690a-151">IID</span><span class="sxs-lookup"><span data-stu-id="5690a-151">IID</span></span><br/>                      | <span data-ttu-id="5690a-152">IID \_ иадсконтаинер определен как 001677D0-FD16-11CE-ABC4-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="5690a-152">IID\_IADsContainer is defined as 001677D0-FD16-11CE-ABC4-02608C9E7553</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="5690a-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5690a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5690a-154">**иадсконтаинер**</span><span class="sxs-lookup"><span data-stu-id="5690a-154">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[<span data-ttu-id="5690a-155">**IDirectorySearch**</span><span class="sxs-lookup"><span data-stu-id="5690a-155">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
</dt> </dl>

 

 





