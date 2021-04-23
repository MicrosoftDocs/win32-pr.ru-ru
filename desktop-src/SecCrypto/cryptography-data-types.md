---
description: Для криптографических функций, интерфейсов и объектов используются следующие типы данных.
ms.assetid: 9d6a065d-c765-4d17-9f4c-38a984439278
title: Типы данных шифрования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f84c6f21faa25e1ccc478c178a3f21458ff589ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662317"
---
# <a name="cryptography-data-types"></a><span data-ttu-id="0db5a-103">Типы данных шифрования</span><span class="sxs-lookup"><span data-stu-id="0db5a-103">Cryptography Data Types</span></span>

<span data-ttu-id="0db5a-104">Для криптографических функций, интерфейсов и объектов используются следующие типы данных.</span><span class="sxs-lookup"><span data-stu-id="0db5a-104">The following data types are used by cryptography functions, interfaces, and objects.</span></span>



| <span data-ttu-id="0db5a-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0db5a-105">Data type</span></span>                                                                      | <span data-ttu-id="0db5a-106">Описание</span><span class="sxs-lookup"><span data-stu-id="0db5a-106">Description</span></span>                                                                                                                                                                                      |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0db5a-107">**Идентификатор АЛГОРИТМа \_**</span><span class="sxs-lookup"><span data-stu-id="0db5a-107">**ALG\_ID**</span></span>](alg-id.md)                                                      | <span data-ttu-id="0db5a-108">Указывает идентификаторы алгоритма.</span><span class="sxs-lookup"><span data-stu-id="0db5a-108">Specifies algorithm identifiers.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="0db5a-109">**\_ \_ ответ OCSP сервера \_ хцерт**</span><span class="sxs-lookup"><span data-stu-id="0db5a-109">**HCERT\_SERVER\_OCSP\_RESPONSE**</span></span>](hcert-server-ocsp-response.md)            | <span data-ttu-id="0db5a-110">Представляет маркер ответа OCSP, связанного с цепочкой сертификатов сервера.</span><span class="sxs-lookup"><span data-stu-id="0db5a-110">Represents a handle to an OCSP response associated with a server certificate chain.</span></span>                                                                                                              |
| [<span data-ttu-id="0db5a-111">**хкрипсаш**</span><span class="sxs-lookup"><span data-stu-id="0db5a-111">**HCRYPTHASH**</span></span>](hcrypthash.md)                                               | <span data-ttu-id="0db5a-112">Задает дескрипторы для [*хэш-объекта*](../secgloss/h-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0db5a-112">Specifies handles to a [*hash object*](../secgloss/h-gly.md).</span></span>                                                                                      |
| [<span data-ttu-id="0db5a-113">**хкрипткэй**</span><span class="sxs-lookup"><span data-stu-id="0db5a-113">**HCRYPTKEY**</span></span>](hcryptkey.md)                                                 | <span data-ttu-id="0db5a-114">Задает дескрипторы криптографических ключей.</span><span class="sxs-lookup"><span data-stu-id="0db5a-114">Specifies handles to cryptographic keys.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="0db5a-115">**хкриптоидфункаддр**</span><span class="sxs-lookup"><span data-stu-id="0db5a-115">**HCRYPTOIDFUNCADDR**</span></span>](hcryptoidfuncaddr.md)                                 | <span data-ttu-id="0db5a-116">Представляет обработчик функции, которая может быть установлена с помощью [*идентификатора объекта*](../secgloss/o-gly.md) (OID).</span><span class="sxs-lookup"><span data-stu-id="0db5a-116">Represents a handle to a function that can be installed by using an [*object identifier*](../secgloss/o-gly.md) (OID).</span></span>                 |
| [<span data-ttu-id="0db5a-117">**хкриптоидфунксет**</span><span class="sxs-lookup"><span data-stu-id="0db5a-117">**HCRYPTOIDFUNCSET**</span></span>](hcryptoidfuncset.md)                                   | <span data-ttu-id="0db5a-118">Представляет обработчик для набора функций, которые могут быть установлены с помощью OID.</span><span class="sxs-lookup"><span data-stu-id="0db5a-118">Represents a handle to a set of functions that can be installed by using an OID.</span></span>                                                                                                                 |
| [<span data-ttu-id="0db5a-119">**ХКРИПТПРОВ, \_ устаревший**</span><span class="sxs-lookup"><span data-stu-id="0db5a-119">**HCRYPTPROV\_LEGACY**</span></span>](hcryptprov-legacy.md)                                | <span data-ttu-id="0db5a-120">Используется для замены типа данных [**хкриптпров**](hcryptprov.md) , в котором тип данных **хкриптпров** больше не используется.</span><span class="sxs-lookup"><span data-stu-id="0db5a-120">Used to replace the [**HCRYPTPROV**](hcryptprov.md) data type where the **HCRYPTPROV** data type is no longer used.</span></span>                                                                             |
| [<span data-ttu-id="0db5a-121">**\_ \_ \_ маркер ключа хкриптпров или \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="0db5a-121">**HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE**</span></span>](hcryptprov-or-ncrypt-key-handle.md) | <span data-ttu-id="0db5a-122">Указывает маркер для [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP) CRYPTOAPI или CSP CNG.</span><span class="sxs-lookup"><span data-stu-id="0db5a-122">Specifies a handle to a CryptoAPI [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or CNG CSP.</span></span> |
| [<span data-ttu-id="0db5a-123">**хкриптпров**</span><span class="sxs-lookup"><span data-stu-id="0db5a-123">**HCRYPTPROV**</span></span>](hcryptprov.md)                                               | <span data-ttu-id="0db5a-124">Задает маркер для поставщика служб CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="0db5a-124">Specifies a handle to a CryptoAPI CSP.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="0db5a-125">**КЭЙСВКК, \_ обработчик**</span><span class="sxs-lookup"><span data-stu-id="0db5a-125">**KEYSVCC\_HANDLE**</span></span>](keysvcc-handle.md)                                      | <span data-ttu-id="0db5a-126">Задает дескрипторы для службы ключей.</span><span class="sxs-lookup"><span data-stu-id="0db5a-126">Specifies handles to the key service.</span></span>                                                                                                                                                            |



 

 

 
