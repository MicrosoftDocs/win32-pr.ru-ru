---
title: Методы свойств Иадслокалити (iAds. h)
description: Методы интерфейса Иадслокалити считывают и записывают свойства, описанные в этом разделе. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 5d1cea40-62fb-49d4-857f-4563e9db7f51
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадслокалити ADSI
topic_type:
- apiref
api_name:
- IADsLocality Property Methods
- IADsLocality.Description
- IADsLocality.get_Description
- IADsLocality.put_Description
- IADsLocality.LocalityName
- IADsLocality.get_LocalityName
- IADsLocality.put_LocalityName
- IADsLocality.PostalAddress
- IADsLocality.get_PostalAddress
- IADsLocality.put_PostalAddress
- IADsLocality.SeeAlso
- IADsLocality.get_SeeAlso
- IADsLocality.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34023f0af5365deb4f023d53a843dcf688c40afd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989096"
---
# <a name="iadslocality-property-methods"></a><span data-ttu-id="3da1a-105">Методы свойств Иадслокалити</span><span class="sxs-lookup"><span data-stu-id="3da1a-105">IADsLocality Property Methods</span></span>

<span data-ttu-id="3da1a-106">Методы интерфейса [**иадслокалити**](/windows/desktop/api/Iads/nn-iads-iadslocality) считывают и записывают свойства, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="3da1a-106">The methods of the [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="3da1a-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="3da1a-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="3da1a-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="3da1a-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="3da1a-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3da1a-109">**Description**</span></span>
<span data-ttu-id="3da1a-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3da1a-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="3da1a-111">Указывает текст, описывающий локальность.</span><span class="sxs-lookup"><span data-stu-id="3da1a-111">Indicates the text that describes the locality.</span></span>

<dt>

<span data-ttu-id="3da1a-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3da1a-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3da1a-113">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="3da1a-113">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="3da1a-114">**локалитинаме**</span><span class="sxs-lookup"><span data-stu-id="3da1a-114">**LocalityName**</span></span>
<span data-ttu-id="3da1a-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3da1a-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="3da1a-116">Указывает имя географического региона, представленного этим объектом расположения.</span><span class="sxs-lookup"><span data-stu-id="3da1a-116">Indicates the name of the geographical region as represented by this locality object.</span></span>

<dt>

<span data-ttu-id="3da1a-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3da1a-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3da1a-118">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="3da1a-118">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="3da1a-119">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="3da1a-119">**PostalAddress**</span></span>
<span data-ttu-id="3da1a-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3da1a-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="3da1a-121">Указывает основной почтовый адрес в локальной области.</span><span class="sxs-lookup"><span data-stu-id="3da1a-121">Indicates the main postal address of the locality.</span></span>

<dt>

<span data-ttu-id="3da1a-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3da1a-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3da1a-123">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="3da1a-123">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="3da1a-124">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="3da1a-124">**SeeAlso**</span></span>
<span data-ttu-id="3da1a-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3da1a-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="3da1a-126">Указывает массив ADsPathх имен объектов каталога, относящихся к этому объекту.</span><span class="sxs-lookup"><span data-stu-id="3da1a-126">Indicates an array of ADsPath names of directory objects relevant to this object.</span></span>

<dt>

<span data-ttu-id="3da1a-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3da1a-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3da1a-128">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="3da1a-128">Scripting data type: **VARIANT**</span></span>
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


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="3da1a-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="3da1a-129">Examples</span></span>

<span data-ttu-id="3da1a-130">В следующем примере кода отображаются данные о локализации объекта контейнера.</span><span class="sxs-lookup"><span data-stu-id="3da1a-130">The following code example displays the locality data of a container object.</span></span> <span data-ttu-id="3da1a-131">Предполагается, что для объекта-контейнера был создан объект Localization с именем «Милокалити», а свойства были заданы.</span><span class="sxs-lookup"><span data-stu-id="3da1a-131">It assumes that a locality object, named "myLocality", has been created for the container object and the properties have been set.</span></span>


```VB
Dim dom As IADsContainer
Dim loc As IADsLocality
On Error GoTo Cleanup
 
Set dom = getObject("LDAP://adsrv1/dc=Fabrikam, dc=Com")
Set loc = dom.GetObject("locality","L=myLocality")
Debug.Print loc.Name
Debug.Print loc.LocalityName
Debug.Print loc.Description
Debug.Print loc.PostalAddress
Debug.Print loc.SeeAlso

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set dom = Nothing
    Set loc = Nothing
```



## <a name="requirements"></a><span data-ttu-id="3da1a-132">Требования</span><span class="sxs-lookup"><span data-stu-id="3da1a-132">Requirements</span></span>



| <span data-ttu-id="3da1a-133">Требование</span><span class="sxs-lookup"><span data-stu-id="3da1a-133">Requirement</span></span> | <span data-ttu-id="3da1a-134">Значение</span><span class="sxs-lookup"><span data-stu-id="3da1a-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3da1a-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3da1a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3da1a-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3da1a-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3da1a-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3da1a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3da1a-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3da1a-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3da1a-139">Header</span><span class="sxs-lookup"><span data-stu-id="3da1a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="3da1a-140"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="3da1a-140"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="3da1a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3da1a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3da1a-142"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3da1a-142"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="3da1a-143">IID</span><span class="sxs-lookup"><span data-stu-id="3da1a-143">IID</span></span><br/>                      | <span data-ttu-id="3da1a-144">IID \_ иадслокалити определен как A05E03A2-Effe-11CF-8ABC-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="3da1a-144">IID\_IADsLocality is defined as A05E03A2-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="3da1a-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3da1a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3da1a-146">**IADs**</span><span class="sxs-lookup"><span data-stu-id="3da1a-146">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="3da1a-147">**иадслокалити**</span><span class="sxs-lookup"><span data-stu-id="3da1a-147">**IADsLocality**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslocality)
</dt> <dt>

[<span data-ttu-id="3da1a-148">Методы свойств интерфейса</span><span class="sxs-lookup"><span data-stu-id="3da1a-148">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





