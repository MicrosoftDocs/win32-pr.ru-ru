---
description: Показывает, как отправить зашифрованное сообщение.
ms.assetid: 928b1863-7a54-4bf0-b447-85b8c2868bcd
title: Обмен ключами сеансов вручную
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0114f8173084126a72519d291158f15f3e1c171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552169"
---
# <a name="manual-session-key-exchanges"></a><span data-ttu-id="be691-103">Обмен ключами сеансов вручную</span><span class="sxs-lookup"><span data-stu-id="be691-103">Manual Session Key Exchanges</span></span>

> [!Note]  
> <span data-ttu-id="be691-104">В процедуре, описанной в этом разделе, предполагается, что пользователи (или клиенты CryptoAPI) уже имеют собственный набор [*пар открытого и закрытого ключей*](../secgloss/p-gly.md) , а также получили [*открытые ключи*](../secgloss/p-gly.md)друг друга.</span><span class="sxs-lookup"><span data-stu-id="be691-104">The procedure described in this section assumes that the users (or CryptoAPI clients) already possess their own set of [*public/private key pairs*](../secgloss/p-gly.md) and have also obtained each other's [*public keys*](../secgloss/p-gly.md).</span></span>

 

<span data-ttu-id="be691-105">На следующем рисунке показано, как использовать эту процедуру для отправки зашифрованного сообщения.</span><span class="sxs-lookup"><span data-stu-id="be691-105">The following illustration shows how to use this procedure to send an encrypted message.</span></span>

![Отправка зашифрованного сообщения](images/capi04.png)

<span data-ttu-id="be691-107">Этот подход уязвим по крайней мере для одной из распространенных форм атак.</span><span class="sxs-lookup"><span data-stu-id="be691-107">This approach is vulnerable to at least one common form of attack.</span></span> <span data-ttu-id="be691-108">Перехватчик может получать копии одного или нескольких зашифрованных сообщений и зашифрованных ключей.</span><span class="sxs-lookup"><span data-stu-id="be691-108">An eavesdropper can acquire copies of one or more encrypted messages and the encrypted keys.</span></span> <span data-ttu-id="be691-109">Затем через некоторое время перехватчик может отправить одно из этих сообщений получателю, и получатель не сможет узнать, что сообщение не получено непосредственно от исходного отправителя.</span><span class="sxs-lookup"><span data-stu-id="be691-109">Then, at some later time, the eavesdropper can send one of these messages to the receiver and the receiver will have no way of knowing the message did not come directly from the original sender.</span></span> <span data-ttu-id="be691-110">Этот риск можно уменьшить за счет отметки времени всех сообщений или с помощью серийных номеров.</span><span class="sxs-lookup"><span data-stu-id="be691-110">This risk can be reduced by time-stamping all messages or by using serial numbers.</span></span>

<span data-ttu-id="be691-111">Самым простым способом отправки зашифрованных сообщений другому пользователю является отправка сообщения, зашифрованного с помощью случайного ключа сеанса, и ключа сеанса, зашифрованного с помощью [*открытого ключа*](../secgloss/k-gly.md)получателя.</span><span class="sxs-lookup"><span data-stu-id="be691-111">The easiest way to send encrypted messages to another user is to send the message encrypted with a random session key along with the session key encrypted with the receiver's [*key exchange public key*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="be691-112">Ниже приведены действия по отправке зашифрованного ключа сеанса.</span><span class="sxs-lookup"><span data-stu-id="be691-112">Following are the steps for sending an encrypted session key.</span></span>

<span data-ttu-id="be691-113">**Отправка зашифрованного ключа сеанса**</span><span class="sxs-lookup"><span data-stu-id="be691-113">**To send an encrypted session key**</span></span>

1.  <span data-ttu-id="be691-114">Создайте случайный [*сеансовый ключ*](../secgloss/s-gly.md) с помощью функции [**криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .</span><span class="sxs-lookup"><span data-stu-id="be691-114">Create a random [*session key*](../secgloss/s-gly.md) by using the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function.</span></span>
2.  <span data-ttu-id="be691-115">Шифрование сообщения с помощью ключа сеанса.</span><span class="sxs-lookup"><span data-stu-id="be691-115">Encrypt the message by using the session key.</span></span> <span data-ttu-id="be691-116">Эта процедура обсуждается в разделе [Шифрование и расшифровка данных](data-encryption-and-decryption.md).</span><span class="sxs-lookup"><span data-stu-id="be691-116">This procedure is discussed in [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>
3.  <span data-ttu-id="be691-117">Экспортируйте ключ сеанса в [*большой двоичный объект ключа*](../secgloss/k-gly.md) с помощью функции [**криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , указав, что ключ должен быть зашифрован с помощью открытого ключа пользователя для обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="be691-117">Export the session key into a [*key BLOB*](../secgloss/k-gly.md) with the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function, specifying that the key be encrypted with the destination user's key exchange public key.</span></span>
4.  <span data-ttu-id="be691-118">Отправьте зашифрованное сообщение и зашифрованный ключевой BLOB-объект пользователю назначения.</span><span class="sxs-lookup"><span data-stu-id="be691-118">Send both the encrypted message and the encrypted key BLOB to the destination user.</span></span>
5.  <span data-ttu-id="be691-119">Конечный пользователь импортирует большой двоичный объект ключа в свой CSP с помощью функции [**криптимпорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) .</span><span class="sxs-lookup"><span data-stu-id="be691-119">The destination user imports the key BLOB into his or her CSP by using the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function.</span></span> <span data-ttu-id="be691-120">При этом ключ сеанса будет автоматически расшифрован, если на шаге 3 был указан открытый ключ для обмена ключами конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="be691-120">This will automatically decrypt the session key, provided the destination user's key exchange public key was specified in step 3.</span></span>
6.  <span data-ttu-id="be691-121">Затем конечный пользователь может расшифровать сообщение с помощью ключа сеанса, следуя процедуре, описанной в разделе [Шифрование и расшифровка данных](data-encryption-and-decryption.md).</span><span class="sxs-lookup"><span data-stu-id="be691-121">The destination user can then decrypt the message by using the session key, following the procedure discussed in [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>

 

 
