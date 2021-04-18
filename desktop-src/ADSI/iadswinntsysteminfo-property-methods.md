---
title: Методы свойств Иадсвиннтсистеминфо (iAds. h)
description: Методы свойств интерфейса Иадсвиннтсистеминфо получают или задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 5ba36851-3d03-4179-8cee-dbebe24b7c4e
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсвиннтсистеминфо ADSI
topic_type:
- apiref
api_name:
- IADsWinNTSystemInfo Property Methods
- IADsWinNTSystemInfo.UserName
- IADsWinNTSystemInfo.get_UserName
- IADsWinNTSystemInfo.ComputerName
- IADsWinNTSystemInfo.get_ComputerName
- IADsWinNTSystemInfo.DomainName
- IADsWinNTSystemInfo.get_DomainName
- IADsWinNTSystemInfo.PDC
- IADsWinNTSystemInfo.get_PDC
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d647cf672032a4a06967ee034eb7b6430faf8dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654431"
---
# <a name="iadswinntsysteminfo-property-methods"></a><span data-ttu-id="00252-105">Методы свойств Иадсвиннтсистеминфо</span><span class="sxs-lookup"><span data-stu-id="00252-105">IADsWinNTSystemInfo Property Methods</span></span>

<span data-ttu-id="00252-106">Методы свойств интерфейса [**иадсвиннтсистеминфо**](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo) получают или задают свойства, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="00252-106">The property methods of the [**IADsWinNTSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="00252-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="00252-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="00252-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="00252-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="00252-109">**ИмяКомпьютера**</span><span class="sxs-lookup"><span data-stu-id="00252-109">**ComputerName**</span></span>
<span data-ttu-id="00252-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="00252-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="00252-111">Имя главного компьютера, на котором работает приложение.</span><span class="sxs-lookup"><span data-stu-id="00252-111">Name of the host computer where the application is running.</span></span>

<dt>

<span data-ttu-id="00252-112">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00252-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00252-113">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="00252-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerName(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="00252-114">**Имя_домена**</span><span class="sxs-lookup"><span data-stu-id="00252-114">**DomainName**</span></span>
<span data-ttu-id="00252-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="00252-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="00252-116">Имя домена, к которому принадлежит пользователь.</span><span class="sxs-lookup"><span data-stu-id="00252-116">Name of the domain to which the user belongs.</span></span>

<dt>

<span data-ttu-id="00252-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00252-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00252-118">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="00252-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainName(
  [out] BSTR* pbstrDomain
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="00252-119">**ХОЗЯИН**</span><span class="sxs-lookup"><span data-stu-id="00252-119">**PDC**</span></span>
<span data-ttu-id="00252-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="00252-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="00252-121">Имя основного контроллера домена, к которому принадлежит главный компьютер.</span><span class="sxs-lookup"><span data-stu-id="00252-121">Name of the primary domain controller to which the host computer belongs.</span></span>

<dt>

<span data-ttu-id="00252-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00252-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00252-123">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="00252-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PDC(
  [out] BSTR* pbstrPDC
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="00252-124">**UserName**</span><span class="sxs-lookup"><span data-stu-id="00252-124">**UserName**</span></span>
<span data-ttu-id="00252-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="00252-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="00252-126">Имя учетной записи пользователя, под которой создается объект **виннтсистеминфо** .</span><span class="sxs-lookup"><span data-stu-id="00252-126">Name of the user account under which the **WinNTSystemInfo** object is created.</span></span>

<dt>

<span data-ttu-id="00252-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00252-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00252-128">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="00252-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserName(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="00252-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="00252-129">Examples</span></span>

<span data-ttu-id="00252-130">В следующем примере кода C/C++ извлекаются сведения о системе WinNT.</span><span class="sxs-lookup"><span data-stu-id="00252-130">The following C/C++ code example retrieves the WinNT system information.</span></span> <span data-ttu-id="00252-131">Для краткости проверка ошибок пропущена.</span><span class="sxs-lookup"><span data-stu-id="00252-131">For brevity, error checking is omitted.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
int main()
{
   HRESULT hr;
 
   hr = CoInitialize(NULL);
 
    IADsWinNTSystemInfo *pNtSys;
    hr = CoCreateInstance(CLSID_WinNTSystemInfo,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsWinNTSystemInfo,
                          (void**)&pNTsys);
 
   BSTR bstr;
   hr = pNtSys->get_UserName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("User: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_ComputerName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Computer: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_DomainName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Domain: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_PDC(&bstr);
   if (SUCCEEDED(hr)) {
      printf("PDC: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   if(pNtSys) {
      pNtSys->Release();
   }
 
   CoUninitialize();
   return 0;
}
```



<span data-ttu-id="00252-132">В следующем Visual Basic примере кода извлекаются сведения о системе WinNT.</span><span class="sxs-lookup"><span data-stu-id="00252-132">The following Visual Basic code example retrieves the WinNT system information.</span></span>


```VB
Dim ntsys As New WinNTSystemInfo
Debug.print "User: " & ntsys.UserName
Debug.print "Computer: " & ntsys.ComputerName
Debug.print "Domain: " & ntsys.DomainName
Debug.print "PDC: " & ntsys.PDC
```



<span data-ttu-id="00252-133">Следующий пример кода Visual Basic Scripting Edition/Active Server Pages извлекает сведения о системе WinNT.</span><span class="sxs-lookup"><span data-stu-id="00252-133">The following Visual Basic Scripting Edition/Active Server Pages code example retrieves the WinNT system information.</span></span>


```VB
<%
Dim ntsys
Set ntsys = CreateObject("WinNTSystemInfo")
Response.Write "User: " & ntsys.UserName
Response.Write "Computer: " & ntsys.ComputerName
Response.Write "Domain: " & ntsys.DomainName
Response.Write "PDC: " & ntsys.PDC
%>
```



## <a name="requirements"></a><span data-ttu-id="00252-134">Требования</span><span class="sxs-lookup"><span data-stu-id="00252-134">Requirements</span></span>



| <span data-ttu-id="00252-135">Требование</span><span class="sxs-lookup"><span data-stu-id="00252-135">Requirement</span></span> | <span data-ttu-id="00252-136">Значение</span><span class="sxs-lookup"><span data-stu-id="00252-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00252-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00252-137">Minimum supported client</span></span><br/> | <span data-ttu-id="00252-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00252-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="00252-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00252-139">Minimum supported server</span></span><br/> | <span data-ttu-id="00252-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00252-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="00252-141">Header</span><span class="sxs-lookup"><span data-stu-id="00252-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="00252-142"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="00252-142"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="00252-143">DLL</span><span class="sxs-lookup"><span data-stu-id="00252-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00252-144"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00252-144"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="00252-145">IID</span><span class="sxs-lookup"><span data-stu-id="00252-145">IID</span></span><br/>                      | <span data-ttu-id="00252-146">IID \_ иадсвиннтсистеминфо определен как 6C6D65DC-AFD1-11d2-9CB9-0000F87A369E</span><span class="sxs-lookup"><span data-stu-id="00252-146">IID\_IADsWinNTSystemInfo is defined as 6C6D65DC-AFD1-11D2-9CB9-0000F87A369E</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="00252-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00252-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00252-148">**иадсвиннтсистеминфо**</span><span class="sxs-lookup"><span data-stu-id="00252-148">**IADsWinNTSystemInfo**</span></span>](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo)
</dt> </dl>

 

 





