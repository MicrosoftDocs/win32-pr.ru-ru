---
title: IWMDRMDevice2 Жетпартиалсинклист, метод
description: Метод Жетпартиалсинклист получает список частичной синхронизации.
ms.assetid: 4ee8e9d7-d5d1-4614-b7a1-1dcb7f07b161
keywords:
- Метод Жетпартиалсинклист Windows Media диспетчер устройств
- Метод Жетпартиалсинклист Windows Media диспетчер устройств, интерфейс IWMDRMDevice2
- Интерфейс IWMDRMDevice2 Windows Media диспетчер устройств, метод Жетпартиалсинклист
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetPartialSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68c9c9a0bc47dcbea25158bb1f25db6cd084075
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699065"
---
# <a name="iwmdrmdevice2getpartialsynclist-method"></a><span data-ttu-id="c8d36-106">Метод IWMDRMDevice2:: Жетпартиалсинклист</span><span class="sxs-lookup"><span data-stu-id="c8d36-106">IWMDRMDevice2::GetPartialSyncList method</span></span>

<span data-ttu-id="c8d36-107">Метод **жетпартиалсинклист** получает список частичной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="c8d36-107">The **GetPartialSyncList** method gets a partial synchronization list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8d36-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8d36-108">Syntax</span></span>


```C++
HRESULT GetPartialSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [in]  DWORD dwStartingIndex,
  [in]  DWORD cItems,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList,
  [out] DWORD *pdwNextStartingIndex,
  [out] DWORD *pcItemsProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="c8d36-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8d36-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8d36-110">*кминкаунтсрешолд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c8d36-110">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d36-111">Пороговое значение минимального числа.</span><span class="sxs-lookup"><span data-stu-id="c8d36-111">Minimum count threshold.</span></span>

</dd> <dt>

<span data-ttu-id="c8d36-112">*кминхаурссрешолд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c8d36-112">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d36-113">Минимальное пороговое значение часов.</span><span class="sxs-lookup"><span data-stu-id="c8d36-113">Minimum hours threshold.</span></span>

</dd> <dt>

<span data-ttu-id="c8d36-114">*двстартингиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c8d36-114">*dwStartingIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d36-115">Начальное расположение для индексирования.</span><span class="sxs-lookup"><span data-stu-id="c8d36-115">Start position for indexing.</span></span>

</dd> <dt>

<span data-ttu-id="c8d36-116">*Цитемс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c8d36-116">*cItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d36-117">Число индексируемых элементов.</span><span class="sxs-lookup"><span data-stu-id="c8d36-117">Count of items to be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="c8d36-118">*ппбсинклист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c8d36-118">*ppbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d36-119">Получен список синхронизации лицензий.</span><span class="sxs-lookup"><span data-stu-id="c8d36-119">Retrieved license synchronization list.</span></span>

</dd> <dt>

<span data-ttu-id="c8d36-120">*пкбсинклист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c8d36-120">*pcbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d36-121">Размер списка синхронизации лицензий в байтах.</span><span class="sxs-lookup"><span data-stu-id="c8d36-121">Size of the license synchronization list, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c8d36-122">*пдвнекстстартингиндекс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c8d36-122">*pdwNextStartingIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d36-123">Следующее начальное расположение для индексирования.</span><span class="sxs-lookup"><span data-stu-id="c8d36-123">Next start position for indexing.</span></span>

</dd> <dt>

<span data-ttu-id="c8d36-124">*пЦитемспроцессед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c8d36-124">*pcItemsProcessed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d36-125">Количество обрабатываемых элементов.</span><span class="sxs-lookup"><span data-stu-id="c8d36-125">Count of items being processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8d36-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8d36-126">Return value</span></span>

<span data-ttu-id="c8d36-127">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c8d36-127">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c8d36-128">Все методы интерфейса в диспетчер устройств Windows Media могут возвращать любой из следующих классов кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="c8d36-128">All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:</span></span>

-   <span data-ttu-id="c8d36-129">Стандартные коды ошибок COM</span><span class="sxs-lookup"><span data-stu-id="c8d36-129">Standard COM error codes</span></span>
-   <span data-ttu-id="c8d36-130">Коды ошибок Windows преобразованы в значения HRESULT</span><span class="sxs-lookup"><span data-stu-id="c8d36-130">Windows error codes converted to HRESULT values</span></span>
-   <span data-ttu-id="c8d36-131">Коды ошибок Windows Media диспетчер устройств</span><span class="sxs-lookup"><span data-stu-id="c8d36-131">Windows Media Device Manager error codes</span></span>

<span data-ttu-id="c8d36-132">Расширенный список возможных кодов ошибок см. в разделе [коды ошибок](error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c8d36-132">For an extensive list of possible error codes, see [Error Codes](error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8d36-133">Требования</span><span class="sxs-lookup"><span data-stu-id="c8d36-133">Requirements</span></span>



| <span data-ttu-id="c8d36-134">Требование</span><span class="sxs-lookup"><span data-stu-id="c8d36-134">Requirement</span></span> | <span data-ttu-id="c8d36-135">Значение</span><span class="sxs-lookup"><span data-stu-id="c8d36-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8d36-136">Header</span><span class="sxs-lookup"><span data-stu-id="c8d36-136">Header</span></span><br/>  | <dl> <span data-ttu-id="c8d36-137"><dt>ВМДДРМСП. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c8d36-137"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="c8d36-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c8d36-138">Library</span></span><br/> | <dl> <span data-ttu-id="c8d36-139"><dt>Мссачлп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8d36-139"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8d36-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8d36-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8d36-141">**Ивмдрмдевице:: Жетсинклист**</span><span class="sxs-lookup"><span data-stu-id="c8d36-141">**IWMDRMDevice::GetSyncList**</span></span>](iwmdrmdevice-getsynclist.md)
</dt> <dt>

[<span data-ttu-id="c8d36-142">**Интерфейс IWMDRMDevice2**</span><span class="sxs-lookup"><span data-stu-id="c8d36-142">**IWMDRMDevice2 Interface**</span></span>](iwmdrmdevice2.md)
</dt> </dl>

 

 





