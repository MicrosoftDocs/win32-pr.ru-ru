---
title: Методы свойств Иадссекуритидескриптор (iAds. h)
description: Методы свойств интерфейса Иадссекуритидескриптор получают или задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: e0c50740-de98-4913-b3df-6fd53263bcc8
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадссекуритидескриптор ADSI
topic_type:
- apiref
api_name:
- IADsSecurityDescriptor Property Methods
- IADsSecurityDescriptor.Revision
- IADsSecurityDescriptor.get_Revision
- IADsSecurityDescriptor.put_Revision
- IADsSecurityDescriptor.Control
- IADsSecurityDescriptor.get_Control
- IADsSecurityDescriptor.put_Control
- IADsSecurityDescriptor.Owner
- IADsSecurityDescriptor.get_Owner
- IADsSecurityDescriptor.put_Owner
- IADsSecurityDescriptor.OwnerDefaulted
- IADsSecurityDescriptor.get_OwnerDefaulted
- IADsSecurityDescriptor.put_OwnerDefaulted
- IADsSecurityDescriptor.Group
- IADsSecurityDescriptor.get_Group
- IADsSecurityDescriptor.put_Group
- IADsSecurityDescriptor.GroupDefaulted
- IADsSecurityDescriptor.get_GroupDefaultedY
- IADsSecurityDescriptor.put_GroupDefaulted
- IADsSecurityDescriptor.DiscretionaryAcl
- IADsSecurityDescriptor.get_DiscretionaryAcl
- IADsSecurityDescriptor.put_DiscretionaryAcl
- IADsSecurityDescriptor.DaclDefaulted
- IADsSecurityDescriptor.get_DaclDefaulted
- IADsSecurityDescriptor.put_DaclDefaulted
- IADsSecurityDescriptor.SystemAcl
- IADsSecurityDescriptor.get_SystemAcl
- IADsSecurityDescriptor.put_SystemAcl
- IADsSecurityDescriptor.SaclDefaulted
- IADsSecurityDescriptor.get_SaclDefaulted
- IADsSecurityDescriptor.put_SaclDefaulted
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c5c07213a2d2a3a1b64621dbc40f707b0900703
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135731"
---
# <a name="iadssecuritydescriptor-property-methods"></a><span data-ttu-id="a8154-105">Методы свойств Иадссекуритидескриптор</span><span class="sxs-lookup"><span data-stu-id="a8154-105">IADsSecurityDescriptor Property Methods</span></span>

<span data-ttu-id="a8154-106">Методы свойств интерфейса [**иадссекуритидескриптор**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) получают или задают свойства, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a8154-106">The property methods of the [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="a8154-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="a8154-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="a8154-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="a8154-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="a8154-109">**Управление**</span><span class="sxs-lookup"><span data-stu-id="a8154-109">**Control**</span></span>
<span data-ttu-id="a8154-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a8154-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="a8154-111">Флаги, которые соответствуют значению дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="a8154-111">Flags that qualify the meaning of the security descriptor.</span></span> <span data-ttu-id="a8154-112">Значения берутся из структуры [**\_ \_ управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) Win32.</span><span class="sxs-lookup"><span data-stu-id="a8154-112">Values are taken from the Win32 [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) structure.</span></span>

<dt>

<span data-ttu-id="a8154-113">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8154-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8154-114">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="a8154-114">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Control(
  [out] LONG* plControl
);
HRESULT put_Control(
  [in] LONG lControl
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8154-115">**даклдефаултед**</span><span class="sxs-lookup"><span data-stu-id="a8154-115">**DaclDefaulted**</span></span>
<span data-ttu-id="a8154-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a8154-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="a8154-117">Флаг типа BOOL, который указывает, является ли список DACL производным от механизма по умолчанию, а не явно предоставленным исходным поставщиком дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="a8154-117">A flag of the BOOL type that indicates if the DACL is derived from a default mechanism, rather than being provided explicitly by the original provider of the security descriptor.</span></span> <span data-ttu-id="a8154-118">Например, если создатель объекта не указывает DACL, объект получает DACL по умолчанию от маркера доступа создателя.</span><span class="sxs-lookup"><span data-stu-id="a8154-118">For example, if an object's creator does not specify a DACL, the object receives the default DACL from the creator's access token.</span></span> <span data-ttu-id="a8154-119">Этот флаг может повлиять на то, как система рассматривает DACL, по отношению к наследованию ACE.</span><span class="sxs-lookup"><span data-stu-id="a8154-119">This flag can affect how the system treats the DACL, with respect to ACE inheritance.</span></span> <span data-ttu-id="a8154-120">Система пропускает этот флаг, если \_ \_ флаг присутствия DACL SE не установлен.</span><span class="sxs-lookup"><span data-stu-id="a8154-120">The system ignores this flag if the SE\_DACL\_PRESENT flag is not set.</span></span>

<dt>

<span data-ttu-id="a8154-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8154-121">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8154-122">Тип данных скрипта: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="a8154-122">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DaclDefaulted(
  [out] VARIANT_BOOL* fDaclDefaulted
);
HRESULT put_DaclDefaulted(
  [in] VARIANT_BOOL fDaclDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8154-123">**дискретионарякл**</span><span class="sxs-lookup"><span data-stu-id="a8154-123">**DiscretionaryAcl**</span></span>
<span data-ttu-id="a8154-124"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a8154-124"></dt> <dd> <dl></span></span>

<span data-ttu-id="a8154-125">Избирательный список управления доступом (DACL), указывающий типы доступа, предоставленные объекту для указанных пользователей и групп.</span><span class="sxs-lookup"><span data-stu-id="a8154-125">Discretionary access-control list (DACL) that specifies the types of access granted to the object for specified users and groups.</span></span> <span data-ttu-id="a8154-126">Дополнительные сведения о списках DACL см. в разделе пустые [списки DACL и пустой список DACL](/windows/desktop/AD/null-dacls-and-empty-dacls).</span><span class="sxs-lookup"><span data-stu-id="a8154-126">For more information about DACLs, see [Null DACLs and Empty DACLs](/windows/desktop/AD/null-dacls-and-empty-dacls).</span></span>

<dt>

<span data-ttu-id="a8154-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8154-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8154-128">Тип данных скрипта: **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="a8154-128">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DiscretionaryAcl(
  [out] IDispatch** ppIDispDACL
);
HRESULT put_DiscretionaryAcl(
  [in] IDispatch* pIDispDACL
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8154-129">**Группа**</span><span class="sxs-lookup"><span data-stu-id="a8154-129">**Group**</span></span>
<span data-ttu-id="a8154-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a8154-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="a8154-131">Группа, которой принадлежит идентификатор безопасности владельца.</span><span class="sxs-lookup"><span data-stu-id="a8154-131">Group to which the owner's security ID belongs.</span></span>

<dt>

<span data-ttu-id="a8154-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8154-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8154-133">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a8154-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Group(
  [out] BSTR* pbstrGroupl
);
HRESULT put_Group(
  [in] BSTR bstrGroup
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8154-134">**граупдефаултед**</span><span class="sxs-lookup"><span data-stu-id="a8154-134">**GroupDefaulted**</span></span>
<span data-ttu-id="a8154-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a8154-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="a8154-136">Флаг типа BOOL, указывающий, являются ли данные группы производными от механизма по умолчанию, а не явно предоставленными исходным поставщиком дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="a8154-136">A flag of the BOOL type that indicates if the group data is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span>

<dt>

<span data-ttu-id="a8154-137">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8154-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8154-138">Тип данных скрипта: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="a8154-138">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GroupDefaultedY(
  [out] VARIANT_BOOL* fGroupDefaulted
);
HRESULT put_GroupDefaulted(
  [in] VARIANT_BOOL fGroupDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8154-139">**Владелец**</span><span class="sxs-lookup"><span data-stu-id="a8154-139">**Owner**</span></span>
<span data-ttu-id="a8154-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a8154-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="a8154-141">Владелец объекта.</span><span class="sxs-lookup"><span data-stu-id="a8154-141">Object owner.</span></span>

<dt>

<span data-ttu-id="a8154-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8154-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8154-143">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a8154-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Owner(
  [out] BSTR* pbstrOwnerl
);
HRESULT put_Owner(
  [in] BSTR bstrOwner
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8154-144">**овнердефаултед**</span><span class="sxs-lookup"><span data-stu-id="a8154-144">**OwnerDefaulted**</span></span>
<span data-ttu-id="a8154-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a8154-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="a8154-146">Флаг типа BOOL, указывающий, что данные владельца являются производными от механизма по умолчанию, а не предоставляются явным образом исходным поставщиком дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="a8154-146">A flag of the BOOL type that indicates that the owner data is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span>

<dt>

<span data-ttu-id="a8154-147">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8154-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8154-148">Тип данных скрипта: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="a8154-148">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OwnerDefaulted(
  [out] VARIANT_BOOL* fOwnerDefaulted
);
HRESULT put_OwnerDefaulted(
  [in] VARIANT_BOOL fOwnerDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8154-149">**Редакции**</span><span class="sxs-lookup"><span data-stu-id="a8154-149">**Revision**</span></span>
<span data-ttu-id="a8154-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a8154-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="a8154-151">Уровень редакции дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="a8154-151">Revision level of the security descriptor.</span></span> <span data-ttu-id="a8154-152">Это значение берется из структуры [**\_ \_ информации о редакции ACL**](/windows/desktop/api/winnt/ns-winnt-acl_revision_information) Win32.</span><span class="sxs-lookup"><span data-stu-id="a8154-152">This value is taken from the Win32 [**ACL\_REVISION\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-acl_revision_information) structure.</span></span> <span data-ttu-id="a8154-153">Все ACE в списке ACL должны иметь одинаковый уровень редакции.</span><span class="sxs-lookup"><span data-stu-id="a8154-153">All ACEs in an ACL must be at the same revision level.</span></span>

<dt>

<span data-ttu-id="a8154-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8154-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8154-155">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="a8154-155">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Revision(
  [out] LONG* plRevision
);
HRESULT put_Revision(
  [in] LONG lRevision
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8154-156">**саклдефаултед**</span><span class="sxs-lookup"><span data-stu-id="a8154-156">**SaclDefaulted**</span></span>
<span data-ttu-id="a8154-157"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a8154-157"></dt> <dd> <dl></span></span>

<span data-ttu-id="a8154-158">Флаг типа BOOL, указывающий, что список SACL является производным от механизма по умолчанию, а не явно предоставленным исходным поставщиком дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="a8154-158">A flag of the BOOL type that indicates that the SACL is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span> <span data-ttu-id="a8154-159">Этот флаг может влиять на то, как система обрабатывает список SACL по отношению к наследованию ACE.</span><span class="sxs-lookup"><span data-stu-id="a8154-159">This flag can affect how the system handles the SACL, with respect to ACE inheritance.</span></span> <span data-ttu-id="a8154-160">Система пропускает этот флаг, если \_ \_ не установлен флаг присутствия в списке SACL для SE.</span><span class="sxs-lookup"><span data-stu-id="a8154-160">The system ignores this flag if the SE\_SACL\_PRESENT flag is not set.</span></span>

<dt>

<span data-ttu-id="a8154-161">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8154-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8154-162">Тип данных скрипта: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="a8154-162">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SaclDefaulted(
  [out] VARIANT_BOOL* fSaclDefaulted
);
HRESULT put_SaclDefaulted(
  [in] VARIANT_BOOL fSaclDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8154-163">**системакл**</span><span class="sxs-lookup"><span data-stu-id="a8154-163">**SystemAcl**</span></span>
<span data-ttu-id="a8154-164"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a8154-164"></dt> <dd> <dl></span></span>

<span data-ttu-id="a8154-165">Системный список управления доступом, используемый для создания записей аудита для объекта.</span><span class="sxs-lookup"><span data-stu-id="a8154-165">System access-control list used to generate audit records for the object.</span></span>

<dt>

<span data-ttu-id="a8154-166">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8154-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8154-167">Тип данных скрипта: **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="a8154-167">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SystemAcl(
  [out] IDispatch** ppIDispSACL
);
HRESULT put_SystemAcl(
  [in] IDispatch* pIDispSACL
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="a8154-168">Примеры</span><span class="sxs-lookup"><span data-stu-id="a8154-168">Examples</span></span>

<span data-ttu-id="a8154-169">В следующем примере кода показано, как перечислить существующий дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="a8154-169">The following code example shows how to enumerate an existing security descriptor.</span></span>


```VB
Dim ou As IADs
Dim sd As IADsSecurityDescriptor
Dim dacl As IADsAccessControlList
Dim sacl As IADsAccessControlList

On Error GoTo Cleanup 
 
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
Set sd = ou.Get("ntSecurityDescriptor")
Debug.Print sd.Owner
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision
Set dacl = sd.DiscretionaryAcl
Set sacl = sd.SystemAcl
' Add code to perform an operation with the Discretionary and System ACLs.

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
    Set sd = Nothing
    Set dacl = Nothing
    Set sacl = Nothing
```



## <a name="requirements"></a><span data-ttu-id="a8154-170">Требования</span><span class="sxs-lookup"><span data-stu-id="a8154-170">Requirements</span></span>



| <span data-ttu-id="a8154-171">Требование</span><span class="sxs-lookup"><span data-stu-id="a8154-171">Requirement</span></span> | <span data-ttu-id="a8154-172">Значение</span><span class="sxs-lookup"><span data-stu-id="a8154-172">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8154-173">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8154-173">Minimum supported client</span></span><br/> | <span data-ttu-id="a8154-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8154-174">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="a8154-175">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8154-175">Minimum supported server</span></span><br/> | <span data-ttu-id="a8154-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8154-176">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="a8154-177">Header</span><span class="sxs-lookup"><span data-stu-id="a8154-177">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8154-178"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8154-178"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="a8154-179">DLL</span><span class="sxs-lookup"><span data-stu-id="a8154-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8154-180"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8154-180"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="a8154-181">IID</span><span class="sxs-lookup"><span data-stu-id="a8154-181">IID</span></span><br/>                      | <span data-ttu-id="a8154-182">IID \_ иадссекуритидескриптор определен как B8C787CA-9BDD-11D0-852C-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="a8154-182">IID\_IADsSecurityDescriptor is defined as B8C787CA-9BDD-11D0-852C-00C04FD8D503</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8154-183">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8154-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8154-184">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a8154-184">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[<span data-ttu-id="a8154-185">**IADsAccessControlEntry**</span><span class="sxs-lookup"><span data-stu-id="a8154-185">**IADsAccessControlEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[<span data-ttu-id="a8154-186">**IADsAccessControlList**</span><span class="sxs-lookup"><span data-stu-id="a8154-186">**IADsAccessControlList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> </dl>

 

