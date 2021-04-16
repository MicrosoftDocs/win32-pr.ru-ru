---
description: Криптксмл изначально поддерживает указанные ниже URI.
ms.assetid: 012bad01-228a-4bb0-b883-0c2c7abd9271
title: Алгоритмы шифрования цифровых подписей XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896348375d1d1a51288980aad3793dfffc69eb18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682697"
---
# <a name="xml-digital-signature-cryptographic-algorithms"></a><span data-ttu-id="3d851-103">Алгоритмы шифрования цифровых подписей XML</span><span class="sxs-lookup"><span data-stu-id="3d851-103">XML Digital Signature Cryptographic Algorithms</span></span>

<span data-ttu-id="3d851-104">Криптксмл изначально поддерживает указанные ниже URI.</span><span class="sxs-lookup"><span data-stu-id="3d851-104">CryptXML natively supports the URIs listed below.</span></span> <span data-ttu-id="3d851-105">Если для криптографических алгоритмов и преобразований, которые не являются частью встроенной поддержки, требуется поддержка, вы можете использовать криптографические [криптографические расширения](xml-digital-signature-cryptographic-extensions.md) [следующего поколения](../seccng/cng-portal.md) и XML для поддержки новых алгоритмов.</span><span class="sxs-lookup"><span data-stu-id="3d851-105">If support is required for cryptographic algorithms and transforms that are not part of the native support, you can use [Cryptography API: Next Generation](../seccng/cng-portal.md) and [XML Digital Signature Cryptographic Extensions](xml-digital-signature-cryptographic-extensions.md) to support new algorithms.</span></span>

## <a name="supported-uris"></a><span data-ttu-id="3d851-106">Поддерживаемые URI</span><span class="sxs-lookup"><span data-stu-id="3d851-106">Supported URIs</span></span>

<span data-ttu-id="3d851-107">Методы дайджеста</span><span class="sxs-lookup"><span data-stu-id="3d851-107">Digest Methods</span></span>



| <span data-ttu-id="3d851-108">Константа</span><span class="sxs-lookup"><span data-stu-id="3d851-108">Constant</span></span>                                 | <span data-ttu-id="3d851-109">Значение URI</span><span class="sxs-lookup"><span data-stu-id="3d851-109">URI value</span></span>                                                   |
|------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="3d851-110">Всзури \_ xmlns \_ дигсиг \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="3d851-110">wszURI\_XMLNS\_DIGSIG\_SHA1</span></span><br/>   | <span data-ttu-id="3d851-111">"https://www.w3.org/2000/09/xmldsig\#sha1"</span><span class="sxs-lookup"><span data-stu-id="3d851-111">"https://www.w3.org/2000/09/xmldsig\#sha1"</span></span><br/>        |
| <span data-ttu-id="3d851-112">Всзури \_ xmlns \_ дигсиг \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="3d851-112">wszURI\_XMLNS\_DIGSIG\_SHA256</span></span><br/> | <span data-ttu-id="3d851-113">"https://www.w3.org/2001/04/xmlenc\#sha256"</span><span class="sxs-lookup"><span data-stu-id="3d851-113">"https://www.w3.org/2001/04/xmlenc\#sha256"</span></span><br/>       |
| <span data-ttu-id="3d851-114">Всзури \_ xmlns \_ дигсиг \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="3d851-114">wszURI\_XMLNS\_DIGSIG\_SHA384</span></span><br/> | <span data-ttu-id="3d851-115">"https://www.w3.org/2001/04/xmldsig-more\#sha384"</span><span class="sxs-lookup"><span data-stu-id="3d851-115">"https://www.w3.org/2001/04/xmldsig-more\#sha384"</span></span><br/> |
| <span data-ttu-id="3d851-116">Всзури \_ xmlns \_ дигсиг \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="3d851-116">wszURI\_XMLNS\_DIGSIG\_SHA512</span></span><br/> | <span data-ttu-id="3d851-117">"https://www.w3.org/2001/04/xmlenc\#sha512"</span><span class="sxs-lookup"><span data-stu-id="3d851-117">"https://www.w3.org/2001/04/xmlenc\#sha512"</span></span><br/>       |



 

<span data-ttu-id="3d851-118">Методы подписи</span><span class="sxs-lookup"><span data-stu-id="3d851-118">Signature Methods</span></span>



| <span data-ttu-id="3d851-119">Константа</span><span class="sxs-lookup"><span data-stu-id="3d851-119">Constant</span></span>                                        | <span data-ttu-id="3d851-120">Значение URI</span><span class="sxs-lookup"><span data-stu-id="3d851-120">URI value</span></span>                                                         |
|-------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="3d851-121">Всзури \_ xmlns \_ дигсиг \_ RSA \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="3d851-121">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA1</span></span><br/>     | <span data-ttu-id="3d851-122">"https://www.w3.org/2000/09/xmldsig\#rsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="3d851-122">"https://www.w3.org/2000/09/xmldsig\#rsa-sha1"</span></span><br/>          |
| <span data-ttu-id="3d851-123">\_ \_ \_ SHA1 дигсиг DSA \_ всзури</span><span class="sxs-lookup"><span data-stu-id="3d851-123">wszURI\_XMLNS\_DIGSIG\_DSA\_SHA1</span></span><br/>     | <span data-ttu-id="3d851-124">"https://www.w3.org/2000/09/xmldsig\#dsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="3d851-124">"https://www.w3.org/2000/09/xmldsig\#dsa-sha1"</span></span><br/>          |
| <span data-ttu-id="3d851-125">Всзури \_ xmlns \_ дигсиг \_ RSA \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="3d851-125">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA256</span></span><br/>   | <span data-ttu-id="3d851-126">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha256"</span><span class="sxs-lookup"><span data-stu-id="3d851-126">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha256"</span></span><br/>   |
| <span data-ttu-id="3d851-127">Всзури \_ xmlns \_ дигсиг \_ RSA \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="3d851-127">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA384</span></span><br/>   | <span data-ttu-id="3d851-128">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha384"</span><span class="sxs-lookup"><span data-stu-id="3d851-128">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha384"</span></span><br/>   |
| <span data-ttu-id="3d851-129">Всзури \_ xmlns \_ дигсиг \_ RSA \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="3d851-129">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA512</span></span><br/>   | <span data-ttu-id="3d851-130">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha512"</span><span class="sxs-lookup"><span data-stu-id="3d851-130">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha512"</span></span><br/>   |
| <span data-ttu-id="3d851-131">Всзури \_ xmlns \_ дигсиг \_ ECDSA \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="3d851-131">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA1</span></span><br/>   | <span data-ttu-id="3d851-132">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="3d851-132">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha1"</span></span><br/>   |
| <span data-ttu-id="3d851-133">Всзури \_ xmlns \_ дигсиг \_ ECDSA \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="3d851-133">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA256</span></span><br/> | <span data-ttu-id="3d851-134">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha256"</span><span class="sxs-lookup"><span data-stu-id="3d851-134">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha256"</span></span><br/> |
| <span data-ttu-id="3d851-135">Всзури \_ xmlns \_ дигсиг \_ ECDSA \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="3d851-135">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA384</span></span><br/> | <span data-ttu-id="3d851-136">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha384"</span><span class="sxs-lookup"><span data-stu-id="3d851-136">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha384"</span></span><br/> |
| <span data-ttu-id="3d851-137">Всзури \_ xmlns \_ дигсиг \_ ECDSA \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="3d851-137">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA512</span></span><br/> | <span data-ttu-id="3d851-138">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha512"</span><span class="sxs-lookup"><span data-stu-id="3d851-138">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha512"</span></span><br/> |
| <span data-ttu-id="3d851-139">Всзури \_ xmlns \_ дигсиг \_ HMAC \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="3d851-139">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA1</span></span><br/>    | <span data-ttu-id="3d851-140">"https://www.w3.org/2000/09/xmldsig\#hmac-sha1"</span><span class="sxs-lookup"><span data-stu-id="3d851-140">"https://www.w3.org/2000/09/xmldsig\#hmac-sha1"</span></span><br/>         |
| <span data-ttu-id="3d851-141">Всзури \_ xmlns \_ дигсиг \_ HMAC \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="3d851-141">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA256</span></span><br/>  | <span data-ttu-id="3d851-142">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha256"</span><span class="sxs-lookup"><span data-stu-id="3d851-142">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha256"</span></span><br/>  |
| <span data-ttu-id="3d851-143">Всзури \_ xmlns \_ дигсиг \_ HMAC \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="3d851-143">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA384</span></span><br/>  | <span data-ttu-id="3d851-144">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha384"</span><span class="sxs-lookup"><span data-stu-id="3d851-144">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha384"</span></span><br/>  |
| <span data-ttu-id="3d851-145">Всзури \_ xmlns \_ дигсиг \_ HMAC \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="3d851-145">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA512</span></span><br/>  | <span data-ttu-id="3d851-146">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha512"</span><span class="sxs-lookup"><span data-stu-id="3d851-146">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha512"</span></span><br/>  |



 

 

 
