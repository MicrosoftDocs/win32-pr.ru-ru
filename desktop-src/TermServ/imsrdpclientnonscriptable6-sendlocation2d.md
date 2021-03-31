---
title: Метод IMsRdpClientNonScriptable6 SendLocation2D
description: Отправляет на сервер значение широты и долготы, благодаря чему географическое расположение клиента может быть отражено в удаленном сеансе.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода SendLocation2D
- Службы удаленных рабочих столов метода SendLocation2D, интерфейс IMsRdpClientNonScriptable6
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable6, метод SendLocation2D
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation2D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: b706fdb35ba8360b294d25021c0c1a18bbe90188
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "103805158"
---
# <a name="imsrdpclientnonscriptable6sendlocation2d-method"></a><span data-ttu-id="7d394-106">Метод IMsRdpClientNonScriptable6:: SendLocation2D</span><span class="sxs-lookup"><span data-stu-id="7d394-106">IMsRdpClientNonScriptable6::SendLocation2D method</span></span>

<span data-ttu-id="7d394-107">Отправляет на сервер значение широты и долготы, благодаря чему географическое расположение клиента может быть отражено в удаленном сеансе.</span><span class="sxs-lookup"><span data-stu-id="7d394-107">Sends a latitude and longitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d394-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d394-108">Syntax</span></span>

```C++
HRESULT SendLocation2D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude
);
```

## <a name="parameters"></a><span data-ttu-id="7d394-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d394-109">Parameters</span></span>

<span data-ttu-id="7d394-110">*Широта* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7d394-110">*latitude* \[in\]</span></span>

<span data-ttu-id="7d394-111">Широта географического расположения.</span><span class="sxs-lookup"><span data-stu-id="7d394-111">The latitude of a geographic location.</span></span> <span data-ttu-id="7d394-112">Допустимый диапазон значений широты — от-90,0 до 90,0 градусов.</span><span class="sxs-lookup"><span data-stu-id="7d394-112">The valid range of latitude values is from -90.0 to 90.0 degrees.</span></span>

<span data-ttu-id="7d394-113">*Долгота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7d394-113">*longitude* \[in\]</span></span>

<span data-ttu-id="7d394-114">Долгота географического расположения.</span><span class="sxs-lookup"><span data-stu-id="7d394-114">The longitude of a geographic location.</span></span> <span data-ttu-id="7d394-115">Допустимый диапазон значений широты — от-180,0 до 180,0 градусов.</span><span class="sxs-lookup"><span data-stu-id="7d394-115">The valid range of latitude values is from -180.0 to 180.0 degrees.</span></span>

## <a name="return-value"></a><span data-ttu-id="7d394-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d394-116">Return value</span></span>

<span data-ttu-id="7d394-117">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="7d394-117">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d394-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7d394-118">Requirements</span></span>

| <span data-ttu-id="7d394-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7d394-119">Requirement</span></span> | <span data-ttu-id="7d394-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7d394-120">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="7d394-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d394-121">Minimum supported client</span></span>| <span data-ttu-id="7d394-122">Windows 10, версия 1709 (сборка 16299)</span><span class="sxs-lookup"><span data-stu-id="7d394-122">Windows 10, version 1709 (build 16299)</span></span>      |
| <span data-ttu-id="7d394-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7d394-123">Type library</span></span>            | <span data-ttu-id="7d394-124">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="7d394-124">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="7d394-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7d394-125">DLL</span></span>                  | <span data-ttu-id="7d394-126">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="7d394-126">MsTscAx.dll</span></span>     |
| <span data-ttu-id="7d394-127">IID</span><span class="sxs-lookup"><span data-stu-id="7d394-127">IID</span></span>                      | <span data-ttu-id="7d394-128">IID \_ IMsRdpClientNonScriptable6 определен как 05293249-B28B-4DB8-BE64-1B2F496B910E</span><span class="sxs-lookup"><span data-stu-id="7d394-128">IID\_IMsRdpClientNonScriptable6 is defined as 05293249-B28B-4DB8-BE64-1B2F496B910E</span></span>            |

## <a name="see-also"></a><span data-ttu-id="7d394-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d394-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d394-130">**IMsRdpClientNonScriptable6**</span><span class="sxs-lookup"><span data-stu-id="7d394-130">**IMsRdpClientNonScriptable6**</span></span>](imsrdpclientnonscriptable6.md)
</dt> </dl>
