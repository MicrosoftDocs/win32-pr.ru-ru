---
description: Общие задачи, необходимые для декодирования сообщения, упакованного в оболочку.
ms.assetid: cb71ea3a-0edd-4d46-8088-a395fab89d2b
title: Декодирование упакованных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1a0ba12e967f5a0cd56347c0839ce9fca40f02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104570336"
---
# <a name="decoding-enveloped-data"></a><span data-ttu-id="5b92a-103">Декодирование упакованных данных</span><span class="sxs-lookup"><span data-stu-id="5b92a-103">Decoding Enveloped Data</span></span>

<span data-ttu-id="5b92a-104">Общие задачи, необходимые для декодирования сообщения с оболочкой, показаны на следующем рисунке и описаны в приведенном ниже списке.</span><span class="sxs-lookup"><span data-stu-id="5b92a-104">The general tasks required to decode an enveloped message are depicted in the following illustration and described in the list that follows it.</span></span>

![декодирование упакованных данных](images/decemsg.png)

<span data-ttu-id="5b92a-106">Последовательность событий декодирования запечатанных данных с помощью управления ключами транспортных ключей, как показано на предыдущем рисунке, выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5b92a-106">The sequence of events for decoding enveloped data using key transport key management, as depicted in the previous illustration, is as follows:</span></span>

-   <span data-ttu-id="5b92a-107">Извлекается указатель на сообщение с [*цифровым конвертом*](../secgloss/d-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="5b92a-107">A pointer to the [*digitally enveloped*](../secgloss/d-gly.md) message is retrieved.</span></span>
-   <span data-ttu-id="5b92a-108">Открыто [*хранилище сертификатов*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="5b92a-108">A [*certificate store*](../secgloss/c-gly.md) is opened.</span></span>
-   <span data-ttu-id="5b92a-109">В сообщении извлекается идентификатор получателя (My ID).</span><span class="sxs-lookup"><span data-stu-id="5b92a-109">From the message, the recipient ID (My ID) is retrieved.</span></span>
-   <span data-ttu-id="5b92a-110">Идентификатор получателя используется для получения сертификата.</span><span class="sxs-lookup"><span data-stu-id="5b92a-110">The recipient ID is used to retrieve the certificate.</span></span>
-   <span data-ttu-id="5b92a-111">Получен [*закрытый ключ*](../secgloss/p-gly.md) , связанный с этим сертификатом.</span><span class="sxs-lookup"><span data-stu-id="5b92a-111">The [*private key*](../secgloss/p-gly.md) associated with that certificate is retrieved.</span></span>
-   <span data-ttu-id="5b92a-112">Закрытый ключ используется для расшифровки [*симметричного*](../secgloss/s-gly.md) ключа ([*сеанса*](../secgloss/s-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="5b92a-112">The private key is used to decrypt the [*symmetric*](../secgloss/s-gly.md) ([*session*](../secgloss/s-gly.md)) key.</span></span>
-   <span data-ttu-id="5b92a-113">Алгоритм шифрования извлекается из сообщения.</span><span class="sxs-lookup"><span data-stu-id="5b92a-113">The encryption algorithm is retrieved from the message.</span></span>
-   <span data-ttu-id="5b92a-114">При использовании закрытого ключа и алгоритма шифрования данные расшифровываются.</span><span class="sxs-lookup"><span data-stu-id="5b92a-114">Using the private key and encryption algorithm, the data is decrypted.</span></span>

<span data-ttu-id="5b92a-115">В следующей процедуре используются функции обработки сообщений низкого уровня для выполнения только что перечисленных задач.</span><span class="sxs-lookup"><span data-stu-id="5b92a-115">The following procedure uses low-level message functions to accomplish the tasks just listed.</span></span>

<span data-ttu-id="5b92a-116">**Декодирование сообщения, упакованного в оболочку**</span><span class="sxs-lookup"><span data-stu-id="5b92a-116">**To decode an enveloped message**</span></span>

1.  <span data-ttu-id="5b92a-117">Получение указателя на закодированный BLOB-объект.</span><span class="sxs-lookup"><span data-stu-id="5b92a-117">Get a pointer to the encoded BLOB.</span></span>
2.  <span data-ttu-id="5b92a-118">Вызовите [**криптмсгопентодекоде**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), передав необходимые аргументы.</span><span class="sxs-lookup"><span data-stu-id="5b92a-118">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passing the necessary arguments.</span></span>
3.  <span data-ttu-id="5b92a-119">Вызовите [**криптмсгупдате**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) один раз, передав маркер, полученный на шаге 2, и указатель на данные, которые необходимо декодировать.</span><span class="sxs-lookup"><span data-stu-id="5b92a-119">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) once, passing in the handle retrieved in step 2 and a pointer to the data that is to be decoded.</span></span> <span data-ttu-id="5b92a-120">Это приводит к тому, что в зависимости от типа сообщений в сообщении будут выполняться соответствующие действия.</span><span class="sxs-lookup"><span data-stu-id="5b92a-120">This causes the appropriate actions to be taken on the message, depending on the message type.</span></span>
4.  <span data-ttu-id="5b92a-121">Вызовите [**криптмсгжетпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), передав маркер, полученный на шаге 2, и КМСГ \_ типа \_ param, чтобы убедиться, что сообщение имеет тип данных, упакованный в оболочку.</span><span class="sxs-lookup"><span data-stu-id="5b92a-121">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the handle retrieved in step 2 and CMSG\_TYPE\_PARAM to verify that the message is of the enveloped data type.</span></span>
5.  <span data-ttu-id="5b92a-122">Снова вызовите [**криптмсгжетпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), передав \_ \_ параметр типа внутреннего содержимого КМСГ, \_ \_ чтобы получить тип данных [*внутреннего содержимого*](../secgloss/i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5b92a-122">Again call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in CMSG\_INNER\_CONTENT\_TYPE\_PARAM to get the data type of the [*inner content*](../secgloss/i-gly.md).</span></span>
6.  <span data-ttu-id="5b92a-123">Если тип данных внутреннего содержимого — **Data**, приступите к расшифровке и декодированию содержимого.</span><span class="sxs-lookup"><span data-stu-id="5b92a-123">If the inner content data type is **data**, proceed to decrypt and decode the content.</span></span> <span data-ttu-id="5b92a-124">В противном случае выполните процедуру декодирования, подходящую для типа данных Content.</span><span class="sxs-lookup"><span data-stu-id="5b92a-124">Otherwise, run a decoding procedure appropriate for the content data type.</span></span>
7.  <span data-ttu-id="5b92a-125">При условии, что тип внутреннего содержимого — "Data", инициализируйте [**КМСГ \_ CTRL \_ расшифровать \_ абзац**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) данных и вызовите [**криптмсгконтрол**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), передав КМСГ \_ CTRL \_ расшифровывает и адрес структуры.</span><span class="sxs-lookup"><span data-stu-id="5b92a-125">Assuming the inner content type is "data", initialize the [**CMSG\_CTRL\_DECRYPT\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) data structure, and call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passing in CMSG\_CTRL\_DECRYPT and the address of the structure.</span></span> <span data-ttu-id="5b92a-126">Содержимое будет расшифровано.</span><span class="sxs-lookup"><span data-stu-id="5b92a-126">The content will be decrypted.</span></span>
8.  <span data-ttu-id="5b92a-127">Вызовите [**криптмсгжетпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), передав \_ параметр содержимого КМСГ, \_ чтобы получить указатель на Раскодированный BLOB-объект данных содержимого (строка в **байтах** ).</span><span class="sxs-lookup"><span data-stu-id="5b92a-127">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in CMSG\_CONTENT\_PARAM to get a pointer to the decoded content data BLOB (**BYTE** string).</span></span>
9.  <span data-ttu-id="5b92a-128">Вызовите [**криптмсгклосе**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) , чтобы закрыть сообщение.</span><span class="sxs-lookup"><span data-stu-id="5b92a-128">Call [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) to close the message.</span></span>

<span data-ttu-id="5b92a-129">Результатом этой процедуры является декодирование и расшифровка сообщения, а также получение указателя на большой двоичный объект данных содержимого.</span><span class="sxs-lookup"><span data-stu-id="5b92a-129">The result of this procedure is that the message is decoded and decrypted and a pointer is retrieved to the content data BLOB.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b92a-130">См. также</span><span class="sxs-lookup"><span data-stu-id="5b92a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b92a-131">Пример программы на языке C. кодирование подписанного сообщения с подписью</span><span class="sxs-lookup"><span data-stu-id="5b92a-131">Example C Program: Encoding an Enveloped, Signed Message</span></span>](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
