---
title: Методы свойств Иадспропертентри (iAds. h)
description: Предоставьте доступ к следующим свойствам.
ms.assetid: 73b0f6d4-55db-46cf-a781-e10bc4fcf2db
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадспропертентри ADSI
topic_type:
- apiref
api_name:
- IADsPropertyEntry Property Methods
- IADsPropertyEntry.Name
- IADsPropertyEntry.get_Name
- IADsPropertyEntry.put_Name
- IADsPropertyEntry.ADsType
- IADsPropertyEntry.get_ADsType
- IADsPropertyEntry.put_ADsType
- IADsPropertyEntry.ControlCode
- IADsPropertyEntry.get_ControlCode
- IADsPropertyEntry.put_ControlCode
- IADsPropertyEntry.Values
- IADsPropertyEntry.get_Values
- IADsPropertyEntry.put_Values
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e82344b2b659395bb14c0500fde3214530e000
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892645"
---
# <a name="iadspropertyentry-property-methods"></a><span data-ttu-id="eb8c3-104">Методы свойств Иадспропертентри</span><span class="sxs-lookup"><span data-stu-id="eb8c3-104">IADsPropertyEntry Property Methods</span></span>

<span data-ttu-id="eb8c3-105">Методы свойств интерфейса [**иадспропертентри**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) предоставляют доступ к следующим свойствам.</span><span class="sxs-lookup"><span data-stu-id="eb8c3-105">The property methods of the [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) interface provide access to the following properties.</span></span> <span data-ttu-id="eb8c3-106">Дополнительные сведения о методах свойств см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="eb8c3-106">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="eb8c3-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="eb8c3-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="eb8c3-108">**адстипе**</span><span class="sxs-lookup"><span data-stu-id="eb8c3-108">**ADsType**</span></span>
<span data-ttu-id="eb8c3-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="eb8c3-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="eb8c3-110">Тип данных свойства **Name** .</span><span class="sxs-lookup"><span data-stu-id="eb8c3-110">The data type of the **Name** property.</span></span> <span data-ttu-id="eb8c3-111">Значения типа данных определяются в перечислении [**адстипинум**](/windows/win32/api/iads/ne-iads-adstypeenum) .</span><span class="sxs-lookup"><span data-stu-id="eb8c3-111">The values of the data type is defined in the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) enumeration.</span></span>

<dt>

<span data-ttu-id="eb8c3-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="eb8c3-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eb8c3-113">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="eb8c3-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsType(
  [out] LONG* plADsType
);
HRESULT put_ADsType(
  [in] LONG lADsType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb8c3-114">**контролкоде**</span><span class="sxs-lookup"><span data-stu-id="eb8c3-114">**ControlCode**</span></span>
<span data-ttu-id="eb8c3-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="eb8c3-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="eb8c3-116">Константа, указывающая операцию, которая должна быть выполнена над именованным свойством.</span><span class="sxs-lookup"><span data-stu-id="eb8c3-116">A constant that specifies the operation to be performed on the named property.</span></span> <span data-ttu-id="eb8c3-117">Значение определяется в перечислении [**перечисления \_ \_ операции свойства \_ ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) .</span><span class="sxs-lookup"><span data-stu-id="eb8c3-117">The value is defined in the [**ADS\_PROPERTY\_OPERATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) enumeration.</span></span>

<dt>

<span data-ttu-id="eb8c3-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="eb8c3-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eb8c3-119">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="eb8c3-119">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ControlCode(
  [out] LONG* pControlCode
);
HRESULT put_ControlCode(
  [in] LONG lnControlCode
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb8c3-120">**Name**</span><span class="sxs-lookup"><span data-stu-id="eb8c3-120">**Name**</span></span>
<span data-ttu-id="eb8c3-121"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="eb8c3-121"></dt> <dd> <dl></span></span>

<span data-ttu-id="eb8c3-122">Имя записи свойства.</span><span class="sxs-lookup"><span data-stu-id="eb8c3-122">Name of the property entry.</span></span> <span data-ttu-id="eb8c3-123">Это имя должно соответствовать имени атрибута, как определено в схеме.</span><span class="sxs-lookup"><span data-stu-id="eb8c3-123">This name should correspond to the name of an attribute as defined in the schema.</span></span>

<dt>

<span data-ttu-id="eb8c3-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="eb8c3-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eb8c3-125">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="eb8c3-125">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
HRESULT put_Name(
  [in] BSTR bstrName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb8c3-126">**Значения**</span><span class="sxs-lookup"><span data-stu-id="eb8c3-126">**Values**</span></span>
<span data-ttu-id="eb8c3-127"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="eb8c3-127"></dt> <dd> <dl></span></span>

<span data-ttu-id="eb8c3-128">Массив **Variant** .</span><span class="sxs-lookup"><span data-stu-id="eb8c3-128">A **VARIANT** array.</span></span> <span data-ttu-id="eb8c3-129">Каждый элемент в этом массиве представляет значение именованного свойства.</span><span class="sxs-lookup"><span data-stu-id="eb8c3-129">Each element in this array represents a value of the named property.</span></span> <span data-ttu-id="eb8c3-130">Такие значения свойств представлены объектами ADSI, реализующими интерфейсы [**иадспропертивалуе**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) и [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) .</span><span class="sxs-lookup"><span data-stu-id="eb8c3-130">Such property values are represented by ADSI objects implementing the [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) and [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) interfaces.</span></span> <span data-ttu-id="eb8c3-131">Таким образом, массив **вариантов** содержит массив указателей на интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) в объектах ADSI, реализующих интерфейсы **иадспропертивалуе** и **IADsPropertyValue2** .</span><span class="sxs-lookup"><span data-stu-id="eb8c3-131">Therefore, the **VARIANT** array holds an array of pointers to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface on the ADSI objects implementing the **IADsPropertyValue** and **IADsPropertyValue2** interfaces.</span></span>

<dt>

<span data-ttu-id="eb8c3-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="eb8c3-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eb8c3-133">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="eb8c3-133">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Values(
  [out] VARIANT* pvValues
);
HRESULT put_Values(
  [in] VARIANT vValues
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="eb8c3-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb8c3-134">Remarks</span></span>

<span data-ttu-id="eb8c3-135">Каждый метод свойства поддерживает стандартные возвращаемые значения **HRESULT** , включая S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="eb8c3-135">Each property method supports the standard **HRESULT** return values, including S\_OK.</span></span> <span data-ttu-id="eb8c3-136">Дополнительные сведения о других возвращаемых значениях см. в разделе [коды ошибок ADSI](adsi-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="eb8c3-136">For more information about other return values, see [ADSI Error Codes](adsi-error-codes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="eb8c3-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="eb8c3-137">Examples</span></span>

<span data-ttu-id="eb8c3-138">В следующем примере кода показано, как получить именованное свойство из кэша и создать новую запись свойства.</span><span class="sxs-lookup"><span data-stu-id="eb8c3-138">The following code example shows how to retrieve a named property from the cache and create a new property entry.</span></span>


```VB
 
Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim propVal As IADsPropertyValue

On Error GoTo Cleanup

'------------------------------------------------------------
'----- Getting IADsPropertyEntry ----------------------------
'------------------------------------------------------------
 
' Create the property list object.
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
propList.GetInfo
 
' Get a named property entry object.
Set propEntry = propList.GetPropertyItem("dc", ADSTYPE_CASE_IGNORE_STRING)

' Insert code to do something with propEntry
Set propEntry = Nothing
 
'------------------------------------------------------------
'---- Setting IADsPropertyEntry -----------------------------
'------------------------------------------------------------
 
' Create a property value object.
Set propVal = New PropertyValue
 
'---- Property Value -----
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
 
'---- Create a new Property Entry ----
Set propEntry = New PropertyEntry
propEntry.Name = "adminDescription"
propEntry.Values = Array(propVal)
propEntry.ControlCode = ADS_PROPERTY_UPDATE
propEntry.ADsType = ADS_CASE_IGNORE_STRING
 
' ---- Put the newly created property entry to the cache ----
propList.PutPropertyItem (propEntry)
 
' Commit the entry to the directory store.
propList.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set propList = Nothing
    Set propEntry = Nothing
    Set propVal = Nothing
```



<span data-ttu-id="eb8c3-139">В следующем примере кода показано, как получить именованное свойство из кэша.</span><span class="sxs-lookup"><span data-stu-id="eb8c3-139">The following code example shows how to get a named property from a cache.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
IADsPropertyList *pList = NULL;
IADsPropertyEntry *pEntry = NULL;
IADs *pObj = NULL;
VARIANT var;
long valType = ADSTYPE_CASE_IGNORE_STRING;
 
VariantInit(&var);
 
// Bind to directory object.
HRESULT hr = ADsGetObject(L"LDAP://dc01/DC=Fabrikam,DC=com",
                          IID_IADsPropertyList,
                          (void**)&pList);
if(FAILED(hr)){return;}
 
// Initialize the property cache.
hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
if(FAILED(hr)){goto Cleanup;}
pObj->GetInfo();
pObj->Release();
 
// Get a property entry.
hr = pList->GetPropertyItem(CComBSTR("description"), valType, &var);
pList->Release();
if(FAILED(hr)){goto Cleanup;}
hr = V_DISPATCH(&var)->QueryInterface(IID_IADsPropertyEntry,
                                      (void**)&pEntry);
VariantClear(&var);
if(FAILED(hr)){goto Cleanup;}
 
// Get the name and the type of the property entry.
BSTR nm = NULL;
hr = pEntry->get_Name(&nm);
printf("Property name = %S\n",nm);
VariantClear(&var);
long at;
hr = pEntry->get_ADsType(&at);
printf("Property type = %d\n",a);

Cleanup:
    if(nm)
        SysFreeString(nm);

    if(pList)
        pList->Release();

    if(pEntry)
        pEntry->Release();

    if(pObj)
        pObj->Release();

    VariantClear(&var);
```



## <a name="requirements"></a><span data-ttu-id="eb8c3-140">Требования</span><span class="sxs-lookup"><span data-stu-id="eb8c3-140">Requirements</span></span>



| <span data-ttu-id="eb8c3-141">Требование</span><span class="sxs-lookup"><span data-stu-id="eb8c3-141">Requirement</span></span> | <span data-ttu-id="eb8c3-142">Значение</span><span class="sxs-lookup"><span data-stu-id="eb8c3-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb8c3-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb8c3-143">Minimum supported client</span></span><br/> | <span data-ttu-id="eb8c3-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb8c3-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb8c3-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb8c3-145">Minimum supported server</span></span><br/> | <span data-ttu-id="eb8c3-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb8c3-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb8c3-147">Header</span><span class="sxs-lookup"><span data-stu-id="eb8c3-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb8c3-148"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb8c3-148"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="eb8c3-149">DLL</span><span class="sxs-lookup"><span data-stu-id="eb8c3-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb8c3-150"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb8c3-150"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="eb8c3-151">IID</span><span class="sxs-lookup"><span data-stu-id="eb8c3-151">IID</span></span><br/>                      | <span data-ttu-id="eb8c3-152">IID \_ иадспропертентри определен как 05792C8E-941F-11D0-8529-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="eb8c3-152">IID\_IADsPropertyEntry is defined as 05792C8E-941F-11D0-8529-00C04FD8D503</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="eb8c3-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb8c3-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb8c3-154">**\_ \_ перечисление операций свойства ADS \_**</span><span class="sxs-lookup"><span data-stu-id="eb8c3-154">**ADS\_PROPERTY\_OPERATION\_ENUM**</span></span>](/windows/win32/api/iads/ne-iads-ads_property_operation_enum)
</dt> <dt>

[<span data-ttu-id="eb8c3-155">Коды ошибок ADSI</span><span class="sxs-lookup"><span data-stu-id="eb8c3-155">ADSI Error Codes</span></span>](adsi-error-codes.md)
</dt> <dt>

[<span data-ttu-id="eb8c3-156">**адстипинум**</span><span class="sxs-lookup"><span data-stu-id="eb8c3-156">**ADSTYPEENUM**</span></span>](/windows/win32/api/iads/ne-iads-adstypeenum)
</dt> <dt>

[<span data-ttu-id="eb8c3-157">**иадспропертентри**</span><span class="sxs-lookup"><span data-stu-id="eb8c3-157">**IADsPropertyEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)
</dt> <dt>

[<span data-ttu-id="eb8c3-158">**иадспропертивалуе**</span><span class="sxs-lookup"><span data-stu-id="eb8c3-158">**IADsPropertyValue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)
</dt> <dt>

[<span data-ttu-id="eb8c3-159">**IADsPropertyValue2**</span><span class="sxs-lookup"><span data-stu-id="eb8c3-159">**IADsPropertyValue2**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)
</dt> <dt>

[<span data-ttu-id="eb8c3-160">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="eb8c3-160">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> </dl>

 

