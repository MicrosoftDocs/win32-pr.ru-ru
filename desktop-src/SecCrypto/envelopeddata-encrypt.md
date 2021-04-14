---
description: Создание ключа сеанса и шифрование данных и конвертов.
ms.assetid: 7ae0c908-207b-4a74-a195-d12e9e7dec76
title: Енвелопеддата. Encrypt, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ecdb665a8e70ff329f25398eb855ff3e82c96cfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648143"
---
# <a name="envelopeddataencrypt-method"></a><span data-ttu-id="7cd6e-103">Енвелопеддата. Encrypt, метод</span><span class="sxs-lookup"><span data-stu-id="7cd6e-103">EnvelopedData.Encrypt method</span></span>

<span data-ttu-id="7cd6e-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7cd6e-105">Вместо этого используйте [**класс EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="7cd6e-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="7cd6e-106">Метод **Encrypt** создает ключ сеанса, использует этот ключ для шифрования содержимого, енвелопс зашифрованное содержимое для каждого получателя путем шифрования ключа сеанса с помощью открытого ключа получателя, а затем возвращает [*большой двоичный объект*](../secgloss/b-gly.md) , содержащий зашифрованное содержимое и зашифрованные ключи сеанса в виде закодированной строки.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-106">The **Encrypt** method generates a session key, uses that key to encrypt the contents, envelops the encrypted content for each recipient by encrypting the session key with each recipient's public key, and then returns the [*BLOB*](../secgloss/b-gly.md) that contains the encrypted contents and the encrypted session keys as an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd6e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cd6e-107">Syntax</span></span>


```VB
EnvelopedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7cd6e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7cd6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cd6e-109">*Енкодингтипе* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="7cd6e-109">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd6e-110">Значение перечисления типа " [**CAPICOM \_ Encoding \_**](capicom-encoding-type.md) ", которое указывает тип кодировки, используемый для кодирования данных, упакованных в оболочку.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-110">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the encoding type used to encode the enveloped data.</span></span> <span data-ttu-id="7cd6e-111">Значение кодировки по умолчанию — CAPICOM- \_ кодировать \_ Base64.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-111">The default encoding value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="7cd6e-112">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="7cd6e-113">Значение</span><span class="sxs-lookup"><span data-stu-id="7cd6e-113">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="7cd6e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7cd6e-114">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="7cd6e-115"><dt>**CAPICOM \_ кодирует \_ ANY**</dt></span><span class="sxs-lookup"><span data-stu-id="7cd6e-115"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="7cd6e-116">Этот тип кодирования используется только в том случае, если входные данные имеют неизвестный тип кодирования.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-116">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="7cd6e-117">Если это значение используется для указания типа кодирования вывода, \_ \_ вместо этого будет использоваться CAPICOM-Encoding Base64.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-117">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="7cd6e-118">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-118">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="7cd6e-119"><dt>**CAPICOM \_ кодирует \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="7cd6e-119"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="7cd6e-120">Данные сохраняются в виде строки в кодировке Base64.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-120">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="7cd6e-121"><dt>**\_двоичная кодировка CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7cd6e-121"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="7cd6e-122">Данные сохраняются в виде чисто двоичной последовательности.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-122">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cd6e-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7cd6e-123">Return value</span></span>

<span data-ttu-id="7cd6e-124">Этот метод возвращает большой двоичный объект, содержащий запечатанные данные в закодированной строке.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-124">This method returns a BLOB that contains the enveloped data in an encoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cd6e-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7cd6e-125">Remarks</span></span>

<span data-ttu-id="7cd6e-126">Возвращенный BLOB-объект содержит зашифрованное содержимое и зашифрованный ключ сеанса для каждого предполагаемого получателя.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-126">The returned BLOB contains the encrypted content and an encrypted session key for each intended recipient.</span></span> <span data-ttu-id="7cd6e-127">Эти сеансовые ключи шифруются с помощью открытого ключа каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-127">These session keys are encrypted using the public key of each recipient.</span></span> <span data-ttu-id="7cd6e-128">Зашифрованные ключи сеанса можно расшифровать только с помощью закрытого ключа получателя.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-128">The encrypted session keys can be decrypted only with a recipient's private key.</span></span>

<span data-ttu-id="7cd6e-129">Если свойство [**Recipients**](envelopeddata-recipients.md) не содержит никаких сведений, этот метод выполняет поиск потенциальных получателей в хранилище сертификатов AddressBook текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-129">If the [**Recipients**](envelopeddata-recipients.md) property does not contain any information, this method searches the current user's AddressBook certificate store for potential recipients.</span></span> <span data-ttu-id="7cd6e-130">Если найдено несколько потенциальных получателей, пользователю предлагается выбрать получателя в диалоговом окне выбора.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-130">If more than one potential recipient is found, the user is prompted to select a recipient from a selection dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cd6e-131">Требования</span><span class="sxs-lookup"><span data-stu-id="7cd6e-131">Requirements</span></span>



| <span data-ttu-id="7cd6e-132">Требование</span><span class="sxs-lookup"><span data-stu-id="7cd6e-132">Requirement</span></span> | <span data-ttu-id="7cd6e-133">Значение</span><span class="sxs-lookup"><span data-stu-id="7cd6e-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd6e-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7cd6e-134">End of client support</span></span><br/> | <span data-ttu-id="7cd6e-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7cd6e-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7cd6e-136">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="7cd6e-136">End of server support</span></span><br/> | <span data-ttu-id="7cd6e-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7cd6e-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7cd6e-138">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="7cd6e-138">Redistributable</span></span><br/>       | <span data-ttu-id="7cd6e-139">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="7cd6e-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7cd6e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="7cd6e-140">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7cd6e-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cd6e-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cd6e-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7cd6e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cd6e-143">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="7cd6e-143">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="7cd6e-144">**енвелопеддата**</span><span class="sxs-lookup"><span data-stu-id="7cd6e-144">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
