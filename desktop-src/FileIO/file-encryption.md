---
description: Шифрованная файловая система (EFS) обеспечивает криптографическую защиту отдельных файлов на томах файловой системы NTFS с помощью системы с открытым ключом.
ms.assetid: 5f20109f-727d-44a9-90a1-0adc19b00d28
title: Шифрование файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55c05d8d746e597fe180feffe25f7f553819e822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684374"
---
# <a name="file-encryption"></a><span data-ttu-id="65891-103">Шифрование файлов</span><span class="sxs-lookup"><span data-stu-id="65891-103">File Encryption</span></span>

<span data-ttu-id="65891-104">Зашифрованная файловая система (EFS) обеспечивает дополнительный уровень безопасности для файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="65891-104">The Encrypted File System, or EFS, provides an additional level of security for files and directories.</span></span> <span data-ttu-id="65891-105">Он обеспечивает криптографическую защиту отдельных файлов на томах файловой системы NTFS с помощью системы с открытым ключом.</span><span class="sxs-lookup"><span data-stu-id="65891-105">It provides cryptographic protection of individual files on NTFS file system volumes using a public-key system.</span></span>

<span data-ttu-id="65891-106">Как правило, управление доступом к объектам файлов и каталогов, предоставляемым моделью безопасности Windows, достаточно для защиты несанкционированного доступа к конфиденциальной информации.</span><span class="sxs-lookup"><span data-stu-id="65891-106">Typically, the access control to file and directory objects provided by the Windows security model is sufficient to protect unauthorized access to sensitive information.</span></span> <span data-ttu-id="65891-107">Однако в случае утери или кражи ноутбука, содержащего конфиденциальные данные, защита этих данных может быть скомпрометирована.</span><span class="sxs-lookup"><span data-stu-id="65891-107">However, if a laptop that contains sensitive data is lost or stolen, the security protection of that data may be compromised.</span></span> <span data-ttu-id="65891-108">Шифрование файлов повышает безопасность.</span><span class="sxs-lookup"><span data-stu-id="65891-108">Encrypting the files increases security.</span></span>

<span data-ttu-id="65891-109">Чтобы определить, поддерживает ли файловая система шифрование файлов и каталогов, вызовите функцию [**жетволумеинформатион**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) и изучите флаг битов **\_ \_ шифрования файлов FS** .</span><span class="sxs-lookup"><span data-stu-id="65891-109">To determine whether a file system supports file encryption for files and directories, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the **FS\_FILE\_ENCRYPTION** bit flag.</span></span> <span data-ttu-id="65891-110">Обратите внимание, что следующие элементы не могут быть зашифрованы:</span><span class="sxs-lookup"><span data-stu-id="65891-110">Note that the following items cannot be encrypted:</span></span>

-   <span data-ttu-id="65891-111">сжатые файлы</span><span class="sxs-lookup"><span data-stu-id="65891-111">Compressed files</span></span>
-   <span data-ttu-id="65891-112">системных файлов;</span><span class="sxs-lookup"><span data-stu-id="65891-112">System files</span></span>
-   <span data-ttu-id="65891-113">Системные каталоги</span><span class="sxs-lookup"><span data-stu-id="65891-113">System directories</span></span>
-   <span data-ttu-id="65891-114">Корневые каталоги</span><span class="sxs-lookup"><span data-stu-id="65891-114">Root directories</span></span>
-   <span data-ttu-id="65891-115">Transactions</span><span class="sxs-lookup"><span data-stu-id="65891-115">Transactions</span></span>

<span data-ttu-id="65891-116">Разреженные файлы могут быть зашифрованы.</span><span class="sxs-lookup"><span data-stu-id="65891-116">Sparse files can be encrypted.</span></span>

<span data-ttu-id="65891-117">TxF не поддерживает большинство операций с файлами шифрованной файловой системы (EFS).</span><span class="sxs-lookup"><span data-stu-id="65891-117">TxF does not support most operations on Encrypted File System (EFS) files.</span></span> <span data-ttu-id="65891-118">Единственными операциями, поддерживаемыми TxF, являются операции чтения, такие как [**реаденкриптедфилерав**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw).</span><span class="sxs-lookup"><span data-stu-id="65891-118">The only operations TxF supports are read operations, such as [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="65891-119">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="65891-119">In this section</span></span>



| <span data-ttu-id="65891-120">Раздел</span><span class="sxs-lookup"><span data-stu-id="65891-120">Topic</span></span>                                                                                               | <span data-ttu-id="65891-121">Описание</span><span class="sxs-lookup"><span data-stu-id="65891-121">Description</span></span>                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65891-122">Обработка зашифрованных файлов и каталогов</span><span class="sxs-lookup"><span data-stu-id="65891-122">Handling Encrypted Files and Directories</span></span>](handling-encrypted-files-and-directories.md)<br/> | <span data-ttu-id="65891-123">Файл, помеченный как зашифрованный, шифруется файловой системой NTFS с использованием текущего драйвера шифрования.</span><span class="sxs-lookup"><span data-stu-id="65891-123">A file marked encrypted is encrypted by the NTFS file system by using the current encryption driver.</span></span><br/>                                                          |
| [<span data-ttu-id="65891-124">Зашифрованные файлы и ключи пользователей</span><span class="sxs-lookup"><span data-stu-id="65891-124">Encrypted Files and User Keys</span></span>](encrypted-files-and-user-keys.md)<br/>                       | <span data-ttu-id="65891-125">Список функций, используемых для создания нового ключа, добавления ключа в зашифрованный файл, запроса ключей для зашифрованного файла и удаления ключей из зашифрованного файла.</span><span class="sxs-lookup"><span data-stu-id="65891-125">Lists the functions to use to create a new key, add a key to an encrypted file, query the keys for an encrypted file, and remove keys from an encrypted file.</span></span><br/> |
| [<span data-ttu-id="65891-126">Резервное копирование и восстановление зашифрованных файлов</span><span class="sxs-lookup"><span data-stu-id="65891-126">Backup and Restore of Encrypted Files</span></span>](backup-and-restore-of-encrypted-files.md)<br/>       | <span data-ttu-id="65891-127">Функции необработанного шифрования обеспечивают резервное копирование зашифрованных файлов.</span><span class="sxs-lookup"><span data-stu-id="65891-127">The raw encryption functions enable backup of encrypted files.</span></span><br/>                                                                                                |



 

<span data-ttu-id="65891-128">Дополнительные сведения о шифровании см. [в разделе Добавление пользователей в зашифрованный файл](adding-users-to-an-encrypted-file.md).</span><span class="sxs-lookup"><span data-stu-id="65891-128">For more information about encryption, see [Adding Users to an Encrypted File](adding-users-to-an-encrypted-file.md).</span></span>

<span data-ttu-id="65891-129">Дополнительные сведения о шифровании см. в разделе [Криптография](/windows/desktop/SecCrypto/cryptography-portal).</span><span class="sxs-lookup"><span data-stu-id="65891-129">For more information about cryptography, see [Cryptography](/windows/desktop/SecCrypto/cryptography-portal).</span></span>

 

