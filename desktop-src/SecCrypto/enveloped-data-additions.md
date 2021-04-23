---
description: Перечисляет изменения возможностей для данных запечатывание.
ms.assetid: b025a9c6-d6a3-40b2-9b7f-1e6caa706b59
title: Добавленные в оболочку данные
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360cc7cb6a65853ae6c23bb995df94566d0adc09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662855"
---
# <a name="enveloped-data-additions"></a><span data-ttu-id="1a0bd-103">Добавленные в оболочку данные</span><span class="sxs-lookup"><span data-stu-id="1a0bd-103">Enveloped Data Additions</span></span>

<span data-ttu-id="1a0bd-104">В функции запечатанных данных были внесены следующие изменения:</span><span class="sxs-lookup"><span data-stu-id="1a0bd-104">The following changes have been made to enveloped data capabilities:</span></span>

-   <span data-ttu-id="1a0bd-105">Идентификация получателей может выполняться не только издателем и серийным номером (PKCS \# 7 1,5), но и идентификатором ключа.</span><span class="sxs-lookup"><span data-stu-id="1a0bd-105">Recipient identification can be done not only by Issuer and Serial Number (PKCS \#7 1.5), but also by Key Identifier.</span></span>
-   <span data-ttu-id="1a0bd-106">Предоставляются три варианта обмена ключами получателей:</span><span class="sxs-lookup"><span data-stu-id="1a0bd-106">Three recipient key exchange choices are provided:</span></span>
    -   <span data-ttu-id="1a0bd-107">Передача ключей с помощью ключей RSA.</span><span class="sxs-lookup"><span data-stu-id="1a0bd-107">Key Transport using RSA keys.</span></span>
    -   <span data-ttu-id="1a0bd-108">Ключевое соглашение использует Ephemeral-Static Diffie-Hellman ключи алгоритмов, заключенные в оболочку 3DES или RC2, или Ephemeral-Static алгоритмы эллиптической кривой Diffie-Hellman, инкапсулированные с помощью AES.</span><span class="sxs-lookup"><span data-stu-id="1a0bd-108">Key Agreement using either Ephemeral-Static Diffie-Hellman algorithm keys wrapped with 3DES or RC2, or Ephemeral-Static Elliptic Curve Diffie-Hellman algorithm keys wrapped with AES.</span></span>
    -   <span data-ttu-id="1a0bd-109">Перенос ключа шифрования ключей или списка рассылки, когда ключ, используемый для шифрования ключа шифрования содержимого, уже был передан получателям.</span><span class="sxs-lookup"><span data-stu-id="1a0bd-109">Key Encryption Key or Mail List key transfer where the key used to encrypt the content encryption key has already been distributed to the recipients.</span></span> <span data-ttu-id="1a0bd-110">В качестве алгоритмов подписывания ключа могут использоваться RC2, 3DES и AES.</span><span class="sxs-lookup"><span data-stu-id="1a0bd-110">RC2, 3DES and AES are allowed as key-wrapping algorithms.</span></span>
-   <span data-ttu-id="1a0bd-111">В сообщение можно включить незащищенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="1a0bd-111">Unprotected attributes can be included in the message.</span></span>
-   <span data-ttu-id="1a0bd-112">Добавленное поле **оригинаторинфо** , содержащее сведения об инициаторе, которое может содержать сертификаты и списки отзыва сертификатов.</span><span class="sxs-lookup"><span data-stu-id="1a0bd-112">An **OriginatorInfo** field that contains information about the originator has been added that can contain certificates and CRLs.</span></span>
-   <span data-ttu-id="1a0bd-113">Для алгоритмов с шифрованием на основе эллиптических кривых (ECC) и AES требуется Windows Vista или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="1a0bd-113">Elliptic Curve Cryptography (ECC) based algorithms and AES require Windows Vista or later.</span></span>

 

 



