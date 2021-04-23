---
title: Ивмдрмдевице Жетсекуреклоккчалленже, метод
description: Метод Жетсекуреклоккчалленже извлекает результат запроса на безопасное время.
ms.assetid: cbef160c-91a3-47d1-9d7a-e649ce2c77ff
keywords:
- Метод Жетсекуреклоккчалленже Windows Media диспетчер устройств
- Метод Жетсекуреклоккчалленже Windows Media диспетчер устройств, интерфейс Ивмдрмдевице
- Интерфейс Ивмдрмдевице Windows Media диспетчер устройств, метод Жетсекуреклоккчалленже
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClockChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e57165f75a23d13d847e028deb69de383e2855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694412"
---
# <a name="iwmdrmdevicegetsecureclockchallenge-method"></a><span data-ttu-id="60b70-106">Метод Ивмдрмдевице:: Жетсекуреклоккчалленже</span><span class="sxs-lookup"><span data-stu-id="60b70-106">IWMDRMDevice::GetSecureClockChallenge method</span></span>

<span data-ttu-id="60b70-107">Метод **жетсекуреклоккчалленже** извлекает результат запроса на безопасное время.</span><span class="sxs-lookup"><span data-stu-id="60b70-107">The **GetSecureClockChallenge** method retrieves the secure clock challenge result.</span></span>

## <a name="syntax"></a><span data-ttu-id="60b70-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60b70-108">Syntax</span></span>


```C++
HRESULT GetSecureClockChallenge(
  [out] BYTE  **ppbChallenge,
  [out] DWORD *pcbChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="60b70-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="60b70-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60b70-110">*ппбчалленже* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="60b70-110">*ppbChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60b70-111">Получен результат запроса.</span><span class="sxs-lookup"><span data-stu-id="60b70-111">Retrieved challenge result.</span></span>

</dd> <dt>

<span data-ttu-id="60b70-112">*пкбчалленже* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="60b70-112">*pcbChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60b70-113">Размер результата запроса в байтах.</span><span class="sxs-lookup"><span data-stu-id="60b70-113">Size of the challenge result, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60b70-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60b70-114">Return value</span></span>

<span data-ttu-id="60b70-115">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="60b70-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="60b70-116">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="60b70-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="60b70-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="60b70-117">Return code</span></span>                                                                          | <span data-ttu-id="60b70-118">Описание</span><span class="sxs-lookup"><span data-stu-id="60b70-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="60b70-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="60b70-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="60b70-120">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="60b70-120">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="60b70-121">Требования</span><span class="sxs-lookup"><span data-stu-id="60b70-121">Requirements</span></span>



| <span data-ttu-id="60b70-122">Требование</span><span class="sxs-lookup"><span data-stu-id="60b70-122">Requirement</span></span> | <span data-ttu-id="60b70-123">Значение</span><span class="sxs-lookup"><span data-stu-id="60b70-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60b70-124">Header</span><span class="sxs-lookup"><span data-stu-id="60b70-124">Header</span></span><br/>  | <dl> <span data-ttu-id="60b70-125"><dt>ВМДДРМСП. idl</dt></span><span class="sxs-lookup"><span data-stu-id="60b70-125"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="60b70-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="60b70-126">Library</span></span><br/> | <dl> <span data-ttu-id="60b70-127"><dt>Мссачлп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60b70-127"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60b70-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60b70-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b70-129">**жетсекуреклокк**</span><span class="sxs-lookup"><span data-stu-id="60b70-129">**GetSecureClock**</span></span>](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[<span data-ttu-id="60b70-130">**Интерфейс Ивмдрмдевице**</span><span class="sxs-lookup"><span data-stu-id="60b70-130">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





