---
title: Метод Ивмдрмнеттрансмиттер Жетрутлиценсереспонсе (Вмдрмсдк. h)
description: Метод Жетрутлиценсереспонсе создает сообщение о корневом ответе лицензии.
ms.assetid: c735ee52-f0e0-4404-881b-18ee9a7fa9f9
keywords:
- Формат Windows Media, Жетрутлиценсереспонсе метод
- Жетрутлиценсереспонсе метод Windows Media Format, интерфейс Ивмдрмнеттрансмиттер
- Интерфейс Ивмдрмнеттрансмиттер Windows Media Format, метод Жетрутлиценсереспонсе
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetRootLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3497a3eaedb872b7d2c9eb5d7782d01f8b35462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675390"
---
# <a name="iwmdrmnettransmittergetrootlicenseresponse-method"></a><span data-ttu-id="3ca40-106">Метод Ивмдрмнеттрансмиттер:: Жетрутлиценсереспонсе</span><span class="sxs-lookup"><span data-stu-id="3ca40-106">IWMDRMNetTransmitter::GetRootLicenseResponse method</span></span>

<span data-ttu-id="3ca40-107">Метод **жетрутлиценсереспонсе** создает сообщение о корневом ответе лицензии.</span><span class="sxs-lookup"><span data-stu-id="3ca40-107">The **GetRootLicenseResponse** method generates a root license response message.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ca40-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ca40-108">Syntax</span></span>


```C++
HRESULT GetRootLicenseResponse(
  [in]  BSTR  bstrKID,
  [out] BYTE  **ppbLicenseResponse,
  [out] DWORD *pcbLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="3ca40-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ca40-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ca40-110">*бстркид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ca40-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca40-111">Идентификатор ключа в кодировке Base64, используемый для новой корневой лицензии.</span><span class="sxs-lookup"><span data-stu-id="3ca40-111">Base64-encoded key identifier to be used for the new root license.</span></span> <span data-ttu-id="3ca40-112">Идентификатор ключа должен быть случайным образом сгенерированным значением GUID.</span><span class="sxs-lookup"><span data-stu-id="3ca40-112">The key identifier should be a randomly generated GUID value.</span></span>

</dd> <dt>

<span data-ttu-id="3ca40-113">*ппблиценсереспонсе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3ca40-113">*ppbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca40-114">Адрес переменной, которая получает адрес созданного ответа на лицензию.</span><span class="sxs-lookup"><span data-stu-id="3ca40-114">Address of a variable that receives the address of the generated license response.</span></span> <span data-ttu-id="3ca40-115">После завершения работы с этими данными необходимо освободить память, вызвав **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="3ca40-115">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="3ca40-116">*пкблиценсереспонсе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3ca40-116">*pcbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca40-117">Адрес переменной, которая получает размер ответа на лицензию в байтах.</span><span class="sxs-lookup"><span data-stu-id="3ca40-117">Address of a variable that receives the size of the license response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ca40-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ca40-118">Return value</span></span>

<span data-ttu-id="3ca40-119">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3ca40-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3ca40-120">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3ca40-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3ca40-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3ca40-121">Return code</span></span>                                                                                                | <span data-ttu-id="3ca40-122">Описание</span><span class="sxs-lookup"><span data-stu-id="3ca40-122">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="3ca40-123"><dt>**\_ \_ \_ \_ слишком \_ маленький Рив для NS E DRM**</dt></span><span class="sxs-lookup"><span data-stu-id="3ca40-123"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="3ca40-124">Требуется обновленный список отзыва содержимого.</span><span class="sxs-lookup"><span data-stu-id="3ca40-124">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="3ca40-125"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3ca40-125"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="3ca40-126">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="3ca40-126">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="3ca40-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ca40-127">Remarks</span></span>

<span data-ttu-id="3ca40-128">Созданная корневая лицензия создается с использованием сведений из данных запроса лицензии, которые обрабатываются для интерфейса путем вызова [**сетлиценсечалленже**](iwmdrmnettransmitter-setlicensechallenge.md).</span><span class="sxs-lookup"><span data-stu-id="3ca40-128">The generated root license is created using the information from the license challenge data, which is processed for the interface by calling [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md).</span></span>

<span data-ttu-id="3ca40-129">Корневая лицензия используется в поколении конечных лицензий, что выполняется путем вызова метода [**жетлеафлиценсереспонсе**](iwmdrmnettransmitter-getleaflicenseresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="3ca40-129">The root license is used in the generation of leaf licenses, which is accomplished by calling the [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) method.</span></span> <span data-ttu-id="3ca40-130">Интерфейс **ивмдрмнеттрансмиттер** поддерживает копию корневой лицензии для этого использования.</span><span class="sxs-lookup"><span data-stu-id="3ca40-130">The **IWMDRMNetTransmitter** interface maintains a copy of the root license for that use.</span></span>

<span data-ttu-id="3ca40-131">Корневая лицензия, созданная путем вызова этого метода, не имеет политик и настроена таким образом, чтобы ее нельзя было сохранить на принимающем устройстве.</span><span class="sxs-lookup"><span data-stu-id="3ca40-131">The root license created by calling this method does not have any policies and is configured so that it cannot be persisted on the receiving device.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ca40-132">Требования</span><span class="sxs-lookup"><span data-stu-id="3ca40-132">Requirements</span></span>



| <span data-ttu-id="3ca40-133">Требование</span><span class="sxs-lookup"><span data-stu-id="3ca40-133">Requirement</span></span> | <span data-ttu-id="3ca40-134">Значение</span><span class="sxs-lookup"><span data-stu-id="3ca40-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ca40-135">Header</span><span class="sxs-lookup"><span data-stu-id="3ca40-135">Header</span></span><br/> | <dl> <span data-ttu-id="3ca40-136"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ca40-136"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ca40-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ca40-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ca40-138">**Интерфейс Ивмдрмнеттрансмиттер**</span><span class="sxs-lookup"><span data-stu-id="3ca40-138">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





