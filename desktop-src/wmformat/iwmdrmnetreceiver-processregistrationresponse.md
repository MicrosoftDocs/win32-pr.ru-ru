---
title: Метод Ивмдрмнетрецеивер Процессрегистратионреспонсе (Вмдрмсдк. h)
description: Метод Процессрегистратионреспонсе обрабатывает ответ регистрации, отправленный передатчиком, в ответ на запрос регистрации.
ms.assetid: d0260e93-0a5e-494b-a723-bb62206ed55b
keywords:
- Формат Windows Media, Процессрегистратионреспонсе метод
- Процессрегистратионреспонсе метод Windows Media Format, интерфейс Ивмдрмнетрецеивер
- Интерфейс Ивмдрмнетрецеивер Windows Media Format, метод Процессрегистратионреспонсе
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessRegistrationResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77b01f443d57825d82b7cf9556d7585745bb99e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675048"
---
# <a name="iwmdrmnetreceiverprocessregistrationresponse-method"></a><span data-ttu-id="b0080-106">Ивмдрмнетрецеивер: метод:P Роцессрегистратионреспонсе</span><span class="sxs-lookup"><span data-stu-id="b0080-106">IWMDRMNetReceiver::ProcessRegistrationResponse method</span></span>

<span data-ttu-id="b0080-107">Метод **процессрегистратионреспонсе** обрабатывает ответ регистрации, отправленный передатчиком, в ответ на запрос регистрации.</span><span class="sxs-lookup"><span data-stu-id="b0080-107">The **ProcessRegistrationResponse** method processes a registration response sent by the transmitter in reply to a registration challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0080-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0080-108">Syntax</span></span>


```C++
HRESULT ProcessRegistrationResponse(
  [in]  BYTE     *pbRegistrationResponse,
  [in]  DWORD    cbRegistrationResponse,
  [out] IUnknown **ppunkCancellationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="b0080-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0080-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0080-110">*пбрегистратионреспонсе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0080-110">*pbRegistrationResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0080-111">Получен ответ регистрации от передатчика.</span><span class="sxs-lookup"><span data-stu-id="b0080-111">Registration response received from the transmitter.</span></span>

</dd> <dt>

<span data-ttu-id="b0080-112">*кбрегистратионреспонсе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0080-112">*cbRegistrationResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0080-113">Размер ответа при регистрации в байтах.</span><span class="sxs-lookup"><span data-stu-id="b0080-113">Size of the registration response in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b0080-114">*ппункканцеллатионкукие* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b0080-114">*ppunkCancellationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0080-115">Указатель, получающий указатель на интерфейс **IUnknown** объекта, определяющий этот асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="b0080-115">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="b0080-116">Этот указатель интерфейса можно использовать для отмены асинхронного вызова путем вызова метода [**ивмдрмевентженератор:: канцеласинкоператион**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="b0080-116">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0080-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0080-117">Return value</span></span>

<span data-ttu-id="b0080-118">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b0080-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b0080-119">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b0080-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b0080-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b0080-120">Return code</span></span>                                                                          | <span data-ttu-id="b0080-121">Описание</span><span class="sxs-lookup"><span data-stu-id="b0080-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b0080-122"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b0080-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b0080-123">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="b0080-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b0080-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0080-124">Remarks</span></span>

<span data-ttu-id="b0080-125">Этот метод выполняется асинхронно; После завершения обработки событие Мепроксимитикомплетед отправляется в интерфейс **имфмедиаевентженератор** .</span><span class="sxs-lookup"><span data-stu-id="b0080-125">This method executes asynchronously; when processing is complete, the MEProximityCompleted event is sent to the **IMFMediaEventGenerator** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0080-126">Требования</span><span class="sxs-lookup"><span data-stu-id="b0080-126">Requirements</span></span>



| <span data-ttu-id="b0080-127">Требование</span><span class="sxs-lookup"><span data-stu-id="b0080-127">Requirement</span></span> | <span data-ttu-id="b0080-128">Значение</span><span class="sxs-lookup"><span data-stu-id="b0080-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0080-129">Header</span><span class="sxs-lookup"><span data-stu-id="b0080-129">Header</span></span><br/> | <dl> <span data-ttu-id="b0080-130"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0080-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0080-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0080-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0080-132">**Интерфейс Ивмдрмнетрецеивер**</span><span class="sxs-lookup"><span data-stu-id="b0080-132">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="b0080-133">**Ивмдрмнетрецеивер:: Жетрегистратиончалленже**</span><span class="sxs-lookup"><span data-stu-id="b0080-133">**IWMDRMNetReceiver::GetRegistrationChallenge**</span></span>](iwmdrmnetreceiver-getregistrationchallenge.md)
</dt> </dl>

 

 





