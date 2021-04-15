---
description: Описывает процедуру, используемую для хранения ключа сеанса.
ms.assetid: 9ab7f747-9c69-40b5-af78-163f3ba315bf
title: Сохранение ключа сеанса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b17de657ddba47dd77f68c1ee7a2adfdf93e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683498"
---
# <a name="storing-a-session-key"></a><span data-ttu-id="8a4e3-103">Сохранение ключа сеанса</span><span class="sxs-lookup"><span data-stu-id="8a4e3-103">Storing a Session Key</span></span>

> [!Note]  
> <span data-ttu-id="8a4e3-104">В этом разделе предполагается, что пользователи обладают набором [*пар открытого и закрытого ключей*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8a4e3-104">This section assumes that users possess a set of [*public/private key pairs*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="8a4e3-105">Инструкции и пример создания пар ключей можно найти в [примере программы на языке C: создание контейнера ключей и создание ключей](example-c-program-creating-a-key-container-and-generating-keys.md).</span><span class="sxs-lookup"><span data-stu-id="8a4e3-105">Instructions and an example for creating key pairs can be found in [Example C Program: Creating a Key Container and Generating Keys](example-c-program-creating-a-key-container-and-generating-keys.md).</span></span>

 

<span data-ttu-id="8a4e3-106">**Сохранение ключа сеанса**</span><span class="sxs-lookup"><span data-stu-id="8a4e3-106">**To store a session key**</span></span>

1.  <span data-ttu-id="8a4e3-107">Создайте [*большой двоичный объект простого ключа*](../secgloss/k-gly.md) с помощью функции [**криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) .</span><span class="sxs-lookup"><span data-stu-id="8a4e3-107">Create a simple [*key BLOB*](../secgloss/k-gly.md) by using the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function.</span></span> <span data-ttu-id="8a4e3-108">Это приведет к переносу ключа сеанса из CSP в пространство памяти приложения.</span><span class="sxs-lookup"><span data-stu-id="8a4e3-108">This will transfer the session key from the CSP to an application's memory space.</span></span> <span data-ttu-id="8a4e3-109">Укажите, что для подписи ключевого BLOB-объекта используется открытый ключ Exchange.</span><span class="sxs-lookup"><span data-stu-id="8a4e3-109">Specify that an exchange public key be used to sign the key BLOB.</span></span>
2.  <span data-ttu-id="8a4e3-110">Сохраните большой двоичный объект подписанного ключа на диск.</span><span class="sxs-lookup"><span data-stu-id="8a4e3-110">Store the signed key BLOB to disk.</span></span> <span data-ttu-id="8a4e3-111">Предполагается, что все диски являются небезопасными.</span><span class="sxs-lookup"><span data-stu-id="8a4e3-111">It is assumed that all disks are nonsecure.</span></span>
3.  <span data-ttu-id="8a4e3-112">При необходимости Прочитайте ключ большого двоичного объекта с диска.</span><span class="sxs-lookup"><span data-stu-id="8a4e3-112">When the key is needed, read the key BLOB from disk.</span></span>
4.  <span data-ttu-id="8a4e3-113">Импортируйте большой двоичный объект ключа обратно в CSP с помощью функции [**криптимпорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) .</span><span class="sxs-lookup"><span data-stu-id="8a4e3-113">Import the key BLOB back into the CSP by using the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function.</span></span>

<span data-ttu-id="8a4e3-114">Пример создания [*ключа сеанса*](../secgloss/s-gly.md) и экспорта этого ключа в [*простой ключевой BLOB-объект*](../secgloss/s-gly.md) , который можно записать в файл на диске, см. в разделе [Пример программы C: экспорт ключа сеанса](example-c-program-exporting-a-session-key.md).</span><span class="sxs-lookup"><span data-stu-id="8a4e3-114">For an example of creating a [*session key*](../secgloss/s-gly.md) and exporting that key to a [*simple key BLOB*](../secgloss/s-gly.md) that can be written to a disk file, see [Example C Program: Exporting a Session Key](example-c-program-exporting-a-session-key.md).</span></span>

<span data-ttu-id="8a4e3-115">Эта процедура обеспечивает только минимальную безопасность.</span><span class="sxs-lookup"><span data-stu-id="8a4e3-115">This procedure provides only minimal security.</span></span> <span data-ttu-id="8a4e3-116">Если сохраненный ключ сеанса будет использоваться для шифрования данных позднее, то предыдущая процедура не обеспечит адекватной безопасности.</span><span class="sxs-lookup"><span data-stu-id="8a4e3-116">If the stored session key will be used to encrypt data at a later date, the preceding procedure does not provide adequate security.</span></span>

<span data-ttu-id="8a4e3-117">Чтобы обеспечить более высокий уровень безопасности, подпишите большой двоичный объект ключа с помощью закрытого ключа Exchange, прежде чем он будет сохранен на диске.</span><span class="sxs-lookup"><span data-stu-id="8a4e3-117">To provide greater security, sign the key BLOB with an exchange private key before it is stored to disk.</span></span> <span data-ttu-id="8a4e3-118">После последующего считывания большого двоичного объекта ключа с диска его подпись может быть проверена, чтобы гарантировать, что большой двоичный объект ключа не будет поврежден.</span><span class="sxs-lookup"><span data-stu-id="8a4e3-118">When the key BLOB is later read from disk, its signature can be validated to ensure that the key BLOB is intact.</span></span>

<span data-ttu-id="8a4e3-119">Если большой двоичный объект ключа не подписан, любой пользователь, имеющий доступ к диску или другому носителю, на котором хранится ключ, может создать новый ключ сеанса.</span><span class="sxs-lookup"><span data-stu-id="8a4e3-119">If the key BLOB is not signed, anyone with access to the disk or other media where the key is stored can create a new session key.</span></span>

<span data-ttu-id="8a4e3-120">Новый ключ сеанса можно зашифровать с помощью [*ключа обмена*](../secgloss/e-gly.md) [*открытым ключом*](../secgloss/p-gly.md) исходного пользователя. Этот новый ключ можно заменить на исходный.</span><span class="sxs-lookup"><span data-stu-id="8a4e3-120">The new session key can be encrypted with the original user's [*public key*](../secgloss/p-gly.md) [*exchange key*](../secgloss/e-gly.md), and this new key can be substituted for the original.</span></span> <span data-ttu-id="8a4e3-121">Если пользователь не знает, что использовал замененный ключ сеанса для шифрования файлов и сообщений, человек, создавший заменяющий ключ, может легко расшифровывать их.</span><span class="sxs-lookup"><span data-stu-id="8a4e3-121">If the user unknowingly used the substituted session key to encrypt files and messages, the individual who created the substitute key could easily decrypt them.</span></span>

<span data-ttu-id="8a4e3-122">Цифровые подписи подробно обсуждаются в разделе [хэши и Цифровые подписи](hashes-and-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="8a4e3-122">Digital signatures are discussed in detail in [Hashes and Digital Signatures](hashes-and-digital-signatures.md).</span></span>

 

 
