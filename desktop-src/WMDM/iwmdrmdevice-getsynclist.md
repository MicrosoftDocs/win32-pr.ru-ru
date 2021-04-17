---
title: Ивмдрмдевице Жетсинклист, метод
description: Метод Жетсинклист извлекает список синхронизации лицензий на устройстве. Синхронизация лицензий позволяет главному компьютеру передавать обновленные лицензии на устройство в соответствии с указанными критериями.
ms.assetid: 772ac03b-3339-4c5f-a8fc-1c216ec665b7
keywords:
- Метод Жетсинклист Windows Media диспетчер устройств
- Метод Жетсинклист Windows Media диспетчер устройств, интерфейс Ивмдрмдевице
- Интерфейс Ивмдрмдевице Windows Media диспетчер устройств, метод Жетсинклист
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381d410bd938cb90855b182e62354d48e72f16d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694951"
---
# <a name="iwmdrmdevicegetsynclist-method"></a><span data-ttu-id="4e3c2-107">Метод Ивмдрмдевице:: Жетсинклист</span><span class="sxs-lookup"><span data-stu-id="4e3c2-107">IWMDRMDevice::GetSyncList method</span></span>

<span data-ttu-id="4e3c2-108">Метод **жетсинклист** извлекает список синхронизации лицензий на устройстве.</span><span class="sxs-lookup"><span data-stu-id="4e3c2-108">The **GetSyncList** method retrieves the license synchronization list on the device.</span></span> <span data-ttu-id="4e3c2-109">Синхронизация лицензий позволяет главному компьютеру передавать обновленные лицензии на устройство в соответствии с указанными критериями.</span><span class="sxs-lookup"><span data-stu-id="4e3c2-109">License synchronization allows the host computer to transfer updated licenses to a device according to the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e3c2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e3c2-110">Syntax</span></span>


```C++
HRESULT GetSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList
);
```



## <a name="parameters"></a><span data-ttu-id="4e3c2-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e3c2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e3c2-112">*кминкаунтсрешолд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4e3c2-112">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e3c2-113">Пороговое значение минимального числа.</span><span class="sxs-lookup"><span data-stu-id="4e3c2-113">Minimum count threshold.</span></span>

</dd> <dt>

<span data-ttu-id="4e3c2-114">*кминхаурссрешолд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4e3c2-114">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e3c2-115">Минимальное пороговое значение часов.</span><span class="sxs-lookup"><span data-stu-id="4e3c2-115">Minimum hours threshold.</span></span>

</dd> <dt>

<span data-ttu-id="4e3c2-116">*ппбсинклист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4e3c2-116">*ppbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e3c2-117">Получен список синхронизации лицензий.</span><span class="sxs-lookup"><span data-stu-id="4e3c2-117">Retrieved license synchronization list.</span></span>

</dd> <dt>

<span data-ttu-id="4e3c2-118">*пкбсинклист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4e3c2-118">*pcbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e3c2-119">Размер списка синхронизации лицензий в байтах.</span><span class="sxs-lookup"><span data-stu-id="4e3c2-119">Size of the license synchronization list, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e3c2-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e3c2-120">Return value</span></span>

<span data-ttu-id="4e3c2-121">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4e3c2-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4e3c2-122">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4e3c2-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4e3c2-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4e3c2-123">Return code</span></span>                                                                          | <span data-ttu-id="4e3c2-124">Описание</span><span class="sxs-lookup"><span data-stu-id="4e3c2-124">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4e3c2-125"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4e3c2-125"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4e3c2-126">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="4e3c2-126">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4e3c2-127">Требования</span><span class="sxs-lookup"><span data-stu-id="4e3c2-127">Requirements</span></span>



| <span data-ttu-id="4e3c2-128">Требование</span><span class="sxs-lookup"><span data-stu-id="4e3c2-128">Requirement</span></span> | <span data-ttu-id="4e3c2-129">Значение</span><span class="sxs-lookup"><span data-stu-id="4e3c2-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e3c2-130">Header</span><span class="sxs-lookup"><span data-stu-id="4e3c2-130">Header</span></span><br/>  | <dl> <span data-ttu-id="4e3c2-131"><dt>ВМДДРМСП. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4e3c2-131"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="4e3c2-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4e3c2-132">Library</span></span><br/> | <dl> <span data-ttu-id="4e3c2-133"><dt>Мссачлп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e3c2-133"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e3c2-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e3c2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e3c2-135">**Интерфейс Ивмдрмдевице**</span><span class="sxs-lookup"><span data-stu-id="4e3c2-135">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





