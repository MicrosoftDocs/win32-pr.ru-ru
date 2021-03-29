---
description: Расшифровывает зашифрованную и закодированную строку данных.
ms.assetid: 7601083d-0adb-48e1-98a7-804a49f71206
title: Метод EncryptedData. дешифровки
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aa702a5cefc46f6d0cbe5d7e0fba17ff03596b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647973"
---
# <a name="encrypteddatadecrypt-method"></a><span data-ttu-id="e8bcb-103">Метод EncryptedData. дешифровки</span><span class="sxs-lookup"><span data-stu-id="e8bcb-103">EncryptedData.Decrypt method</span></span>

<span data-ttu-id="e8bcb-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e8bcb-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e8bcb-105">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций API Win32 [**криптенкриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) и [**криптдекриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) для шифрования и расшифровки сообщений.</span><span class="sxs-lookup"><span data-stu-id="e8bcb-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="e8bcb-106">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="e8bcb-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="e8bcb-107">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="e8bcb-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="e8bcb-108">Метод **дешифровки** расшифровывает зашифрованную и закодированную строку данных.</span><span class="sxs-lookup"><span data-stu-id="e8bcb-108">The **Decrypt** method decrypts an encrypted and encoded data string.</span></span> <span data-ttu-id="e8bcb-109">Результирующие данные в виде открытого текста становятся свойством [**Content**](encrypteddata-content.md) объекта [**EncryptedData**](encrypteddata.md) .</span><span class="sxs-lookup"><span data-stu-id="e8bcb-109">The resulting plaintext data becomes the [**Content**](encrypteddata-content.md) property of the [**EncryptedData**](encrypteddata.md) object.</span></span> <span data-ttu-id="e8bcb-110">Расшифровка содержимого завершается ошибкой, если только секрет, заданный методом [**сетсекрет**](encrypteddata-setsecret.md) , точно совпадает с секретом, используемым для получения ключа, используемого для шифрования содержимого.</span><span class="sxs-lookup"><span data-stu-id="e8bcb-110">Decryption of the content fails unless the secret, set by the [**SetSecret**](encrypteddata-setsecret.md) method, is exactly the same as the secret used to derive the key used to encrypt the content.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8bcb-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8bcb-111">Syntax</span></span>


```VB
EncryptedData.Decrypt( _
  ByVal EncryptedMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="e8bcb-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8bcb-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8bcb-113">*Енкриптедмессаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8bcb-113">*EncryptedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8bcb-114">Строка, содержащая закодированные зашифрованные данные для расшифровки.</span><span class="sxs-lookup"><span data-stu-id="e8bcb-114">String that contains the encoded, encrypted data to be decrypted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8bcb-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8bcb-115">Return value</span></span>

<span data-ttu-id="e8bcb-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e8bcb-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8bcb-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8bcb-117">Remarks</span></span>

<span data-ttu-id="e8bcb-118">Ключ сеанса, полученный из текущего секрета, используется для расшифровки.</span><span class="sxs-lookup"><span data-stu-id="e8bcb-118">The session key derived from the current secret is used for the decryption.</span></span> <span data-ttu-id="e8bcb-119">Этот метод не будет создавать правильный открытый текст, если только текущий секрет не совпадает с секретом, используемым для шифрования сообщения.</span><span class="sxs-lookup"><span data-stu-id="e8bcb-119">This method will not produce the correct plaintext unless the current secret exactly matches the secret used to encrypt the message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8bcb-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e8bcb-120">Requirements</span></span>



| <span data-ttu-id="e8bcb-121">Требование</span><span class="sxs-lookup"><span data-stu-id="e8bcb-121">Requirement</span></span> | <span data-ttu-id="e8bcb-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e8bcb-122">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8bcb-123">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e8bcb-123">End of client support</span></span><br/> | <span data-ttu-id="e8bcb-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8bcb-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e8bcb-125">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="e8bcb-125">End of server support</span></span><br/> | <span data-ttu-id="e8bcb-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8bcb-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e8bcb-127">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="e8bcb-127">Redistributable</span></span><br/>       | <span data-ttu-id="e8bcb-128">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="e8bcb-128">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e8bcb-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e8bcb-129">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e8bcb-130"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8bcb-130"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8bcb-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8bcb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8bcb-132">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="e8bcb-132">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="e8bcb-133">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="e8bcb-133">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
