---
title: IMsRdpDeviceV2 Кмдевицеинстанце, свойство
description: Содержит экземпляр устройства Configuration Manager.
ms.assetid: 2a3e7001-7889-417f-8f9d-cc7a1776249f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Кмдевицеинстанце
- Службы удаленных рабочих столов свойства Кмдевицеинстанце, интерфейс IMsRdpDeviceV2
- Службы удаленных рабочих столов интерфейса IMsRdpDeviceV2, свойство Кмдевицеинстанце
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmDeviceInstance
- IMsRdpDeviceV2.get_CmDeviceInstance
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec036d5e2497f45fff389ec8af457a05fcc9fef9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681760"
---
# <a name="imsrdpdevicev2cmdeviceinstance-property"></a><span data-ttu-id="ebd30-106">Свойство IMsRdpDeviceV2:: Кмдевицеинстанце</span><span class="sxs-lookup"><span data-stu-id="ebd30-106">IMsRdpDeviceV2::CmDeviceInstance property</span></span>

<span data-ttu-id="ebd30-107">Содержит экземпляр устройства Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ebd30-107">Contains the configuration manager device instance of the device.</span></span>

<span data-ttu-id="ebd30-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ebd30-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd30-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebd30-109">Syntax</span></span>


```C++
HRESULT get_CmDeviceInstance(
  [out, retval] DWORD *pCmDeviceInstance
);
```



## <a name="property-value"></a><span data-ttu-id="ebd30-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ebd30-110">Property value</span></span>

<span data-ttu-id="ebd30-111">Экземпляр устройства Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ebd30-111">The configuration manager device instance of the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebd30-112">Требования</span><span class="sxs-lookup"><span data-stu-id="ebd30-112">Requirements</span></span>



| <span data-ttu-id="ebd30-113">Требование</span><span class="sxs-lookup"><span data-stu-id="ebd30-113">Requirement</span></span> | <span data-ttu-id="ebd30-114">Значение</span><span class="sxs-lookup"><span data-stu-id="ebd30-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd30-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ebd30-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ebd30-116">Windows 7 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="ebd30-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="ebd30-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ebd30-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ebd30-118">Windows Server 2008 R2 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="ebd30-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="ebd30-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ebd30-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="ebd30-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebd30-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ebd30-121">DLL</span><span class="sxs-lookup"><span data-stu-id="ebd30-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebd30-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebd30-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ebd30-123">IID</span><span class="sxs-lookup"><span data-stu-id="ebd30-123">IID</span></span><br/>                      | <span data-ttu-id="ebd30-124">IID \_ IMsRdpDeviceV2 определен как 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="ebd30-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="ebd30-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ebd30-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd30-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="ebd30-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





