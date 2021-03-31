---
title: Свойство IMsRdpCameraRedirConfig SymbolicLink
description: Возвращает символьную ссылку интерфейса **KSCATEGORY_VIDEO_CAMERA** для камеры.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства SymbolicLink
- Службы удаленных рабочих столов свойства SymbolicLink, интерфейс Имсрдпкамераредирконфиг
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфиг, свойство SymbolicLink
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.SymbolicLink
- IMsRdpCameraRedirConfig.SymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 439ead6fa0868887cc5965205b22236abb5aada6
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "103894010"
---
# <a name="imsrdpcameraredirconfigsymboliclink-property"></a><span data-ttu-id="f7c53-106">Свойство Имсрдпкамераредирконфиг:: SymbolicLink</span><span class="sxs-lookup"><span data-stu-id="f7c53-106">IMsRdpCameraRedirConfig::SymbolicLink property</span></span>

<span data-ttu-id="f7c53-107">Возвращает символьную ссылку интерфейса **KSCATEGORY_VIDEO_CAMERA** для камеры.</span><span class="sxs-lookup"><span data-stu-id="f7c53-107">Gets the symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

<span data-ttu-id="f7c53-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f7c53-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7c53-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7c53-109">Syntax</span></span>

```C++
HRESULT get_SymbolicLink(
    [out, retval] BSTR* pSymbolicLink
);
```

## <a name="property-value"></a><span data-ttu-id="f7c53-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f7c53-110">Property value</span></span>

<span data-ttu-id="f7c53-111">Символьная ссылка на интерфейс **KSCATEGORY_VIDEO_CAMERA** для камеры.</span><span class="sxs-lookup"><span data-stu-id="f7c53-111">The symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7c53-112">Требования</span><span class="sxs-lookup"><span data-stu-id="f7c53-112">Requirements</span></span>

| <span data-ttu-id="f7c53-113">Требование</span><span class="sxs-lookup"><span data-stu-id="f7c53-113">Requirement</span></span> | <span data-ttu-id="f7c53-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f7c53-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="f7c53-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7c53-115">Minimum supported client</span></span>| <span data-ttu-id="f7c53-116">Windows 10, версия 1803 (сборка 17134)</span><span class="sxs-lookup"><span data-stu-id="f7c53-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="f7c53-117">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f7c53-117">Type library</span></span>            | <span data-ttu-id="f7c53-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f7c53-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="f7c53-119">DLL</span><span class="sxs-lookup"><span data-stu-id="f7c53-119">DLL</span></span>                  | <span data-ttu-id="f7c53-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f7c53-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="f7c53-121">IID</span><span class="sxs-lookup"><span data-stu-id="f7c53-121">IID</span></span>                      | <span data-ttu-id="f7c53-122">IID \_ имсрдпкамераредирконфиг определен как 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="f7c53-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="f7c53-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7c53-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7c53-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="f7c53-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>