---
title: Ивмдрмдевице Сетсекуреклоккреспонсе, метод
description: Метод Сетсекуреклоккреспонсе задает ответ на безопасных синхронизирующих импульсов.
ms.assetid: 3f0a1487-d8c4-478d-bfb0-8d09931fd4b6
keywords:
- Метод Сетсекуреклоккреспонсе Windows Media диспетчер устройств
- Метод Сетсекуреклоккреспонсе Windows Media диспетчер устройств, интерфейс Ивмдрмдевице
- Интерфейс Ивмдрмдевице Windows Media диспетчер устройств, метод Сетсекуреклоккреспонсе
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetSecureClockResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821aceda734aceb7a80774db05465f31213eec47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694573"
---
# <a name="iwmdrmdevicesetsecureclockresponse-method"></a><span data-ttu-id="5249b-106">Метод Ивмдрмдевице:: Сетсекуреклоккреспонсе</span><span class="sxs-lookup"><span data-stu-id="5249b-106">IWMDRMDevice::SetSecureClockResponse method</span></span>

<span data-ttu-id="5249b-107">Метод **сетсекуреклоккреспонсе** задает ответ на безопасных синхронизирующих импульсов.</span><span class="sxs-lookup"><span data-stu-id="5249b-107">The **SetSecureClockResponse** method sets the secure clock response.</span></span>

## <a name="syntax"></a><span data-ttu-id="5249b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5249b-108">Syntax</span></span>


```C++
HRESULT SetSecureClockResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a><span data-ttu-id="5249b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5249b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5249b-110">*пбреспонсе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5249b-110">*pbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5249b-111">Установленный отклик на безопасное время.</span><span class="sxs-lookup"><span data-stu-id="5249b-111">The secure clock response to be set.</span></span>

</dd> <dt>

<span data-ttu-id="5249b-112">*кбреспонсе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5249b-112">*cbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5249b-113">Заданный размер ответа на безопасное время в байтах.</span><span class="sxs-lookup"><span data-stu-id="5249b-113">The specified size of the secure clock response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5249b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5249b-114">Return value</span></span>

<span data-ttu-id="5249b-115">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5249b-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5249b-116">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5249b-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5249b-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5249b-117">Return code</span></span>                                                                          | <span data-ttu-id="5249b-118">Описание</span><span class="sxs-lookup"><span data-stu-id="5249b-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5249b-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5249b-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5249b-120">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="5249b-120">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5249b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="5249b-121">Requirements</span></span>



| <span data-ttu-id="5249b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="5249b-122">Requirement</span></span> | <span data-ttu-id="5249b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="5249b-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5249b-124">Header</span><span class="sxs-lookup"><span data-stu-id="5249b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5249b-125"><dt>ВМДДРМСП. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5249b-125"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="5249b-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5249b-126">Library</span></span><br/> | <dl> <span data-ttu-id="5249b-127"><dt>Мссачлп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5249b-127"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5249b-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5249b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5249b-129">**жетсекуреклокк**</span><span class="sxs-lookup"><span data-stu-id="5249b-129">**GetSecureClock**</span></span>](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[<span data-ttu-id="5249b-130">**Интерфейс Ивмдрмдевице**</span><span class="sxs-lookup"><span data-stu-id="5249b-130">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





