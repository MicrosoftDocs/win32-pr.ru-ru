---
description: Описывает задачи, которые необходимо выполнить для создания подписанного сообщения.
ms.assetid: 61896022-28c2-4f70-977a-c990b4b23c55
title: Создание подписанного сообщения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f68511c41a10fc0f690574e71c1dfe8a354efbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265194"
---
# <a name="creating-a-signed-message"></a><span data-ttu-id="c13ff-103">Создание подписанного сообщения</span><span class="sxs-lookup"><span data-stu-id="c13ff-103">Creating a Signed Message</span></span>

<span data-ttu-id="c13ff-104">На следующем рисунке показаны задачи, которые необходимо выполнить для создания подписанного сообщения.</span><span class="sxs-lookup"><span data-stu-id="c13ff-104">The following illustration depicts the tasks that must be accomplished to create a signed message.</span></span> <span data-ttu-id="c13ff-105">Шаги приведены на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="c13ff-105">The steps are listed following the illustration.</span></span>

![Подписывание сообщения](images/signdmsg.png)

<span data-ttu-id="c13ff-107">**Создание подписанного сообщения**</span><span class="sxs-lookup"><span data-stu-id="c13ff-107">**To create a signed message**</span></span>

1.  <span data-ttu-id="c13ff-108">Создайте данные (при необходимости) и получите указатель на него.</span><span class="sxs-lookup"><span data-stu-id="c13ff-108">Create the data (if necessary) and get a pointer to it.</span></span>
2.  <span data-ttu-id="c13ff-109">Откройте [*хранилище сертификатов*](../secgloss/c-gly.md) , содержащее сертификат подписи.</span><span class="sxs-lookup"><span data-stu-id="c13ff-109">Open a [*certificate store*](../secgloss/c-gly.md) that contains the signer's certificate.</span></span>
3.  <span data-ttu-id="c13ff-110">Получите [*закрытый ключ*](../secgloss/p-gly.md) для сертификата.</span><span class="sxs-lookup"><span data-stu-id="c13ff-110">Get the [*private key*](../secgloss/p-gly.md) for the certificate.</span></span> <span data-ttu-id="c13ff-111">Перед использованием сертификата необходимо задать для него свойство, чтобы связать сертификат с определенным [*CSP*](../secgloss/c-gly.md), а в пределах этого CSP — с определенным закрытым ключом.</span><span class="sxs-lookup"><span data-stu-id="c13ff-111">A property must be set on the certificate before using it, to tie a certificate to a particular [*CSP*](../secgloss/c-gly.md), and, within that CSP, to a particular private key.</span></span> <span data-ttu-id="c13ff-112">Этот параметр необходимо задать один раз.</span><span class="sxs-lookup"><span data-stu-id="c13ff-112">This needs to be set once.</span></span>
4.  <span data-ttu-id="c13ff-113">Выберите алгоритм хэширования для операции дайджеста.</span><span class="sxs-lookup"><span data-stu-id="c13ff-113">Choose a hashing algorithm for the digest operation.</span></span> <span data-ttu-id="c13ff-114">Рекомендуется выбирать алгоритм хеширования из настраиваемого расположения, которое впоследствии можно обновить без внесения изменений в код.</span><span class="sxs-lookup"><span data-stu-id="c13ff-114">We recommend that the hashing algorithm be selected from a configurable location that can be subsequently updated without requiring changes to code.</span></span>
5.  <span data-ttu-id="c13ff-115">Отправьте данные с помощью функции хэширования, используя алгоритм хэширования, создавая [*хэш*](../secgloss/h-gly.md) (дайджест) данных.</span><span class="sxs-lookup"><span data-stu-id="c13ff-115">Send the data through the hashing function by using the hashing algorithm, thus creating a [*hash*](../secgloss/h-gly.md) (digest) of the data.</span></span>
6.  <span data-ttu-id="c13ff-116">С помощью [*закрытого ключа*](../secgloss/p-gly.md) , полученного через свойство сертификата, зашифруйте дайджест, создавая сигнатуру.</span><span class="sxs-lookup"><span data-stu-id="c13ff-116">Using the [*private key*](../secgloss/p-gly.md) obtained through the property on the certificate, encrypt the digest, creating the signature.</span></span>
7.  <span data-ttu-id="c13ff-117">Включите в подписанное сообщение следующее:</span><span class="sxs-lookup"><span data-stu-id="c13ff-117">Include the following in the signed message:</span></span>

    -   <span data-ttu-id="c13ff-118">Подписанные данные</span><span class="sxs-lookup"><span data-stu-id="c13ff-118">The signed data</span></span>
    -   <span data-ttu-id="c13ff-119">Хэш-алгоритм</span><span class="sxs-lookup"><span data-stu-id="c13ff-119">The hash algorithm</span></span>
    -   <span data-ttu-id="c13ff-120">Подпись</span><span class="sxs-lookup"><span data-stu-id="c13ff-120">The signature</span></span>
    -   <span data-ttu-id="c13ff-121">Идентификатор подписавший (поставщик сертификата и серийный номер);</span><span class="sxs-lookup"><span data-stu-id="c13ff-121">The signer identifier (certificate issuer and serial number)</span></span>
    -   <span data-ttu-id="c13ff-122">Сертификат подписавший (необязательно)</span><span class="sxs-lookup"><span data-stu-id="c13ff-122">The signer's certificate (optional)</span></span>

<span data-ttu-id="c13ff-123">Подробные процедуры и примеры см. в разделе [процедура подписывания данных](procedure-for-signing-data.md) и [Пример программы на языке C: подписывание сообщения и проверка подписи сообщения](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span><span class="sxs-lookup"><span data-stu-id="c13ff-123">For a detailed procedure and example, see [Procedure for Signing Data](procedure-for-signing-data.md) and [Example C Program: Signing a Message and Verifying a Message Signature](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span></span>

 

 
