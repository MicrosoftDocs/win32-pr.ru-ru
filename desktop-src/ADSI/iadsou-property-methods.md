---
title: Методы свойств Иадсау (iAds. h)
description: Методы свойств интерфейса Иадсау получают или задают свойства, перечисленные в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 8cb84972-733b-47ca-8647-1b7a85c97021
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсау ADSI
topic_type:
- apiref
api_name:
- IADsOU Property Methods
- IADsOU.BusinessCategory
- IADsOU.get_BusinessCategory
- IADsOU.put_BusinessCategory
- IADsOU.Description
- IADsOU.get_Description
- IADsOU.put_Description
- IADsOU.FaxNumber
- IADsOU.get_FaxNumber
- IADsOU.put_FaxNumber
- IADsOU.LocalityName
- IADsOU.get_LocalityName
- IADsOU.put_LocalityName
- IADsOU.PostalAddress
- IADsOU.get_PostalAddress
- IADsOU.put_PostalAddress
- IADsOU.TelephoneNumber
- IADsOU.get_TelephoneNumber
- IADsOU.put_TelephoneNumber
- IADsOU.SeeAlso
- IADsOU.get_SeeAlso
- IADsOU.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0ce30fad6a690a26a8e16b817b77b129dee25f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654612"
---
# <a name="iadsou-property-methods"></a><span data-ttu-id="dd549-105">Методы свойств Иадсау</span><span class="sxs-lookup"><span data-stu-id="dd549-105">IADsOU Property Methods</span></span>

<span data-ttu-id="dd549-106">Методы свойств интерфейса [**иадсау**](/windows/desktop/api/Iads/nn-iads-iadsou) получают или задают свойства, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="dd549-106">The property methods of the [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou) interface get or set the properties listed in the following table.</span></span> <span data-ttu-id="dd549-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="dd549-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="dd549-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="dd549-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="dd549-109">**бусинесскатегори**</span><span class="sxs-lookup"><span data-stu-id="dd549-109">**BusinessCategory**</span></span>
<span data-ttu-id="dd549-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="dd549-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="dd549-111">Строка, содержащая общую бизнес-функцию или функции, выполняемые подразделением, например "Бухгалтерия".</span><span class="sxs-lookup"><span data-stu-id="dd549-111">A string that contains the general business function or functions performed by the organizational unit, for example "Accounting".</span></span>

<dt>

<span data-ttu-id="dd549-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd549-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dd549-113">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="dd549-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BusinessCategory(
  [out] BSTR* pbstrBusinessCategory
);
HRESULT put_BusinessCategory(
  [in] BSTR bstrBusinessCategory
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="dd549-114">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dd549-114">**Description**</span></span>
<span data-ttu-id="dd549-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="dd549-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="dd549-116">Строка, содержащая текстовое описание подразделения.</span><span class="sxs-lookup"><span data-stu-id="dd549-116">A string that contains a textual description of the organizational unit.</span></span>

<dt>

<span data-ttu-id="dd549-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd549-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dd549-118">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="dd549-118">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="dd549-119">**факснумбер**</span><span class="sxs-lookup"><span data-stu-id="dd549-119">**FaxNumber**</span></span>
<span data-ttu-id="dd549-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="dd549-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="dd549-121">Строка, содержащая номер факса подразделения.</span><span class="sxs-lookup"><span data-stu-id="dd549-121">A string that contains the facsimile number of the organizational unit.</span></span>

<dt>

<span data-ttu-id="dd549-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd549-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dd549-123">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="dd549-123">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="dd549-124">**локалитинаме**</span><span class="sxs-lookup"><span data-stu-id="dd549-124">**LocalityName**</span></span>
<span data-ttu-id="dd549-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="dd549-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="dd549-126">Строка, содержащая имя географического региона подразделения.</span><span class="sxs-lookup"><span data-stu-id="dd549-126">A string that contains the name of the geographic region of the organizational unit.</span></span>

<dt>

<span data-ttu-id="dd549-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd549-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dd549-128">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="dd549-128">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="dd549-129">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="dd549-129">**PostalAddress**</span></span>
<span data-ttu-id="dd549-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="dd549-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="dd549-131">Строка, содержащая почтовый адрес подразделения.</span><span class="sxs-lookup"><span data-stu-id="dd549-131">A string that contains the postal address of the organizational unit.</span></span>

<dt>

<span data-ttu-id="dd549-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd549-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dd549-133">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="dd549-133">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="dd549-134">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="dd549-134">**SeeAlso**</span></span>
<span data-ttu-id="dd549-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="dd549-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="dd549-136">Массив строк, содержащий отличительные имена других объектов каталога, которые могут быть связаны с этим объектом.</span><span class="sxs-lookup"><span data-stu-id="dd549-136">An array of strings that contains the distinguished names of other directory objects which may be relevant to this object.</span></span>

<dt>

<span data-ttu-id="dd549-137">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd549-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dd549-138">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="dd549-138">Scripting data type: **VARIANT**</span></span>
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

<span data-ttu-id="dd549-139">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="dd549-139">**TelephoneNumber**</span></span>
<span data-ttu-id="dd549-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="dd549-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="dd549-141">Строка, содержащая номер телефона подразделения.</span><span class="sxs-lookup"><span data-stu-id="dd549-141">A string that contains the telephone number of the organizational unit.</span></span>

<dt>

<span data-ttu-id="dd549-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd549-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dd549-143">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="dd549-143">Scripting data type: **BSTR**</span></span>
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

 

## <a name="examples"></a><span data-ttu-id="dd549-144">Примеры</span><span class="sxs-lookup"><span data-stu-id="dd549-144">Examples</span></span>

<span data-ttu-id="dd549-145">В следующем примере кода отображаются **бусинесскатегори** и **Описание** всех единиц Организации в контейнере.</span><span class="sxs-lookup"><span data-stu-id="dd549-145">The following code example displays the **BusinessCategory** and **Description** of all organization units in a container.</span></span> <span data-ttu-id="dd549-146">Предполагается, что базовая служба каталогов поддерживает группирование объектов каталога по подразделениям.</span><span class="sxs-lookup"><span data-stu-id="dd549-146">It assumes that the underlying directory service supports grouping of directory objects by organization unit.</span></span>


```VB
Dim dom As IADsContainer
Dim ou As IADsOU

' Bind to the container.
Set dom = GetObject("LDAP://server1/domain1")

' Filter out all objects that are not of class "organizationalUnit".
dom.filter = Array("organizationalUnit")

' Enumerate the organizational units in the container and display  
' the BusinessCategory and Description properties of each OU.
For Each ou In dom
    MsgBox ou.BusinessCategory & ": " & ou.Description
Next
```



## <a name="requirements"></a><span data-ttu-id="dd549-147">Требования</span><span class="sxs-lookup"><span data-stu-id="dd549-147">Requirements</span></span>



| <span data-ttu-id="dd549-148">Требование</span><span class="sxs-lookup"><span data-stu-id="dd549-148">Requirement</span></span> | <span data-ttu-id="dd549-149">Значение</span><span class="sxs-lookup"><span data-stu-id="dd549-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd549-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd549-150">Minimum supported client</span></span><br/> | <span data-ttu-id="dd549-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd549-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dd549-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd549-152">Minimum supported server</span></span><br/> | <span data-ttu-id="dd549-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd549-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dd549-154">Header</span><span class="sxs-lookup"><span data-stu-id="dd549-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd549-155"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd549-155"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="dd549-156">DLL</span><span class="sxs-lookup"><span data-stu-id="dd549-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd549-157"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd549-157"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="dd549-158">IID</span><span class="sxs-lookup"><span data-stu-id="dd549-158">IID</span></span><br/>                      | <span data-ttu-id="dd549-159">IID \_ иадсау определен как A2F733B8-Effe-11CF-8ABC-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="dd549-159">IID\_IADsOU is defined as A2F733B8-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="dd549-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd549-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd549-161">**иадсау**</span><span class="sxs-lookup"><span data-stu-id="dd549-161">**IADsOU**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsou)
</dt> <dt>

[<span data-ttu-id="dd549-162">Методы свойств интерфейса</span><span class="sxs-lookup"><span data-stu-id="dd549-162">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





