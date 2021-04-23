---
title: IMsRdpDeviceV2 Искомпоситедевице, свойство
description: Указывает, является ли устройство составным.
ms.assetid: cc54f3f0-de0b-4f75-b5a1-4f061ac95ab5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Искомпоситедевице
- Службы удаленных рабочих столов свойства Искомпоситедевице, интерфейс IMsRdpDeviceV2
- Службы удаленных рабочих столов интерфейса IMsRdpDeviceV2, свойство Искомпоситедевице
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsCompositeDevice
- IMsRdpDeviceV2.get_IsCompositeDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2341544543f436272486a839ffdd3ee68a4a4478
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489111"
---
# <a name="imsrdpdevicev2iscompositedevice-property"></a><span data-ttu-id="56e36-106">Свойство IMsRdpDeviceV2:: Искомпоситедевице</span><span class="sxs-lookup"><span data-stu-id="56e36-106">IMsRdpDeviceV2::IsCompositeDevice property</span></span>

<span data-ttu-id="56e36-107">Указывает, является ли устройство составным.</span><span class="sxs-lookup"><span data-stu-id="56e36-107">Specifies if the device is a composite device.</span></span>

<span data-ttu-id="56e36-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="56e36-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="56e36-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56e36-109">Syntax</span></span>


```C++
HRESULT get_IsCompositeDevice(
  [out, retval] VARIANT_BOOL *pvboolCompositeDevice
);
```



## <a name="property-value"></a><span data-ttu-id="56e36-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="56e36-110">Property value</span></span>

<span data-ttu-id="56e36-111">**значение true** , если устройство является составным устройством; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="56e36-111">**true** if the device is a composite device; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="56e36-112">Требования</span><span class="sxs-lookup"><span data-stu-id="56e36-112">Requirements</span></span>



| <span data-ttu-id="56e36-113">Требование</span><span class="sxs-lookup"><span data-stu-id="56e36-113">Requirement</span></span> | <span data-ttu-id="56e36-114">Значение</span><span class="sxs-lookup"><span data-stu-id="56e36-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56e36-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56e36-115">Minimum supported client</span></span><br/> | <span data-ttu-id="56e36-116">Windows 7 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="56e36-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="56e36-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56e36-117">Minimum supported server</span></span><br/> | <span data-ttu-id="56e36-118">Windows Server 2008 R2 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="56e36-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="56e36-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="56e36-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="56e36-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56e36-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="56e36-121">DLL</span><span class="sxs-lookup"><span data-stu-id="56e36-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56e36-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56e36-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="56e36-123">IID</span><span class="sxs-lookup"><span data-stu-id="56e36-123">IID</span></span><br/>                      | <span data-ttu-id="56e36-124">IID \_ IMsRdpDeviceV2 определен как 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="56e36-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="56e36-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56e36-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56e36-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="56e36-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





