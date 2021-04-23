---
title: IMsRdpDeviceV2 Исоптионалдевице, свойство
description: Указывает, является ли устройство необязательным для перенаправления USB.
ms.assetid: a7226c40-7e22-48af-9895-b1fb1f861b58
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Исоптионалдевице
- Службы удаленных рабочих столов свойства Исоптионалдевице, интерфейс IMsRdpDeviceV2
- Службы удаленных рабочих столов интерфейса IMsRdpDeviceV2, свойство Исоптионалдевице
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsOptionalDevice
- IMsRdpDeviceV2.get_IsOptionalDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad0e459a91e88573515128ca37033768f7839ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491634"
---
# <a name="imsrdpdevicev2isoptionaldevice-property"></a><span data-ttu-id="89e3e-106">Свойство IMsRdpDeviceV2:: Исоптионалдевице</span><span class="sxs-lookup"><span data-stu-id="89e3e-106">IMsRdpDeviceV2::IsOptionalDevice property</span></span>

<span data-ttu-id="89e3e-107">Указывает, является ли устройство необязательным для перенаправления USB.</span><span class="sxs-lookup"><span data-stu-id="89e3e-107">Specifies if the device is optional for USB redirection.</span></span>

<span data-ttu-id="89e3e-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="89e3e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="89e3e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89e3e-109">Syntax</span></span>


```C++
HRESULT get_IsOptionalDevice(
  [out, retval] VARIANT_BOOL *pvboolOptionalDevice
);
```



## <a name="property-value"></a><span data-ttu-id="89e3e-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="89e3e-110">Property value</span></span>

<span data-ttu-id="89e3e-111">**значение true** , если устройство является необязательным; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="89e3e-111">**true** if the device is a optional; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="89e3e-112">Требования</span><span class="sxs-lookup"><span data-stu-id="89e3e-112">Requirements</span></span>



| <span data-ttu-id="89e3e-113">Требование</span><span class="sxs-lookup"><span data-stu-id="89e3e-113">Requirement</span></span> | <span data-ttu-id="89e3e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="89e3e-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89e3e-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89e3e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="89e3e-116">Windows 7 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="89e3e-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="89e3e-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89e3e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="89e3e-118">Windows Server 2008 R2 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="89e3e-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="89e3e-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="89e3e-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="89e3e-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89e3e-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="89e3e-121">DLL</span><span class="sxs-lookup"><span data-stu-id="89e3e-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89e3e-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89e3e-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="89e3e-123">IID</span><span class="sxs-lookup"><span data-stu-id="89e3e-123">IID</span></span><br/>                      | <span data-ttu-id="89e3e-124">IID \_ IMsRdpDeviceV2 определен как 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="89e3e-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="89e3e-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89e3e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89e3e-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="89e3e-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





