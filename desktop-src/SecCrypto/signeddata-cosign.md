---
description: Создает цифровую подпись для ранее подписанного содержимого.
ms.assetid: c0a3de75-afba-45ba-b701-2729f4495eda
title: Сигнеддата. кознаковый метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.CoSign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1ab2a24a20fd65fad9622b775bedc59cfa28301a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669313"
---
# <a name="signeddatacosign-method"></a><span data-ttu-id="84d07-103">Сигнеддата. кознаковый метод</span><span class="sxs-lookup"><span data-stu-id="84d07-103">SignedData.CoSign method</span></span>

<span data-ttu-id="84d07-104">\[Метод **подписывания** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="84d07-104">\[The **CoSign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="84d07-105">Вместо этого используйте [**класс SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="84d07-105">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="84d07-106">Метод **подписывания** создает [*цифровую подпись*](../secgloss/d-gly.md) для ранее подписанного содержимого.</span><span class="sxs-lookup"><span data-stu-id="84d07-106">The **CoSign** method creates a [*digital signature*](../secgloss/d-gly.md) on previously signed content.</span></span>

## <a name="syntax"></a><span data-ttu-id="84d07-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84d07-107">Syntax</span></span>


```VB
SignedData.CoSign( _
  [ ByVal Signer ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="84d07-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="84d07-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84d07-109">*Подписавший* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="84d07-109">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="84d07-110">Ссылка на объект- [**подписывающий**](signer.md) подписи данных.</span><span class="sxs-lookup"><span data-stu-id="84d07-110">A reference to the [**Signer**](signer.md) object of the signer of the data.</span></span> <span data-ttu-id="84d07-111">Объект " **подписавший** " должен иметь доступ к закрытому ключу сертификата, используемого для подписания.</span><span class="sxs-lookup"><span data-stu-id="84d07-111">The **Signer** object must have access to the private key of the certificate used to sign.</span></span> <span data-ttu-id="84d07-112">Этот параметр может иметь **значение NULL**. Дополнительные сведения см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="84d07-112">This parameter can be **NULL**; for more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="84d07-113">*Енкодингтипе* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="84d07-113">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="84d07-114">Значение перечисления типа " [**CAPICOM \_ Encoding \_**](capicom-encoding-type.md) ", указывающее способ кодирования подписанных данных.</span><span class="sxs-lookup"><span data-stu-id="84d07-114">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates how the signed data is to be encoded.</span></span> <span data-ttu-id="84d07-115">Значение по умолчанию — CAPICOM- \_ кодировать \_ Base64.</span><span class="sxs-lookup"><span data-stu-id="84d07-115">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="84d07-116">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="84d07-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="84d07-117">Значение</span><span class="sxs-lookup"><span data-stu-id="84d07-117">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="84d07-118">Значение</span><span class="sxs-lookup"><span data-stu-id="84d07-118">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="84d07-119"><dt>**CAPICOM \_ кодирует \_ ANY**</dt></span><span class="sxs-lookup"><span data-stu-id="84d07-119"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="84d07-120">Этот тип кодирования используется только в том случае, если входные данные имеют неизвестный тип кодирования.</span><span class="sxs-lookup"><span data-stu-id="84d07-120">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="84d07-121">Если это значение используется для указания типа кодирования вывода, \_ \_ вместо этого будет использоваться CAPICOM-Encoding Base64.</span><span class="sxs-lookup"><span data-stu-id="84d07-121">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="84d07-122">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="84d07-122">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="84d07-123"><dt>**CAPICOM \_ кодирует \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="84d07-123"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="84d07-124">Данные сохраняются в виде строки в кодировке Base64.</span><span class="sxs-lookup"><span data-stu-id="84d07-124">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="84d07-125"><dt>**\_двоичная кодировка CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="84d07-125"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="84d07-126">Данные сохраняются в виде чисто двоичной последовательности.</span><span class="sxs-lookup"><span data-stu-id="84d07-126">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84d07-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84d07-127">Return value</span></span>

<span data-ttu-id="84d07-128">Этот метод возвращает строку, содержащую закодированные подписанные данные.</span><span class="sxs-lookup"><span data-stu-id="84d07-128">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="84d07-129">В случае сбоя этого метода возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="84d07-129">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="84d07-130">Объект **Err** будет содержать дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="84d07-130">The **Err** object will contain additional information about the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="84d07-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84d07-131">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="84d07-132">При вызове этого метода из веб-скрипта скрипту необходимо использовать [*закрытый ключ*](../secgloss/p-gly.md) для создания цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="84d07-132">When this method is called from a web script, the script needs to use your [*private key*](../secgloss/p-gly.md) to create a digital signature.</span></span> <span data-ttu-id="84d07-133">Предоставление недоверенным веб-узлам использования закрытого ключа является угрозой безопасности.</span><span class="sxs-lookup"><span data-stu-id="84d07-133">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="84d07-134">Диалоговое окно с запросом на то, может ли веб-сайт использовать закрытый ключ при первом вызове этого метода.</span><span class="sxs-lookup"><span data-stu-id="84d07-134">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="84d07-135">Если вы разрешите скрипту использовать закрытый ключ для создания цифровой подписи и установите флажок "больше не показывать это окно", диалоговое окно больше не будет отображаться для любого скрипта в этом домене, который использует закрытый ключ для создания цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="84d07-135">If you allow the script to use your private key to create a digital signature and select "Do not show this dialog box again," the dialog box will no longer appear for any script within that domain that uses your private key to create a digital signature.</span></span> <span data-ttu-id="84d07-136">Однако скрипты за пределами этого домена, которые пытаются использовать закрытый ключ для создания цифровой подписи, все равно приведут к появлению этого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="84d07-136">However, scripts outside that domain that attempt to use your private key to create a digital signature will still cause this dialog box to appear.</span></span> <span data-ttu-id="84d07-137">Если вы не разрешите скрипту использовать закрытый ключ и установите флажок "больше не выводить это диалоговое окно", скрипты внутри этого домена автоматически не смогут использовать закрытый ключ для создания цифровых подписей.</span><span class="sxs-lookup"><span data-stu-id="84d07-137">If you do not allow the script to use your private key and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to use your private key to create digital signatures.</span></span>

 

<span data-ttu-id="84d07-138">Подписывание не гарантируется в каком бы то ни было определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="84d07-138">Cosigners are not guaranteed to be in any particular order.</span></span>

<span data-ttu-id="84d07-139">Следующие результаты применяются к значению параметра *SignIn* :</span><span class="sxs-lookup"><span data-stu-id="84d07-139">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="84d07-140">Если параметр- *подписывающий* имеет значение, отличное от **null**, этот метод использует закрытый ключ, на который указывает соответствующий сертификат, для шифрования сосигнатуры.</span><span class="sxs-lookup"><span data-stu-id="84d07-140">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the cosignature.</span></span> <span data-ttu-id="84d07-141">Если закрытый ключ, на который указывает сертификат, недоступен, метод завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="84d07-141">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="84d07-142">Если параметр- *подписывающий* имеет **значение NULL** и в хранилище текущего пользователя есть ровно один сертификат \_ с доступом к закрытому ключу, этот сертификат используется для создания соподписи.</span><span class="sxs-lookup"><span data-stu-id="84d07-142">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key, that certificate is used to create the cosignature.</span></span>
-   <span data-ttu-id="84d07-143">Если параметр- *подписывающий* имеет значение **null**, то значением свойства [**Settings. енаблепромптфорцертификатеуи**](settings-enablepromptforcertificateui.md) является true, и в \_ хранилище текущего пользователя с доступным закрытым ключом существует несколько сертификатов. в этом случае появляется диалоговое окно, позволяющее пользователю выбрать используемый сертификат.</span><span class="sxs-lookup"><span data-stu-id="84d07-143">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="84d07-144">Если параметр- *подписывающий* имеет **значение NULL** , а свойство [**Settings. енаблепромптфорцертификатеуи**](settings-enablepromptforcertificateui.md) имеет значение false, то метод завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="84d07-144">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="84d07-145">Если параметр- *подписывающий* имеет **значение NULL** и в хранилище текущего пользователя нет сертификата \_ с доступным закрытым ключом, метод завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="84d07-145">If the *Signer* parameter is **NULL** and there is no certificate in the CURRENT\_USER MY store with an available private key, the method fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="84d07-146">Требования</span><span class="sxs-lookup"><span data-stu-id="84d07-146">Requirements</span></span>



| <span data-ttu-id="84d07-147">Требование</span><span class="sxs-lookup"><span data-stu-id="84d07-147">Requirement</span></span> | <span data-ttu-id="84d07-148">Значение</span><span class="sxs-lookup"><span data-stu-id="84d07-148">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="84d07-149">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="84d07-149">Redistributable</span></span><br/> | <span data-ttu-id="84d07-150">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="84d07-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="84d07-151">DLL</span><span class="sxs-lookup"><span data-stu-id="84d07-151">DLL</span></span><br/>             | <dl> <span data-ttu-id="84d07-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84d07-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84d07-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84d07-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84d07-154">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="84d07-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="84d07-155">**сигнеддата**</span><span class="sxs-lookup"><span data-stu-id="84d07-155">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
