---
title: Методы свойств Иадспаснаме (iAds. h)
description: Возвращает или задает свойства Ескапедмоде.
ms.assetid: 007ec617-cff2-492a-a62c-50d65fefcd3b
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадспаснаме ADSI
topic_type:
- apiref
api_name:
- IADsPathname Property Methods
- IADsPathname.EscapedMode
- IADsPathname.get_EscapedMode
- IADsPathname.get_EscapedMode
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 949bd41ddb04618d238c0ddf09782e12fb228b26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262207"
---
# <a name="iadspathname-property-methods"></a><span data-ttu-id="71cef-104">Методы свойств Иадспаснаме</span><span class="sxs-lookup"><span data-stu-id="71cef-104">IADsPathname Property Methods</span></span>

<span data-ttu-id="71cef-105">Методы свойств интерфейса [**иадспаснаме**](/windows/desktop/api/Iads/nn-iads-iadspathname) получают или задают свойства **ескапедмоде** .</span><span class="sxs-lookup"><span data-stu-id="71cef-105">The property methods of the [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) interface get or set the **EscapedMode** properties.</span></span> <span data-ttu-id="71cef-106">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="71cef-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="71cef-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="71cef-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="71cef-108">**ескапедмоде**</span><span class="sxs-lookup"><span data-stu-id="71cef-108">**EscapedMode**</span></span>
<span data-ttu-id="71cef-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="71cef-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="71cef-110">Проверьте или укажите, как экранированные символы обрабатываются в пути.</span><span class="sxs-lookup"><span data-stu-id="71cef-110">Examine or specify how escaped characters are handled in a pathname.</span></span> <span data-ttu-id="71cef-111">Дополнительные сведения и определенные параметры см. в [**разделе \_ \_ \_ перечислимый режим экранирования ADS**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span><span class="sxs-lookup"><span data-stu-id="71cef-111">For more information and defined options, see [**ADS\_ESCAPE\_MODE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span></span>

<dt>

<span data-ttu-id="71cef-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="71cef-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="71cef-113">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="71cef-113">Scripting data type: **Long**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EscapedMode(
  [out] long* retval
);
HRESULT get_EscapedMode(
  [in] long* lnEscapedMode
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="71cef-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71cef-114">Remarks</span></span>

<span data-ttu-id="71cef-115">**Ескапедмоде** представляет состояние.</span><span class="sxs-lookup"><span data-stu-id="71cef-115">**EscapedMode** represents a state.</span></span> <span data-ttu-id="71cef-116">Его можно включить или отключить, задав для него AD \_ ескапедмоде \_ On или AD \_ ЕСКАПЕДМОДЕ \_ Off/AD \_ ескапедмоде \_ Off \_ ex.</span><span class="sxs-lookup"><span data-stu-id="71cef-116">You can turn it on or off, by setting it to ADS\_ESCAPEDMODE\_ON or ADS\_ESCAPEDMODE\_OFF/ADS\_ESCAPEDMODE\_OFF\_EX.</span></span> <span data-ttu-id="71cef-117">При включении или отключении все последующие извлечения создают экранированные или неэкранированные строки пути.</span><span class="sxs-lookup"><span data-stu-id="71cef-117">When it is turned on, or off, all subsequent retrievals produce escaped or unescaped path strings.</span></span>

<span data-ttu-id="71cef-118">В ADSI только [**иадспаснаме**](/windows/desktop/api/Iads/nn-iads-iadspathname) поддерживает рассылку путей.</span><span class="sxs-lookup"><span data-stu-id="71cef-118">In ADSI only the [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) is capable of unescaping paths.</span></span> <span data-ttu-id="71cef-119">Все остальные интерфейсы ADSI всегда возвращают экранированные пути.</span><span class="sxs-lookup"><span data-stu-id="71cef-119">All other ADSI interfaces always return escaped paths.</span></span> <span data-ttu-id="71cef-120">По умолчанию **ескапедмоде** является ADS \_ ескапедмоде \_ по умолчанию, как определено в [**\_ \_ \_ перечислении режима экранирования ADS**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span><span class="sxs-lookup"><span data-stu-id="71cef-120">The default state of **EscapedMode** is ADS\_ESCAPEDMODE\_DEFAULT as defined in [**ADS\_ESCAPE\_MODE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span></span>

## <a name="examples"></a><span data-ttu-id="71cef-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="71cef-121">Examples</span></span>

<span data-ttu-id="71cef-122">В следующем примере кода показано, как использовать включение/выключение свойства **ескапедмоде** для экранирования следующих трех специальных символов: "=", "," и "/".</span><span class="sxs-lookup"><span data-stu-id="71cef-122">The following code example shows how to use the **EscapedMode** property turn on/off escaping of the following three special characters: "=",",", and "/".</span></span>


```VB
Dim path As New Pathname
path.Set "CN=joy\=ful\,\/*", ADS_SETTYPE_DN
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' All escaped, producing:
                                          ' "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' Only "/" is unescaped:
                                          ' "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEDMODE_OFF_EX
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' All are unescaped:
                                          ' "LDAP://CN=joy=ful,/*"
 
 
path.Set "LDAP://CN=joy\=ful\,\/*", ADS_SETTYPE_FULL
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF_EX
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy=ful,/*"
```



<span data-ttu-id="71cef-123">В следующем примере кода показано, как использовать включение/выключение свойства **ескапедмоде** для экранирования следующих трех специальных символов: "=", "," и "/".</span><span class="sxs-lookup"><span data-stu-id="71cef-123">The following code example shows how to use the **EscapedMode** property turn on/off escaping of the following three special characters: "=",",", and "/".</span></span>


```VB
<%
Dim path
const ADS_SETTYPE_FULL = 1
const ADS_SETTYPE_DN   = 4
const ADS_FORMAT_WINDOWS = 1
const ADS_ESCAPEDMODE_ON = 2
const ADS_ESCAPEDMODE_OFF = 3
const ADS_ESCAPEDMODE_OFF_EX = 4
 
Set path = CreateObject("Pathname")
path.Set "CN=joy\=ful\,\/*", ADS_SETTYPE_DN
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  
' All escaped, producing:  "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  
' Only "/" is unescaped: "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEDMODE_OFF_EX
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  ' All are unescaped:
                                          ' "LDAP://CN=joy=ful,/*"
 
 
path.Set "LDAP://CN=joy\=ful\,\/*", ADS_SETTYPE_FULL
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF_EX
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy=ful,/*"
%>
```



<span data-ttu-id="71cef-124">В следующем примере кода показано, как работать со свойством **ескапедмоде** .</span><span class="sxs-lookup"><span data-stu-id="71cef-124">The following code example shows how to work with the **EscapedMode** property.</span></span> <span data-ttu-id="71cef-125">Проверка ошибок игнорируется.</span><span class="sxs-lookup"><span data-stu-id="71cef-125">Error checking is ignored.</span></span>


```C++
IADsPathname *pPathname=NULL;
HRESULT hr;
 
hr = CoCreateInstance(CLSID_Pathname,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IADsPathname,
                      (void**)&pPathname);
 
if(FAILED(hr)) 
{
    if(pPathname) pPathname->Release();
    return NULL;
}
 
pPathname->AddRef();
hr = pPathname->Set(CComBSTR("LDAP://CN=joy/ful\/*"), 
                    ADS_SETTYPE_FULL); 
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_OFF);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Unescaped path: %S\n",bstr);   

// Producing "LDAP://CN=joy/ful/*"

SysFreeString(bstr);
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_ON);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Escaped path: %S\n",bstr);

// Producing "LDAP://CN=joy/ful\/*"

SysFreeString(bstr);
 
// Set the path using ADS_SETTYPE_DN
 
hr = pPathname->Set(CComBSTR("CN=joy/ful\/*"), ADS_SETTYPE_DN); 
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_OFF);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Unescaped path: %S\n",bstr);   

// Producing "LDAP://CN=joy/ful/*"

SysFreeString(bstr);
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_ON);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Escaped path: %S\n",bstr);

// Producing "LDAP://CN=joy\/ful\/*"

SysFreeString(bstr);
 
hr = pPathname->Release();
```



## <a name="requirements"></a><span data-ttu-id="71cef-126">Требования</span><span class="sxs-lookup"><span data-stu-id="71cef-126">Requirements</span></span>



| <span data-ttu-id="71cef-127">Требование</span><span class="sxs-lookup"><span data-stu-id="71cef-127">Requirement</span></span> | <span data-ttu-id="71cef-128">Значение</span><span class="sxs-lookup"><span data-stu-id="71cef-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71cef-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71cef-129">Minimum supported client</span></span><br/> | <span data-ttu-id="71cef-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71cef-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="71cef-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71cef-131">Minimum supported server</span></span><br/> | <span data-ttu-id="71cef-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71cef-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="71cef-133">Header</span><span class="sxs-lookup"><span data-stu-id="71cef-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="71cef-134"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="71cef-134"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="71cef-135">DLL</span><span class="sxs-lookup"><span data-stu-id="71cef-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71cef-136"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71cef-136"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="71cef-137">IID</span><span class="sxs-lookup"><span data-stu-id="71cef-137">IID</span></span><br/>                      | <span data-ttu-id="71cef-138">IID \_ иадспаснаме определен как D592AED4-F420-11D0-A36E-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="71cef-138">IID\_IADsPathname is defined as D592AED4-F420-11D0-A36E-00C04FB950DC</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="71cef-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71cef-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71cef-140">**IADsPathname**</span><span class="sxs-lookup"><span data-stu-id="71cef-140">**IADsPathname**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspathname)
</dt> <dt>

[<span data-ttu-id="71cef-141">**\_ \_ перечислимый режим ЭКРАНИРОВАНия ADS \_**</span><span class="sxs-lookup"><span data-stu-id="71cef-141">**ADS\_ESCAPE\_MODE\_ENUM**</span></span>](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)
</dt> </dl>

 

 





