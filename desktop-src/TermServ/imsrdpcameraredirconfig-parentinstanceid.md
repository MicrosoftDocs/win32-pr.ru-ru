---
title: Свойство IMsRdpCameraRedirConfig ParentInstanceId
description: Возвращает идентификатор родительского экземпляра устройства камеры.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Парентинстанцеид
- Службы удаленных рабочих столов свойства Парентинстанцеид, интерфейс Имсрдпкамераредирконфиг
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфиг, свойство Парентинстанцеид
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.ParentInstanceId
- IMsRdpCameraRedirConfig.get_ParentInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e4a399659c33000207930bfe7d17818a2ad8438f
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "105719224"
---
# <a name="imsrdpcameraredirconfigparentinstanceid-property"></a><span data-ttu-id="8c768-106">Имсрдпкамераредирконфиг: свойство Арентинстанцеид:P</span><span class="sxs-lookup"><span data-stu-id="8c768-106">IMsRdpCameraRedirConfig::ParentInstanceId property</span></span>

<span data-ttu-id="8c768-107">Возвращает идентификатор родительского экземпляра устройства камеры.</span><span class="sxs-lookup"><span data-stu-id="8c768-107">Gets the parent device instance ID of the camera.</span></span>

<span data-ttu-id="8c768-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8c768-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c768-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c768-109">Syntax</span></span>

```C++
HRESULT get_ParentInstanceId(
    [out, retval] BSTR* pParentInstanceId
);
```

## <a name="property-value"></a><span data-ttu-id="8c768-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8c768-110">Property value</span></span>

<span data-ttu-id="8c768-111">Идентификатор родительского экземпляра устройства камеры.</span><span class="sxs-lookup"><span data-stu-id="8c768-111">The parent device instance ID of the camera.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c768-112">Требования</span><span class="sxs-lookup"><span data-stu-id="8c768-112">Requirements</span></span>

| <span data-ttu-id="8c768-113">Требование</span><span class="sxs-lookup"><span data-stu-id="8c768-113">Requirement</span></span> | <span data-ttu-id="8c768-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8c768-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="8c768-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c768-115">Minimum supported client</span></span>| <span data-ttu-id="8c768-116">Windows 10, версия 1803 (сборка 17134)</span><span class="sxs-lookup"><span data-stu-id="8c768-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="8c768-117">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="8c768-117">Type library</span></span>            | <span data-ttu-id="8c768-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="8c768-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="8c768-119">DLL</span><span class="sxs-lookup"><span data-stu-id="8c768-119">DLL</span></span>                  | <span data-ttu-id="8c768-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="8c768-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="8c768-121">IID</span><span class="sxs-lookup"><span data-stu-id="8c768-121">IID</span></span>                      | <span data-ttu-id="8c768-122">IID \_ имсрдпкамераредирконфиг определен как 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="8c768-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="8c768-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c768-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c768-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="8c768-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>