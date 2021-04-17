---
title: Метод Ивмдрмнетрецеивер Процесслиценсереспонсе (Вмдрмсдк. h)
description: Метод Процесслиценсереспонсе обрабатывает ответ лицензии, который отправляется передатчиком в ответ на запрос лицензии.
ms.assetid: b6d04651-746b-474e-8a02-6b7cbee9db46
keywords:
- Формат Windows Media, Процесслиценсереспонсе метод
- Процесслиценсереспонсе метод Windows Media Format, интерфейс Ивмдрмнетрецеивер
- Интерфейс Ивмдрмнетрецеивер Windows Media Format, метод Процесслиценсереспонсе
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a09ebab81b71e21b9ef922423a7bbe67b20596
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675049"
---
# <a name="iwmdrmnetreceiverprocesslicenseresponse-method"></a><span data-ttu-id="bc611-106">Ивмдрмнетрецеивер: метод:P Роцесслиценсереспонсе</span><span class="sxs-lookup"><span data-stu-id="bc611-106">IWMDRMNetReceiver::ProcessLicenseResponse method</span></span>

<span data-ttu-id="bc611-107">Метод **процесслиценсереспонсе** обрабатывает ответ лицензии, который отправляется передатчиком в ответ на запрос лицензии.</span><span class="sxs-lookup"><span data-stu-id="bc611-107">The **ProcessLicenseResponse** method processes the license response that is sent by the transmitter in reply to a license challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc611-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc611-108">Syntax</span></span>


```C++
HRESULT ProcessLicenseResponse(
  [in]  BYTE  *pbLicenseResponse,
  [in]  DWORD cbLicenseResponse,
  [out] BYTE  **ppbWMDRMNetLicenseRepresentation,
  [out] DWORD *pcbWMDRMNetLicenseRepresentation
);
```



## <a name="parameters"></a><span data-ttu-id="bc611-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc611-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc611-110">*пблиценсереспонсе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bc611-110">*pbLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc611-111">От передатчика получен ответ на лицензию.</span><span class="sxs-lookup"><span data-stu-id="bc611-111">License response received from the transmitter.</span></span>

</dd> <dt>

<span data-ttu-id="bc611-112">*кблиценсереспонсе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bc611-112">*cbLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc611-113">Размер ответа в байтах.</span><span class="sxs-lookup"><span data-stu-id="bc611-113">Size of the response in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="bc611-114">*ппбвмдрмнетлиценсерепресентатион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bc611-114">*ppbWMDRMNetLicenseRepresentation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc611-115">Адрес переменной, которая получает адрес внутреннего представления лицензии для лицензии, содержащейся в сообщении ответа лицензии.</span><span class="sxs-lookup"><span data-stu-id="bc611-115">Address of a variable that receives the address of the internal license representation for the license contained in the license response message.</span></span> <span data-ttu-id="bc611-116">После завершения работы с этими данными необходимо освободить память, вызвав **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="bc611-116">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span> <span data-ttu-id="bc611-117">Если представление лицензии не требуется, этот параметр может иметь значение **null** .</span><span class="sxs-lookup"><span data-stu-id="bc611-117">This parameter may be set to **NULL** if the license representation is not needed.</span></span>

</dd> <dt>

<span data-ttu-id="bc611-118">*пкбвмдрмнетлиценсерепресентатион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bc611-118">*pcbWMDRMNetLicenseRepresentation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc611-119">Адрес переменной, получающей размер представления лицензии.</span><span class="sxs-lookup"><span data-stu-id="bc611-119">Address of a variable that receives the size of the license representation.</span></span> <span data-ttu-id="bc611-120">Если *ппбвмдрмнетлиценсерепресентатион* имеет **значение NULL**, необходимо задать значение **null** .</span><span class="sxs-lookup"><span data-stu-id="bc611-120">Must be set to **NULL** if *ppbWMDRMNetLicenseRepresentation* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc611-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc611-121">Return value</span></span>

<span data-ttu-id="bc611-122">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="bc611-122">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bc611-123">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="bc611-123">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bc611-124">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bc611-124">Return code</span></span>                                                                                                | <span data-ttu-id="bc611-125">Описание</span><span class="sxs-lookup"><span data-stu-id="bc611-125">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="bc611-126"><dt>**\_ \_ \_ \_ слишком \_ маленький Рив для NS E DRM**</dt></span><span class="sxs-lookup"><span data-stu-id="bc611-126"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="bc611-127">Требуется обновленный список отзыва содержимого.</span><span class="sxs-lookup"><span data-stu-id="bc611-127">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="bc611-128"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="bc611-128"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="bc611-129">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="bc611-129">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="bc611-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc611-130">Remarks</span></span>

<span data-ttu-id="bc611-131">Ответ лицензии, обработанный с помощью этого метода, должен соответствовать последнему вызову лицензии, созданному на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="bc611-131">The license response processed by using this method must correspond to the last license challenge generated on the client computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc611-132">Требования</span><span class="sxs-lookup"><span data-stu-id="bc611-132">Requirements</span></span>



| <span data-ttu-id="bc611-133">Требование</span><span class="sxs-lookup"><span data-stu-id="bc611-133">Requirement</span></span> | <span data-ttu-id="bc611-134">Значение</span><span class="sxs-lookup"><span data-stu-id="bc611-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc611-135">Header</span><span class="sxs-lookup"><span data-stu-id="bc611-135">Header</span></span><br/> | <dl> <span data-ttu-id="bc611-136"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc611-136"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc611-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc611-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc611-138">**Интерфейс Ивмдрмнетрецеивер**</span><span class="sxs-lookup"><span data-stu-id="bc611-138">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="bc611-139">**Ивмдрмнетрецеивер:: Жетлиценсечалленже**</span><span class="sxs-lookup"><span data-stu-id="bc611-139">**IWMDRMNetReceiver::GetLicenseChallenge**</span></span>](iwmdrmnetreceiver-getlicensechallenge.md)
</dt> </dl>

 

 





