---
title: Свойство IMsRdpCameraRedirConfig DeviceExists
description: Указывает, существует ли устройство камеры (т. е. Камера подключено).
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Девицеексистс
- Службы удаленных рабочих столов свойства Девицеексистс, интерфейс Имсрдпкамераредирконфиг
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфиг, свойство Девицеексистс
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.DeviceExists
- IMsRdpCameraRedirConfig.get_DeviceExists
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 368b2d46e6dfc2c32c0bb294edceda31f8a58f4e
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104494175"
---
# <a name="imsrdpcameraredirconfigdeviceexists-property"></a><span data-ttu-id="002b9-106">Имсрдпкамераредирконфиг: свойство Евицеексистс:D</span><span class="sxs-lookup"><span data-stu-id="002b9-106">IMsRdpCameraRedirConfig::DeviceExists property</span></span>

<span data-ttu-id="002b9-107">Указывает, существует ли устройство камеры (т. е. Камера подключено).</span><span class="sxs-lookup"><span data-stu-id="002b9-107">Specifies whether or not the camera device currently exists (that is, the camera is connected).</span></span>

<span data-ttu-id="002b9-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="002b9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="002b9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="002b9-109">Syntax</span></span>

```C++
HRESULT get_DeviceExists(
    [out, retval] VARIANT_BOOL* pfExists
);
```

## <a name="property-value"></a><span data-ttu-id="002b9-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="002b9-110">Property value</span></span>

<span data-ttu-id="002b9-111">Значение, указывающее, существует ли устройство камеры в данный момент (то есть подключение камеры).</span><span class="sxs-lookup"><span data-stu-id="002b9-111">A value that indicates whether or not the camera device currently exists (that is, the camera is connected).</span></span>

## <a name="requirements"></a><span data-ttu-id="002b9-112">Требования</span><span class="sxs-lookup"><span data-stu-id="002b9-112">Requirements</span></span>

| <span data-ttu-id="002b9-113">Требование</span><span class="sxs-lookup"><span data-stu-id="002b9-113">Requirement</span></span> | <span data-ttu-id="002b9-114">Значение</span><span class="sxs-lookup"><span data-stu-id="002b9-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="002b9-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="002b9-115">Minimum supported client</span></span>| <span data-ttu-id="002b9-116">Windows 10, версия 1803 (сборка 17134)</span><span class="sxs-lookup"><span data-stu-id="002b9-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="002b9-117">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="002b9-117">Type library</span></span>            | <span data-ttu-id="002b9-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="002b9-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="002b9-119">DLL</span><span class="sxs-lookup"><span data-stu-id="002b9-119">DLL</span></span>                  | <span data-ttu-id="002b9-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="002b9-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="002b9-121">IID</span><span class="sxs-lookup"><span data-stu-id="002b9-121">IID</span></span>                      | <span data-ttu-id="002b9-122">IID \_ имсрдпкамераредирконфиг определен как 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="002b9-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="002b9-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="002b9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="002b9-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="002b9-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>