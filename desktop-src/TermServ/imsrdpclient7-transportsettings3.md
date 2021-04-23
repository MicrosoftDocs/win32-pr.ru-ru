---
title: IMsRdpClient7 TransportSettings3, свойство
description: Извлекает объект, который поддерживает интерфейс IMsRdpClientTransportSettings3.
ms.assetid: d11f0943-241e-44cd-a98c-595916ab0718
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства TransportSettings3
- Службы удаленных рабочих столов свойства TransportSettings3, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство TransportSettings3
- Службы удаленных рабочих столов свойства TransportSettings3, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство TransportSettings3
- Службы удаленных рабочих столов свойства TransportSettings3, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство TransportSettings3
- Службы удаленных рабочих столов свойства TransportSettings3, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство TransportSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient7.TransportSettings3
- IMsRdpClient7.get_TransportSettings3
- IMsRdpClient8.TransportSettings3
- IMsRdpClient8.get_TransportSettings3
- IMsRdpClient9.TransportSettings3
- IMsRdpClient9.get_TransportSettings3
- IMsRdpClient10.TransportSettings3
- IMsRdpClient10.get_TransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c60b58f8f2438de0d43f69ce0b3bb73607e7551
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801571"
---
# <a name="imsrdpclient7transportsettings3-property"></a><span data-ttu-id="28850-112">Свойство IMsRdpClient7:: TransportSettings3</span><span class="sxs-lookup"><span data-stu-id="28850-112">IMsRdpClient7::TransportSettings3 property</span></span>

<span data-ttu-id="28850-113">Извлекает объект, который поддерживает интерфейс [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) .</span><span class="sxs-lookup"><span data-stu-id="28850-113">Retrieves an object that supports the [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) interface.</span></span>

<span data-ttu-id="28850-114">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="28850-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="28850-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28850-115">Syntax</span></span>


```C++
HRESULT get_TransportSettings3(
  [out, retval] IMsRdpClientTransportSettings3 **ppXportSet3
);
```



## <a name="property-value"></a><span data-ttu-id="28850-116">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="28850-116">Property value</span></span>

<span data-ttu-id="28850-117">Адрес указателя интерфейса [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) , который получает объект.</span><span class="sxs-lookup"><span data-stu-id="28850-117">The address of an [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="28850-118">Требования</span><span class="sxs-lookup"><span data-stu-id="28850-118">Requirements</span></span>



| <span data-ttu-id="28850-119">Требование</span><span class="sxs-lookup"><span data-stu-id="28850-119">Requirement</span></span> | <span data-ttu-id="28850-120">Значение</span><span class="sxs-lookup"><span data-stu-id="28850-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28850-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28850-121">Minimum supported client</span></span><br/> | <span data-ttu-id="28850-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="28850-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="28850-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28850-123">Minimum supported server</span></span><br/> | <span data-ttu-id="28850-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="28850-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="28850-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="28850-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="28850-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28850-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="28850-127">DLL</span><span class="sxs-lookup"><span data-stu-id="28850-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28850-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28850-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="28850-129">IID</span><span class="sxs-lookup"><span data-stu-id="28850-129">IID</span></span><br/>                      | <span data-ttu-id="28850-130">IID \_ IMsRdpClient7 определен как b2a5b5ce-3461-444a-91d4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="28850-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="28850-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28850-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28850-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="28850-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="28850-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="28850-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="28850-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="28850-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="28850-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="28850-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





