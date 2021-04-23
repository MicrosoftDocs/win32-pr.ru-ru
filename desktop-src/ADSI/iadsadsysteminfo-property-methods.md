---
title: Методы свойств Иадсадсистеминфо (iAds. h)
description: Методы свойств интерфейса Иадсадсистеминфо получают или задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 1cdaa610-4341-4825-b2f9-dd495a9147ff
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсадсистеминфо ADSI
topic_type:
- apiref
api_name:
- IADsADSystemInfo Property Methods
- IADsADSystemInfo.UserName
- IADsADSystemInfo.get_UserName
- IADsADSystemInfo.ComputerName
- IADsADSystemInfo.get_ComputerName
- IADsADSystemInfo.SiteName
- IADsADSystemInfo.get_SiteName
- IADsADSystemInfo.DomainShortName
- IADsADSystemInfo.get_DomainShortName
- IADsADSystemInfo.DomainDNSName
- IADsADSystemInfo.get_DomainDNSName
- IADsADSystemInfo.ForestDNSName
- IADsADSystemInfo.get_ForestDNSName
- IADsADSystemInfo.PDCRoleOwner
- IADsADSystemInfo.get_PDCRoleOwner
- IADsADSystemInfo.SchemaRoleOwner
- IADsADSystemInfo.get_SchemaRoleOwner
- IADsADSystemInfo.IsNativeMode
- IADsADSystemInfo.get_IsNativeMode
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8dba53dfda4bb8f4dd3290cb2737cdeb4e8a6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136890"
---
# <a name="iadsadsysteminfo-property-methods"></a><span data-ttu-id="d796e-105">Методы свойств Иадсадсистеминфо</span><span class="sxs-lookup"><span data-stu-id="d796e-105">IADsADSystemInfo Property Methods</span></span>

<span data-ttu-id="d796e-106">Методы свойств интерфейса [**иадсадсистеминфо**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo) получают или задают свойства, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d796e-106">The property methods of the [**IADsADSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="d796e-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="d796e-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="d796e-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="d796e-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="d796e-109">**ИмяКомпьютера**</span><span class="sxs-lookup"><span data-stu-id="d796e-109">**ComputerName**</span></span>
<span data-ttu-id="d796e-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d796e-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="d796e-111">Получает различающееся имя локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="d796e-111">Retrieves the distinguished name of the local computer.</span></span>

<dt>

<span data-ttu-id="d796e-112">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d796e-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d796e-113">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d796e-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerName(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d796e-114">**домаинднснаме**</span><span class="sxs-lookup"><span data-stu-id="d796e-114">**DomainDNSName**</span></span>
<span data-ttu-id="d796e-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d796e-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="d796e-116">Возвращает DNS-имя домена локального компьютера, например "domainName.companyName.com".</span><span class="sxs-lookup"><span data-stu-id="d796e-116">Retrieves the DNS name of the local computer's domain, such as "domainName.companyName.com".</span></span>

<dt>

<span data-ttu-id="d796e-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d796e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d796e-118">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d796e-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d796e-119">**домаиншортнаме**</span><span class="sxs-lookup"><span data-stu-id="d796e-119">**DomainShortName**</span></span>
<span data-ttu-id="d796e-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d796e-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="d796e-121">Получает короткое имя домена локального компьютера, например "имя_домена".</span><span class="sxs-lookup"><span data-stu-id="d796e-121">Retrieves the short name of the local computer's domain, such as "domainName".</span></span>

<dt>

<span data-ttu-id="d796e-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d796e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d796e-123">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d796e-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainShortName(
  [out] BSTR* pbstrDSN
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d796e-124">**форестднснаме**</span><span class="sxs-lookup"><span data-stu-id="d796e-124">**ForestDNSName**</span></span>
<span data-ttu-id="d796e-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d796e-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="d796e-126">Возвращает DNS-имя леса локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="d796e-126">Retrieves the DNS name of the local computer's forest.</span></span>

<dt>

<span data-ttu-id="d796e-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d796e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d796e-128">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d796e-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ForestDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d796e-129">**иснативемоде**</span><span class="sxs-lookup"><span data-stu-id="d796e-129">**IsNativeMode**</span></span>
<span data-ttu-id="d796e-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d796e-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="d796e-131">Определяет, находится ли домен локального компьютера в собственном или смешанном режиме.</span><span class="sxs-lookup"><span data-stu-id="d796e-131">Determines whether the local computer's domain is in native or mixed mode.</span></span>

<dt>

<span data-ttu-id="d796e-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d796e-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d796e-133">Тип данных скрипта: **bool**</span><span class="sxs-lookup"><span data-stu-id="d796e-133">Scripting data type: **BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsNativeMode(
  [out] BOOL* pvBool
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d796e-134">**пдкролеовнер**</span><span class="sxs-lookup"><span data-stu-id="d796e-134">**PDCRoleOwner**</span></span>
<span data-ttu-id="d796e-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d796e-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="d796e-136">Извлекает различающееся имя объекта агента службы каталогов (DSA), владеющего ролью основного контроллера домена в домене локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="d796e-136">Retrieves the distinguished name of the directory service agent (DSA) object for the DC that owns the primary domain controller role in the local computer's domain.</span></span>

<dt>

<span data-ttu-id="d796e-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d796e-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d796e-138">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d796e-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PDCRoleOwner(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d796e-139">**SchemaRoleOwner**</span><span class="sxs-lookup"><span data-stu-id="d796e-139">**SchemaRoleOwner**</span></span>
<span data-ttu-id="d796e-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d796e-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="d796e-141">Извлекает различающееся имя объекта агента службы каталогов (DSA) для контроллера домена, владеющего ролью хозяина схемы в лесу локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="d796e-141">Retrieves the distinguished name of the directory service agent (DSA) object for the DC that owns the schema master role in the local computer's forest.</span></span>

<dt>

<span data-ttu-id="d796e-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d796e-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d796e-143">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d796e-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SchemaRoleOwner(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d796e-144">**Значением**</span><span class="sxs-lookup"><span data-stu-id="d796e-144">**SiteName**</span></span>
<span data-ttu-id="d796e-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d796e-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="d796e-146">Возвращает имя сайта локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="d796e-146">Retrieves the site name of the local computer.</span></span>

<dt>

<span data-ttu-id="d796e-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d796e-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d796e-148">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d796e-148">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SiteName(
  [out] BSTR* pbstrSite
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d796e-149">**UserName**</span><span class="sxs-lookup"><span data-stu-id="d796e-149">**UserName**</span></span>
<span data-ttu-id="d796e-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d796e-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="d796e-151">Возвращает Active Directory различающееся имя текущего пользователя, вошедшего в систему или пользователя, олицетворяемого вызывающим потоком.</span><span class="sxs-lookup"><span data-stu-id="d796e-151">Retrieves the Active Directory distinguished name of the current user, which is the logged-on user or the user impersonated by the calling thread.</span></span>

<dt>

<span data-ttu-id="d796e-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d796e-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d796e-153">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d796e-153">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserName(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="d796e-154">Примеры</span><span class="sxs-lookup"><span data-stu-id="d796e-154">Examples</span></span>

<span data-ttu-id="d796e-155">В следующем примере кода C++ извлекаются сведения о системе Windows.</span><span class="sxs-lookup"><span data-stu-id="d796e-155">The following C++ code example retrieves the Windows system information.</span></span> <span data-ttu-id="d796e-156">Для краткости проверка ошибок пропущена.</span><span class="sxs-lookup"><span data-stu-id="d796e-156">For brevity, error checking is omitted.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
int main()
{
   HRESULT hr;
 
   hr = CoInitialize(NULL);
 
    IADsADSystemInfo *pSys;
    hr = CoCreateInstance(CLSID_ADSystemInfo,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsADSystemInfo,
                          (void**)&pSys);
 
   BSTR bstr;
   hr = pSys->get_UserName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("User: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_ComputerName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Computer: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_DomainDNSName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Domain: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_PDCRoleOwner(&bstr);
   if (SUCCEEDED(hr)) {
      printf("PDC Role owner: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   if(pSys) {
      pSys->Release();
   }
 
   CoUninitialize();
   return 0;
}
```



<span data-ttu-id="d796e-157">В следующем Visual Basic примере кода извлекаются сведения о системе Windows.</span><span class="sxs-lookup"><span data-stu-id="d796e-157">The following Visual Basic code example retrieves the Windows system information.</span></span>


```VB
Dim sys As New ADSystemInfo
Debug.print "User: " & sys.UserName
Debug.print "Computer: " & sys.ComputerName
Debug.print "Domain: " & sys.DomainDNSName
Debug.print "PDC Role Owner: " & sys.PDCRoleOwner
```



<span data-ttu-id="d796e-158">Следующий пример кода VBScript/ASP извлекает сведения о системе Windows.</span><span class="sxs-lookup"><span data-stu-id="d796e-158">The following VBScript/ASP code example retrieves the Windows system information.</span></span>


```VB
<%
Dim sys
Set sys = CreateObject("ADSystemInfo")
Response.Write "User: " & sys.UserName
Response.Write "Computer: " & sys.ComputerName
Response.Write "Domain: " & sys.DomainDNSName
Response.Write "PDC Role Owner: " & sys.PDCRoleOwner
%>
```



## <a name="requirements"></a><span data-ttu-id="d796e-159">Требования</span><span class="sxs-lookup"><span data-stu-id="d796e-159">Requirements</span></span>



| <span data-ttu-id="d796e-160">Требование</span><span class="sxs-lookup"><span data-stu-id="d796e-160">Requirement</span></span> | <span data-ttu-id="d796e-161">Значение</span><span class="sxs-lookup"><span data-stu-id="d796e-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d796e-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d796e-162">Minimum supported client</span></span><br/> | <span data-ttu-id="d796e-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d796e-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d796e-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d796e-164">Minimum supported server</span></span><br/> | <span data-ttu-id="d796e-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d796e-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d796e-166">Header</span><span class="sxs-lookup"><span data-stu-id="d796e-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="d796e-167"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="d796e-167"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="d796e-168">DLL</span><span class="sxs-lookup"><span data-stu-id="d796e-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d796e-169"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d796e-169"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="d796e-170">IID</span><span class="sxs-lookup"><span data-stu-id="d796e-170">IID</span></span><br/>                      | <span data-ttu-id="d796e-171">IID \_ иадсадсистеминфо определен как 5BB11929-AFD1-11d2-9CB9-0000F87A369E</span><span class="sxs-lookup"><span data-stu-id="d796e-171">IID\_IADsADSystemInfo is defined as 5BB11929-AFD1-11D2-9CB9-0000F87A369E</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="d796e-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d796e-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d796e-173">**IADsADSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="d796e-173">**IADsADSystemInfo**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo)
</dt> <dt>

[<span data-ttu-id="d796e-174">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="d796e-174">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

