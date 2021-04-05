---
title: Методы свойств Иадсо (iAds. h)
description: Методы свойств интерфейса Иадсо получают или задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: d4bc1d29-98de-462d-b59c-2bc2641c25a0
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсо ADSI
topic_type:
- apiref
api_name:
- IADsO Property Methods
- IADsO.Description
- IADsO.get_Description
- IADsO.put_Description
- IADsO.FaxNumber
- IADsO.get_FaxNumber
- IADsO.put_FaxNumber
- IADsO.LocalityName
- IADsO.get_LocalityName
- IADsO.put_LocalityName
- IADsO.PostalAddress
- IADsO.get_PostalAddress
- IADsO.put_PostalAddress
- IADsO.TelephoneNumber
- IADsO.get_TelephoneNumber
- IADsO.put_TelephoneNumber
- IADsO.SeeAlso
- IADsO.get_SeeAlso
- IADsO.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09840cf62d6883eb4f5ca326998b697a34698c90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803166"
---
# <a name="iadso-property-methods"></a><span data-ttu-id="37038-105">Методы свойств Иадсо</span><span class="sxs-lookup"><span data-stu-id="37038-105">IADsO Property Methods</span></span>

<span data-ttu-id="37038-106">Методы свойств интерфейса [**иадсо**](/windows/desktop/api/Iads/nn-iads-iadso) получают или задают свойства, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="37038-106">The property methods of the [**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="37038-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="37038-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="37038-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="37038-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="37038-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="37038-109">**Description**</span></span>
<span data-ttu-id="37038-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="37038-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="37038-111">Описание организации.</span><span class="sxs-lookup"><span data-stu-id="37038-111">The description of the organization.</span></span>

<dt>

<span data-ttu-id="37038-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="37038-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="37038-113">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="37038-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="37038-114">**факснумбер**</span><span class="sxs-lookup"><span data-stu-id="37038-114">**FaxNumber**</span></span>
<span data-ttu-id="37038-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="37038-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="37038-116">Номер факса организации.</span><span class="sxs-lookup"><span data-stu-id="37038-116">The facsimile (fax) number of the organization.</span></span>

<dt>

<span data-ttu-id="37038-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="37038-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="37038-118">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="37038-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_FaxNumber(
  [out] BSTR* pbstrFaxNumber
);
HRESULT put_FaxNumber(
  [in] BSTR bstrFaxNumber
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="37038-119">**локалитинаме**</span><span class="sxs-lookup"><span data-stu-id="37038-119">**LocalityName**</span></span>
<span data-ttu-id="37038-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="37038-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="37038-121">Имя места расположения Организации.</span><span class="sxs-lookup"><span data-stu-id="37038-121">The name of the place in which the organization is located.</span></span>

<dt>

<span data-ttu-id="37038-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="37038-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="37038-123">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="37038-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LocalityName(
  [out] BSTR* pbstrLocalityName
);
HRESULT put_LocalityName(
  [in] BSTR bstrLocalityName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="37038-124">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="37038-124">**PostalAddress**</span></span>
<span data-ttu-id="37038-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="37038-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="37038-126">Почтовый адрес Организации.</span><span class="sxs-lookup"><span data-stu-id="37038-126">The postal address of the organization.</span></span>

<dt>

<span data-ttu-id="37038-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="37038-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="37038-128">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="37038-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] BSTR* pbstrPostalAddress
);
HRESULT put_PostalAddress(
  [in] BSTR bstrPostalAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="37038-129">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="37038-129">**SeeAlso**</span></span>
<span data-ttu-id="37038-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="37038-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="37038-131">Массив ADsPath имен других объектов ADSI, которые могут быть связаны с этим объектом.</span><span class="sxs-lookup"><span data-stu-id="37038-131">An array of ADsPath names of other ADSI objects which may be relevant to this object.</span></span>

<dt>

<span data-ttu-id="37038-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="37038-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="37038-133">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="37038-133">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SeeAlso(
  [out] VARIANT* pvSeeAlso
);
HRESULT put_SeeAlso(
  [in] VARIANT vSeeAlso
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="37038-134">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="37038-134">**TelephoneNumber**</span></span>
<span data-ttu-id="37038-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="37038-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="37038-136">Номер телефона Организации.</span><span class="sxs-lookup"><span data-stu-id="37038-136">The telephone number of the organization.</span></span>

<dt>

<span data-ttu-id="37038-137">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="37038-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="37038-138">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="37038-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneNumber(
  [out] BSTR* pbstrTelephoneNumber
);
HRESULT put_TelephoneNumber(
  [in] BSTR bstrTelephoneNumber
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="37038-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="37038-139">Examples</span></span>

<span data-ttu-id="37038-140">В следующем примере кода отображается описание данной Организации.</span><span class="sxs-lookup"><span data-stu-id="37038-140">The following code example displays the description of a given organization.</span></span> <span data-ttu-id="37038-141">Предполагается, что базовая служба каталогов поддерживает группирование объектов каталога по организациям.</span><span class="sxs-lookup"><span data-stu-id="37038-141">It assumes the underlying directory service supports grouping directory objects by organization.</span></span>


```VB
Dim dom As IADsContainer
Dim dso As IADsOpenDSObject
Dim szUsername As String
Dim szPassword As String
On Error GoTo Cleanup

' Insert code to securely retrieve the user name and password
 
Set dso = GetObject("LDAP:")
Set dom = dso.OpenDSObject("LDAP://adsrv1/dc=Fabrikam, dc=Com", _
                           szUsername, szPassword,1)
dom.Filter = Array("organization")
For Each o In dom
    MsgBox "Fax number of " & o.Name & " : " & o.Description
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set dom = Nothing
    Set dso = Nothing
```



## <a name="requirements"></a><span data-ttu-id="37038-142">Требования</span><span class="sxs-lookup"><span data-stu-id="37038-142">Requirements</span></span>



| <span data-ttu-id="37038-143">Требование</span><span class="sxs-lookup"><span data-stu-id="37038-143">Requirement</span></span> | <span data-ttu-id="37038-144">Значение</span><span class="sxs-lookup"><span data-stu-id="37038-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37038-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="37038-145">Minimum supported client</span></span><br/> | <span data-ttu-id="37038-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37038-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="37038-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="37038-147">Minimum supported server</span></span><br/> | <span data-ttu-id="37038-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37038-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="37038-149">Header</span><span class="sxs-lookup"><span data-stu-id="37038-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="37038-150"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="37038-150"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="37038-151">DLL</span><span class="sxs-lookup"><span data-stu-id="37038-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37038-152"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37038-152"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="37038-153">IID</span><span class="sxs-lookup"><span data-stu-id="37038-153">IID</span></span><br/>                      | <span data-ttu-id="37038-154">IID \_ иадсо определен как A1CD2DC6-Effe-11CF-8ABC-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="37038-154">IID\_IADsO is defined as A1CD2DC6-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="37038-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37038-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37038-156">**иадсо**</span><span class="sxs-lookup"><span data-stu-id="37038-156">**IADsO**</span></span>](/windows/desktop/api/Iads/nn-iads-iadso)
</dt> <dt>

[<span data-ttu-id="37038-157">Методы свойств интерфейса</span><span class="sxs-lookup"><span data-stu-id="37038-157">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





