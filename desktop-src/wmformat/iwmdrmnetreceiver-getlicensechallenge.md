---
title: Метод Ивмдрмнетрецеивер Жетлиценсечалленже (Вмдрмсдк. h)
description: Метод Жетлиценсечалленже создает запрос на лицензию Windows Media DRM для сетевых устройств, который может быть отправлен передатчику при запросе защищенного содержимого.
ms.assetid: c13b9e9e-b076-411b-a106-b602544faaba
keywords:
- Формат Windows Media, Жетлиценсечалленже метод
- Жетлиценсечалленже метод Windows Media Format, интерфейс Ивмдрмнетрецеивер
- Интерфейс Ивмдрмнетрецеивер Windows Media Format, метод Жетлиценсечалленже
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f58b85b8dc5edd6c23e809dda8c18bf30137f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675050"
---
# <a name="iwmdrmnetreceivergetlicensechallenge-method"></a><span data-ttu-id="cbfe2-106">Метод Ивмдрмнетрецеивер:: Жетлиценсечалленже</span><span class="sxs-lookup"><span data-stu-id="cbfe2-106">IWMDRMNetReceiver::GetLicenseChallenge method</span></span>

<span data-ttu-id="cbfe2-107">Метод **жетлиценсечалленже** создает запрос на лицензию Windows Media DRM для сетевых устройств, который может быть отправлен передатчику при запросе защищенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="cbfe2-107">The **GetLicenseChallenge** method generates a Windows Media DRM for Network Devices license challenge that can be sent to a transmitter when requesting protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbfe2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbfe2-108">Syntax</span></span>


```C++
HRESULT GetLicenseChallenge(
  [in]  BSTR  bstrAction,
  [out] BYTE  **ppbLicenseChallenge,
  [out] DWORD *pcbLicenseChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="cbfe2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbfe2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbfe2-110">*бстрактион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbfe2-110">*bstrAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbfe2-111">Действие, для которого создается запрос.</span><span class="sxs-lookup"><span data-stu-id="cbfe2-111">Action for which to generate the challenge.</span></span>

</dd> <dt>

<span data-ttu-id="cbfe2-112">*ппблиценсечалленже* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cbfe2-112">*ppbLicenseChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbfe2-113">Адрес указателя, которому присваивается адрес созданного запроса.</span><span class="sxs-lookup"><span data-stu-id="cbfe2-113">Address of a pointer that is set to the address of the generated challenge.</span></span> <span data-ttu-id="cbfe2-114">После завершения работы с этими данными необходимо освободить память, вызвав **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="cbfe2-114">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="cbfe2-115">*пкблиценсечалленже* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cbfe2-115">*pcbLicenseChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbfe2-116">Адрес переменной, которая получает размер запроса лицензии в байтах.</span><span class="sxs-lookup"><span data-stu-id="cbfe2-116">Address of a variable that receives the size of the license challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbfe2-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbfe2-117">Return value</span></span>

<span data-ttu-id="cbfe2-118">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="cbfe2-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="cbfe2-119">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="cbfe2-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="cbfe2-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cbfe2-120">Return code</span></span>                                                                          | <span data-ttu-id="cbfe2-121">Описание</span><span class="sxs-lookup"><span data-stu-id="cbfe2-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="cbfe2-122"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="cbfe2-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="cbfe2-123">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="cbfe2-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cbfe2-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cbfe2-124">Remarks</span></span>

<span data-ttu-id="cbfe2-125">Нет.</span><span class="sxs-lookup"><span data-stu-id="cbfe2-125">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbfe2-126">Требования</span><span class="sxs-lookup"><span data-stu-id="cbfe2-126">Requirements</span></span>



| <span data-ttu-id="cbfe2-127">Требование</span><span class="sxs-lookup"><span data-stu-id="cbfe2-127">Requirement</span></span> | <span data-ttu-id="cbfe2-128">Значение</span><span class="sxs-lookup"><span data-stu-id="cbfe2-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cbfe2-129">Header</span><span class="sxs-lookup"><span data-stu-id="cbfe2-129">Header</span></span><br/> | <dl> <span data-ttu-id="cbfe2-130"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbfe2-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbfe2-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbfe2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbfe2-132">**Интерфейс Ивмдрмнетрецеивер**</span><span class="sxs-lookup"><span data-stu-id="cbfe2-132">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="cbfe2-133">**Ивмдрмнетрецеивер::P Роцесслиценсереспонсе**</span><span class="sxs-lookup"><span data-stu-id="cbfe2-133">**IWMDRMNetReceiver::ProcessLicenseResponse**</span></span>](iwmdrmnetreceiver-processlicenseresponse.md)
</dt> </dl>

 

 





