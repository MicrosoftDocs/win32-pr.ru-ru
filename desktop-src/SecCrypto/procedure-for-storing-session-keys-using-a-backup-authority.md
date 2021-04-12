---
description: Приложение, использующее центр архивации для хранения ключей сеансов, обычно выполняет эти действия.
ms.assetid: 859310ed-6000-44c8-92f7-974326ce0fc9
title: Хранение ключей сеанса с помощью центра архивации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59906874f384d4eed9e20d6a781b14e3feba313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345725"
---
# <a name="storing-session-keys-using-a-backup-authority"></a><span data-ttu-id="e7c0c-103">Хранение ключей сеанса с помощью центра архивации</span><span class="sxs-lookup"><span data-stu-id="e7c0c-103">Storing Session Keys Using a Backup Authority</span></span>

<span data-ttu-id="e7c0c-104">Приложение, использующее [*Центр архивации*](../secgloss/b-gly.md) для хранения ключей сеансов, обычно выполняет эти действия.</span><span class="sxs-lookup"><span data-stu-id="e7c0c-104">An application using a [*backup authority*](../secgloss/b-gly.md) to store session keys typically follows these steps.</span></span>

<span data-ttu-id="e7c0c-105">**Использование центра архивации**</span><span class="sxs-lookup"><span data-stu-id="e7c0c-105">**To use a backup authority**</span></span>

1.  <span data-ttu-id="e7c0c-106">Зашифровать файл обычным образом.</span><span class="sxs-lookup"><span data-stu-id="e7c0c-106">Encrypt the file as usual.</span></span>
2.  <span data-ttu-id="e7c0c-107">Экспортируйте [*ключ сеанса*](../secgloss/s-gly.md) , используемый для шифрования файла, в [*простой ключевой BLOB-объект*](../secgloss/s-gly.md), указав, что ваш собственный [*открытый ключ обмена ключами*](../secgloss/k-gly.md) используется для шифрования большого двоичного объекта ключа.</span><span class="sxs-lookup"><span data-stu-id="e7c0c-107">Export the [*session key*](../secgloss/s-gly.md) used to encrypt the file into a [*simple key BLOB*](../secgloss/s-gly.md), specifying that your own [*key exchange public key*](../secgloss/k-gly.md) be used to encrypt the key BLOB.</span></span> <span data-ttu-id="e7c0c-108">Сохраните этот ключевой BLOB-объект с помощью зашифрованного файла.</span><span class="sxs-lookup"><span data-stu-id="e7c0c-108">Store this key BLOB with the encrypted file.</span></span>
3.  <span data-ttu-id="e7c0c-109">Снова экспортируйте ключ сеанса. это указывает, что открытый ключ центра архивации будет использоваться для шифрования большого двоичного объекта ключа.</span><span class="sxs-lookup"><span data-stu-id="e7c0c-109">Export the session key again, this time specifying that the backup authority's public key be used to encrypt the key BLOB.</span></span> <span data-ttu-id="e7c0c-110">Отправьте этот ключевой BLOB-объект в Центр архивации вместе с описанием ключа, серийным номером и т. д.</span><span class="sxs-lookup"><span data-stu-id="e7c0c-110">Send this key BLOB to the backup authority, along with the key's description, serial number, and so on.</span></span>

<span data-ttu-id="e7c0c-111">Если [*пара ключей*](../secgloss/k-gly.md) потеряна, ключи можно будет получить из [*центра архивации*](../secgloss/b-gly.md) , если можно установить удостоверение владельца ключей.</span><span class="sxs-lookup"><span data-stu-id="e7c0c-111">If a [*key pair*](../secgloss/k-gly.md) is lost, the keys can be retrieved from the [*backup authority*](../secgloss/b-gly.md) if the identity of the keys' owner can be established.</span></span> <span data-ttu-id="e7c0c-112">Процедура установления удостоверения определяется политикой конкретного центра архивации и не предусматривает использования CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="e7c0c-112">The procedure for establishing identity is determined by the policy of the particular backup authority and does not involve CryptoAPI.</span></span>

<span data-ttu-id="e7c0c-113">Для кода, необходимого для создания ключа сеанса и экспорта этого ключа в [*простой ключевой BLOB-объект*](../secgloss/s-gly.md) , который можно записать в файл на диске, см. [Пример программы C: экспорт ключа сеанса](example-c-program-exporting-a-session-key.md).</span><span class="sxs-lookup"><span data-stu-id="e7c0c-113">For the code needed to create a session key and export that key to a [*simple key BLOB*](../secgloss/s-gly.md) that can be written to a disk file, see [Example C Program: Exporting a Session Key](example-c-program-exporting-a-session-key.md).</span></span>

 

 
