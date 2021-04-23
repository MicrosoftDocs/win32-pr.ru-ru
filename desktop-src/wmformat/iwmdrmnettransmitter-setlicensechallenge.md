---
title: Метод Ивмдрмнеттрансмиттер Сетлиценсечалленже (Вмдрмсдк. h)
description: Метод Сетлиценсечалленже обрабатывает запрос лицензии, отправленный получателем Windows Media DRM для приемника сетевых устройств.
ms.assetid: 3d4cd029-a8f5-49fc-ba8c-d8615ff94366
keywords:
- Формат Windows Media, Сетлиценсечалленже метод
- Сетлиценсечалленже метод Windows Media Format, интерфейс Ивмдрмнеттрансмиттер
- Интерфейс Ивмдрмнеттрансмиттер Windows Media Format, метод Сетлиценсечалленже
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.SetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94b83ca615896039a592d147fe8c14d15493cec0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675046"
---
# <a name="iwmdrmnettransmittersetlicensechallenge-method"></a><span data-ttu-id="c2026-106">Метод Ивмдрмнеттрансмиттер:: Сетлиценсечалленже</span><span class="sxs-lookup"><span data-stu-id="c2026-106">IWMDRMNetTransmitter::SetLicenseChallenge method</span></span>

<span data-ttu-id="c2026-107">Метод **сетлиценсечалленже** обрабатывает запрос лицензии, отправленный получателем Windows Media DRM для приемника сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="c2026-107">The **SetLicenseChallenge** method processes a license challenge sent by a Windows Media DRM for Network Devices receiver.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2026-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2026-108">Syntax</span></span>


```C++
HRESULT SetLicenseChallenge(
  [in] BYTE  *pbLicenseChallenge,
  [in] DWORD cbLicenseChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="c2026-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2026-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2026-110">*пблиценсечалленже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c2026-110">*pbLicenseChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2026-111">Указатель на данные запроса лицензии, отправленные получателем.</span><span class="sxs-lookup"><span data-stu-id="c2026-111">Pointer to the license challenge data that was sent by a receiver.</span></span>

</dd> <dt>

<span data-ttu-id="c2026-112">*кблиценсечалленже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c2026-112">*cbLicenseChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2026-113">Размер запроса лицензии в байтах.</span><span class="sxs-lookup"><span data-stu-id="c2026-113">Size of license challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2026-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2026-114">Return value</span></span>

<span data-ttu-id="c2026-115">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c2026-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c2026-116">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c2026-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c2026-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c2026-117">Return code</span></span>                                                                          | <span data-ttu-id="c2026-118">Описание</span><span class="sxs-lookup"><span data-stu-id="c2026-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c2026-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c2026-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c2026-120">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="c2026-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c2026-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2026-121">Remarks</span></span>

<span data-ttu-id="c2026-122">Если этот метод завершится с ошибкой, последующие вызовы других методов **ивмдрмнеттрансмиттер** будут использовать информацию в обработанном вызове.</span><span class="sxs-lookup"><span data-stu-id="c2026-122">If this method succeeds, subsequent calls to the other methods of **IWMDRMNetTransmitter** will use the information in the processed challenge.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2026-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c2026-123">Requirements</span></span>



| <span data-ttu-id="c2026-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c2026-124">Requirement</span></span> | <span data-ttu-id="c2026-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c2026-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2026-126">Header</span><span class="sxs-lookup"><span data-stu-id="c2026-126">Header</span></span><br/> | <dl> <span data-ttu-id="c2026-127"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2026-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2026-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2026-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2026-129">**Интерфейс Ивмдрмнеттрансмиттер**</span><span class="sxs-lookup"><span data-stu-id="c2026-129">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





