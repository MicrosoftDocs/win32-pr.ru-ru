---
title: Имсрдпдевицеколлектион Девицебид, свойство
description: Извлекает устройство с указанным идентификатором.
ms.assetid: b64e83fa-5a94-4080-8efa-45cbfe5ceb88
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Девицебид
- Службы удаленных рабочих столов свойства Девицебид, интерфейс Имсрдпдевицеколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпдевицеколлектион, свойство Девицебид
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceById
- IMsRdpDeviceCollection.get_DeviceById
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 228e3c7cf03457ca740d4a415257008988215077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490341"
---
# <a name="imsrdpdevicecollectiondevicebyid-property"></a><span data-ttu-id="50a0d-106">Имсрдпдевицеколлектион: свойство Евицебид:D</span><span class="sxs-lookup"><span data-stu-id="50a0d-106">IMsRdpDeviceCollection::DeviceById property</span></span>

<span data-ttu-id="50a0d-107">Извлекает устройство с указанным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="50a0d-107">Retrieves the device with the specified identifier.</span></span>

<span data-ttu-id="50a0d-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="50a0d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="50a0d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50a0d-109">Syntax</span></span>


```C++
HRESULT get_DeviceById(
  [in]          BSTR devInstanceId,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a><span data-ttu-id="50a0d-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="50a0d-110">Property value</span></span>

<span data-ttu-id="50a0d-111">Указатель интерфейса [**имсрдпдевице**](imsrdpdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="50a0d-111">An [**IMsRdpDevice**](imsrdpdevice.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="50a0d-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="50a0d-112">Error codes</span></span>

<span data-ttu-id="50a0d-113">Если метод выполнен успешно, возвращается значение **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="50a0d-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="50a0d-114">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="50a0d-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="50a0d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="50a0d-115">Requirements</span></span>



| <span data-ttu-id="50a0d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="50a0d-116">Requirement</span></span> | <span data-ttu-id="50a0d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="50a0d-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="50a0d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50a0d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="50a0d-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50a0d-119">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="50a0d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50a0d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="50a0d-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50a0d-121">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="50a0d-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="50a0d-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="50a0d-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50a0d-123"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="50a0d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="50a0d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50a0d-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50a0d-125"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="50a0d-126">IID</span><span class="sxs-lookup"><span data-stu-id="50a0d-126">IID</span></span><br/>                      | <span data-ttu-id="50a0d-127">IID \_ имсрдпдевицеколлектион определен как 56540617-d281-488c-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="50a0d-127">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50a0d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50a0d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50a0d-129">**имсрдпдевицеколлектион**</span><span class="sxs-lookup"><span data-stu-id="50a0d-129">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





