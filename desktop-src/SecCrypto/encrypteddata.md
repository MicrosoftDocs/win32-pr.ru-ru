---
description: Предоставляет свойства и методы для шифрования и расшифровки данных с помощью ключа сеанса, полученного из секрета.
ms.assetid: 3b9bd0a2-6e15-4d58-a682-588a93895799
title: Объект EncryptedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 123e0973343e4990dd2d49cfb321d739085358f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665179"
---
# <a name="encrypteddata-object"></a><span data-ttu-id="7adf6-103">Объект EncryptedData</span><span class="sxs-lookup"><span data-stu-id="7adf6-103">EncryptedData object</span></span>

<span data-ttu-id="7adf6-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7adf6-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7adf6-105">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций API Win32 [**криптенкриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) и [**криптдекриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) для шифрования и расшифровки сообщений.</span><span class="sxs-lookup"><span data-stu-id="7adf6-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="7adf6-106">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="7adf6-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="7adf6-107">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="7adf6-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="7adf6-108">Объект **EncryptedData** предоставляет свойства и методы для шифрования и расшифровки данных с помощью [*ключа сеанса*](../secgloss/s-gly.md) , полученного из секрета.</span><span class="sxs-lookup"><span data-stu-id="7adf6-108">The **EncryptedData** object provides properties and methods to encrypt and decrypt data using a [*session key*](../secgloss/s-gly.md) derived from a secret.</span></span>

> [!Note]  
> <span data-ttu-id="7adf6-109">CAPICOM не поддерживает \# тип содержимого EncryptedData, но использует нестандартную структуру ASN для **EncryptedData**.</span><span class="sxs-lookup"><span data-stu-id="7adf6-109">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a nonstandard ASN structure for **EncryptedData**.</span></span> <span data-ttu-id="7adf6-110">Таким образом, только CAPICOM может расшифровать объект CAPICOM **EncryptedData** .</span><span class="sxs-lookup"><span data-stu-id="7adf6-110">Therefore, only CAPICOM can decrypt a CAPICOM **EncryptedData** object.</span></span>

 

## <a name="members"></a><span data-ttu-id="7adf6-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="7adf6-111">Members</span></span>

<span data-ttu-id="7adf6-112">Объект **EncryptedData** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7adf6-112">The **EncryptedData** object has these types of members:</span></span>

-   [<span data-ttu-id="7adf6-113">Методы</span><span class="sxs-lookup"><span data-stu-id="7adf6-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="7adf6-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="7adf6-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7adf6-115">Методы</span><span class="sxs-lookup"><span data-stu-id="7adf6-115">Methods</span></span>

<span data-ttu-id="7adf6-116">Объект **EncryptedData** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="7adf6-116">The **EncryptedData** object has these methods.</span></span>



| <span data-ttu-id="7adf6-117">Метод</span><span class="sxs-lookup"><span data-stu-id="7adf6-117">Method</span></span>                                       | <span data-ttu-id="7adf6-118">Описание</span><span class="sxs-lookup"><span data-stu-id="7adf6-118">Description</span></span>                                                                             |
|:---------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="7adf6-119">**расшифровка;**</span><span class="sxs-lookup"><span data-stu-id="7adf6-119">**Decrypt**</span></span>](encrypteddata-decrypt.md)     | <span data-ttu-id="7adf6-120">Расшифровывает зашифрованное содержимое с использованием секрета.</span><span class="sxs-lookup"><span data-stu-id="7adf6-120">Decrypts encrypted content using the secret.</span></span><br/>                                 |
| [<span data-ttu-id="7adf6-121">**Шифрование**</span><span class="sxs-lookup"><span data-stu-id="7adf6-121">**Encrypt**</span></span>](encrypteddata-encrypt.md)     | <span data-ttu-id="7adf6-122">Шифрует содержимое с использованием текущего секрета и алгоритма шифрования.</span><span class="sxs-lookup"><span data-stu-id="7adf6-122">Encrypts the content using the current secret and encryption algorithm.</span></span><br/>      |
| [<span data-ttu-id="7adf6-123">**сетсекрет**</span><span class="sxs-lookup"><span data-stu-id="7adf6-123">**SetSecret**</span></span>](encrypteddata-setsecret.md) | <span data-ttu-id="7adf6-124">Задает секрет, который является производным ключом сеанса шифрования или расшифровки.</span><span class="sxs-lookup"><span data-stu-id="7adf6-124">Sets the secret from which the encryption/decryption session key is derived.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7adf6-125">Свойства</span><span class="sxs-lookup"><span data-stu-id="7adf6-125">Properties</span></span>

<span data-ttu-id="7adf6-126">Объект **EncryptedData** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="7adf6-126">The **EncryptedData** object has these properties.</span></span>



| <span data-ttu-id="7adf6-127">Свойство</span><span class="sxs-lookup"><span data-stu-id="7adf6-127">Property</span></span>                                                | <span data-ttu-id="7adf6-128">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="7adf6-128">Access type</span></span>           | <span data-ttu-id="7adf6-129">Описание</span><span class="sxs-lookup"><span data-stu-id="7adf6-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7adf6-130">**Алгоритм**</span><span class="sxs-lookup"><span data-stu-id="7adf6-130">**Algorithm**</span></span>](encrypteddata-algorithm.md)<br/> | <span data-ttu-id="7adf6-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7adf6-131">Read-only</span></span><br/>  | <span data-ttu-id="7adf6-132">Алгоритм, используемый для шифрования и расшифровки.</span><span class="sxs-lookup"><span data-stu-id="7adf6-132">Algorithm used for encryption/decryption.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="7adf6-133">**Содержани**</span><span class="sxs-lookup"><span data-stu-id="7adf6-133">**Content**</span></span>](encrypteddata-content.md)<br/>     | <span data-ttu-id="7adf6-134">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="7adf6-134">Read/write</span></span><br/> | <span data-ttu-id="7adf6-135">Содержимое для шифрования или расшифровки.</span><span class="sxs-lookup"><span data-stu-id="7adf6-135">The content to be encrypted or decrypted.</span></span> <span data-ttu-id="7adf6-136">Задание этого свойства должно выполняться до вызова метода [**Encrypt**](encrypteddata-encrypt.md) .</span><span class="sxs-lookup"><span data-stu-id="7adf6-136">Setting this property must be done before the [**Encrypt**](encrypteddata-encrypt.md) method is called.</span></span> <br/> <span data-ttu-id="7adf6-137">Если значение этого свойства сбрасывается прямо или косвенно, все [*состояние*](../secgloss/s-gly.md) объекта сбрасывается, а все зашифрованное содержимое объекта теряется.</span><span class="sxs-lookup"><span data-stu-id="7adf6-137">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span><br/> <span data-ttu-id="7adf6-138">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7adf6-138">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7adf6-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7adf6-139">Remarks</span></span>

<span data-ttu-id="7adf6-140">Объект **EncryptedData** можно создать и обеспечить безопасность сценариев.</span><span class="sxs-lookup"><span data-stu-id="7adf6-140">The **EncryptedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="7adf6-141">ProgID для объекта **EncryptedData** — CAPICOM. EncryptedData. 1.</span><span class="sxs-lookup"><span data-stu-id="7adf6-141">The ProgID for the **EncryptedData** object is CAPICOM.EncryptedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="7adf6-142">Требования</span><span class="sxs-lookup"><span data-stu-id="7adf6-142">Requirements</span></span>



| <span data-ttu-id="7adf6-143">Требование</span><span class="sxs-lookup"><span data-stu-id="7adf6-143">Requirement</span></span> | <span data-ttu-id="7adf6-144">Значение</span><span class="sxs-lookup"><span data-stu-id="7adf6-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7adf6-145">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7adf6-145">End of client support</span></span><br/> | <span data-ttu-id="7adf6-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7adf6-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7adf6-147">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="7adf6-147">End of server support</span></span><br/> | <span data-ttu-id="7adf6-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7adf6-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7adf6-149">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="7adf6-149">Redistributable</span></span><br/>       | <span data-ttu-id="7adf6-150">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="7adf6-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7adf6-151">DLL</span><span class="sxs-lookup"><span data-stu-id="7adf6-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7adf6-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7adf6-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7adf6-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7adf6-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7adf6-154">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="7adf6-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
