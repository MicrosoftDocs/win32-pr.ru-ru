---
title: IMsRdpClient7 RemoteProgram2, свойство
description: Извлекает объект, который поддерживает интерфейс ITSRemoteProgram2.
ms.assetid: fabdc933-c941-487f-9e49-c20a39e0c86e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства RemoteProgram2
- Службы удаленных рабочих столов свойства RemoteProgram2, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство RemoteProgram2
- Службы удаленных рабочих столов свойства RemoteProgram2, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство RemoteProgram2
- Службы удаленных рабочих столов свойства RemoteProgram2, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство RemoteProgram2
- Службы удаленных рабочих столов свойства RemoteProgram2, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство RemoteProgram2
topic_type:
- apiref
api_name:
- IMsRdpClient7.RemoteProgram2
- IMsRdpClient7.get_RemoteProgram2
- IMsRdpClient8.RemoteProgram2
- IMsRdpClient8.get_RemoteProgram2
- IMsRdpClient9.RemoteProgram2
- IMsRdpClient9.get_RemoteProgram2
- IMsRdpClient10.RemoteProgram2
- IMsRdpClient10.get_RemoteProgram2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1572aada1384a7edfe88b198826050927ae3cff5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988342"
---
# <a name="imsrdpclient7remoteprogram2-property"></a><span data-ttu-id="923c0-112">Свойство IMsRdpClient7:: RemoteProgram2</span><span class="sxs-lookup"><span data-stu-id="923c0-112">IMsRdpClient7::RemoteProgram2 property</span></span>

<span data-ttu-id="923c0-113">Извлекает объект, который поддерживает интерфейс [**ITSRemoteProgram2**](itsremoteprogram2.md) .</span><span class="sxs-lookup"><span data-stu-id="923c0-113">Retrieves an object that supports the [**ITSRemoteProgram2**](itsremoteprogram2.md) interface.</span></span>

<span data-ttu-id="923c0-114">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="923c0-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="923c0-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="923c0-115">Syntax</span></span>


```C++
HRESULT get_RemoteProgram2(
  [out, retval] ITSRemoteProgram2 **ppRemoteProgram
);
```



## <a name="property-value"></a><span data-ttu-id="923c0-116">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="923c0-116">Property value</span></span>

<span data-ttu-id="923c0-117">Адрес указателя интерфейса [**ITSRemoteProgram2**](itsremoteprogram2.md) , который получает объект.</span><span class="sxs-lookup"><span data-stu-id="923c0-117">The address of an [**ITSRemoteProgram2**](itsremoteprogram2.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="923c0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="923c0-118">Requirements</span></span>



| <span data-ttu-id="923c0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="923c0-119">Requirement</span></span> | <span data-ttu-id="923c0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="923c0-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="923c0-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="923c0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="923c0-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="923c0-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="923c0-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="923c0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="923c0-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="923c0-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="923c0-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="923c0-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="923c0-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="923c0-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="923c0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="923c0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="923c0-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="923c0-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="923c0-129">IID</span><span class="sxs-lookup"><span data-stu-id="923c0-129">IID</span></span><br/>                      | <span data-ttu-id="923c0-130">IID \_ IMsRdpClient7 определен как b2a5b5ce-3461-444a-91d4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="923c0-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="923c0-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="923c0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="923c0-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="923c0-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="923c0-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="923c0-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="923c0-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="923c0-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="923c0-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="923c0-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





