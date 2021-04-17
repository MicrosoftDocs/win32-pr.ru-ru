---
title: Метод Ивмдрмнеттрансмиттер Жетлеафлиценсереспонсе (Вмдрмсдк. h)
description: Метод Жетлеафлиценсереспонсе создает сообщение с конечным ответом лицензии.
ms.assetid: b2893d22-b6f3-44d2-b6db-e2b07fbe098d
keywords:
- Формат Windows Media, Жетлеафлиценсереспонсе метод
- Жетлеафлиценсереспонсе метод Windows Media Format, интерфейс Ивмдрмнеттрансмиттер
- Интерфейс Ивмдрмнеттрансмиттер Windows Media Format, метод Жетлеафлиценсереспонсе
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetLeafLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf2374966abfae4353a72755313c1cbbdfb7287
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675047"
---
# <a name="iwmdrmnettransmittergetleaflicenseresponse-method"></a><span data-ttu-id="b79e5-106">Метод Ивмдрмнеттрансмиттер:: Жетлеафлиценсереспонсе</span><span class="sxs-lookup"><span data-stu-id="b79e5-106">IWMDRMNetTransmitter::GetLeafLicenseResponse method</span></span>

<span data-ttu-id="b79e5-107">Метод **жетлеафлиценсереспонсе** создает сообщение с конечным ответом лицензии.</span><span class="sxs-lookup"><span data-stu-id="b79e5-107">The **GetLeafLicenseResponse** method generates a leaf license response message.</span></span>

## <a name="syntax"></a><span data-ttu-id="b79e5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b79e5-108">Syntax</span></span>


```C++
HRESULT GetLeafLicenseResponse(
  [in]  BSTR            bstrKID,
  [in]  WMDRMNET_POLICY *pPolicy,
  [out] IWMDRMEncrypt   **ppIWMDRMEncrypt,
  [out] BYTE            **ppbLicenseResponse,
  [out] DWORD           *pcbLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="b79e5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b79e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b79e5-110">*бстркид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b79e5-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b79e5-111">Идентификатор ключа в кодировке Base64, используемый для новой конечной лицензии.</span><span class="sxs-lookup"><span data-stu-id="b79e5-111">Base64-encoded key identifier to be used for the new leaf license.</span></span> <span data-ttu-id="b79e5-112">Идентификатор ключа должен быть случайным образом сгенерированным значением GUID.</span><span class="sxs-lookup"><span data-stu-id="b79e5-112">The key identifier should be a randomly generated GUID value.</span></span>

</dd> <dt>

<span data-ttu-id="b79e5-113">*пполици* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b79e5-113">*pPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b79e5-114">Указатель на структуру [**\_ политики вмдрмнет**](wmdrmnet-policy.md) , определяющую политику, используемую для конечной лицензии.</span><span class="sxs-lookup"><span data-stu-id="b79e5-114">Pointer to the [**WMDRMNET\_POLICY**](wmdrmnet-policy.md) structure that defines the policy to use for the leaf license.</span></span>

</dd> <dt>

<span data-ttu-id="b79e5-115">*ппивмдрменкрипт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b79e5-115">*ppIWMDRMEncrypt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b79e5-116">Адрес переменной, которая получает указатель на интерфейс [**ивмдрменкрипт**](iwmdrmencrypt.md) , который может использоваться для шифрования данных для новой конечной лицензии.</span><span class="sxs-lookup"><span data-stu-id="b79e5-116">Address of a variable that receives a pointer to the [**IWMDRMEncrypt**](iwmdrmencrypt.md) interface that can be used to encrypt data for the new leaf license.</span></span>

</dd> <dt>

<span data-ttu-id="b79e5-117">*ппблиценсереспонсе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b79e5-117">*ppbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b79e5-118">Адрес переменной, которая получает адрес созданного ответа на лицензию.</span><span class="sxs-lookup"><span data-stu-id="b79e5-118">Address of a variable that receives the address of the generated license response.</span></span> <span data-ttu-id="b79e5-119">После завершения работы с этими данными необходимо освободить память, вызвав **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="b79e5-119">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="b79e5-120">*пкблиценсереспонсе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b79e5-120">*pcbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b79e5-121">Адрес переменной, которая получает размер ответа на лицензию в байтах.</span><span class="sxs-lookup"><span data-stu-id="b79e5-121">Address of a variable that receives the size of the license response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b79e5-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b79e5-122">Return value</span></span>

<span data-ttu-id="b79e5-123">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b79e5-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b79e5-124">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b79e5-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b79e5-125">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b79e5-125">Return code</span></span>                                                                                                | <span data-ttu-id="b79e5-126">Описание</span><span class="sxs-lookup"><span data-stu-id="b79e5-126">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="b79e5-127"><dt>**\_ \_ \_ \_ слишком \_ маленький Рив для NS E DRM**</dt></span><span class="sxs-lookup"><span data-stu-id="b79e5-127"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="b79e5-128">Требуется обновленный список отзыва содержимого.</span><span class="sxs-lookup"><span data-stu-id="b79e5-128">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="b79e5-129"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b79e5-129"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="b79e5-130">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="b79e5-130">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="b79e5-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b79e5-131">Remarks</span></span>

<span data-ttu-id="b79e5-132">Нет.</span><span class="sxs-lookup"><span data-stu-id="b79e5-132">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="b79e5-133">Требования</span><span class="sxs-lookup"><span data-stu-id="b79e5-133">Requirements</span></span>



| <span data-ttu-id="b79e5-134">Требование</span><span class="sxs-lookup"><span data-stu-id="b79e5-134">Requirement</span></span> | <span data-ttu-id="b79e5-135">Значение</span><span class="sxs-lookup"><span data-stu-id="b79e5-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b79e5-136">Header</span><span class="sxs-lookup"><span data-stu-id="b79e5-136">Header</span></span><br/> | <dl> <span data-ttu-id="b79e5-137"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="b79e5-137"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b79e5-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b79e5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b79e5-139">**Интерфейс Ивмдрмнеттрансмиттер**</span><span class="sxs-lookup"><span data-stu-id="b79e5-139">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





