---
description: С помощью функций хэширования и цифровой подписи пользователь может подписать данные цифровой подписью, чтобы любой другой пользователь мог проверить, что данные не были изменены с момента подписания. Также можно проверить подлинность пользователя, подписавшего данные.
ms.assetid: dbe70506-f0d9-4239-a3af-8494fd6d4149
title: Хэши и Цифровые подписи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc2894cbf53834551afef375fb5056df89675a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664125"
---
# <a name="hashes-and-digital-signatures"></a><span data-ttu-id="4da37-104">Хэши и Цифровые подписи</span><span class="sxs-lookup"><span data-stu-id="4da37-104">Hashes and Digital Signatures</span></span>

<span data-ttu-id="4da37-105">С помощью [функций хэширования и цифровой подписи](cryptography-functions.md)пользователь может подписать данные цифровой подписью, чтобы любой другой пользователь мог проверить, что данные не были изменены с момента подписания.</span><span class="sxs-lookup"><span data-stu-id="4da37-105">With [Hash and Digital Signature Functions](cryptography-functions.md), a user can digitally sign data so that any other user can verify that the data has not been changed since it was signed.</span></span> <span data-ttu-id="4da37-106">Также можно проверить подлинность пользователя, подписавшего данные.</span><span class="sxs-lookup"><span data-stu-id="4da37-106">The identity of the user who signed the data can also be verified.</span></span>

<span data-ttu-id="4da37-107">[*Цифровая подпись*](../secgloss/d-gly.md) состоит из небольшого объема двоичных данных, обычно менее 256 байт.</span><span class="sxs-lookup"><span data-stu-id="4da37-107">A [*digital signature*](../secgloss/d-gly.md) consists of a small amount of binary data, typically less than 256 bytes.</span></span> <span data-ttu-id="4da37-108">Эту подпись можно объединить с подписанным сообщением или хранить отдельно, в зависимости от того, как было реализовано конкретное приложение.</span><span class="sxs-lookup"><span data-stu-id="4da37-108">This signature can be bundled with the signed message or stored separately, depending on how a particular application has been implemented.</span></span>

<span data-ttu-id="4da37-109">Поставщик строгой криптографии Майкрософт создает цифровые подписи, которые соответствуют [*стандартам шифрования открытого ключа*](../secgloss/p-gly.md) RSA (PKCS) \# 1.</span><span class="sxs-lookup"><span data-stu-id="4da37-109">The Microsoft Strong Cryptographic Provider creates digital signatures that conform to the RSA [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \#1.</span></span>

 

 
