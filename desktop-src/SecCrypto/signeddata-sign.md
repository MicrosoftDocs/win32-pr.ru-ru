---
description: Создает цифровую подпись для подписанного содержимого. Цифровая подпись состоит из хэша содержимого, подписывания которого шифруется с помощью закрытого ключа подписавшего.
ms.assetid: ee98a36c-f9a9-4247-ae48-7b1a10b92be4
title: Сигнеддата. Sign, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9f885bb110b51264bc6108ca8c0f881cc48f7710
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685175"
---
# <a name="signeddatasign-method"></a><span data-ttu-id="3e918-104">Сигнеддата. Sign, метод</span><span class="sxs-lookup"><span data-stu-id="3e918-104">SignedData.Sign method</span></span>

<span data-ttu-id="3e918-105">\[Метод **Sign** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="3e918-105">\[The **Sign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3e918-106">Вместо этого используйте [**класс SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="3e918-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="3e918-107">Метод **Sign** создает [*цифровую подпись*](../secgloss/d-gly.md) для подписанного содержимого.</span><span class="sxs-lookup"><span data-stu-id="3e918-107">The **Sign** method creates a [*digital signature*](../secgloss/d-gly.md) on the content to be signed.</span></span> <span data-ttu-id="3e918-108">Цифровая подпись состоит из [*хэша*](../secgloss/h-gly.md) содержимого, подписывания которого шифруется с помощью закрытого ключа подписавшего.</span><span class="sxs-lookup"><span data-stu-id="3e918-108">A digital signature consists of a [*hash*](../secgloss/h-gly.md) of the content to be signed that is encrypted by using the private key of the signer.</span></span> <span data-ttu-id="3e918-109">Этот метод можно использовать только после инициализации свойства [**сигнеддата. Content**](signeddata-content.md) .</span><span class="sxs-lookup"><span data-stu-id="3e918-109">This method can only be used after the [**SignedData.Content**](signeddata-content.md) property has been initialized.</span></span> <span data-ttu-id="3e918-110">Если метод **Sign** вызывается для объекта, который уже имеет сигнатуру, старая сигнатура заменяется.</span><span class="sxs-lookup"><span data-stu-id="3e918-110">If the **Sign** method is called on an object that already has a signature, the old signature is replaced.</span></span> <span data-ttu-id="3e918-111">Подпись создается с помощью алгоритма подписи SHA1.</span><span class="sxs-lookup"><span data-stu-id="3e918-111">The signature is created by using the SHA1 signing algorithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e918-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e918-112">Syntax</span></span>


```VB
SignedData.Sign( _
  [ ByVal Signer ], _
  [ ByVal bDetached ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="3e918-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e918-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e918-114">*Подписавший* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="3e918-114">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3e918-115">Ссылка на объект- [**подписывающий**](signer.md) подписи данных.</span><span class="sxs-lookup"><span data-stu-id="3e918-115">A reference to the [**Signer**](signer.md) object of the signer of the data.</span></span> <span data-ttu-id="3e918-116">Объект " **подписавший** " должен иметь доступ к [*закрытому ключу*](../secgloss/p-gly.md) [*сертификата*](../secgloss/c-gly.md) , используемого для подписания.</span><span class="sxs-lookup"><span data-stu-id="3e918-116">The **Signer** object must have access to the [*private key*](../secgloss/p-gly.md) of the [*certificate*](../secgloss/c-gly.md) used to sign.</span></span> <span data-ttu-id="3e918-117">Этот параметр может иметь **значение NULL**. Дополнительные сведения см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="3e918-117">This parameter can be **NULL**; for more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3e918-118">*бдетачед* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="3e918-118">*bDetached* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3e918-119">Если **значение равно true**, данные для подписи отсоединяются; Это значит, что подписанное содержимое не входит в состав подписанного объекта.</span><span class="sxs-lookup"><span data-stu-id="3e918-119">If **True**, the data to be signed is detached; that is, the content that is signed is not included as part of the signed object.</span></span> <span data-ttu-id="3e918-120">Чтобы проверить подпись отсоединенного содержимого, приложение должно иметь копию исходного содержимого.</span><span class="sxs-lookup"><span data-stu-id="3e918-120">To verify the signature on detached content, an application must have a copy of the original content.</span></span> <span data-ttu-id="3e918-121">Отсоединенное содержимое часто используется для уменьшения размера подписанного объекта для отправки через Интернет, если получатель подписанного сообщения имеет исходную копию подписанных данных.</span><span class="sxs-lookup"><span data-stu-id="3e918-121">Detached content is often used to decrease the size of a signed object to be sent across the web, if the recipient of the signed message has an original copy of the signed data.</span></span> <span data-ttu-id="3e918-122">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="3e918-122">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="3e918-123">*Енкодингтипе* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="3e918-123">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3e918-124">Значение перечисления типа " [CAPICOM \_ Encoding \_ ](capicom-encoding-type.md) ", указывающее способ кодирования подписанных данных.</span><span class="sxs-lookup"><span data-stu-id="3e918-124">A value of the [CAPICOM\_ENCODING\_TYPE](capicom-encoding-type.md) enumeration that indicates how the signed data is to be encoded.</span></span> <span data-ttu-id="3e918-125">Значение по умолчанию — CAPICOM- \_ кодировать \_ Base64.</span><span class="sxs-lookup"><span data-stu-id="3e918-125">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="3e918-126">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="3e918-126">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="3e918-127">Значение</span><span class="sxs-lookup"><span data-stu-id="3e918-127">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="3e918-128">Значение</span><span class="sxs-lookup"><span data-stu-id="3e918-128">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="3e918-129"><dt>**CAPICOM \_ кодирует \_ ANY**</dt></span><span class="sxs-lookup"><span data-stu-id="3e918-129"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="3e918-130">Этот тип кодирования используется только в том случае, если входные данные имеют неизвестный тип кодирования.</span><span class="sxs-lookup"><span data-stu-id="3e918-130">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="3e918-131">Если это значение используется для указания типа кодирования вывода, \_ \_ вместо этого будет использоваться CAPICOM-Encoding Base64.</span><span class="sxs-lookup"><span data-stu-id="3e918-131">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="3e918-132">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="3e918-132">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="3e918-133"><dt>**CAPICOM \_ кодирует \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="3e918-133"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="3e918-134">Данные сохраняются в виде строки в кодировке Base64.</span><span class="sxs-lookup"><span data-stu-id="3e918-134">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="3e918-135"><dt>**\_двоичная кодировка CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e918-135"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="3e918-136">Данные сохраняются в виде чисто двоичной последовательности.</span><span class="sxs-lookup"><span data-stu-id="3e918-136">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e918-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e918-137">Return value</span></span>

<span data-ttu-id="3e918-138">Этот метод возвращает строку, содержащую закодированные подписанные данные.</span><span class="sxs-lookup"><span data-stu-id="3e918-138">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="3e918-139">В случае сбоя этого метода возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="3e918-139">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="3e918-140">Объект **Err** будет содержать дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3e918-140">The **Err** object will contain additional information about the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e918-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3e918-141">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3e918-142">При вызове этого метода из веб-скрипта скрипту необходимо использовать закрытый ключ для создания цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="3e918-142">When this method is called from a web script, the script needs to use your private key to create a digital signature.</span></span> <span data-ttu-id="3e918-143">Предоставление недоверенным веб-узлам использования закрытого ключа является угрозой безопасности.</span><span class="sxs-lookup"><span data-stu-id="3e918-143">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="3e918-144">Диалоговое окно с запросом на то, может ли веб-сайт использовать закрытый ключ при первом вызове этого метода.</span><span class="sxs-lookup"><span data-stu-id="3e918-144">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="3e918-145">Если вы разрешите скрипту использовать закрытый ключ для создания цифровой подписи и установите флажок "больше не показывать это окно", диалоговое окно больше не будет отображаться для любого скрипта в этом домене, который использует закрытый ключ для создания цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="3e918-145">If you allow the script to use your private key to create a digital signature and select "Do not show this dialog box again," the dialog box will no longer appear for any script within that domain that uses your private key to create a digital signature.</span></span> <span data-ttu-id="3e918-146">Однако скрипты за пределами этого домена, которые пытаются использовать закрытый ключ для создания цифровой подписи, все равно приведут к появлению этого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="3e918-146">However, scripts outside that domain that attempt to use your private key to create a digital signature will still cause this dialog box to appear.</span></span> <span data-ttu-id="3e918-147">Если вы не разрешите скрипту использовать закрытый ключ и установите флажок "больше не выводить это диалоговое окно", скрипты внутри этого домена автоматически не смогут использовать закрытый ключ для создания цифровых подписей.</span><span class="sxs-lookup"><span data-stu-id="3e918-147">If you do not allow the script to use your private key and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to use your private key to create digital signatures.</span></span>

 

<span data-ttu-id="3e918-148">Поскольку создание [*цифровой подписи*](../secgloss/d-gly.md) требует использования [*закрытого ключа*](../secgloss/p-gly.md), веб-приложения, которые пытаются использовать этот метод, потребуются запросы пользовательского интерфейса, позволяющие пользователю утверждать использование закрытого ключа по соображениям безопасности.</span><span class="sxs-lookup"><span data-stu-id="3e918-148">Because creating a [*digital signature*](../secgloss/d-gly.md) requires the use of a [*private key*](../secgloss/p-gly.md), web-based applications that attempt to use this method will require user interface prompts that allow the user to approve the use of the private key, for security reasons.</span></span>

<span data-ttu-id="3e918-149">Следующие результаты применяются к значению параметра *SignIn* :</span><span class="sxs-lookup"><span data-stu-id="3e918-149">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="3e918-150">Если параметр- *подписывающий* имеет значение, отличное от **null**, этот метод использует закрытый ключ, указанный в соответствующем сертификате, для шифрования подписи.</span><span class="sxs-lookup"><span data-stu-id="3e918-150">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the signature.</span></span> <span data-ttu-id="3e918-151">Если закрытый ключ, на который указывает сертификат, недоступен, метод завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="3e918-151">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="3e918-152">Если параметр- *подписывающий* имеет **значение NULL** и в хранилище текущего пользователя есть ровно один сертификат \_ с доступом к закрытому ключу, этот сертификат используется для создания подписи.</span><span class="sxs-lookup"><span data-stu-id="3e918-152">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key, that certificate is used to create the signature.</span></span>
-   <span data-ttu-id="3e918-153">Если параметр- *подписывающий* имеет значение **null**, то значением свойства [**Settings. енаблепромптфорцертификатеуи**](settings-enablepromptforcertificateui.md) является true, и в \_ хранилище текущего пользователя с доступным закрытым ключом существует несколько сертификатов. в этом случае появляется диалоговое окно, позволяющее пользователю выбрать используемый сертификат.</span><span class="sxs-lookup"><span data-stu-id="3e918-153">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="3e918-154">Если параметр- *подписывающий* имеет **значение NULL** , а свойство [**Settings. енаблепромптфорцертификатеуи**](settings-enablepromptforcertificateui.md) имеет значение false, то метод завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="3e918-154">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="3e918-155">Если параметр- *подписывающий* имеет **значение NULL** и в хранилище текущего пользователя нет сертификата \_ с доступным закрытым ключом, метод завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="3e918-155">If the *Signer* parameter is **NULL** and there is no certificate in the CURRENT\_USER MY store with an available private key, the method fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e918-156">Требования</span><span class="sxs-lookup"><span data-stu-id="3e918-156">Requirements</span></span>



| <span data-ttu-id="3e918-157">Требование</span><span class="sxs-lookup"><span data-stu-id="3e918-157">Requirement</span></span> | <span data-ttu-id="3e918-158">Значение</span><span class="sxs-lookup"><span data-stu-id="3e918-158">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e918-159">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="3e918-159">Redistributable</span></span><br/> | <span data-ttu-id="3e918-160">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e918-160">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3e918-161">DLL</span><span class="sxs-lookup"><span data-stu-id="3e918-161">DLL</span></span><br/>             | <dl> <span data-ttu-id="3e918-162"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e918-162"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e918-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e918-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e918-164">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="3e918-164">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="3e918-165">**сигнеддата**</span><span class="sxs-lookup"><span data-stu-id="3e918-165">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
