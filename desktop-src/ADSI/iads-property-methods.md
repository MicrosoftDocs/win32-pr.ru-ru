---
title: Методы свойства IADs (iAds. h)
description: Методы свойств интерфейса IADs получают или задают свойства, описанные в следующей таблице. Дополнительные сведения о методах свойств см. в разделе методы свойств интерфейса.
ms.assetid: d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12
ms.tgt_platform: multiple
keywords:
- Свойства IADs методы интерфейса ADSI
topic_type:
- apiref
api_name:
- IADs Property Methods
- IADs.ADsPath
- IADs.get_ADsPath
- IADs.Class
- IADs.get_Class
- IADs.GUID
- IADs.get_GUID
- IADs.Name
- IADs.get_Name
- IADs.Parent
- IADs.get_Parent
- IADs.Schema
- IADs.get_Schema
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1134260c780958bcdba8d1f14eac535ddbf4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533818"
---
# <a name="iads-property-methods"></a><span data-ttu-id="0750e-105">Методы свойства IADs</span><span class="sxs-lookup"><span data-stu-id="0750e-105">IADs Property Methods</span></span>

<span data-ttu-id="0750e-106">Методы свойств интерфейса [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) получают или задают свойства, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0750e-106">The property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="0750e-107">Дополнительные сведения о методах свойств см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="0750e-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="0750e-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="0750e-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="0750e-109">**Действитель**</span><span class="sxs-lookup"><span data-stu-id="0750e-109">**ADsPath**</span></span>
<span data-ttu-id="0750e-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0750e-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="0750e-111">Строка ADsPath этого объекта.</span><span class="sxs-lookup"><span data-stu-id="0750e-111">The ADsPath string of this object.</span></span> <span data-ttu-id="0750e-112">Строка уникально идентифицирует этот объект в сетевой среде.</span><span class="sxs-lookup"><span data-stu-id="0750e-112">The string uniquely identifies this object in a network environment.</span></span> <span data-ttu-id="0750e-113">Объект всегда может быть получен с помощью этого пути.</span><span class="sxs-lookup"><span data-stu-id="0750e-113">The object can always be retrieved using this path.</span></span>

<dt>

<span data-ttu-id="0750e-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0750e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0750e-115">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0750e-115">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsPath(
  [out] BSTR* pbstrADsPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0750e-116">**Класс**</span><span class="sxs-lookup"><span data-stu-id="0750e-116">**Class**</span></span>
<span data-ttu-id="0750e-117"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0750e-117"></dt> <dd> <dl></span></span>

<span data-ttu-id="0750e-118">Имя класса схемы объекта.</span><span class="sxs-lookup"><span data-stu-id="0750e-118">The name of the object Schema class.</span></span>

<dt>

<span data-ttu-id="0750e-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0750e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0750e-120">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0750e-120">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Class(
  [out] BSTR* pbstrClass
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0750e-121">**GUID**</span><span class="sxs-lookup"><span data-stu-id="0750e-121">**GUID**</span></span>
<span data-ttu-id="0750e-122"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0750e-122"></dt> <dd> <dl></span></span>

<span data-ttu-id="0750e-123">Глобальный уникальный идентификатор объекта каталога.</span><span class="sxs-lookup"><span data-stu-id="0750e-123">The globally unique identifier of the directory object.</span></span> <span data-ttu-id="0750e-124">Интерфейс [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) преобразует **идентификатор GUID** из строки октета, которая хранится на сервере каталогов, в строковом формате.</span><span class="sxs-lookup"><span data-stu-id="0750e-124">The [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface converts the **GUID** from an octet string, as stored on a directory server, into a string format.</span></span>

<dt>

<span data-ttu-id="0750e-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0750e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0750e-126">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0750e-126">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GUID(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0750e-127">**Name**</span><span class="sxs-lookup"><span data-stu-id="0750e-127">**Name**</span></span>
<span data-ttu-id="0750e-128"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0750e-128"></dt> <dd> <dl></span></span>

<span data-ttu-id="0750e-129">Относительное имя объекта, именованное в базовой службе каталогов.</span><span class="sxs-lookup"><span data-stu-id="0750e-129">The relative name of the object as named within the underlying directory service.</span></span> <span data-ttu-id="0750e-130">Это имя отличает этот объект от его одноуровневых элементов.</span><span class="sxs-lookup"><span data-stu-id="0750e-130">This name distinguishes this object from its siblings.</span></span>

<dt>

<span data-ttu-id="0750e-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0750e-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0750e-132">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0750e-132">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0750e-133">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="0750e-133">**Parent**</span></span>
<span data-ttu-id="0750e-134"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0750e-134"></dt> <dd> <dl></span></span>

<span data-ttu-id="0750e-135">Строка ADsPath родительского контейнера.</span><span class="sxs-lookup"><span data-stu-id="0750e-135">The ADsPath string of the parent container.</span></span> <span data-ttu-id="0750e-136">Active Directory не допускают формирования ADsPath для данного объекта путем сцепления свойств **Parent** и **Name** .</span><span class="sxs-lookup"><span data-stu-id="0750e-136">Active Directory does not permit the formation of the ADsPath of a given object by concatenating the **Parent** and **Name** properties.</span></span> <span data-ttu-id="0750e-137">Хотя эта операция может работать в некоторых поставщиках, не гарантируется, что она будет работать для всех реализаций.</span><span class="sxs-lookup"><span data-stu-id="0750e-137">While this operation might work in some providers, it is not guaranteed to work for all implementations.</span></span> <span data-ttu-id="0750e-138">Значение ADsPath гарантированно является допустимым и всегда должно использоваться для получения указателя интерфейса объекта.</span><span class="sxs-lookup"><span data-stu-id="0750e-138">The ADsPath is guaranteed to be valid and should always be used to retrieve an object's interface pointer.</span></span>

<dt>

<span data-ttu-id="0750e-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0750e-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0750e-140">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0750e-140">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parent(
  [out] BSTR* pbstrParent
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0750e-141">**Схема**</span><span class="sxs-lookup"><span data-stu-id="0750e-141">**Schema**</span></span>
<span data-ttu-id="0750e-142"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0750e-142"></dt> <dd> <dl></span></span>

<span data-ttu-id="0750e-143">Строка ADsPath объекта класса схемы данного объекта.</span><span class="sxs-lookup"><span data-stu-id="0750e-143">The ADsPath string of the Schema class object of this object.</span></span>

<dt>

<span data-ttu-id="0750e-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0750e-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0750e-145">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0750e-145">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Schema(
  [out] BSTR* pbstrSchema
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="0750e-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0750e-146">Remarks</span></span>

<span data-ttu-id="0750e-147">В Active Directory **идентификатор GUID** , возвращенный из GUID, является строкой шестнадцатеричного числа.</span><span class="sxs-lookup"><span data-stu-id="0750e-147">In Active Directory, the **GUID** returned from GUID is a string of hexadecimals.</span></span> <span data-ttu-id="0750e-148">Используйте результирующий **идентификатор GUID** для непосредственной привязки к объекту.</span><span class="sxs-lookup"><span data-stu-id="0750e-148">Use the resultant **GUID** to bind to the object directly.</span></span>


```VB
Dim x As IADs
Set x = GetObject("LDAP://servername/<GUID=xxx>")
```



<span data-ttu-id="0750e-149">где XXX — значение, возвращаемое свойством GUID.</span><span class="sxs-lookup"><span data-stu-id="0750e-149">where xxx is the value returned from the GUID property.</span></span> <span data-ttu-id="0750e-150">Дополнительные сведения см. в разделе [Использование objectGUID для привязки к объекту](/windows/desktop/AD/using-objectguid-to-bind-to-an-object).</span><span class="sxs-lookup"><span data-stu-id="0750e-150">For more information, see [Using objectGUID to Bind to an Object](/windows/desktop/AD/using-objectguid-to-bind-to-an-object).</span></span> <span data-ttu-id="0750e-151">Имейте в виду, что при использовании идентификатора GUID для привязки к объекту метод свойства **ADsPath** возвращает значения, отличные от обычных значений, которые будут возвращаться, если для привязки к тому же объекту использовалось различающееся имя (DN).</span><span class="sxs-lookup"><span data-stu-id="0750e-151">Be aware that if you use a GUID to bind to an object, the **ADsPath** property method returns values that are different from the normal values that would be returned if you used a distinguished name (DN) to bind to the same object.</span></span> <span data-ttu-id="0750e-152">Например, в следующей таблице перечислены значения, возвращаемые при использовании двух различных методов привязки для привязки к одному и тому же объекту пользователя.</span><span class="sxs-lookup"><span data-stu-id="0750e-152">For example, the following table lists the values returned when using the two different binding methods to bind to the same user object.</span></span>



|             | <span data-ttu-id="0750e-153">Привязка с помощью DN</span><span class="sxs-lookup"><span data-stu-id="0750e-153">Bind using DN</span></span>                                           | <span data-ttu-id="0750e-154">Привязка с использованием идентификатора GUID</span><span class="sxs-lookup"><span data-stu-id="0750e-154">Bind using GUID</span></span>                                             |
|-------------|---------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="0750e-155">**Name**</span><span class="sxs-lookup"><span data-stu-id="0750e-155">**Name**</span></span>    | <span data-ttu-id="0750e-156">CN = Джефф Иванов</span><span class="sxs-lookup"><span data-stu-id="0750e-156">CN=Jeff Smith</span></span>                                           | <span data-ttu-id="0750e-157">CN = Джефф Иванов</span><span class="sxs-lookup"><span data-stu-id="0750e-157">CN=Jeff Smith</span></span>                                               |
| <span data-ttu-id="0750e-158">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="0750e-158">**Parent**</span></span>  | <span data-ttu-id="0750e-159">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span><span class="sxs-lookup"><span data-stu-id="0750e-159">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span></span>               | <span data-ttu-id="0750e-160">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span><span class="sxs-lookup"><span data-stu-id="0750e-160">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span></span>                   |
| <span data-ttu-id="0750e-161">**Действитель**</span><span class="sxs-lookup"><span data-stu-id="0750e-161">**ADsPath**</span></span> | <span data-ttu-id="0750e-162">LDAP://server/CN=Jeff Смит, CN = Users, DC = Fabrikam, DC = com</span><span class="sxs-lookup"><span data-stu-id="0750e-162">LDAP://server/CN=Jeff Smith,CN=Users,DC=Fabrikam,DC=com</span></span> | <span data-ttu-id="0750e-163">LDAP://server/<GUID = c0f59dfcf507d311a99e0000f879f7c7></span><span class="sxs-lookup"><span data-stu-id="0750e-163">LDAP://server/<GUID=c0f59dfcf507d311a99e0000f879f7c7></span></span> |



 

> [!Note]  
> <span data-ttu-id="0750e-164">Поставщик WinNT не поддерживает привязку с использованием **идентификатора GUID** объекта и возвращает свойство **GUID** в слегка другом строковом формате.</span><span class="sxs-lookup"><span data-stu-id="0750e-164">The WinNT provider does not support binding using the object **GUID**, and returns the **GUID** property in a slightly different string format.</span></span>

 

## <a name="examples"></a><span data-ttu-id="0750e-165">Примеры</span><span class="sxs-lookup"><span data-stu-id="0750e-165">Examples</span></span>

<span data-ttu-id="0750e-166">В следующем примере кода показано, как получить данные объекта с помощью методов свойств интерфейса [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="0750e-166">The following code example shows how to retrieve object data using property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


```VB
Dim x As IADs
Dim parent As IADsContainer
Dim cls As IADsClass
Dim op As Variant

On Error GoTo Cleanup

Set x = GetObject("WinNT://Fabrikam/Administrator")
Debug.Print "Object Name: " & x.Name
Debug.Print "Object Path: " & x.ADsPath
Debug.Print "Object Class: " & x.Class
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Debug.Print "Class Name is: " & cls.Name
For Each op In cls.OptionalProperties
    Debug.Print "Optional Property: " & op
Next op

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set x = Nothing
    Set parent = Nothing
    Set cls = Nothing
```



<span data-ttu-id="0750e-167">В следующем примере кода показано, как получить данные объекта с помощью методов свойств интерфейса [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="0750e-167">The following code example shows how to retrieve object data using property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


```VB
<HTML>
<head><title></title></head>

<body>
<%
Dim x 
On Error Resume Next
 
Set x = GetObject("WinNT://Fabrikam/Administrator")
Response.Write "Object Name: " & x.Name & "<br>"
Response.Write "Object Path: " & x.ADsPath & "<br>"
Response.Write "Object Class: " & x.Class & "<br>"
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Response.Write "Class Name is: " & cls.Name & "<br>"
For Each op In cls.OptionalProperties
    Response.Write "Optional Property: " & op & "<br>"
Next op
%>

</body>
</html>
```



<span data-ttu-id="0750e-168">В следующем примере кода показано, как работать со методами свойств интерфейса [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="0750e-168">The following code example shows how to work with the property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


```C++
#include <stdio.h>
#include <activeds.h>
 
int main(int argc, char* argv[])
{
    IADs *pADs = NULL;
    IADsUser *pADsUser = NULL;
    IADsClass *pCls = NULL;
    CComBSTR sbstr;
 
    HRESULT hr = CoInitialize(NULL);
    if (hr != S_OK) { return 0; }
 
    hr=ADsGetObject(L"WinNT://Fabrikam/Administrator",
                IID_IADsUser,
                (void**) &pADsUser);
    if (hr != S_OK) { goto Cleanup; }
 
    hr = pADsUser->QueryInterface(IID_IADs, (void**) &pADs);
    if( hr !=S_OK) { goto Cleanup;}
 
    pADsUser->Release();
 
    if( S_OK == pADs->get_Name(&sbstr) ) {
        printf("Object Name: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_ADsPath(&sbstr) ) {
        printf("Object path: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_Class(&sbstr) ) {
        printf("Object class: %S\n",sbstr);
    }
 
    hr = pADs->get_Schema(&sbstr);
    if ( hr != S_OK) {goto Cleanup;}
 
    hr = ADsGetObject(sbstr,IID_IADsClass, (void**)&pCls);
    if ( hr != S_OK) {goto Cleanup;}
    if( S_OK == pCls->get_Name(&sbstr) ) {
        printf("Class name is %S\n", sbstr);
    }
 
 Cleanup:
    if(pADs)
        pADs->Release();

    if(pIADsUser)
        pADsUser->Release();

    if(IADsClass)
        pADsClass->Release();

    CoUninitialize();

    if(hr==S_OK)
    {
        return 1;
    }
    else
    {
        return 0;
    }
}
```



## <a name="requirements"></a><span data-ttu-id="0750e-169">Требования</span><span class="sxs-lookup"><span data-stu-id="0750e-169">Requirements</span></span>



| <span data-ttu-id="0750e-170">Требование</span><span class="sxs-lookup"><span data-stu-id="0750e-170">Requirement</span></span> | <span data-ttu-id="0750e-171">Значение</span><span class="sxs-lookup"><span data-stu-id="0750e-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0750e-172">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0750e-172">Minimum supported client</span></span><br/> | <span data-ttu-id="0750e-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0750e-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0750e-174">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0750e-174">Minimum supported server</span></span><br/> | <span data-ttu-id="0750e-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0750e-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0750e-176">Header</span><span class="sxs-lookup"><span data-stu-id="0750e-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="0750e-177"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="0750e-177"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="0750e-178">DLL</span><span class="sxs-lookup"><span data-stu-id="0750e-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0750e-179"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0750e-179"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="0750e-180">IID</span><span class="sxs-lookup"><span data-stu-id="0750e-180">IID</span></span><br/>                      | <span data-ttu-id="0750e-181">IID \_ iAds определяется как FD8256D0-FD15-11CE-ABC4-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="0750e-181">IID\_IADs is defined as FD8256D0-FD15-11CE-ABC4-02608C9E7553</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="0750e-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0750e-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0750e-183">**IADs**</span><span class="sxs-lookup"><span data-stu-id="0750e-183">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="0750e-184">**иадсконтаинер**</span><span class="sxs-lookup"><span data-stu-id="0750e-184">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> </dl>

 

