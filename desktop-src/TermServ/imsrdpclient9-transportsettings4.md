---
title: IMsRdpClient9 TransportSettings4, свойство
description: Извлекает объект, который поддерживает интерфейс IMsRdpClientTransportSettings4.
ms.assetid: 808259b9-a1a4-4611-8602-b6877013c4f6
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства TransportSettings4
- Службы удаленных рабочих столов свойства TransportSettings4, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство TransportSettings4
- Службы удаленных рабочих столов свойства TransportSettings4, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство TransportSettings4
topic_type:
- apiref
api_name:
- IMsRdpClient9.TransportSettings4
- IMsRdpClient9.get_TransportSettings4
- IMsRdpClient10.TransportSettings4
- IMsRdpClient10.get_TransportSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765d2ad5a50e0608e4c11731742debbaede51737
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340380"
---
# <a name="imsrdpclient9transportsettings4-property"></a><span data-ttu-id="0f80b-108">Свойство IMsRdpClient9:: TransportSettings4</span><span class="sxs-lookup"><span data-stu-id="0f80b-108">IMsRdpClient9::TransportSettings4 property</span></span>

<span data-ttu-id="0f80b-109">Извлекает объект, который поддерживает интерфейс [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="0f80b-109">Retrieves an object that supports the [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) interface.</span></span>

<span data-ttu-id="0f80b-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0f80b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f80b-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f80b-111">Syntax</span></span>


```C++
HRESULT get_TransportSettings4(
  [out, retval] IMsRdpClientTransportSettings4 **ppXportSet4
);
```



## <a name="property-value"></a><span data-ttu-id="0f80b-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0f80b-112">Property value</span></span>

<span data-ttu-id="0f80b-113">Возвращает указатель на интерфейс [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="0f80b-113">Returns an [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f80b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0f80b-114">Requirements</span></span>



| <span data-ttu-id="0f80b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0f80b-115">Requirement</span></span> | <span data-ttu-id="0f80b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0f80b-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f80b-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f80b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0f80b-118">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0f80b-118">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="0f80b-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f80b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0f80b-120">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0f80b-120">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="0f80b-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="0f80b-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="0f80b-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f80b-122"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="0f80b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0f80b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f80b-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f80b-124"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="0f80b-125">IID</span><span class="sxs-lookup"><span data-stu-id="0f80b-125">IID</span></span><br/>                      | <span data-ttu-id="0f80b-126">\_MSRDPCLIENT9 CLSID определен как 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="0f80b-126">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="0f80b-127">\_MSRDPCLIENT9NOTSAFEFORSCRIPTING CLSID определен как 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="0f80b-127">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="0f80b-128">IID \_ IMsRdpClient9 определен как 28904001-04B6-436C-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="0f80b-128">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0f80b-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f80b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f80b-130">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="0f80b-130">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="0f80b-131">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="0f80b-131">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





