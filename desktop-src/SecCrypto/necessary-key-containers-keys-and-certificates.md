---
description: В примерах программ в следующих разделах выполняются операции, требующие, чтобы пары открытого и закрытого ключей были доступны для шифрования и расшифровки файлов, сообщений и подписей.
ms.assetid: b03528ff-0170-4dde-ae35-f5c3951d6b1f
title: Необходимые контейнеры ключей, ключи и сертификаты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d1f01a59c83ea21437608608e033a2ee0f8fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817641"
---
# <a name="necessary-key-containers-keys-and-certificates"></a><span data-ttu-id="1c2e6-103">Необходимые контейнеры ключей, ключи и сертификаты</span><span class="sxs-lookup"><span data-stu-id="1c2e6-103">Necessary Key Containers, Keys, and Certificates</span></span>

<span data-ttu-id="1c2e6-104">В примерах программ в следующих разделах выполняются операции, требующие, чтобы [*пары открытого и закрытого ключей*](../secgloss/p-gly.md) были доступны для шифрования и расшифровки файлов, сообщений и подписей.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-104">Example programs in the following sections perform operations that require [*public/private key pairs*](../secgloss/p-gly.md) to be available for encrypting and decrypting files, messages, and signatures.</span></span> <span data-ttu-id="1c2e6-105">Во время выполнения многие из этих программ компилируются, связываются и запускаются, но при этом не имеют соответствующих [*контейнеров ключей*](../secgloss/k-gly.md), ключей, [*хранилищ сертификатов*](../secgloss/c-gly.md)и сертификатов в этих хранилищах.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-105">Many of these programs will compile, link, and run but fail at run time without the existence of proper [*key containers*](../secgloss/k-gly.md), keys, [*certificate stores*](../secgloss/c-gly.md), and certificates in those stores.</span></span>

<span data-ttu-id="1c2e6-106">Кроме того, некоторые из сертификатов в хранилище MY должны иметь некоторые из своих расширенных свойств.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-106">In addition, some of the certificates in the MY store must have some of their extended properties set.</span></span>

<span data-ttu-id="1c2e6-107">Создание необходимого контейнера ключей по умолчанию можно выполнить, запустив программу в [примере программы на языке C: создание контейнера ключей и создание ключей](example-c-program-creating-a-key-container-and-generating-keys.md).</span><span class="sxs-lookup"><span data-stu-id="1c2e6-107">Creating the needed default key container can be done by running the program in [Example C Program: Creating a Key Container and Generating Keys](example-c-program-creating-a-key-container-and-generating-keys.md).</span></span> <span data-ttu-id="1c2e6-108">Обратите внимание, что при создании контейнера ключей не создаются автоматически пары открытого и закрытого ключей.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-108">Note that the creation of a key container does not automatically generate public/private key pairs.</span></span> <span data-ttu-id="1c2e6-109">Однако в примере программы создается контейнер ключей и создаются пары открытого и закрытого ключей.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-109">The example program, however, both creates the key container and generates the public/private key pairs.</span></span>

<span data-ttu-id="1c2e6-110">После создания пар открытого и закрытого ключей тестовые сертификаты, использующие эти ключи, можно получить из [*центра сертификации*](../secgloss/c-gly.md) (ЦС).</span><span class="sxs-lookup"><span data-stu-id="1c2e6-110">After public/private key pairs have been generated, test certificates using those keys can be obtained from a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="1c2e6-111">В некоторых программах предполагается, что сертификаты с конкретными именами субъектов существуют в моем системном хранилище.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-111">Several of the programs assume that certificates with specific subject names exist in the MY system store.</span></span> <span data-ttu-id="1c2e6-112">В частности, несколько программ ищут сертификаты с именами субъектов "полный тестовый сертификат" и "Хортенсе".</span><span class="sxs-lookup"><span data-stu-id="1c2e6-112">In particular, several programs look for certificates with the subject names "Full Test Cert" and "Hortense."</span></span> <span data-ttu-id="1c2e6-113">Имена субъектов для сертификатов могут быть изменены в коде в соответствии с именами субъектов сертификатов, которые существуют в хранилище сертификатов MY.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-113">The subject names for the certificates may be changed in the code to match the subject names of certificates that exist in the MY certificate store.</span></span>

<span data-ttu-id="1c2e6-114">Выполнение примера программы в [примере программы на языке C: вывод списка сертификатов в хранилище](example-c-program-listing-the-certificates-in-a-store.md) приведет к отображению всех сертификатов в хранилище и всех расширенных свойств, заданных для этих сертификатов.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-114">Running the example program in [Example C Program: Listing the Certificates in a Store](example-c-program-listing-the-certificates-in-a-store.md) will display all of the certificates in a store and all of the extended properties that are set on those certificates.</span></span>

 

 
