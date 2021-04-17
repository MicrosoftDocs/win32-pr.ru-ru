---
title: Метод Ивмдрмлиценсе Креатесекуредекриптор (Вмдрмсдк. h)
description: Метод Креатесекуредекриптор создает объект Secure дешифратора. Безопасный дешифратор отличается от обычного дешифратора в том, что расшифровывает содержимое, а затем повторно шифрует его в соответствии с параметрами, заданными в параметрах этого метода.
ms.assetid: f3fe8d47-ec7b-4ba5-b5ae-6262cb455ffc
keywords:
- Формат Windows Media, Креатесекуредекриптор метод
- Креатесекуредекриптор метод Windows Media Format, интерфейс Ивмдрмлиценсе
- Интерфейс Ивмдрмлиценсе Windows Media Format, метод Креатесекуредекриптор
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateSecureDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ededb4c985e345c1e40563d02c87bfe447b8960f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704074"
---
# <a name="iwmdrmlicensecreatesecuredecryptor-method"></a><span data-ttu-id="445e5-107">Метод Ивмдрмлиценсе:: Креатесекуредекриптор</span><span class="sxs-lookup"><span data-stu-id="445e5-107">IWMDRMLicense::CreateSecureDecryptor method</span></span>

<span data-ttu-id="445e5-108">Метод **креатесекуредекриптор** создает объект Secure дешифратора.</span><span class="sxs-lookup"><span data-stu-id="445e5-108">The **CreateSecureDecryptor** method creates a secure decryptor object.</span></span> <span data-ttu-id="445e5-109">Безопасный дешифратор отличается от обычного дешифратора в том, что расшифровывает содержимое, а затем повторно шифрует его в соответствии с параметрами, заданными в параметрах этого метода.</span><span class="sxs-lookup"><span data-stu-id="445e5-109">The secure decryptor differs from the normal decryptor in that it decrypts the content and then re-encrypts it according to the settings specified in the parameters of this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="445e5-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="445e5-110">Syntax</span></span>


```C++
HRESULT CreateSecureDecryptor(
  [in]      BYTE          *pbCertificate,
  [in]      DWORD         cbCertificate,
  [in]      DWORD         dwCertificateType,
  [in]      DWORD         dwFlags,
  [out]     BYTE          *pbInitializationVector,
  [in, out] DWORD         *pcbInitializationVector,
  [out]     IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a><span data-ttu-id="445e5-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="445e5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="445e5-112">*пбцертификате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="445e5-112">*pbCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="445e5-113">Сертификат вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="445e5-113">Certificate of the calling application.</span></span>

</dd> <dt>

<span data-ttu-id="445e5-114">*кбцертификате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="445e5-114">*cbCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="445e5-115">Размер сертификата в байтах.</span><span class="sxs-lookup"><span data-stu-id="445e5-115">Size of the certificate in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="445e5-116">*двцертификатетипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="445e5-116">*dwCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="445e5-117">Тип сертификата.</span><span class="sxs-lookup"><span data-stu-id="445e5-117">The type of the certificate.</span></span> <span data-ttu-id="445e5-118">Укажите \_ \_ XML типа сертификата WMDRM \_ .</span><span class="sxs-lookup"><span data-stu-id="445e5-118">Set to WMDRM\_CERTIFICATE\_TYPE\_XML.</span></span>

</dd> <dt>

<span data-ttu-id="445e5-119">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="445e5-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="445e5-120">Тип защиты сеанса, используемый для повторной кодировки.</span><span class="sxs-lookup"><span data-stu-id="445e5-120">The type of session protection to use for re-encoding.</span></span> <span data-ttu-id="445e5-121">Необходимо задать одну из констант в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="445e5-121">Must be set to one of the constants in the following table:</span></span>



| <span data-ttu-id="445e5-122">Константа</span><span class="sxs-lookup"><span data-stu-id="445e5-122">Constant</span></span>                     | <span data-ttu-id="445e5-123">Описание</span><span class="sxs-lookup"><span data-stu-id="445e5-123">Description</span></span>                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="445e5-124">\_Тип защиты \_ WMDRM \_ RC4</span><span class="sxs-lookup"><span data-stu-id="445e5-124">WMDRM\_PROTECTION\_TYPE\_RC4</span></span> | <span data-ttu-id="445e5-125">Использует алгоритм шифрования RC4 для шифрования сеанса.</span><span class="sxs-lookup"><span data-stu-id="445e5-125">Uses RC4 encryption for session encryption.</span></span> <span data-ttu-id="445e5-126">Это единственная поддерживаемая защита сеанса для этой версии.</span><span class="sxs-lookup"><span data-stu-id="445e5-126">This is the only supported session protection for this version.</span></span> |



 

</dd> <dt>

<span data-ttu-id="445e5-127">*пбинитиализатионвектор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="445e5-127">*pbInitializationVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="445e5-128">Получает вектор инициализации.</span><span class="sxs-lookup"><span data-stu-id="445e5-128">Receives the initialization vector.</span></span> <span data-ttu-id="445e5-129">Вектор инициализации зашифрован RSA с использованием схемы заполнения OAEP с открытым ключом RSA, найденным в сертификате.</span><span class="sxs-lookup"><span data-stu-id="445e5-129">The initialization vector is RSA encrypted using the OAEP padding scheme with the RSA public key found in the certificate.</span></span> <span data-ttu-id="445e5-130">Задайте **значение NULL** , чтобы получить требуемый размер буфера в *пкбинитиализатионвектор*.</span><span class="sxs-lookup"><span data-stu-id="445e5-130">Set to **NULL** to receive the required buffer size in *pcbInitializationVector*.</span></span>

</dd> <dt>

<span data-ttu-id="445e5-131">*пкбинитиализатионвектор* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="445e5-131">*pcbInitializationVector* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="445e5-132">При вводе размер буфера передается как *пбинитиализатионвектор*.</span><span class="sxs-lookup"><span data-stu-id="445e5-132">On input, the size of the buffer passed as *pbInitializationVector*.</span></span> <span data-ttu-id="445e5-133">На выходе — размер используемой части буфера.</span><span class="sxs-lookup"><span data-stu-id="445e5-133">On output, the size of the used portion of the buffer.</span></span> <span data-ttu-id="445e5-134">Если передать **значение NULL** для *пбинитиализатионвектор*, то для этого параметра задается требуемый размер буфера в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="445e5-134">If you pass **NULL** for *pbInitializationVector*, this value is set to the required buffer size on output.</span></span>

</dd> <dt>

<span data-ttu-id="445e5-135">*ппдекриптор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="445e5-135">*ppDecryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="445e5-136">Получает указатель на интерфейс [**ивмдрмдекрипт**](iwmdrmdecrypt.md) только что созданного объекта.</span><span class="sxs-lookup"><span data-stu-id="445e5-136">Receives a pointer to the [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="445e5-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="445e5-137">Return value</span></span>

<span data-ttu-id="445e5-138">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="445e5-138">The method returns an **HRESULT**.</span></span> <span data-ttu-id="445e5-139">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="445e5-139">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="445e5-140">Код возврата</span><span class="sxs-lookup"><span data-stu-id="445e5-140">Return code</span></span>                                                                          | <span data-ttu-id="445e5-141">Описание</span><span class="sxs-lookup"><span data-stu-id="445e5-141">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="445e5-142"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="445e5-142"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="445e5-143">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="445e5-143">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="445e5-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="445e5-144">Remarks</span></span>

<span data-ttu-id="445e5-145">Нет.</span><span class="sxs-lookup"><span data-stu-id="445e5-145">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="445e5-146">Требования</span><span class="sxs-lookup"><span data-stu-id="445e5-146">Requirements</span></span>



| <span data-ttu-id="445e5-147">Требование</span><span class="sxs-lookup"><span data-stu-id="445e5-147">Requirement</span></span> | <span data-ttu-id="445e5-148">Значение</span><span class="sxs-lookup"><span data-stu-id="445e5-148">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="445e5-149">Header</span><span class="sxs-lookup"><span data-stu-id="445e5-149">Header</span></span><br/> | <dl> <span data-ttu-id="445e5-150"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="445e5-150"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="445e5-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="445e5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="445e5-152">**Интерфейс Ивмдрмлиценсе**</span><span class="sxs-lookup"><span data-stu-id="445e5-152">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





