---
description: Расшифровывает содержимое, упакованное в оболочку.
ms.assetid: 717d0595-e8bb-4725-bd53-fc1281cbc8ee
title: Енвелопеддата. дешифровки, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0c4c71ba0e3e0c2d421ad7bcbc9b1a61bb71d284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648715"
---
# <a name="envelopeddatadecrypt-method"></a><span data-ttu-id="c07b0-103">Енвелопеддата. дешифровки, метод</span><span class="sxs-lookup"><span data-stu-id="c07b0-103">EnvelopedData.Decrypt method</span></span>

<span data-ttu-id="c07b0-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c07b0-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c07b0-105">Вместо этого используйте [**класс EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="c07b0-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="c07b0-106">Метод **дешифровки** расшифровывает содержимое, упакованное в оболочку.</span><span class="sxs-lookup"><span data-stu-id="c07b0-106">The **Decrypt** method decrypts enveloped content.</span></span> <span data-ttu-id="c07b0-107">Расшифровка выполняется, если получатель сообщения имеет доступ к [*закрытому ключу*](../secgloss/p-gly.md) , связанному с одним из [*открытых ключей*](../secgloss/p-gly.md) , используемых для учетом неизбежного увеличения сообщения.</span><span class="sxs-lookup"><span data-stu-id="c07b0-107">Decryption is done if the recipient of the message has access to the [*private key*](../secgloss/p-gly.md) paired with one of the [*public keys*](../secgloss/p-gly.md) used to envelop the message.</span></span> <span data-ttu-id="c07b0-108">Вызов метода **дешифровки** сбрасывает [*состояние*](../secgloss/s-gly.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="c07b0-108">Calling the **Decrypt** method resets the [*state*](../secgloss/s-gly.md) of the object.</span></span> <span data-ttu-id="c07b0-109">Если метод **дешифровки** выполнен, свойство [**Content**](envelopeddata-content.md) объекта [**енвелопеддата**](envelopeddata.md) устанавливается в сообщение с открытым текстом.</span><span class="sxs-lookup"><span data-stu-id="c07b0-109">If the **Decrypt** method succeeds, the [**Content**](envelopeddata-content.md) property of the [**EnvelopedData**](envelopeddata.md) object is set to the plaintext message.</span></span>

## <a name="syntax"></a><span data-ttu-id="c07b0-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c07b0-110">Syntax</span></span>


```VB
EnvelopedData.Decrypt( _
  ByVal EnvelopedMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="c07b0-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="c07b0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c07b0-112">*Енвелопедмессаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c07b0-112">*EnvelopedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c07b0-113">Строка, содержащая запечатанные данные для расшифровки.</span><span class="sxs-lookup"><span data-stu-id="c07b0-113">String that contains the enveloped data to be decrypted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c07b0-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c07b0-114">Return value</span></span>

<span data-ttu-id="c07b0-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c07b0-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c07b0-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c07b0-116">Remarks</span></span>

<span data-ttu-id="c07b0-117">Расшифрованные данные становятся значением свойства [**содержимого**](envelopeddata-content.md) для объекта [**енвелопеддата**](envelopeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="c07b0-117">The decrypted data becomes the [**Content**](envelopeddata-content.md) property value for the [**EnvelopedData**](envelopeddata.md) object.</span></span>

<span data-ttu-id="c07b0-118">Если у пользователя этого метода нет доступа к закрытому ключу, который соответствует одному из открытых ключей, используемых для учетом неизбежного увеличения сообщения, метод завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="c07b0-118">If the user of this method does not have access to a private key that matches one of the public keys used to envelop the message, the method fails.</span></span> <span data-ttu-id="c07b0-119">Этот метод завершится ошибкой, если сертификат для связанного закрытого ключа находится не на локальном компьютере MY Store или текущем пользователе MY Store.</span><span class="sxs-lookup"><span data-stu-id="c07b0-119">This method will fail if the certificate for the associated private key is not in either the local computer MY store or the current user MY store.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c07b0-120">При вызове этого метода из веб-скрипта скрипту необходимо использовать [*закрытый ключ*](../secgloss/p-gly.md) для расшифровки данных.</span><span class="sxs-lookup"><span data-stu-id="c07b0-120">When this method is called from a web script, the script needs to use your [*private key*](../secgloss/p-gly.md) to decrypt the data.</span></span> <span data-ttu-id="c07b0-121">Предоставление недоверенным веб-узлам использования закрытого ключа является угрозой безопасности.</span><span class="sxs-lookup"><span data-stu-id="c07b0-121">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="c07b0-122">Диалоговое окно с запросом на то, может ли веб-сайт использовать закрытый ключ при первом вызове этого метода.</span><span class="sxs-lookup"><span data-stu-id="c07b0-122">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="c07b0-123">Если вы разрешите скрипту использовать закрытый ключ и установите флажок "больше не спрашивать", диалоговое окно больше не будет отображаться для сценариев, использующих закрытый ключ для расшифровки данных внутри этого домена.</span><span class="sxs-lookup"><span data-stu-id="c07b0-123">If you allow the script to use your private key and select "Do not ask me this again," the dialog box will no longer appear for any script that uses your private key to decrypt data within that domain.</span></span> <span data-ttu-id="c07b0-124">Однако скрипты за пределами этого домена, которые пытаются использовать закрытый ключ для расшифровки данных, все равно приведут к появлению этого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="c07b0-124">However, scripts outside that domain that attempt to use your private key to decrypt data will still cause this dialog box to appear.</span></span> <span data-ttu-id="c07b0-125">Если вы не разрешите скрипту использовать закрытый ключ и установите флажок "больше не спрашивать, скрипты внутри этого домена автоматически не смогут использовать закрытый ключ для расшифровки данных.</span><span class="sxs-lookup"><span data-stu-id="c07b0-125">If you do not allow the script to use your private key and select "Do not ask me this again," scripts within that domain will automatically be refused the ability to use your private key to decrypt data.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c07b0-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c07b0-126">Requirements</span></span>



| <span data-ttu-id="c07b0-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c07b0-127">Requirement</span></span> | <span data-ttu-id="c07b0-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c07b0-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c07b0-129">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c07b0-129">End of client support</span></span><br/> | <span data-ttu-id="c07b0-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c07b0-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c07b0-131">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="c07b0-131">End of server support</span></span><br/> | <span data-ttu-id="c07b0-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c07b0-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c07b0-133">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="c07b0-133">Redistributable</span></span><br/>       | <span data-ttu-id="c07b0-134">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="c07b0-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c07b0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c07b0-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c07b0-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c07b0-136"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c07b0-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c07b0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c07b0-138">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="c07b0-138">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="c07b0-139">**енвелопеддата**</span><span class="sxs-lookup"><span data-stu-id="c07b0-139">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
