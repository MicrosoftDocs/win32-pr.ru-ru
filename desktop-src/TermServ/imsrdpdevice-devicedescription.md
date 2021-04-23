---
title: Имсрдпдевице DeviceDescription, свойство
description: Возвращает описание устройства, отображаемое пользователю, если отображаемое имя недоступно.
ms.assetid: 969f96c6-5655-4cac-9e91-059114dc3815
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства DeviceDescription
- Службы удаленных рабочих столов свойства DeviceDescription, интерфейс Имсрдпдевице
- Службы удаленных рабочих столов интерфейса Имсрдпдевице, свойство DeviceDescription
topic_type:
- apiref
api_name:
- IMsRdpDevice.DeviceDescription
- IMsRdpDevice.get_DeviceDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e352acef945c09c6be592174dd86a46cd8689aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136522"
---
# <a name="imsrdpdevicedevicedescription-property"></a><span data-ttu-id="6ca5f-106">Имсрдпдевице: свойство Евицедескриптион:D</span><span class="sxs-lookup"><span data-stu-id="6ca5f-106">IMsRdpDevice::DeviceDescription property</span></span>

<span data-ttu-id="6ca5f-107">Возвращает описание устройства, отображаемое пользователю, если отображаемое имя недоступно.</span><span class="sxs-lookup"><span data-stu-id="6ca5f-107">Retrieves the device description to be displayed to the user if the display name is not available.</span></span>

<span data-ttu-id="6ca5f-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6ca5f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ca5f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ca5f-109">Syntax</span></span>


```C++
HRESULT get_DeviceDescription(
  [out] BSTR *pDeviceDescription
);
```



## <a name="property-value"></a><span data-ttu-id="6ca5f-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6ca5f-110">Property value</span></span>

<span data-ttu-id="6ca5f-111">Описание устройства.</span><span class="sxs-lookup"><span data-stu-id="6ca5f-111">The device description.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6ca5f-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="6ca5f-112">Error codes</span></span>

<span data-ttu-id="6ca5f-113">Если метод выполнен успешно, возвращается значение **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="6ca5f-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="6ca5f-114">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="6ca5f-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ca5f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="6ca5f-115">Requirements</span></span>



| <span data-ttu-id="6ca5f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6ca5f-116">Requirement</span></span> | <span data-ttu-id="6ca5f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6ca5f-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ca5f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ca5f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6ca5f-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ca5f-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6ca5f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ca5f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6ca5f-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ca5f-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6ca5f-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="6ca5f-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="6ca5f-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ca5f-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6ca5f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6ca5f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ca5f-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ca5f-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6ca5f-126">IID</span><span class="sxs-lookup"><span data-stu-id="6ca5f-126">IID</span></span><br/>                      | <span data-ttu-id="6ca5f-127">IID \_ имсрдпдевице определен как 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="6ca5f-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="6ca5f-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ca5f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ca5f-129">**имсрдпдевице**</span><span class="sxs-lookup"><span data-stu-id="6ca5f-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





