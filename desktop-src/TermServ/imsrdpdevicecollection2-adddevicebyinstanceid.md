---
title: IMsRdpDeviceCollection2 Адддевицебинстанцеид, метод
description: Добавляет устройство, не имеющее список, в коллекцию устройств.
ms.assetid: 7ef200c5-b99e-40c9-80e1-0758ddfa0902
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Адддевицебинстанцеид
- Службы удаленных рабочих столов метода Адддевицебинстанцеид, интерфейс IMsRdpDeviceCollection2
- Службы удаленных рабочих столов интерфейса IMsRdpDeviceCollection2, метод Адддевицебинстанцеид
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.AddDeviceByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f817a5beb4d8762787c4bf2f8a3995d3918e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071140"
---
# <a name="imsrdpdevicecollection2adddevicebyinstanceid-method"></a><span data-ttu-id="a5ecf-106">Метод IMsRdpDeviceCollection2:: Адддевицебинстанцеид</span><span class="sxs-lookup"><span data-stu-id="a5ecf-106">IMsRdpDeviceCollection2::AddDeviceByInstanceId method</span></span>

<span data-ttu-id="a5ecf-107">Добавляет устройство, не имеющее список, в коллекцию устройств.</span><span class="sxs-lookup"><span data-stu-id="a5ecf-107">Adds an unlisted device to the device collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5ecf-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5ecf-108">Syntax</span></span>


```C++
HRESULT AddDeviceByInstanceId(
  [in] RedirectDeviceType Type,
  [in] BSTR               InstanceId
);
```



## <a name="parameters"></a><span data-ttu-id="a5ecf-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5ecf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5ecf-110">*Тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5ecf-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5ecf-111">Тип: **[ **редиректдевицетипе**](redirectdevicetype.md)**</span><span class="sxs-lookup"><span data-stu-id="a5ecf-111">Type: **[**RedirectDeviceType**](redirectdevicetype.md)**</span></span>

<span data-ttu-id="a5ecf-112">Значение перечисления [**редиректдевицетипе**](redirectdevicetype.md) , указывающее тип добавляемого устройства.</span><span class="sxs-lookup"><span data-stu-id="a5ecf-112">A value of the [**RedirectDeviceType**](redirectdevicetype.md) enumeration that specifies the type of device being added.</span></span>

</dd> <dt>

<span data-ttu-id="a5ecf-113">*InstanceId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5ecf-113">*InstanceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5ecf-114">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a5ecf-114">Type: **BSTR**</span></span>

<span data-ttu-id="a5ecf-115">Идентификатор экземпляра добавляемого устройства.</span><span class="sxs-lookup"><span data-stu-id="a5ecf-115">The instance identifier of the device to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5ecf-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5ecf-116">Return value</span></span>

<span data-ttu-id="a5ecf-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a5ecf-117">Type: **HRESULT**</span></span>

<span data-ttu-id="a5ecf-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a5ecf-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a5ecf-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a5ecf-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5ecf-120">Требования</span><span class="sxs-lookup"><span data-stu-id="a5ecf-120">Requirements</span></span>



| <span data-ttu-id="a5ecf-121">Требование</span><span class="sxs-lookup"><span data-stu-id="a5ecf-121">Requirement</span></span> | <span data-ttu-id="a5ecf-122">Значение</span><span class="sxs-lookup"><span data-stu-id="a5ecf-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5ecf-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5ecf-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a5ecf-124">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a5ecf-124">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="a5ecf-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5ecf-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a5ecf-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a5ecf-126">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="a5ecf-127">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a5ecf-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="a5ecf-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5ecf-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a5ecf-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a5ecf-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5ecf-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5ecf-130"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5ecf-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5ecf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5ecf-132">**редиректдевицетипе**</span><span class="sxs-lookup"><span data-stu-id="a5ecf-132">**RedirectDeviceType**</span></span>](redirectdevicetype.md)
</dt> <dt>

[<span data-ttu-id="a5ecf-133">**IMsRdpDeviceCollection2**</span><span class="sxs-lookup"><span data-stu-id="a5ecf-133">**IMsRdpDeviceCollection2**</span></span>](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





