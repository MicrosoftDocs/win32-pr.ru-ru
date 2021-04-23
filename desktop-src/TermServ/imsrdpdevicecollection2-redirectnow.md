---
title: IMsRdpDeviceCollection2 Редиректнов, метод
description: Принудительное перенаправление или удаление устройств, которые были выбраны или отменены из коллекции.
ms.assetid: 9cd5849d-a589-43f3-b904-6b2e15ca033d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Редиректнов
- Службы удаленных рабочих столов метода Редиректнов, интерфейс IMsRdpDeviceCollection2
- Службы удаленных рабочих столов интерфейса IMsRdpDeviceCollection2, метод Редиректнов
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.RedirectNow
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893d1e26f504d5aeb45f795ea7425eeefc3a6232
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988208"
---
# <a name="imsrdpdevicecollection2redirectnow-method"></a><span data-ttu-id="aeb07-106">Метод IMsRdpDeviceCollection2:: Редиректнов</span><span class="sxs-lookup"><span data-stu-id="aeb07-106">IMsRdpDeviceCollection2::RedirectNow method</span></span>

<span data-ttu-id="aeb07-107">Принудительное перенаправление или удаление устройств, которые были выбраны или отменены из коллекции.</span><span class="sxs-lookup"><span data-stu-id="aeb07-107">Forces devices that were selected or unselected from the collection to be redirected or removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeb07-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aeb07-108">Syntax</span></span>


```C++
HRESULT RedirectNow(
  [in] RedirectDeviceType Type
);
```



## <a name="parameters"></a><span data-ttu-id="aeb07-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="aeb07-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeb07-110">*Тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aeb07-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeb07-111">Тип: **[ **редиректдевицетипе**](redirectdevicetype.md)**</span><span class="sxs-lookup"><span data-stu-id="aeb07-111">Type: **[**RedirectDeviceType**](redirectdevicetype.md)**</span></span>

<span data-ttu-id="aeb07-112">Значение перечисления [**редиректдевицетипе**](redirectdevicetype.md) , указывающее тип устройства для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="aeb07-112">A value of the [**RedirectDeviceType**](redirectdevicetype.md) enumeration that specifies the type of device to be redirected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeb07-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aeb07-113">Return value</span></span>

<span data-ttu-id="aeb07-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="aeb07-114">Type: **HRESULT**</span></span>

<span data-ttu-id="aeb07-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="aeb07-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aeb07-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aeb07-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeb07-117">Требования</span><span class="sxs-lookup"><span data-stu-id="aeb07-117">Requirements</span></span>



| <span data-ttu-id="aeb07-118">Требование</span><span class="sxs-lookup"><span data-stu-id="aeb07-118">Requirement</span></span> | <span data-ttu-id="aeb07-119">Значение</span><span class="sxs-lookup"><span data-stu-id="aeb07-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aeb07-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aeb07-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aeb07-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="aeb07-121">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="aeb07-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aeb07-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aeb07-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aeb07-123">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="aeb07-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="aeb07-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="aeb07-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aeb07-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aeb07-126">DLL</span><span class="sxs-lookup"><span data-stu-id="aeb07-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aeb07-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aeb07-127"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeb07-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aeb07-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeb07-129">**редиректдевицетипе**</span><span class="sxs-lookup"><span data-stu-id="aeb07-129">**RedirectDeviceType**</span></span>](redirectdevicetype.md)
</dt> <dt>

[<span data-ttu-id="aeb07-130">**IMsRdpDeviceCollection2**</span><span class="sxs-lookup"><span data-stu-id="aeb07-130">**IMsRdpDeviceCollection2**</span></span>](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





