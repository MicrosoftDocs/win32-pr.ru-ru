---
title: Метод Ивмдрмнетрецеивер Жетрегистратиончалленже (Вмдрмсдк. h)
description: Метод Жетрегистратиончалленже создает сообщение с запросом на регистрацию DRM Windows Media для сетевых устройств.
ms.assetid: 7b3641a1-ccc5-4e29-b0e9-808b111f8841
keywords:
- Формат Windows Media, Жетрегистратиончалленже метод
- Жетрегистратиончалленже метод Windows Media Format, интерфейс Ивмдрмнетрецеивер
- Интерфейс Ивмдрмнетрецеивер Windows Media Format, метод Жетрегистратиончалленже
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetRegistrationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a292749e95ca6ba2dabc8f3829eae827dbdd8325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679724"
---
# <a name="iwmdrmnetreceivergetregistrationchallenge-method"></a><span data-ttu-id="a9fef-106">Метод Ивмдрмнетрецеивер:: Жетрегистратиончалленже</span><span class="sxs-lookup"><span data-stu-id="a9fef-106">IWMDRMNetReceiver::GetRegistrationChallenge method</span></span>

<span data-ttu-id="a9fef-107">Метод **жетрегистратиончалленже** создает сообщение с запросом на регистрацию DRM Windows Media для сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="a9fef-107">The **GetRegistrationChallenge** method generates a Windows Media DRM for Network Devices registration challenge message.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9fef-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9fef-108">Syntax</span></span>


```C++
HRESULT GetRegistrationChallenge(
  [out] BYTE  **ppbRegistrationChallenge,
  [out] DWORD *pcbRegistrationChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="a9fef-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9fef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9fef-110">*ппбрегистратиончалленже* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a9fef-110">*ppbRegistrationChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9fef-111">Адрес указателя, получающего адрес созданного запроса.</span><span class="sxs-lookup"><span data-stu-id="a9fef-111">Address of a pointer that receives the address of the generated challenge.</span></span> <span data-ttu-id="a9fef-112">После завершения работы с этими данными необходимо освободить память, вызвав **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="a9fef-112">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="a9fef-113">*пкбрегистратиончалленже* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a9fef-113">*pcbRegistrationChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9fef-114">Адрес переменной, которая получает размер запроса на регистрацию в байтах.</span><span class="sxs-lookup"><span data-stu-id="a9fef-114">Address of a variable that receives the size of the registration challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9fef-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a9fef-115">Return value</span></span>

<span data-ttu-id="a9fef-116">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a9fef-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a9fef-117">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a9fef-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a9fef-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a9fef-118">Return code</span></span>                                                                          | <span data-ttu-id="a9fef-119">Описание</span><span class="sxs-lookup"><span data-stu-id="a9fef-119">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a9fef-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a9fef-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a9fef-121">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="a9fef-121">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a9fef-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a9fef-122">Remarks</span></span>

<span data-ttu-id="a9fef-123">Нет.</span><span class="sxs-lookup"><span data-stu-id="a9fef-123">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9fef-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a9fef-124">Requirements</span></span>



| <span data-ttu-id="a9fef-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a9fef-125">Requirement</span></span> | <span data-ttu-id="a9fef-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a9fef-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9fef-127">Header</span><span class="sxs-lookup"><span data-stu-id="a9fef-127">Header</span></span><br/> | <dl> <span data-ttu-id="a9fef-128"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9fef-128"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9fef-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9fef-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9fef-130">**Интерфейс Ивмдрмнетрецеивер**</span><span class="sxs-lookup"><span data-stu-id="a9fef-130">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="a9fef-131">**Ивмдрмнетрецеивер::P Роцессрегистратионреспонсе**</span><span class="sxs-lookup"><span data-stu-id="a9fef-131">**IWMDRMNetReceiver::ProcessRegistrationResponse**</span></span>](iwmdrmnetreceiver-processregistrationresponse.md)
</dt> </dl>

 

 





