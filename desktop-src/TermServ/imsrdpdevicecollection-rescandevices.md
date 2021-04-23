---
title: Имсрдпдевицеколлектион Рескандевицес, метод
description: Обновляет список объектов в коллекции. | Имсрдпдевицеколлектион Рескандевицес, метод
ms.assetid: 2e2a959d-0a1d-4aca-9daf-3c24fb9b3b08
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Рескандевицес
- Службы удаленных рабочих столов метода Рескандевицес, интерфейс Имсрдпдевицеколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпдевицеколлектион, метод Рескандевицес
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.RescanDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773231ffd89a0998f6073f844a3f974920625987
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674641"
---
# <a name="imsrdpdevicecollectionrescandevices-method"></a><span data-ttu-id="ac392-107">Метод Имсрдпдевицеколлектион:: Рескандевицес</span><span class="sxs-lookup"><span data-stu-id="ac392-107">IMsRdpDeviceCollection::RescanDevices method</span></span>

<span data-ttu-id="ac392-108">Обновляет список объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="ac392-108">Refreshes the list of objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac392-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac392-109">Syntax</span></span>


```C++
HRESULT RescanDevices(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a><span data-ttu-id="ac392-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac392-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac392-111">*вбулдинредир* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac392-111">*vboolDynRedir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac392-112">Состояние перенаправления по умолчанию, которое будет применяться к вновь обнаруженным устройствам или дискам.</span><span class="sxs-lookup"><span data-stu-id="ac392-112">The default redirection state that will be applied to any newly discovered devices or drives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac392-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac392-113">Return value</span></span>

<span data-ttu-id="ac392-114">Если метод выполнен успешно, возвращается значение **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="ac392-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="ac392-115">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="ac392-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac392-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ac392-116">Requirements</span></span>



| <span data-ttu-id="ac392-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ac392-117">Requirement</span></span> | <span data-ttu-id="ac392-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ac392-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac392-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac392-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ac392-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ac392-120">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="ac392-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac392-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ac392-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac392-122">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ac392-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ac392-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="ac392-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac392-124"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="ac392-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ac392-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac392-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac392-126"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="ac392-127">IID</span><span class="sxs-lookup"><span data-stu-id="ac392-127">IID</span></span><br/>                      | <span data-ttu-id="ac392-128">IID \_ имсрдпдевицеколлектион определен как 56540617-d281-488c-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="ac392-128">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ac392-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac392-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac392-130">**имсрдпдевицеколлектион**</span><span class="sxs-lookup"><span data-stu-id="ac392-130">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





