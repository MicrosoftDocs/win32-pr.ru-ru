---
title: IMsRdpClient7 SecuredSettings3, свойство
description: Извлекает объект, который поддерживает интерфейс IMsRdpClientSecuredSettings2.
ms.assetid: 500ce7ed-bd86-434c-baf8-f30dd667dca3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства SecuredSettings3
- Службы удаленных рабочих столов свойства SecuredSettings3, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство SecuredSettings3
- Службы удаленных рабочих столов свойства SecuredSettings3, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство SecuredSettings3
- Службы удаленных рабочих столов свойства SecuredSettings3, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство SecuredSettings3
- Службы удаленных рабочих столов свойства SecuredSettings3, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство SecuredSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient7.SecuredSettings3
- IMsRdpClient7.get_SecuredSettings3
- IMsRdpClient8.SecuredSettings3
- IMsRdpClient8.get_SecuredSettings3
- IMsRdpClient9.SecuredSettings3
- IMsRdpClient9.get_SecuredSettings3
- IMsRdpClient10.SecuredSettings3
- IMsRdpClient10.get_SecuredSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 219e3373a6ecb2f5b963a82800f4415f7de64534
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415065"
---
# <a name="imsrdpclient7securedsettings3-property"></a><span data-ttu-id="7cd16-112">Свойство IMsRdpClient7:: SecuredSettings3</span><span class="sxs-lookup"><span data-stu-id="7cd16-112">IMsRdpClient7::SecuredSettings3 property</span></span>

<span data-ttu-id="7cd16-113">Извлекает объект, который поддерживает интерфейс [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="7cd16-113">Retrieves an object that supports the [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) interface.</span></span>

<span data-ttu-id="7cd16-114">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7cd16-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd16-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cd16-115">Syntax</span></span>


```C++
HRESULT get_SecuredSettings3(
  [out] IMsRdpClientSecuredSettings2 **ppSecuredSettings
);
```



## <a name="property-value"></a><span data-ttu-id="7cd16-116">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7cd16-116">Property value</span></span>

<span data-ttu-id="7cd16-117">Адрес указателя интерфейса [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) , который получает объект.</span><span class="sxs-lookup"><span data-stu-id="7cd16-117">The address of an [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cd16-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7cd16-118">Requirements</span></span>



| <span data-ttu-id="7cd16-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7cd16-119">Requirement</span></span> | <span data-ttu-id="7cd16-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7cd16-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd16-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7cd16-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7cd16-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7cd16-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="7cd16-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7cd16-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7cd16-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7cd16-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="7cd16-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7cd16-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="7cd16-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cd16-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7cd16-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7cd16-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cd16-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cd16-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7cd16-129">IID</span><span class="sxs-lookup"><span data-stu-id="7cd16-129">IID</span></span><br/>                      | <span data-ttu-id="7cd16-130">IID \_ IMsRdpClient7 определен как b2a5b5ce-3461-444a-91d4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="7cd16-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7cd16-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7cd16-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cd16-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="7cd16-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="7cd16-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="7cd16-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="7cd16-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="7cd16-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="7cd16-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="7cd16-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





