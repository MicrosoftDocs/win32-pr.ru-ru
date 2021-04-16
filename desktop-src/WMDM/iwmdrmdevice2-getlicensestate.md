---
title: IWMDRMDevice2 Жетлиценсестате, метод
description: Метод Жетлиценсестате получает состояние лицензии.
ms.assetid: a98847f6-00ec-4211-9716-79714d7ba169
keywords:
- Метод Жетлиценсестате Windows Media диспетчер устройств
- Метод Жетлиценсестате Windows Media диспетчер устройств, интерфейс IWMDRMDevice2
- Интерфейс IWMDRMDevice2 Windows Media диспетчер устройств, метод Жетлиценсестате
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetLicenseState
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d075d123ae99b26767621fb1a958cd172bc9e42c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699278"
---
# <a name="iwmdrmdevice2getlicensestate-method"></a><span data-ttu-id="5323a-106">Метод IWMDRMDevice2:: Жетлиценсестате</span><span class="sxs-lookup"><span data-stu-id="5323a-106">IWMDRMDevice2::GetLicenseState method</span></span>

<span data-ttu-id="5323a-107">Метод **жетлиценсестате** получает состояние лицензии.</span><span class="sxs-lookup"><span data-stu-id="5323a-107">The **GetLicenseState** method gets the license state.</span></span>

## <a name="syntax"></a><span data-ttu-id="5323a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5323a-108">Syntax</span></span>


```C++
HRESULT GetLicenseState(
  [in]  BYTE  *pbStateQueryData,
  [in]  DWORD cbStateQueryData,
  [out] DWORD *pdwCategory,
  [out] DWORD *pcRemainingCounts,
  [out] DWORD *pcRemainingHours,
  [out] DWORD *pdwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="5323a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5323a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5323a-110">*пбстатекуеридата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5323a-110">*pbStateQueryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5323a-111">Указатель на запрашиваемые данные состояния лицензии.</span><span class="sxs-lookup"><span data-stu-id="5323a-111">Pointer to the queried data of the license state.</span></span>

</dd> <dt>

<span data-ttu-id="5323a-112">*кбстатекуеридата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5323a-112">*cbStateQueryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5323a-113">Количество запрошенных данных.</span><span class="sxs-lookup"><span data-stu-id="5323a-113">Count of the queried data.</span></span>

</dd> <dt>

<span data-ttu-id="5323a-114">*пдвкатегори* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5323a-114">*pdwCategory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5323a-115">Указатель на категорию.</span><span class="sxs-lookup"><span data-stu-id="5323a-115">Pointer to the category.</span></span>

</dd> <dt>

<span data-ttu-id="5323a-116">*пкремаинингкаунтс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5323a-116">*pcRemainingCounts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5323a-117">Указатель на оставшиеся счетчики.</span><span class="sxs-lookup"><span data-stu-id="5323a-117">Pointer to the remaining counts.</span></span>

</dd> <dt>

<span data-ttu-id="5323a-118">*пкремаинингхаурс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5323a-118">*pcRemainingHours* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5323a-119">Указатель на оставшиеся часы.</span><span class="sxs-lookup"><span data-stu-id="5323a-119">Pointer to the remaining hours.</span></span>

</dd> <dt>

<span data-ttu-id="5323a-120">*пдвресервед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5323a-120">*pdwReserved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5323a-121">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="5323a-121">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5323a-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5323a-122">Return value</span></span>

<span data-ttu-id="5323a-123">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5323a-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5323a-124">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5323a-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5323a-125">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5323a-125">Return code</span></span>                                                                          | <span data-ttu-id="5323a-126">Описание</span><span class="sxs-lookup"><span data-stu-id="5323a-126">Description</span></span>                     |
|--------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="5323a-127"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5323a-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5323a-128">Метод выполнен.</span><span class="sxs-lookup"><span data-stu-id="5323a-128">The method succeeds.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5323a-129">Требования</span><span class="sxs-lookup"><span data-stu-id="5323a-129">Requirements</span></span>



| <span data-ttu-id="5323a-130">Требование</span><span class="sxs-lookup"><span data-stu-id="5323a-130">Requirement</span></span> | <span data-ttu-id="5323a-131">Значение</span><span class="sxs-lookup"><span data-stu-id="5323a-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5323a-132">Header</span><span class="sxs-lookup"><span data-stu-id="5323a-132">Header</span></span><br/>  | <dl> <span data-ttu-id="5323a-133"><dt>ВМДДРМСП. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5323a-133"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="5323a-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5323a-134">Library</span></span><br/> | <dl> <span data-ttu-id="5323a-135"><dt>Мссачлп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5323a-135"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5323a-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5323a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5323a-137">**Интерфейс IWMDRMDevice2**</span><span class="sxs-lookup"><span data-stu-id="5323a-137">**IWMDRMDevice2 Interface**</span></span>](iwmdrmdevice2.md)
</dt> </dl>

 

 





