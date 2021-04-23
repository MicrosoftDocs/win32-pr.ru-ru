---
description: Перечисляет изменения в возможностях подписанных данных.
ms.assetid: 0518a336-d996-4a82-9336-a448284c72dd
title: Добавление подписанных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19bfc242072f82afcf0877d713a3437e797f24d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539831"
---
# <a name="signed-data-additions"></a><span data-ttu-id="e790e-103">Добавление подписанных данных</span><span class="sxs-lookup"><span data-stu-id="e790e-103">Signed Data Additions</span></span>

<span data-ttu-id="e790e-104">В возможности подписанных данных были внесены следующие изменения.</span><span class="sxs-lookup"><span data-stu-id="e790e-104">The following changes have been made to signed data capabilities:</span></span>

-   <span data-ttu-id="e790e-105">[*Внутреннее содержимое*](../secgloss/i-gly.md) , не связанное с данными, инкапсулируется в строку октета.</span><span class="sxs-lookup"><span data-stu-id="e790e-105">Nondata [*inner content*](../secgloss/i-gly.md) is encapsulated in an OCTET STRING.</span></span>
-   <span data-ttu-id="e790e-106">Для разных версий сообщений выполняется подготавливается.</span><span class="sxs-lookup"><span data-stu-id="e790e-106">Provision is made for different message versions.</span></span>
-   <span data-ttu-id="e790e-107">Подписавшие можно идентифицировать по издателю и серийному номеру, как в PKCS \# 7 1,5 или с помощью идентификатора ключа субъекта.</span><span class="sxs-lookup"><span data-stu-id="e790e-107">Signers can be identified either by Issuer and Serial Number, as in PKCS \#7 1.5, or by Subject key identifier.</span></span>
-   <span data-ttu-id="e790e-108">Разрешено несколько подписывающих.</span><span class="sxs-lookup"><span data-stu-id="e790e-108">Multiple signers are allowed.</span></span>
-   <span data-ttu-id="e790e-109">Допускается использование подписей RSA, DSA и ECDSA.</span><span class="sxs-lookup"><span data-stu-id="e790e-109">Both RSA, DSA, and ECDSA signatures are allowed.</span></span>
-   <span data-ttu-id="e790e-110">Для алгоритмов с шифрованием на основе эллиптических кривых (ECC) и AES требуется Windows Vista или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="e790e-110">Elliptic Curve Cryptography (ECC) based algorithms and AES require Windows Vista or later.</span></span>

 

 
