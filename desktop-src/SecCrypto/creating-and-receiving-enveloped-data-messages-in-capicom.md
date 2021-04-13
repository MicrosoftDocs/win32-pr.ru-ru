---
description: Сообщение с оболочкой состоит из зашифрованного сообщения, сертификатов предполагаемых получателей и набора зашифрованных ключей, по одному для каждого получателя. Созданное сообщение находится в \# формате PKCS 7/CMS.
ms.assetid: 2acd0b58-1028-478d-bfa1-b02fa457d7e3
title: Создание и получение сообщений с запечатанными данными в CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672d56383ac635a295847777c0e557bbe7c40b69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343152"
---
# <a name="creating-and-receiving-enveloped-data-messages-in-capicom"></a><span data-ttu-id="e7e13-104">Создание и получение сообщений с запечатанными данными в CAPICOM</span><span class="sxs-lookup"><span data-stu-id="e7e13-104">Creating and Receiving Enveloped Data Messages in CAPICOM</span></span>

<span data-ttu-id="e7e13-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e7e13-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e7e13-106">Вместо этого используйте платформа .NET Framework для реализации функций безопасности.</span><span class="sxs-lookup"><span data-stu-id="e7e13-106">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="e7e13-107">Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="e7e13-107">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="e7e13-108">Сообщение, упакованное в оболочку, является сообщением, зашифрованным для набора получателей.</span><span class="sxs-lookup"><span data-stu-id="e7e13-108">An enveloped message is a message that is encrypted for a set of recipients.</span></span> <span data-ttu-id="e7e13-109">В процессе енвелопмент создается ключ шифрования сеанса, и сообщение шифруется с помощью этого ключа.</span><span class="sxs-lookup"><span data-stu-id="e7e13-109">In the envelopment process, a session encryption key is generated and the message is encrypted with that key.</span></span> <span data-ttu-id="e7e13-110">Затем сам ключ шифрования шифруется отдельно для каждого получателя с помощью открытых ключей из каждого назначенного сертификата получателя.</span><span class="sxs-lookup"><span data-stu-id="e7e13-110">The encryption key itself is then encrypted separately for each recipient using the public keys from each intended recipient's certificate.</span></span> <span data-ttu-id="e7e13-111">Сообщение с оболочкой состоит из зашифрованного сообщения, сертификатов предполагаемых получателей и набора зашифрованных ключей, по одному для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="e7e13-111">The enveloped message consists of the encrypted message, the certificates of the intended recipients, and the set of encrypted keys, one for each recipient.</span></span> <span data-ttu-id="e7e13-112">Созданное сообщение находится в \# формате PKCS 7/CMS.</span><span class="sxs-lookup"><span data-stu-id="e7e13-112">The message generated is in PKCS \#7/CMS format.</span></span>

<span data-ttu-id="e7e13-113">В следующих разделах приведены процедуры и примеры задач с упакованными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="e7e13-113">The following sections show procedures and examples for enveloped message tasks:</span></span>

-   [<span data-ttu-id="e7e13-114">Отправка сообщения с запечатанными данными</span><span class="sxs-lookup"><span data-stu-id="e7e13-114">Sending an Enveloped Data Message</span></span>](sending-an-enveloped-data-message.md)
-   [<span data-ttu-id="e7e13-115">Получение сообщения с упакованными данными</span><span class="sxs-lookup"><span data-stu-id="e7e13-115">Receiving an Enveloped Data Message</span></span>](receiving-an-enveloped-data-message.md)

 

 



