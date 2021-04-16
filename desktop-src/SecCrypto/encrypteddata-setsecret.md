---
description: Задает значение секрета, используемого для получения криптографического ключа сеанса, используемого для шифрования и расшифровки данных.
ms.assetid: d940ae0b-a697-4529-b494-0051b9a6db5e
title: Метод EncryptedData. Сетсекрет
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.SetSecret
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c8d30355b022a593ca17519e3ccfa876a5b07b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665180"
---
# <a name="encrypteddatasetsecret-method"></a><span data-ttu-id="5f548-103">Метод EncryptedData. Сетсекрет</span><span class="sxs-lookup"><span data-stu-id="5f548-103">EncryptedData.SetSecret method</span></span>

<span data-ttu-id="5f548-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5f548-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="5f548-105">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций API Win32 [**криптенкриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) и [**криптдекриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) для шифрования и расшифровки сообщений.</span><span class="sxs-lookup"><span data-stu-id="5f548-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="5f548-106">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="5f548-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="5f548-107">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="5f548-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="5f548-108">Метод **сетсекрет** задает значение секрета, используемого для получения криптографического [*ключа сеанса*](../secgloss/s-gly.md) , используемого для шифрования и расшифровки данных.</span><span class="sxs-lookup"><span data-stu-id="5f548-108">The **SetSecret** method sets the value of the secret used to derive the cryptographic [*session key*](../secgloss/s-gly.md) used to encrypt and decrypt data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f548-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f548-109">Syntax</span></span>


```VB
EncryptedData.SetSecret( _
  ByVal newVal, _
  [ ByVal SecretType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="5f548-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f548-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f548-111">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5f548-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f548-112">Строка, содержащая секрет, используемый для создания криптографического ключа сеанса.</span><span class="sxs-lookup"><span data-stu-id="5f548-112">A string that contains a secret used to create a session cryptographic key.</span></span>

</dd> <dt>

<span data-ttu-id="5f548-113">*Секреттипе* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5f548-113">*SecretType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5f548-114">Значение перечисления [**типа CAPICOM- \_ Secret \_**](capicom-secret-type.md) , указывающее тип секрета, используемого для создания ключа сеанса.</span><span class="sxs-lookup"><span data-stu-id="5f548-114">A value of the [**CAPICOM\_SECRET\_TYPE**](capicom-secret-type.md) enumeration that indicates the kind of secret used to generate the session key.</span></span> <span data-ttu-id="5f548-115">Значение по умолчанию — \_ пароль CAPICOM Secret \_ .</span><span class="sxs-lookup"><span data-stu-id="5f548-115">The default value is CAPICOM\_SECRET\_PASSWORD.</span></span> <span data-ttu-id="5f548-116">Этот параметр может иметь следующее значение.</span><span class="sxs-lookup"><span data-stu-id="5f548-116">This parameter can be the following value.</span></span>



| <span data-ttu-id="5f548-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5f548-117">Value</span></span>                                                                                                                                                                                        | <span data-ttu-id="5f548-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5f548-118">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="CAPICOM_SECRET_PASSWORD"></span><span id="capicom_secret_password"></span><dl> <span data-ttu-id="5f548-119"><dt>**\_пароль для секрета CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f548-119"><dt>**CAPICOM\_SECRET\_PASSWORD**</dt></span></span> </dl> | <span data-ttu-id="5f548-120">Ключ шифрования должен быть производным от пароля.</span><span class="sxs-lookup"><span data-stu-id="5f548-120">The encryption key is to be derived from a password.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f548-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f548-121">Return value</span></span>

<span data-ttu-id="5f548-122">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5f548-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f548-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5f548-123">Remarks</span></span>

<span data-ttu-id="5f548-124">Секрет используется для создания ключа сеанса для шифрования или расшифровки.</span><span class="sxs-lookup"><span data-stu-id="5f548-124">The secret is used to create the session key for encryption or decryption.</span></span> <span data-ttu-id="5f548-125">Для обеих операций необходимо использовать один и тот же секрет.</span><span class="sxs-lookup"><span data-stu-id="5f548-125">The same secret must be used for both operations.</span></span> <span data-ttu-id="5f548-126">Если секрет, используемый для шифрования данных, потерян, зашифрованные данные не могут быть расшифрованы.</span><span class="sxs-lookup"><span data-stu-id="5f548-126">If the secret used to encrypt data is lost, the encrypted data cannot be decrypted.</span></span>

<span data-ttu-id="5f548-127">Если это необходимо для вашего приложения, рассмотрите возможность использования [**криптпротектмемори**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) или [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) для защиты секрета до и после использования.</span><span class="sxs-lookup"><span data-stu-id="5f548-127">If appropriate for your application, consider using [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) or [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) to protect the secret before and after use.</span></span> <span data-ttu-id="5f548-128">По завершении очистите память, связанную с секретом.</span><span class="sxs-lookup"><span data-stu-id="5f548-128">Clear the memory associated with the secret when done.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f548-129">Требования</span><span class="sxs-lookup"><span data-stu-id="5f548-129">Requirements</span></span>



| <span data-ttu-id="5f548-130">Требование</span><span class="sxs-lookup"><span data-stu-id="5f548-130">Requirement</span></span> | <span data-ttu-id="5f548-131">Значение</span><span class="sxs-lookup"><span data-stu-id="5f548-131">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f548-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="5f548-132">End of client support</span></span><br/> | <span data-ttu-id="5f548-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f548-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5f548-134">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="5f548-134">End of server support</span></span><br/> | <span data-ttu-id="5f548-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f548-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5f548-136">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="5f548-136">Redistributable</span></span><br/>       | <span data-ttu-id="5f548-137">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="5f548-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5f548-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5f548-138">DLL</span></span><br/>                   | <dl> <span data-ttu-id="5f548-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f548-139"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f548-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f548-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f548-141">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="5f548-141">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="5f548-142">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="5f548-142">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
