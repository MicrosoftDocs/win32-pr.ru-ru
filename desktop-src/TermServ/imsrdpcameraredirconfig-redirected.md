---
title: Свойство IMsRdpCameraRedirConfig Redirected
description: Указывает, будет ли перенаправлена камера.
ms.tgt_platform: multiple
keywords:
- Перенаправленное свойство службы удаленных рабочих столов
- Перенаправленное свойство службы удаленных рабочих столов, интерфейс Имсрдпкамераредирконфиг
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфиг, перенаправленное свойство
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.Redirected
- IMsRdpCameraRedirConfig.put_Redirected
- IMsRdpCameraRedirConfig.get_Redirected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: f81dc643f7911029df088bbb692d7c8c06fddac4
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104494169"
---
# <a name="imsrdpcameraredirconfigredirected-property"></a><span data-ttu-id="e3577-106">Свойство Имсрдпкамераредирконфиг:: Redirected</span><span class="sxs-lookup"><span data-stu-id="e3577-106">IMsRdpCameraRedirConfig::Redirected property</span></span>

<span data-ttu-id="e3577-107">Указывает, будет ли перенаправлена камера.</span><span class="sxs-lookup"><span data-stu-id="e3577-107">Specifies whether or not the camera is redirected.</span></span>

<span data-ttu-id="e3577-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e3577-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3577-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3577-109">Syntax</span></span>

```C++
HRESULT put_Redirected(
    [in] VARIANT_BOOL fRedirected
);

HRESULT get_Redirected(
    [out, retval] VARIANT_BOOL* pfRedirected
);
```

## <a name="property-value"></a><span data-ttu-id="e3577-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e3577-110">Property value</span></span>

<span data-ttu-id="e3577-111">Значение типа, указывающее, перенаправляется ли камера.</span><span class="sxs-lookup"><span data-stu-id="e3577-111">A value that specifies whether or not the camera is redirected.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3577-112">Требования</span><span class="sxs-lookup"><span data-stu-id="e3577-112">Requirements</span></span>

| <span data-ttu-id="e3577-113">Требование</span><span class="sxs-lookup"><span data-stu-id="e3577-113">Requirement</span></span> | <span data-ttu-id="e3577-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e3577-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="e3577-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3577-115">Minimum supported client</span></span>| <span data-ttu-id="e3577-116">Windows 10, версия 1803 (сборка 17134)</span><span class="sxs-lookup"><span data-stu-id="e3577-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="e3577-117">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e3577-117">Type library</span></span>            | <span data-ttu-id="e3577-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="e3577-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="e3577-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e3577-119">DLL</span></span>                  | <span data-ttu-id="e3577-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="e3577-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="e3577-121">IID</span><span class="sxs-lookup"><span data-stu-id="e3577-121">IID</span></span>                      | <span data-ttu-id="e3577-122">IID \_ имсрдпкамераредирконфиг определен как 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="e3577-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="e3577-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3577-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3577-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="e3577-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>