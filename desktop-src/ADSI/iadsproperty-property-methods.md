---
title: Методы свойств Иадспроперти (iAds. h)
description: Чтение и запись свойств, описанных в следующей таблице.
ms.assetid: dd348a3c-0386-4fa2-984d-cdea6f09bd72
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадспроперти ADSI
topic_type:
- apiref
api_name:
- IADsProperty Property Methods
- IADsProperty.OID
- IADsProperty.get_OID
- IADsProperty.put_OID
- IADsProperty.Syntax
- IADsProperty.get_Syntax
- IADsProperty.put_Syntax
- IADsProperty.MaxRange
- IADsProperty.get_MaxRange
- IADsProperty.put_MaxRange
- IADsProperty.MinRange
- IADsProperty.get_MinRange
- IADsProperty.put_MinRange
- IADsProperty.MultiValued
- IADsProperty.get_MultiValued
- IADsProperty.put_MultiValued
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 233bd5411e1c82956ef745255418a1b176af5900
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654433"
---
# <a name="iadsproperty-property-methods"></a><span data-ttu-id="89aa5-104">Методы свойств Иадспроперти</span><span class="sxs-lookup"><span data-stu-id="89aa5-104">IADsProperty Property Methods</span></span>

<span data-ttu-id="89aa5-105">Методы свойств интерфейса [**иадспроперти**](/windows/desktop/api/Iads/nn-iads-iadsproperty) считывают и записывают свойства, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="89aa5-105">The property methods of the [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) interface read and write the properties described in the following table.</span></span> <span data-ttu-id="89aa5-106">Дополнительные сведения о методах свойств см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="89aa5-106">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="89aa5-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="89aa5-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="89aa5-108">**максранже**</span><span class="sxs-lookup"><span data-stu-id="89aa5-108">**MaxRange**</span></span>
<span data-ttu-id="89aa5-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="89aa5-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="89aa5-110">Верхний предел значений.</span><span class="sxs-lookup"><span data-stu-id="89aa5-110">Upper limit of values.</span></span>

<dt>

<span data-ttu-id="89aa5-111">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="89aa5-111">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="89aa5-112">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="89aa5-112">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxRange(
  [out] LONG* lnMaxRange
);
HRESULT put_MaxRange(
  [in] LONG lnMaxRange
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="89aa5-113">**минранже**</span><span class="sxs-lookup"><span data-stu-id="89aa5-113">**MinRange**</span></span>
<span data-ttu-id="89aa5-114"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="89aa5-114"></dt> <dd> <dl></span></span>

<span data-ttu-id="89aa5-115">Нижняя граница значений.</span><span class="sxs-lookup"><span data-stu-id="89aa5-115">Lower limit of values.</span></span>

<dt>

<span data-ttu-id="89aa5-116">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="89aa5-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="89aa5-117">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="89aa5-117">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinRange(
  [out] LONG* lnMinRange
);
HRESULT put_MinRange(
  [in] LONG lnMinRange
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="89aa5-118">**Многозначных**</span><span class="sxs-lookup"><span data-stu-id="89aa5-118">**MultiValued**</span></span>
<span data-ttu-id="89aa5-119"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="89aa5-119"></dt> <dd> <dl></span></span>

<span data-ttu-id="89aa5-120">Поддерживает ли свойство одно или несколько значений.</span><span class="sxs-lookup"><span data-stu-id="89aa5-120">Whether property supports single or multiple values.</span></span>

<dt>

<span data-ttu-id="89aa5-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="89aa5-121">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="89aa5-122">Тип данных скрипта: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="89aa5-122">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MultiValued(
  [out] VARIANT_BOOL* fMultivalued
);
HRESULT put_MultiValued(
  [in] VARIANT_BOOL fMultivalued
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="89aa5-123">**КОДА**</span><span class="sxs-lookup"><span data-stu-id="89aa5-123">**OID**</span></span>
<span data-ttu-id="89aa5-124"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="89aa5-124"></dt> <dd> <dl></span></span>

<span data-ttu-id="89aa5-125">Идентификатор объекта, зависящий от каталога.</span><span class="sxs-lookup"><span data-stu-id="89aa5-125">Directory-specific object identifier.</span></span>

<dt>

<span data-ttu-id="89aa5-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="89aa5-126">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="89aa5-127">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="89aa5-127">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* bstrOID
);
HRESULT put_OID(
  [out] BSTR* bstrOID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="89aa5-128">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="89aa5-128">**Syntax**</span></span>
<span data-ttu-id="89aa5-129"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="89aa5-129"></dt> <dd> <dl></span></span>

<span data-ttu-id="89aa5-130">Относительный путь к объекту синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="89aa5-130">Relative path of syntax object.</span></span>

<dt>

<span data-ttu-id="89aa5-131">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="89aa5-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="89aa5-132">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="89aa5-132">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Syntax(
  [out] BSTR* bstrSyntax
);
HRESULT put_Syntax(
  [in] BSTR* bstrSyntax
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="89aa5-133">Примеры</span><span class="sxs-lookup"><span data-stu-id="89aa5-133">Examples</span></span>

<span data-ttu-id="89aa5-134">В следующем примере кода проверяется атрибут **операционной** системы компьютера в сети с помощью поставщика WinNT.</span><span class="sxs-lookup"><span data-stu-id="89aa5-134">The following code example examines the **OperatingSystem** attribute of a computer on a network through the WinNT provider.</span></span>


```VB
Dim obj As IADs
Dim cl As IADsClass
Dim pr As IADsProperty
Dim sc As IADsContainer

On Error GoTo Cleanup
 
Set obj = GetObject("WinNT://myMachine,computer")
Set cl = GetObject(obj.Schema)
Set sc = GetObject(cl.Parent)
Set pr = sc.GetObject("Property","OperatingSystem")
 
MsgBox "Attribute:  " & pr.Name
MsgBox "Syntax:     " & pr.Syntax
MsgBox "MaxRange:   " & pr.MaxRange
MsgBox "MinRange:   " & pr.MinRange
MsgBox "Multivalued:" & pr.Multivalued

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cl = Nothing
    Set pr = Nothing
    Set sc = Nothing
```



<span data-ttu-id="89aa5-135">В следующем примере кода проверяется атрибут **операционной** системы компьютера в сети с помощью поставщика WinNT.</span><span class="sxs-lookup"><span data-stu-id="89aa5-135">The following code example examines the **OperatingSystem** attribute of a computer on a network through the WinNT provider.</span></span> <span data-ttu-id="89aa5-136">Для краткости проверка ошибок пропущена.</span><span class="sxs-lookup"><span data-stu-id="89aa5-136">For brevity, error checking is omitted.</span></span>


```C++
IADs *pADs = NULL;
IADsClass *pCls = NULL;
IADsProperty* pProp = NULL;
IADsContainer *pCont = NULL;
long lval;
short bval;
HRESULT hr = CoInitialize(NULL);
 
hr = ADsGetObject(L"WinNT://myMachine,computer",
                  IID_IADs, (void**)&pADs);
if(FAILED(hr))
    goto Cleanup;

BSTR bstr;
hr = pADs->get_Schema(&bstr);
if(FAILED(hr))
    goto Cleanup;

hr = ADsGetObject(bstr, IID_IADsClass, (void**)&pCls);
hr = pCls->get_Parent(&bstr);
if(FAILED(hr))
    goto Cleanup;

hr = ADsGetObject(bstr, IID_IADsContainer, (void**)&pCont);
if(FAILED(hr))
    goto Cleanup;
SysFreeString(bstr);

hr = pCont->GetObject(CComBSTR("Property"), CComBSTR("OperatingSystem"), (IDispatch**)&pProp);
if(FAILED(hr))
    goto Cleanup;

hr = pProp->get_Name(&bstr);
if(FAILED(hr))
    goto Cleanup;
printf(" Name : %S\n",bstr);
SysFreeString(bstr);

hr = pProp->get_Syntax(&bstr);
if(FAILED(hr))
    goto Cleanup;
printf(" Syntax : %S\n",bstr);
SysFreeString(bstr);

hr = pProp->get_MaxRange(&lval);
if(FAILED(hr))
    goto Cleanup;
printf(" MaxRange : %d\n",lval);
SysFreeString(bstr);

hr = pProp->get_MinRange(&lval);
if(FAILED(hr))
    goto Cleanup;
printf(" MinRange : %d\n", lval);
SysFreeString(bstr);

hr = pProp->get_Multivalued(&bval);
if(FAILED(hr))
    goto Cleanup;
printf(" MultiValued : %b\n",bval);
SysFreeString(bstr);

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    if(pCont)
        pCont->Release();

    if(pProp)
        pProp->Release(); 
 
CoUninitialize();
```



## <a name="requirements"></a><span data-ttu-id="89aa5-137">Требования</span><span class="sxs-lookup"><span data-stu-id="89aa5-137">Requirements</span></span>



| <span data-ttu-id="89aa5-138">Требование</span><span class="sxs-lookup"><span data-stu-id="89aa5-138">Requirement</span></span> | <span data-ttu-id="89aa5-139">Значение</span><span class="sxs-lookup"><span data-stu-id="89aa5-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89aa5-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89aa5-140">Minimum supported client</span></span><br/> | <span data-ttu-id="89aa5-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89aa5-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89aa5-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89aa5-142">Minimum supported server</span></span><br/> | <span data-ttu-id="89aa5-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89aa5-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89aa5-144">Header</span><span class="sxs-lookup"><span data-stu-id="89aa5-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="89aa5-145"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="89aa5-145"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="89aa5-146">DLL</span><span class="sxs-lookup"><span data-stu-id="89aa5-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89aa5-147"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89aa5-147"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="89aa5-148">IID</span><span class="sxs-lookup"><span data-stu-id="89aa5-148">IID</span></span><br/>                      | <span data-ttu-id="89aa5-149">IID \_ иадспроперти определен как C8F93DD3-4ae0-11CF-9E73-00AA004A5691</span><span class="sxs-lookup"><span data-stu-id="89aa5-149">IID\_IADsProperty is defined as C8F93DD3-4AE0-11CF-9E73-00AA004A5691</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="89aa5-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89aa5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89aa5-151">**иадскласс**</span><span class="sxs-lookup"><span data-stu-id="89aa5-151">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="89aa5-152">**иадспроперти**</span><span class="sxs-lookup"><span data-stu-id="89aa5-152">**IADsProperty**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsproperty)
</dt> <dt>

[<span data-ttu-id="89aa5-153">**иадссинтакс**</span><span class="sxs-lookup"><span data-stu-id="89aa5-153">**IADsSyntax**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssyntax)
</dt> </dl>

 

 





