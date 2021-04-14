---
description: Объект Енвелопеддата предоставляет свойства и методы для учетом неизбежного увеличения данных о конфиденциальности с помощью шифрования.
ms.assetid: 7c5f3e3d-6a70-455d-8921-20495eec4b3e
title: Объект Енвелопеддата
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e5309061c6ab315a089a1e1d8b9488556cae9f31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648142"
---
# <a name="envelopeddata-object"></a><span data-ttu-id="1db4d-103">Объект Енвелопеддата</span><span class="sxs-lookup"><span data-stu-id="1db4d-103">EnvelopedData object</span></span>

<span data-ttu-id="1db4d-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1db4d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="1db4d-105">Вместо этого используйте [**класс EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="1db4d-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="1db4d-106">Объект **енвелопеддата** предоставляет свойства и методы для учетом неизбежного увеличения данных о конфиденциальности с помощью шифрования.</span><span class="sxs-lookup"><span data-stu-id="1db4d-106">The **EnvelopedData** object provides properties and methods to envelop data for privacy by encryption.</span></span> <span data-ttu-id="1db4d-107">Для учетом неизбежного увеличения данных создается криптографический ключ сеанса.</span><span class="sxs-lookup"><span data-stu-id="1db4d-107">To envelop data, a session cryptographic key is generated.</span></span> <span data-ttu-id="1db4d-108">Затем этот [*ключ сеанса*](../secgloss/s-gly.md) шифруется для каждого предполагаемого получателя с помощью [*открытого ключа*](../secgloss/p-gly.md) этого получателя из сертификата получателя.</span><span class="sxs-lookup"><span data-stu-id="1db4d-108">That [*session key*](../secgloss/s-gly.md) is then encrypted for each intended recipient using the [*public key*](../secgloss/p-gly.md) of that intended recipient from the recipient's certificate.</span></span> <span data-ttu-id="1db4d-109">Зашифрованные данные и набор зашифрованных ключей сеанса можно отправить всем получателям.</span><span class="sxs-lookup"><span data-stu-id="1db4d-109">The encrypted data and the set of encrypted session keys can be sent to all intended recipients.</span></span> <span data-ttu-id="1db4d-110">Созданное сообщение находится в \# формате PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="1db4d-110">The message generated is in PKCS \#7 format.</span></span>

## <a name="members"></a><span data-ttu-id="1db4d-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="1db4d-111">Members</span></span>

<span data-ttu-id="1db4d-112">Объект **енвелопеддата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1db4d-112">The **EnvelopedData** object has these types of members:</span></span>

-   [<span data-ttu-id="1db4d-113">Методы</span><span class="sxs-lookup"><span data-stu-id="1db4d-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="1db4d-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="1db4d-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1db4d-115">Методы</span><span class="sxs-lookup"><span data-stu-id="1db4d-115">Methods</span></span>

<span data-ttu-id="1db4d-116">Объект **енвелопеддата** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="1db4d-116">The **EnvelopedData** object has these methods.</span></span>



| <span data-ttu-id="1db4d-117">Метод</span><span class="sxs-lookup"><span data-stu-id="1db4d-117">Method</span></span>                                   | <span data-ttu-id="1db4d-118">Описание</span><span class="sxs-lookup"><span data-stu-id="1db4d-118">Description</span></span>                                                                                                 |
|:-----------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1db4d-119">**расшифровка;**</span><span class="sxs-lookup"><span data-stu-id="1db4d-119">**Decrypt**</span></span>](envelopeddata-decrypt.md) | <span data-ttu-id="1db4d-120">Расшифровывает содержимое, упакованное в оболочку.</span><span class="sxs-lookup"><span data-stu-id="1db4d-120">Decrypts enveloped content.</span></span><br/>                                                                      |
| [<span data-ttu-id="1db4d-121">**Шифрование**</span><span class="sxs-lookup"><span data-stu-id="1db4d-121">**Encrypt**</span></span>](envelopeddata-encrypt.md) | <span data-ttu-id="1db4d-122">Шифрует содержимое, шифрует сеансовый ключ для каждого получателя и возвращает зашифрованный большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="1db4d-122">Encrypts the content, encrypts a session key for each recipient, and returns the encrypted BLOB.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1db4d-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="1db4d-123">Properties</span></span>

<span data-ttu-id="1db4d-124">Объект **енвелопеддата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1db4d-124">The **EnvelopedData** object has these properties.</span></span>



| <span data-ttu-id="1db4d-125">Свойство</span><span class="sxs-lookup"><span data-stu-id="1db4d-125">Property</span></span>                                                  | <span data-ttu-id="1db4d-126">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="1db4d-126">Access type</span></span>           | <span data-ttu-id="1db4d-127">Описание</span><span class="sxs-lookup"><span data-stu-id="1db4d-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:----------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1db4d-128">**Алгоритм**</span><span class="sxs-lookup"><span data-stu-id="1db4d-128">**Algorithm**</span></span>](envelopeddata-algorithm.md)<br/>   | <span data-ttu-id="1db4d-129">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="1db4d-129">Read/write</span></span><br/> | <span data-ttu-id="1db4d-130">Алгоритм шифрования и [*Длина ключа*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1db4d-130">Encryption algorithm and [*key length*](../secgloss/k-gly.md).</span></span><br/>                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="1db4d-131">**Содержани**</span><span class="sxs-lookup"><span data-stu-id="1db4d-131">**Content**</span></span>](envelopeddata-content.md)<br/>       | <span data-ttu-id="1db4d-132">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="1db4d-132">Read/write</span></span><br/> | <span data-ttu-id="1db4d-133">Содержимое открытого текста сообщения, которое должно быть запечатано.</span><span class="sxs-lookup"><span data-stu-id="1db4d-133">The plaintext content of a message to be enveloped.</span></span> <span data-ttu-id="1db4d-134">Задание этого свойства должно выполняться до вызова метода [**Encrypt**](envelopeddata-encrypt.md) .</span><span class="sxs-lookup"><span data-stu-id="1db4d-134">Setting this property must be done before the [**Encrypt**](envelopeddata-encrypt.md) method is called.</span></span><br/> <span data-ttu-id="1db4d-135">Если значение этого свойства сбрасывается прямо или косвенно, все [*состояние*](../secgloss/s-gly.md) объекта сбрасывается, а все зашифрованное содержимое объекта теряется.</span><span class="sxs-lookup"><span data-stu-id="1db4d-135">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span><br/> <span data-ttu-id="1db4d-136">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1db4d-136">This is the default property.</span></span><br/> |
| [<span data-ttu-id="1db4d-137">**Recipients**</span><span class="sxs-lookup"><span data-stu-id="1db4d-137">**Recipients**</span></span>](envelopeddata-recipients.md)<br/> | <span data-ttu-id="1db4d-138">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1db4d-138">Read-only</span></span><br/>  | <span data-ttu-id="1db4d-139">Коллекция объектов [**сертификатов**](certificate.md) для получения сообщения, упакованного в оболочку.</span><span class="sxs-lookup"><span data-stu-id="1db4d-139">Collection of [**Certificate**](certificate.md) objects to receive the enveloped message.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="1db4d-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1db4d-140">Remarks</span></span>

<span data-ttu-id="1db4d-141">Объект **енвелопеддата** может быть создан и защищен для создания скриптов.</span><span class="sxs-lookup"><span data-stu-id="1db4d-141">The **EnvelopedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="1db4d-142">ProgID для объекта **енвелопеддата** — CAPICOM. Енвелопеддата. 1.</span><span class="sxs-lookup"><span data-stu-id="1db4d-142">The ProgID for the **EnvelopedData** object is CAPICOM.EnvelopedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="1db4d-143">Требования</span><span class="sxs-lookup"><span data-stu-id="1db4d-143">Requirements</span></span>



| <span data-ttu-id="1db4d-144">Требование</span><span class="sxs-lookup"><span data-stu-id="1db4d-144">Requirement</span></span> | <span data-ttu-id="1db4d-145">Значение</span><span class="sxs-lookup"><span data-stu-id="1db4d-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1db4d-146">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="1db4d-146">End of client support</span></span><br/> | <span data-ttu-id="1db4d-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1db4d-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1db4d-148">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="1db4d-148">End of server support</span></span><br/> | <span data-ttu-id="1db4d-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1db4d-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1db4d-150">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="1db4d-150">Redistributable</span></span><br/>       | <span data-ttu-id="1db4d-151">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="1db4d-151">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1db4d-152">DLL</span><span class="sxs-lookup"><span data-stu-id="1db4d-152">DLL</span></span><br/>                   | <dl> <span data-ttu-id="1db4d-153"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1db4d-153"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1db4d-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1db4d-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1db4d-155">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="1db4d-155">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
