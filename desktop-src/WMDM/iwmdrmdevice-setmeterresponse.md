---
title: Ивмдрмдевице Сетметерреспонсе, метод
description: Метод Сетметерреспонсе задает ответ измерения.
ms.assetid: 3f2e7d7c-6470-4d53-96b0-d3eebdb08329
keywords:
- Метод Сетметерреспонсе Windows Media диспетчер устройств
- Метод Сетметерреспонсе Windows Media диспетчер устройств, интерфейс Ивмдрмдевице
- Интерфейс Ивмдрмдевице Windows Media диспетчер устройств, метод Сетметерреспонсе
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed70b158215eb831296ad083af8cd2c001cb38f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694944"
---
# <a name="iwmdrmdevicesetmeterresponse-method"></a><span data-ttu-id="42c8c-106">Метод Ивмдрмдевице:: Сетметерреспонсе</span><span class="sxs-lookup"><span data-stu-id="42c8c-106">IWMDRMDevice::SetMeterResponse method</span></span>

<span data-ttu-id="42c8c-107">Метод **сетметерреспонсе** задает ответ измерения.</span><span class="sxs-lookup"><span data-stu-id="42c8c-107">The **SetMeterResponse** method sets the metering response.</span></span>

## <a name="syntax"></a><span data-ttu-id="42c8c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42c8c-108">Syntax</span></span>


```C++
HRESULT SetMeterResponse(
  [in]  BYTE  *pbMeterResponse,
  [in]  DWORD cbMeterResponse,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="42c8c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="42c8c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42c8c-110">*пбметерреспонсе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42c8c-110">*pbMeterResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42c8c-111">Ответ отслеживания, который должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="42c8c-111">The metering response to be set.</span></span>

</dd> <dt>

<span data-ttu-id="42c8c-112">*кбметерреспонсе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42c8c-112">*cbMeterResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42c8c-113">Размер ответа отслеживания в байтах.</span><span class="sxs-lookup"><span data-stu-id="42c8c-113">Size of the metering response, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="42c8c-114">*пдвфлагс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="42c8c-114">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42c8c-115">Флаги ответа.</span><span class="sxs-lookup"><span data-stu-id="42c8c-115">Response flags.</span></span> <span data-ttu-id="42c8c-116">Это значение должно быть одним из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="42c8c-116">This value must be one of the following flags.</span></span>



| <span data-ttu-id="42c8c-117">Flag</span><span class="sxs-lookup"><span data-stu-id="42c8c-117">Flag</span></span>                            | <span data-ttu-id="42c8c-118">Описание</span><span class="sxs-lookup"><span data-stu-id="42c8c-118">Description</span></span>              |
|---------------------------------|--------------------------|
| <span data-ttu-id="42c8c-119">\_ответ от метрики WMDRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="42c8c-119">WMDRM\_METER\_RESPONSE\_ALL</span></span>     | <span data-ttu-id="42c8c-120">Все отклики на счетчики.</span><span class="sxs-lookup"><span data-stu-id="42c8c-120">All meter responses.</span></span>     |
| <span data-ttu-id="42c8c-121">\_ \_ частичный отклик на отслеживание WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="42c8c-121">WMDRM\_METER\_RESPONSE\_PARTIAL</span></span> | <span data-ttu-id="42c8c-122">Частичные ответы на счетчики.</span><span class="sxs-lookup"><span data-stu-id="42c8c-122">Partial meter responses.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42c8c-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42c8c-123">Return value</span></span>

<span data-ttu-id="42c8c-124">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="42c8c-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="42c8c-125">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="42c8c-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="42c8c-126">Код возврата</span><span class="sxs-lookup"><span data-stu-id="42c8c-126">Return code</span></span>                                                                          | <span data-ttu-id="42c8c-127">Описание</span><span class="sxs-lookup"><span data-stu-id="42c8c-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="42c8c-128"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="42c8c-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="42c8c-129">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="42c8c-129">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="42c8c-130">Требования</span><span class="sxs-lookup"><span data-stu-id="42c8c-130">Requirements</span></span>



| <span data-ttu-id="42c8c-131">Требование</span><span class="sxs-lookup"><span data-stu-id="42c8c-131">Requirement</span></span> | <span data-ttu-id="42c8c-132">Значение</span><span class="sxs-lookup"><span data-stu-id="42c8c-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42c8c-133">Header</span><span class="sxs-lookup"><span data-stu-id="42c8c-133">Header</span></span><br/>  | <dl> <span data-ttu-id="42c8c-134"><dt>ВМДДРМСП. idl</dt></span><span class="sxs-lookup"><span data-stu-id="42c8c-134"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="42c8c-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="42c8c-135">Library</span></span><br/> | <dl> <span data-ttu-id="42c8c-136"><dt>Мссачлп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42c8c-136"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42c8c-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42c8c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42c8c-138">**Интерфейс Ивмдрмдевице**</span><span class="sxs-lookup"><span data-stu-id="42c8c-138">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





