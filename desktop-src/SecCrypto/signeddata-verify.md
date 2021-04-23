---
description: Определяет, являются ли сигнатуры подписанных данных в объекте Сигнеддата допустимыми.
ms.assetid: 920ac235-0c1a-4b15-9cdd-c7e0c3ea6107
title: Сигнеддата. Verify, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3cb48943a826296c13df80130171442fc29435f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665243"
---
# <a name="signeddataverify-method"></a><span data-ttu-id="6bd18-103">Сигнеддата. Verify, метод</span><span class="sxs-lookup"><span data-stu-id="6bd18-103">SignedData.Verify method</span></span>

<span data-ttu-id="6bd18-104">\[Метод **Verify** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="6bd18-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6bd18-105">Вместо этого используйте [**класс SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="6bd18-105">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="6bd18-106">Метод **Verify** определяет, являются ли [*подписи*](../secgloss/d-gly.md) подписанных данных в объекте [**сигнеддата**](signeddata.md) допустимыми.</span><span class="sxs-lookup"><span data-stu-id="6bd18-106">The **Verify** method determines whether the [*signatures*](../secgloss/d-gly.md) on signed data in the [**SignedData**](signeddata.md) object are valid.</span></span> <span data-ttu-id="6bd18-107">Чтобы проверить подпись, зашифрованный [*хэш*](../secgloss/h-gly.md) содержимого расшифровывается с помощью открытого ключа подписавший из сертификата подписи.</span><span class="sxs-lookup"><span data-stu-id="6bd18-107">To verify a signature, the encrypted [*hash*](../secgloss/h-gly.md) of the contents is decrypted by using the signer's public key from the signer's certificate.</span></span> <span data-ttu-id="6bd18-108">Расшифрованный хэш сравнивается с новым хэшем содержимого данных.</span><span class="sxs-lookup"><span data-stu-id="6bd18-108">The decrypted hash is compared to a new hash of the data content.</span></span> <span data-ttu-id="6bd18-109">Подпись допустима, если хэши совпадают.</span><span class="sxs-lookup"><span data-stu-id="6bd18-109">A signature is valid if the hashes match.</span></span> <span data-ttu-id="6bd18-110">Кроме того, этот метод также создает цепочку сертификатов для определения допустимости сертификата, предоставляющего [*открытый ключ*](../secgloss/p-gly.md) , используемый для расшифровки хэша.</span><span class="sxs-lookup"><span data-stu-id="6bd18-110">In addition, this method also builds a certificate chain to determine the validity of the certificate that provides the [*public key*](../secgloss/p-gly.md) used to decrypt the hash.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bd18-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6bd18-111">Syntax</span></span>


```VB
SignedData.Verify( _
  ByVal SignedMessage, _
  [ ByVal bDetached ], _
  [ ByVal VerifyFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="6bd18-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="6bd18-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bd18-113">*Сигнедмессаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6bd18-113">*SignedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bd18-114">Строка, содержащая подписанное сообщение для проверки.</span><span class="sxs-lookup"><span data-stu-id="6bd18-114">A string that contains the signed message to be verified.</span></span>

</dd> <dt>

<span data-ttu-id="6bd18-115">*бдетачед* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="6bd18-115">*bDetached* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6bd18-116">Если **значение равно true**, данные для подписи отсоединяются; Это значит, что подписанное содержимое не входит в состав подписанного объекта.</span><span class="sxs-lookup"><span data-stu-id="6bd18-116">If **True**, the data to be signed is detached; that is, the content that is signed is not included as part of the signed object.</span></span> <span data-ttu-id="6bd18-117">Чтобы проверить подпись отсоединенного содержимого, приложение должно иметь копию исходного содержимого.</span><span class="sxs-lookup"><span data-stu-id="6bd18-117">To verify the signature on detached content, an application must have a copy of the original content.</span></span> <span data-ttu-id="6bd18-118">Отсоединенное содержимое часто используется для уменьшения размера подписанного объекта для отправки через Интернет, если получатель подписанного сообщения имеет исходную копию подписанных данных.</span><span class="sxs-lookup"><span data-stu-id="6bd18-118">Detached content is often used to decrease the size of a signed object to be sent across the web, if the recipient of the signed message has an original copy of the signed data.</span></span> <span data-ttu-id="6bd18-119">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="6bd18-119">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="6bd18-120">*Верифифлаг* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="6bd18-120">*VerifyFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6bd18-121">Значение перечисление [ \_ \_ \_ \_ флагов CAPICOM, подписанных проверкой данных](capicom-signed-data-verify-flag.md) , которое указывает политику проверки.</span><span class="sxs-lookup"><span data-stu-id="6bd18-121">A value of the [CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG](capicom-signed-data-verify-flag.md) enumeration that indicates the verification policy.</span></span> <span data-ttu-id="6bd18-122">По умолчанию используется значение CAPICOM \_ проверить \_ подпись \_ и \_ сертификат.</span><span class="sxs-lookup"><span data-stu-id="6bd18-122">The default value is CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE.</span></span> <span data-ttu-id="6bd18-123">При использовании этого значения проверяется как достоверность сертификата, так и достоверность подписи.</span><span class="sxs-lookup"><span data-stu-id="6bd18-123">Using this value, both the validity of the certificate and the validity of the signature are checked.</span></span> <span data-ttu-id="6bd18-124">Этот параметр может быть установлен для проверки подписи, а не сертификата.</span><span class="sxs-lookup"><span data-stu-id="6bd18-124">This parameter may be set to verify the signature and not the certificate.</span></span> <span data-ttu-id="6bd18-125">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="6bd18-125">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="6bd18-126">Значение</span><span class="sxs-lookup"><span data-stu-id="6bd18-126">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="6bd18-127">Значение</span><span class="sxs-lookup"><span data-stu-id="6bd18-127">Meaning</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_VERIFY_SIGNATURE_ONLY"></span><span id="capicom_verify_signature_only"></span><dl> <span data-ttu-id="6bd18-128"><dt>**CAPICOM \_ проверить \_ \_ только подпись**</dt></span><span class="sxs-lookup"><span data-stu-id="6bd18-128"><dt>**CAPICOM\_VERIFY\_SIGNATURE\_ONLY**</dt></span></span> </dl>                                   | <span data-ttu-id="6bd18-129">Проверяется только подпись.</span><span class="sxs-lookup"><span data-stu-id="6bd18-129">Only the signature is checked.</span></span><br/>                                                                   |
| <span id="CAPICOM_VERIFY_SIGNATURE_AND_CERTIFICATE"></span><span id="capicom_verify_signature_and_certificate"></span><dl> <span data-ttu-id="6bd18-130"><dt>**CAPICOM \_ Проверка \_ подписи \_ и \_ сертификата**</dt></span><span class="sxs-lookup"><span data-stu-id="6bd18-130"><dt>**CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE**</dt></span></span> </dl> | <span data-ttu-id="6bd18-131">Проверяется подпись и допустимость сертификата, используемого для создания подписи.</span><span class="sxs-lookup"><span data-stu-id="6bd18-131">Both the signature and the validity of the certificate used to create the signature are checked.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bd18-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6bd18-132">Return value</span></span>

<span data-ttu-id="6bd18-133">Этот метод возвращает строку, содержащую закодированные подписанные данные.</span><span class="sxs-lookup"><span data-stu-id="6bd18-133">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="6bd18-134">В случае сбоя этого метода возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="6bd18-134">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="6bd18-135">Объект **Err** будет содержать дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="6bd18-135">The **Err** object will contain additional information about the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bd18-136">Требования</span><span class="sxs-lookup"><span data-stu-id="6bd18-136">Requirements</span></span>



| <span data-ttu-id="6bd18-137">Требование</span><span class="sxs-lookup"><span data-stu-id="6bd18-137">Requirement</span></span> | <span data-ttu-id="6bd18-138">Значение</span><span class="sxs-lookup"><span data-stu-id="6bd18-138">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bd18-139">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="6bd18-139">Redistributable</span></span><br/> | <span data-ttu-id="6bd18-140">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="6bd18-140">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6bd18-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6bd18-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="6bd18-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bd18-142"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bd18-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6bd18-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bd18-144">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="6bd18-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="6bd18-145">**сигнеддата**</span><span class="sxs-lookup"><span data-stu-id="6bd18-145">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
