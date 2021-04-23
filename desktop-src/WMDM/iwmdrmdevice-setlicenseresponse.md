---
title: Ивмдрмдевице Сетлиценсереспонсе, метод
description: Метод Сетлиценсереспонсе задает ответ лицензии.
ms.assetid: 1ef3ba9d-d14c-4a20-92d6-0bcb604fd9e2
keywords:
- Метод Сетлиценсереспонсе Windows Media диспетчер устройств
- Метод Сетлиценсереспонсе Windows Media диспетчер устройств, интерфейс Ивмдрмдевице
- Интерфейс Ивмдрмдевице Windows Media диспетчер устройств, метод Сетлиценсереспонсе
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetLicenseResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f32a2d27fabe45081b13d658e49171af035b8cc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694947"
---
# <a name="iwmdrmdevicesetlicenseresponse-method"></a><span data-ttu-id="60f16-106">Метод Ивмдрмдевице:: Сетлиценсереспонсе</span><span class="sxs-lookup"><span data-stu-id="60f16-106">IWMDRMDevice::SetLicenseResponse method</span></span>

<span data-ttu-id="60f16-107">Метод **сетлиценсереспонсе** задает ответ лицензии.</span><span class="sxs-lookup"><span data-stu-id="60f16-107">The **SetLicenseResponse** method sets the license response.</span></span>

## <a name="syntax"></a><span data-ttu-id="60f16-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60f16-108">Syntax</span></span>


```C++
HRESULT SetLicenseResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a><span data-ttu-id="60f16-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="60f16-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60f16-110">*пбреспонсе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60f16-110">*pbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60f16-111">Задает ответ, который необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="60f16-111">Specifies the response to be set.</span></span>

</dd> <dt>

<span data-ttu-id="60f16-112">*кбреспонсе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60f16-112">*cbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60f16-113">Размер ответа в байтах.</span><span class="sxs-lookup"><span data-stu-id="60f16-113">Size of the response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60f16-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60f16-114">Return value</span></span>

<span data-ttu-id="60f16-115">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="60f16-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="60f16-116">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="60f16-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="60f16-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="60f16-117">Return code</span></span>                                                                          | <span data-ttu-id="60f16-118">Описание</span><span class="sxs-lookup"><span data-stu-id="60f16-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="60f16-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="60f16-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="60f16-120">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="60f16-120">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="60f16-121">Требования</span><span class="sxs-lookup"><span data-stu-id="60f16-121">Requirements</span></span>



| <span data-ttu-id="60f16-122">Требование</span><span class="sxs-lookup"><span data-stu-id="60f16-122">Requirement</span></span> | <span data-ttu-id="60f16-123">Значение</span><span class="sxs-lookup"><span data-stu-id="60f16-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60f16-124">Header</span><span class="sxs-lookup"><span data-stu-id="60f16-124">Header</span></span><br/>  | <dl> <span data-ttu-id="60f16-125"><dt>ВМДДРМСП. idl</dt></span><span class="sxs-lookup"><span data-stu-id="60f16-125"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="60f16-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="60f16-126">Library</span></span><br/> | <dl> <span data-ttu-id="60f16-127"><dt>Мссачлп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60f16-127"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60f16-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60f16-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60f16-129">**Интерфейс Ивмдрмдевице**</span><span class="sxs-lookup"><span data-stu-id="60f16-129">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





