---
title: Метод Ивмдрмсекурити Жетмачинецертификате (Вмдрмсдк. h)
description: Метод Жетмачинецертификате извлекает сертификат компьютера подсистемы DRM на клиентском компьютере.
ms.assetid: 38b8e812-e997-4a63-b906-ebd26a5556be
keywords:
- Формат Windows Media, Жетмачинецертификате метод
- Жетмачинецертификате метод Windows Media Format, интерфейс Ивмдрмсекурити
- Интерфейс Ивмдрмсекурити Windows Media Format, метод Жетмачинецертификате
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetMachineCertificate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d6c66c54ab9528a458910def5978ec83b191654
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648673"
---
# <a name="iwmdrmsecuritygetmachinecertificate-method"></a><span data-ttu-id="880df-106">Метод Ивмдрмсекурити:: Жетмачинецертификате</span><span class="sxs-lookup"><span data-stu-id="880df-106">IWMDRMSecurity::GetMachineCertificate method</span></span>

<span data-ttu-id="880df-107">Метод **жетмачинецертификате** извлекает сертификат компьютера подсистемы DRM на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="880df-107">The **GetMachineCertificate** method retrieves the machine certificate of the DRM subsystem on the client computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="880df-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="880df-108">Syntax</span></span>


```C++
HRESULT GetMachineCertificate(
  [in]      DWORD dwCertificateType,
  [out]     BYTE  rgbVersion[4],
  [out]     BYTE  **ppbCertificate,
  [in, out] DWORD *pcbCertificate
);
```



## <a name="parameters"></a><span data-ttu-id="880df-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="880df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="880df-110">*двцертификатетипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="880df-110">*dwCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="880df-111">Тип получаемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="880df-111">Type of certificate to retrieve.</span></span> <span data-ttu-id="880df-112">Задайте одно из значений, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="880df-112">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="880df-113">Значение</span><span class="sxs-lookup"><span data-stu-id="880df-113">Value</span></span>                        | <span data-ttu-id="880df-114">Описание</span><span class="sxs-lookup"><span data-stu-id="880df-114">Description</span></span>                                                                           |
|------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="880df-115">\_Тип сертификата \_ WMDRM \_ v1</span><span class="sxs-lookup"><span data-stu-id="880df-115">WMDRM\_CERTIFICATE\_TYPE\_V1</span></span> | <span data-ttu-id="880df-116">Сертификат будет извлечен в формате, используемом компонентами предыдущих версий.</span><span class="sxs-lookup"><span data-stu-id="880df-116">The certificate will be retrieved in the format used by legacy components.</span></span>            |
| <span data-ttu-id="880df-117">\_Тип сертификата \_ WMDRM \_ v2</span><span class="sxs-lookup"><span data-stu-id="880df-117">WMDRM\_CERTIFICATE\_TYPE\_V2</span></span> | <span data-ttu-id="880df-118">Сертификат будет извлечен в формате, используемом компонентами Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="880df-118">The certificate will be retrieved in the format used by the Windows Vista components.</span></span> |



 

</dd> <dt>

<span data-ttu-id="880df-119">*ргбверсион \[ 4 \]* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="880df-119">*rgbVersion\[4\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="880df-120">Массив из четырех байтов, указывающих версию подсистемы DRM на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="880df-120">Array of four bytes specifying the version of the DRM subsystem on the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="880df-121">*ппбцертификате* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="880df-121">*ppbCertificate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="880df-122">Адрес переменной, которая получает указатель на данные сертификата.</span><span class="sxs-lookup"><span data-stu-id="880df-122">Address of a variable that receives a pointer to the certificate data.</span></span> <span data-ttu-id="880df-123">Задайте для параметра **значение NULL** , чтобы метод предоставил размер буфера, необходимый для хранения сертификата в *пкбцертификате*.</span><span class="sxs-lookup"><span data-stu-id="880df-123">Set to **NULL** to have the method provide the buffer size required to hold the certificate in *pcbCertificate*.</span></span>

</dd> <dt>

<span data-ttu-id="880df-124">*пкбцертификате* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="880df-124">*pcbCertificate* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="880df-125">Размер сертификата в байтах.</span><span class="sxs-lookup"><span data-stu-id="880df-125">Size of the certificate in bytes.</span></span> <span data-ttu-id="880df-126">Если *ппбцертификате* имеет **значение NULL**, для этого значения будет задан размер сертификата.</span><span class="sxs-lookup"><span data-stu-id="880df-126">If *ppbCertificate* is **NULL**, this value will be set to the size of the certificate.</span></span> <span data-ttu-id="880df-127">Если *ппбцертификате* не равно **null**, это значение должно быть равно размеру буфера.</span><span class="sxs-lookup"><span data-stu-id="880df-127">If *ppbCertificate* is not **NULL**, this value must be set to the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="880df-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="880df-128">Return value</span></span>

<span data-ttu-id="880df-129">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="880df-129">The method returns an **HRESULT**.</span></span> <span data-ttu-id="880df-130">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="880df-130">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="880df-131">Код возврата</span><span class="sxs-lookup"><span data-stu-id="880df-131">Return code</span></span>                                                                          | <span data-ttu-id="880df-132">Описание</span><span class="sxs-lookup"><span data-stu-id="880df-132">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="880df-133"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="880df-133"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="880df-134">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="880df-134">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="880df-135">Требования</span><span class="sxs-lookup"><span data-stu-id="880df-135">Requirements</span></span>



| <span data-ttu-id="880df-136">Требование</span><span class="sxs-lookup"><span data-stu-id="880df-136">Requirement</span></span> | <span data-ttu-id="880df-137">Значение</span><span class="sxs-lookup"><span data-stu-id="880df-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="880df-138">Header</span><span class="sxs-lookup"><span data-stu-id="880df-138">Header</span></span><br/>  | <dl> <span data-ttu-id="880df-139"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="880df-139"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="880df-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="880df-140">Library</span></span><br/> | <dl> <span data-ttu-id="880df-141"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="880df-141"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="880df-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="880df-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="880df-143">**Интерфейс Ивмдрмсекурити**</span><span class="sxs-lookup"><span data-stu-id="880df-143">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





