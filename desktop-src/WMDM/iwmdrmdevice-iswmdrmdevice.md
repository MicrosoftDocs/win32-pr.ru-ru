---
title: Ивмдрмдевице Исвмдрмдевице, метод
description: Метод Исвмдрмдевице определяет, поддерживает ли устройство Windows Media DRM 10 для переносных устройств.
ms.assetid: 247e7a77-e805-4848-893f-f5522c161232
keywords:
- Метод Исвмдрмдевице Windows Media диспетчер устройств
- Метод Исвмдрмдевице Windows Media диспетчер устройств, интерфейс Ивмдрмдевице
- Интерфейс Ивмдрмдевице Windows Media диспетчер устройств, метод Исвмдрмдевице
topic_type:
- apiref
api_name:
- IWMDRMDevice.IsWMDRMDevice
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9cb79598ea41a996748e383c8fdfc63364dd6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694950"
---
# <a name="iwmdrmdeviceiswmdrmdevice-method"></a><span data-ttu-id="a9684-106">Метод Ивмдрмдевице:: Исвмдрмдевице</span><span class="sxs-lookup"><span data-stu-id="a9684-106">IWMDRMDevice::IsWMDRMDevice method</span></span>

<span data-ttu-id="a9684-107">Метод **исвмдрмдевице** определяет, поддерживает ли устройство Windows Media DRM 10 для переносных устройств.</span><span class="sxs-lookup"><span data-stu-id="a9684-107">The **IsWMDRMDevice** method determines whether the device supports Windows Media DRM 10 for Portable Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9684-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9684-108">Syntax</span></span>


```C++
HRESULT IsWMDRMDevice(
  [out] DWORD *pdwVersion
);
```



## <a name="parameters"></a><span data-ttu-id="a9684-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9684-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9684-110">*пдвверсион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a9684-110">*pdwVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9684-111">Версия Windows Media DRM 10 для переносных устройств со значением 0x00010000.</span><span class="sxs-lookup"><span data-stu-id="a9684-111">Version of Windows Media DRM 10 for Portable Devices, which has value of 0x00010000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9684-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a9684-112">Return value</span></span>

<span data-ttu-id="a9684-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a9684-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a9684-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a9684-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a9684-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a9684-115">Return code</span></span>                                                                          | <span data-ttu-id="a9684-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a9684-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a9684-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a9684-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a9684-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="a9684-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a9684-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a9684-119">Requirements</span></span>



| <span data-ttu-id="a9684-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a9684-120">Requirement</span></span> | <span data-ttu-id="a9684-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a9684-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9684-122">Header</span><span class="sxs-lookup"><span data-stu-id="a9684-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a9684-123"><dt>ВМДДРМСП. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a9684-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="a9684-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a9684-124">Library</span></span><br/> | <dl> <span data-ttu-id="a9684-125"><dt>Мссачлп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9684-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9684-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9684-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9684-127">**Интерфейс Ивмдрмдевице**</span><span class="sxs-lookup"><span data-stu-id="a9684-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





