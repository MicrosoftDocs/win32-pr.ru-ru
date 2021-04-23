---
description: Извлекает ключ сеанса из секрета и шифрует значение свойства содержимого с помощью этого ключа. Он возвращает зашифрованное содержимое в виде закодированной строки.
ms.assetid: aa6f6e6a-208b-4e9c-b530-08673ab9d794
title: Метод EncryptedData. Encrypt (InfoCard. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 04d7bf8a337c1bcfa0a024b84304fe50c035f9dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665181"
---
# <a name="encrypteddataencrypt-method"></a><span data-ttu-id="6b62b-104">Метод EncryptedData. Encrypt</span><span class="sxs-lookup"><span data-stu-id="6b62b-104">EncryptedData.Encrypt method</span></span>

<span data-ttu-id="6b62b-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6b62b-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6b62b-106">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций API Win32 [**криптенкриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) и [**криптдекриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) для шифрования и расшифровки сообщений.</span><span class="sxs-lookup"><span data-stu-id="6b62b-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="6b62b-107">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="6b62b-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="6b62b-108">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="6b62b-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="6b62b-109">Метод **Encrypt** наследует ключ сеанса от секрета и шифрует значение свойства [**Content**](encrypteddata-content.md) с помощью этого ключа.</span><span class="sxs-lookup"><span data-stu-id="6b62b-109">The **Encrypt** method derives a session key from the secret and encrypts the [**Content**](encrypteddata-content.md) property value using that key.</span></span> <span data-ttu-id="6b62b-110">Он возвращает зашифрованное содержимое в виде закодированной строки.</span><span class="sxs-lookup"><span data-stu-id="6b62b-110">It returns the encrypted content as an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b62b-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b62b-111">Syntax</span></span>


```VB
EncryptedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="6b62b-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b62b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b62b-113">*Енкодингтипе* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="6b62b-113">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6b62b-114">Значение перечисления типа " [**CAPICOM \_ Encoding \_**](capicom-encoding-type.md) ", которое указывает тип кодировки, используемый для кодирования зашифрованных данных.</span><span class="sxs-lookup"><span data-stu-id="6b62b-114">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the encoding type used to encode the encrypted data.</span></span> <span data-ttu-id="6b62b-115">Значение по умолчанию — CAPICOM- \_ кодировать \_ Base64.</span><span class="sxs-lookup"><span data-stu-id="6b62b-115">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="6b62b-116">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="6b62b-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="6b62b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6b62b-117">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="6b62b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6b62b-118">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="6b62b-119"><dt>**CAPICOM \_ кодирует \_ ANY**</dt></span><span class="sxs-lookup"><span data-stu-id="6b62b-119"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="6b62b-120">Этот тип кодирования используется только в том случае, если входные данные имеют неизвестный тип кодирования.</span><span class="sxs-lookup"><span data-stu-id="6b62b-120">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="6b62b-121">Если это значение используется для указания типа кодирования вывода, \_ \_ вместо этого будет использоваться CAPICOM-Encoding Base64.</span><span class="sxs-lookup"><span data-stu-id="6b62b-121">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="6b62b-122">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="6b62b-122">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="6b62b-123"><dt>**CAPICOM \_ кодирует \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="6b62b-123"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="6b62b-124">Данные сохраняются в виде строки в кодировке Base64.</span><span class="sxs-lookup"><span data-stu-id="6b62b-124">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="6b62b-125"><dt>**\_двоичная кодировка CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6b62b-125"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="6b62b-126">Данные сохраняются в виде чисто двоичной последовательности.</span><span class="sxs-lookup"><span data-stu-id="6b62b-126">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b62b-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b62b-127">Return value</span></span>

<span data-ttu-id="6b62b-128">Строка, содержащая зашифрованные закодированные данные.</span><span class="sxs-lookup"><span data-stu-id="6b62b-128">A string that contains the encrypted, encoded data.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b62b-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b62b-129">Remarks</span></span>

<span data-ttu-id="6b62b-130">Перед вызовом метода **Encrypt** задайте свойство [**Content**](encrypteddata-content.md) и вызовите метод [**сетсекрет**](encrypteddata-setsecret.md) .</span><span class="sxs-lookup"><span data-stu-id="6b62b-130">Before calling the **Encrypt** method, set the [**Content**](encrypteddata-content.md) property and call the [**SetSecret**](encrypteddata-setsecret.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b62b-131">Требования</span><span class="sxs-lookup"><span data-stu-id="6b62b-131">Requirements</span></span>



| <span data-ttu-id="6b62b-132">Требование</span><span class="sxs-lookup"><span data-stu-id="6b62b-132">Requirement</span></span> | <span data-ttu-id="6b62b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="6b62b-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b62b-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="6b62b-134">End of client support</span></span><br/> | <span data-ttu-id="6b62b-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b62b-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6b62b-136">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="6b62b-136">End of server support</span></span><br/> | <span data-ttu-id="6b62b-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b62b-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6b62b-138">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="6b62b-138">Redistributable</span></span><br/>       | <span data-ttu-id="6b62b-139">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="6b62b-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6b62b-140">Header</span><span class="sxs-lookup"><span data-stu-id="6b62b-140">Header</span></span><br/>                | <dl> <span data-ttu-id="6b62b-141"><dt>InfoCard. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b62b-141"><dt>Infocard.h</dt></span></span> </dl>  |
| <span data-ttu-id="6b62b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6b62b-142">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6b62b-143"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b62b-143"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b62b-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b62b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b62b-145">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="6b62b-145">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="6b62b-146">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="6b62b-146">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
