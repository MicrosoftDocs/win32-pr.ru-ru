---
title: IMsRdpDeviceV2 Исусбдевице, свойство
description: Указывает, что устройство предназначено для перенаправления USB.
ms.assetid: df4c9764-ad96-4f35-9537-3890293a944c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Исусбдевице
- Службы удаленных рабочих столов свойства Исусбдевице, интерфейс IMsRdpDeviceV2
- Службы удаленных рабочих столов интерфейса IMsRdpDeviceV2, свойство Исусбдевице
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsUSBDevice
- IMsRdpDeviceV2.get_IsUSBDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3741972fdd81887713e75ed5b596e0ba1a10fd3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414752"
---
# <a name="imsrdpdevicev2isusbdevice-property"></a><span data-ttu-id="f5d60-106">Свойство IMsRdpDeviceV2:: Исусбдевице</span><span class="sxs-lookup"><span data-stu-id="f5d60-106">IMsRdpDeviceV2::IsUSBDevice property</span></span>

<span data-ttu-id="f5d60-107">Указывает, что устройство предназначено для перенаправления USB.</span><span class="sxs-lookup"><span data-stu-id="f5d60-107">Specifies if the device is for USB redirection.</span></span>

<span data-ttu-id="f5d60-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f5d60-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5d60-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5d60-109">Syntax</span></span>


```C++
HRESULT get_IsUSBDevice(
  [out, retval] VARIANT_BOOL *pvboolUSBDevice
);
```



## <a name="property-value"></a><span data-ttu-id="f5d60-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f5d60-110">Property value</span></span>

<span data-ttu-id="f5d60-111">**значение true** , если устройство предназначено для перенаправления USB; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f5d60-111">**true** if the device is for USB redirection; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5d60-112">Требования</span><span class="sxs-lookup"><span data-stu-id="f5d60-112">Requirements</span></span>



| <span data-ttu-id="f5d60-113">Требование</span><span class="sxs-lookup"><span data-stu-id="f5d60-113">Requirement</span></span> | <span data-ttu-id="f5d60-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f5d60-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5d60-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5d60-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f5d60-116">Windows 7 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="f5d60-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="f5d60-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5d60-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f5d60-118">Windows Server 2008 R2 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="f5d60-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="f5d60-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f5d60-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="f5d60-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5d60-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f5d60-121">DLL</span><span class="sxs-lookup"><span data-stu-id="f5d60-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5d60-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5d60-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f5d60-123">IID</span><span class="sxs-lookup"><span data-stu-id="f5d60-123">IID</span></span><br/>                      | <span data-ttu-id="f5d60-124">IID \_ IMsRdpDeviceV2 определен как 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="f5d60-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="f5d60-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5d60-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5d60-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="f5d60-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





