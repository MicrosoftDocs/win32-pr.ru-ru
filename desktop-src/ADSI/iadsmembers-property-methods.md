---
title: Методы свойств Иадсмемберс (iAds. h)
description: Методы интерфейса Иадсмемберс считывают и записывают свойства, описанные в этом разделе. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: ed4e98e5-053c-4d3b-bcd0-3add96bbe120
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсмемберс ADSI
topic_type:
- apiref
api_name:
- IADsMembers Property Methods
- IADsMembers.Count
- IADsMembers.get_Count
- IADsMembers.Filter
- IADsMembers.get_Filter
- IADsMembers.put_Filter
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af047d6fe52fdd7d808b1d7e5dbfb35303d3ff59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654615"
---
# <a name="iadsmembers-property-methods"></a><span data-ttu-id="ec0c5-105">Методы свойств Иадсмемберс</span><span class="sxs-lookup"><span data-stu-id="ec0c5-105">IADsMembers Property Methods</span></span>

<span data-ttu-id="ec0c5-106">Методы интерфейса [**иадсмемберс**](/windows/desktop/api/Iads/nn-iads-iadsmembers) считывают и записывают свойства, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="ec0c5-106">The methods of the [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="ec0c5-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="ec0c5-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ec0c5-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="ec0c5-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="ec0c5-109">**Количество**</span><span class="sxs-lookup"><span data-stu-id="ec0c5-109">**Count**</span></span>
<span data-ttu-id="ec0c5-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ec0c5-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="ec0c5-111">Указывает количество элементов в контейнере.</span><span class="sxs-lookup"><span data-stu-id="ec0c5-111">Indicates the number of items in the container.</span></span> <span data-ttu-id="ec0c5-112">Если фильтр установлен, то функция Count возвращает только число элементов, соответствующих описанию фильтра.</span><span class="sxs-lookup"><span data-stu-id="ec0c5-112">If the filter is set then count returns only the number of items that fit the filter description.</span></span>

<dt>

<span data-ttu-id="ec0c5-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ec0c5-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec0c5-114">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="ec0c5-114">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCountr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec0c5-115">**Фильтр**</span><span class="sxs-lookup"><span data-stu-id="ec0c5-115">**Filter**</span></span>
<span data-ttu-id="ec0c5-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ec0c5-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="ec0c5-117">Указывает фильтр.</span><span class="sxs-lookup"><span data-stu-id="ec0c5-117">Indicates the filter.</span></span> <span data-ttu-id="ec0c5-118">Синтаксис записей в массиве фильтров совпадает с фильтром, используемым в интерфейсе [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="ec0c5-118">The syntax of the entries in the filter array is the same as the Filter used on the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface.</span></span>

<dt>

<span data-ttu-id="ec0c5-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ec0c5-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ec0c5-120">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ec0c5-120">Scripting data type: **VARIANT**</span></span>
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


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="ec0c5-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec0c5-121">Remarks</span></span>

<span data-ttu-id="ec0c5-122">Поставщики систем ADSI не поддерживают метод свойства **иадсмемберс:: Get \_ Count** .</span><span class="sxs-lookup"><span data-stu-id="ec0c5-122">The ADSI system providers do not support the **IADsMembers::get\_Count** property method.</span></span>

## <a name="examples"></a><span data-ttu-id="ec0c5-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="ec0c5-123">Examples</span></span>

<span data-ttu-id="ec0c5-124">В следующем примере кода показано, как использовать методы свойств этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ec0c5-124">The following code example shows how to use the property methods of this interface.</span></span>


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://myComputer/someGroup")
grp.members.filter = Array("user")
For Each usr In grp.Members
    MsgBox usr.Name & "," & usr.Class & "," & usr.AdsPath
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



<span data-ttu-id="ec0c5-125">В следующем примере кода используется метод **\_ фильтра иадсмемберс::p UT** для подготовки к перечислению коллекции членов группы.</span><span class="sxs-lookup"><span data-stu-id="ec0c5-125">The following code example uses the **IADsMembers::put\_Filter** method to prepare for an enumeration of the collection of members of a group.</span></span>


```C++
IADsGroup *pGroup;
HRESULT hr = S_OK;

LPWSTR grpPath = L"WinNT://myComputer/someGroup";
hr = ADsGetObject(grpPath,IID_IADsGroup,(void**)&pGroup);
if(FAILED(hr)){goto Cleanup;}

IADsMembers *pMembers;
hr = pGroup->Members(&pMembers);
if(FAILED(hr)){goto Cleanup;}

hr = pGroup->Release();

SAFEARRAY *sa = CreateSafeArray(L"user");
hr = pMembers->put_Filter(sa);
if(FAILED(hr)){goto Cleanup;}

hr = EnumMembers(pMembers);    // For more information, and a 
                               // code example, see 
                               // IADsMembers::get__NewEnum.
if(FAILED(hr)){goto Cleanup;}

Cleanup:
    if(pGroup) pGroup->Release();
    if(pMembers) pMembers->Release();
    return hr;
```



## <a name="requirements"></a><span data-ttu-id="ec0c5-126">Требования</span><span class="sxs-lookup"><span data-stu-id="ec0c5-126">Requirements</span></span>



| <span data-ttu-id="ec0c5-127">Требование</span><span class="sxs-lookup"><span data-stu-id="ec0c5-127">Requirement</span></span> | <span data-ttu-id="ec0c5-128">Значение</span><span class="sxs-lookup"><span data-stu-id="ec0c5-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec0c5-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec0c5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ec0c5-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec0c5-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ec0c5-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec0c5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ec0c5-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec0c5-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ec0c5-133">Header</span><span class="sxs-lookup"><span data-stu-id="ec0c5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec0c5-134"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec0c5-134"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="ec0c5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ec0c5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec0c5-136"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec0c5-136"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="ec0c5-137">IID</span><span class="sxs-lookup"><span data-stu-id="ec0c5-137">IID</span></span><br/>                      | <span data-ttu-id="ec0c5-138">IID \_ иадсмемберс определен как 451A0030-72EC-11CF-B03B-00AA006E0975</span><span class="sxs-lookup"><span data-stu-id="ec0c5-138">IID\_IADsMembers is defined as 451A0030-72EC-11CF-B03B-00AA006E0975</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="ec0c5-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec0c5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec0c5-140">**иадсконтаинер**</span><span class="sxs-lookup"><span data-stu-id="ec0c5-140">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[<span data-ttu-id="ec0c5-141">**Иадсмемберс:: Get \_ \_ NewEnum**</span><span class="sxs-lookup"><span data-stu-id="ec0c5-141">**IADsMembers::get\_\_NewEnum**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsmembers-get__newenum)
</dt> <dt>

[<span data-ttu-id="ec0c5-142">**иадсмемберс**</span><span class="sxs-lookup"><span data-stu-id="ec0c5-142">**IADsMembers**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsmembers)
</dt> <dt>

[<span data-ttu-id="ec0c5-143">Методы свойств интерфейса</span><span class="sxs-lookup"><span data-stu-id="ec0c5-143">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





