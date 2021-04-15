---
title: Метод IMsRdpClientNonScriptable6 SendLocation3D
description: Отправляет на сервер значение широты, долготы и высоты, чтобы географическое расположение клиента можно было отражать в удаленном сеансе.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода SendLocation3D
- Службы удаленных рабочих столов метода SendLocation3D, интерфейс IMsRdpClientNonScriptable6
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable6, метод SendLocation3D
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation3D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: c63e779b6d6d090544af40a7ee6d9c05f8c49494
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104494145"
---
# <a name="imsrdpclientnonscriptable6sendlocation3d-method"></a><span data-ttu-id="925b1-106">Метод IMsRdpClientNonScriptable6:: SendLocation3D</span><span class="sxs-lookup"><span data-stu-id="925b1-106">IMsRdpClientNonScriptable6::SendLocation3D method</span></span>

<span data-ttu-id="925b1-107">Отправляет на сервер значение широты, долготы и высоты, чтобы географическое расположение клиента можно было отражать в удаленном сеансе.</span><span class="sxs-lookup"><span data-stu-id="925b1-107">Sends a latitude, longitude and altitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="925b1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="925b1-108">Syntax</span></span>

```C++
HRESULT SendLocation3D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude,
  [in] INT32 altitude
);
```

## <a name="parameters"></a><span data-ttu-id="925b1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="925b1-109">Parameters</span></span>

<span data-ttu-id="925b1-110">*Широта* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="925b1-110">*latitude* \[in\]</span></span>

<span data-ttu-id="925b1-111">Широта географического расположения.</span><span class="sxs-lookup"><span data-stu-id="925b1-111">The latitude of a geographic location.</span></span> <span data-ttu-id="925b1-112">Допустимый диапазон значений широты — от-90,0 до 90,0 градусов.</span><span class="sxs-lookup"><span data-stu-id="925b1-112">The valid range of latitude values is from -90.0 to 90.0 degrees.</span></span>

<span data-ttu-id="925b1-113">*Долгота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="925b1-113">*longitude* \[in\]</span></span>

<span data-ttu-id="925b1-114">Долгота географического расположения.</span><span class="sxs-lookup"><span data-stu-id="925b1-114">The longitude of a geographic location.</span></span> <span data-ttu-id="925b1-115">Допустимый диапазон значений широты — от-180,0 до 180,0 градусов.</span><span class="sxs-lookup"><span data-stu-id="925b1-115">The valid range of latitude values is from -180.0 to 180.0 degrees.</span></span>

<span data-ttu-id="925b1-116">*Высота высотой* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="925b1-116">*altitude* \[in\]</span></span>

<span data-ttu-id="925b1-117">Высота географического расположения в метрах.</span><span class="sxs-lookup"><span data-stu-id="925b1-117">The altitude of a geographic location in meters.</span></span>

## <a name="return-value"></a><span data-ttu-id="925b1-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="925b1-118">Return value</span></span>

<span data-ttu-id="925b1-119">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="925b1-119">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="925b1-120">Требования</span><span class="sxs-lookup"><span data-stu-id="925b1-120">Requirements</span></span>

| <span data-ttu-id="925b1-121">Требование</span><span class="sxs-lookup"><span data-stu-id="925b1-121">Requirement</span></span> | <span data-ttu-id="925b1-122">Значение</span><span class="sxs-lookup"><span data-stu-id="925b1-122">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="925b1-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="925b1-123">Minimum supported client</span></span>| <span data-ttu-id="925b1-124">Windows 10, версия 1709 (сборка 16299)</span><span class="sxs-lookup"><span data-stu-id="925b1-124">Windows 10, version 1709 (build 16299)</span></span>      |
| <span data-ttu-id="925b1-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="925b1-125">Type library</span></span>            | <span data-ttu-id="925b1-126">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="925b1-126">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="925b1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="925b1-127">DLL</span></span>                  | <span data-ttu-id="925b1-128">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="925b1-128">MsTscAx.dll</span></span>     |
| <span data-ttu-id="925b1-129">IID</span><span class="sxs-lookup"><span data-stu-id="925b1-129">IID</span></span>                      | <span data-ttu-id="925b1-130">IID \_ IMsRdpClientNonScriptable6 определен как 05293249-B28B-4DB8-BE64-1B2F496B910E</span><span class="sxs-lookup"><span data-stu-id="925b1-130">IID\_IMsRdpClientNonScriptable6 is defined as 05293249-B28B-4DB8-BE64-1B2F496B910E</span></span>            |

## <a name="see-also"></a><span data-ttu-id="925b1-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="925b1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="925b1-132">**IMsRdpClientNonScriptable6**</span><span class="sxs-lookup"><span data-stu-id="925b1-132">**IMsRdpClientNonScriptable6**</span></span>](imsrdpclientnonscriptable6.md)
</dt> </dl>
