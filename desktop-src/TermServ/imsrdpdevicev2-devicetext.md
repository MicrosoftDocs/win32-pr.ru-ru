---
title: IMsRdpDeviceV2 Девицетекст, свойство
description: Содержит текст устройства.
ms.assetid: 2a67e8d4-2af3-4738-ade2-a79800aea4a1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Девицетекст
- Службы удаленных рабочих столов свойства Девицетекст, интерфейс IMsRdpDeviceV2
- Службы удаленных рабочих столов интерфейса IMsRdpDeviceV2, свойство Девицетекст
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.DeviceText
- IMsRdpDeviceV2.get_DeviceText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fb35142a166db7e7c05fa5c0f00f7fdf2e1219c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262185"
---
# <a name="imsrdpdevicev2devicetext-property"></a><span data-ttu-id="535e1-106">IMsRdpDeviceV2: свойство Евицетекст:D</span><span class="sxs-lookup"><span data-stu-id="535e1-106">IMsRdpDeviceV2::DeviceText property</span></span>

<span data-ttu-id="535e1-107">Содержит текст устройства.</span><span class="sxs-lookup"><span data-stu-id="535e1-107">Contains the device text.</span></span> <span data-ttu-id="535e1-108">Это имя, которое Windows отображает пользователю.</span><span class="sxs-lookup"><span data-stu-id="535e1-108">This is the name that Windows displays to the user.</span></span>

<span data-ttu-id="535e1-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="535e1-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="535e1-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="535e1-110">Syntax</span></span>


```C++
HRESULT get_DeviceText(
  [out, retval] BSTR *pDeviceText
);
```



## <a name="property-value"></a><span data-ttu-id="535e1-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="535e1-111">Property value</span></span>

<span data-ttu-id="535e1-112">Отображаемое имя устройства.</span><span class="sxs-lookup"><span data-stu-id="535e1-112">The display name for the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="535e1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="535e1-113">Requirements</span></span>



| <span data-ttu-id="535e1-114">Требование</span><span class="sxs-lookup"><span data-stu-id="535e1-114">Requirement</span></span> | <span data-ttu-id="535e1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="535e1-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="535e1-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="535e1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="535e1-117">Windows 7 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="535e1-117">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="535e1-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="535e1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="535e1-119">Windows Server 2008 R2 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="535e1-119">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="535e1-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="535e1-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="535e1-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="535e1-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="535e1-122">DLL</span><span class="sxs-lookup"><span data-stu-id="535e1-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="535e1-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="535e1-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="535e1-124">IID</span><span class="sxs-lookup"><span data-stu-id="535e1-124">IID</span></span><br/>                      | <span data-ttu-id="535e1-125">IID \_ IMsRdpDeviceV2 определен как 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="535e1-125">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="535e1-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="535e1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="535e1-127">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="535e1-127">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





