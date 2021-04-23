---
description: Исходный базовый поставщик неправильно сообщил о том, что хэш-алгоритм SHA перечислит алгоритмы, выполнив вызовы Криптжетпровпарам с параметром PP \_ енумалгс.
ms.assetid: 75128a4f-273a-4195-b206-30fc8bc589e9
title: Функциональность SHA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8a06ce5c11dfaa00e2ec7ee3427dfda2f8b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808320"
---
# <a name="sha-functionality"></a><span data-ttu-id="9ed43-103">Функциональность SHA</span><span class="sxs-lookup"><span data-stu-id="9ed43-103">SHA Functionality</span></span>

<span data-ttu-id="9ed43-104">Исходный базовый поставщик неправильно сообщил о том, что хэш-алгоритм [*SHA*](../secgloss/s-gly.md) перечислит алгоритмы, выполнив вызовы [**криптжетпровпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) с параметром PP \_ енумалгс.</span><span class="sxs-lookup"><span data-stu-id="9ed43-104">The original Base Provider incorrectly reported that the [*SHA*](../secgloss/s-gly.md) hash algorithm enumerating algorithms by calls to [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with parameter PP\_ENUMALGS specified.</span></span> <span data-ttu-id="9ed43-105">Это было исправлено в базовом поставщике.</span><span class="sxs-lookup"><span data-stu-id="9ed43-105">This has been fixed in the Base Provider.</span></span> <span data-ttu-id="9ed43-106">Измененный базовый поставщик и расширенный поставщик, и теперь правильно сообщает о SHA-1.</span><span class="sxs-lookup"><span data-stu-id="9ed43-106">Both the revised Base Provider and the Extended Provider and now correctly report SHA-1.</span></span>

<span data-ttu-id="9ed43-107">В \_ винкрипт. h была добавлена определенная константа SHA1 калг с тем же значением, что и в калг \_ SHA.</span><span class="sxs-lookup"><span data-stu-id="9ed43-107">A defined CALG\_SHA1 constant has been added to Wincrypt.h with the same value as CALG\_SHA.</span></span>

 

 
