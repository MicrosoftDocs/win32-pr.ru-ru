---
description: Процесс декодирования подписанных данных.
ms.assetid: 803220d0-7963-4fc4-8451-a979e54a9cc3
title: Декодирование подписанных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdfd327746c5d0ba8e7089e1c273817b76c16370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662311"
---
# <a name="decoding-signed-data"></a><span data-ttu-id="3725e-103">Декодирование подписанных данных</span><span class="sxs-lookup"><span data-stu-id="3725e-103">Decoding Signed Data</span></span>

<span data-ttu-id="3725e-104">Следующий общий процесс декодирует тип [*данных со знаком*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="3725e-104">The following general process decodes a [*signed data*](../secgloss/s-gly.md) type.</span></span>

<span data-ttu-id="3725e-105">**Декодирование подписанного сообщения**</span><span class="sxs-lookup"><span data-stu-id="3725e-105">**To decode a signed message**</span></span>

1.  <span data-ttu-id="3725e-106">Получение указателя на закодированный BLOB-объект.</span><span class="sxs-lookup"><span data-stu-id="3725e-106">Get a pointer to the encoded BLOB.</span></span>
2.  <span data-ttu-id="3725e-107">Вызовите [**криптмсгопентодекоде**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), передав необходимые аргументы.</span><span class="sxs-lookup"><span data-stu-id="3725e-107">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passing the necessary arguments.</span></span>
3.  <span data-ttu-id="3725e-108">Вызовите [**криптмсгупдате**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) один раз, передав маркер, полученный на шаге 2, и указатель на данные, которые необходимо декодировать.</span><span class="sxs-lookup"><span data-stu-id="3725e-108">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) once, passing in the handle retrieved in step 2 and a pointer to the data that is to be decoded.</span></span> <span data-ttu-id="3725e-109">Это приводит к тому, что в зависимости от типа сообщений в сообщении будут выполняться соответствующие действия.</span><span class="sxs-lookup"><span data-stu-id="3725e-109">This causes the appropriate actions to be taken on the message, depending on the message type.</span></span>
4.  <span data-ttu-id="3725e-110">Вызовите [**криптмсгжетпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), передав маркер, полученный на шаге 2, и соответствующие типы параметров для доступа к декодированным данным.</span><span class="sxs-lookup"><span data-stu-id="3725e-110">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the handle retrieved in step 2 and the appropriate parameter types to access the decoded data.</span></span> <span data-ttu-id="3725e-111">Например, передайте значение \_ параметра КМСГ Content \_ param, чтобы получить указатель на декодированное содержимое.</span><span class="sxs-lookup"><span data-stu-id="3725e-111">For example, pass in CMSG\_CONTENT\_PARAM to get a pointer to the decoded content.</span></span>

<span data-ttu-id="3725e-112">В следующем общем процессе проверяется подпись подписанного сообщения.</span><span class="sxs-lookup"><span data-stu-id="3725e-112">The following general process verifies the signature of a decoded, signed message.</span></span>

<span data-ttu-id="3725e-113">**Проверка подписи раскодированного подписанного сообщения**</span><span class="sxs-lookup"><span data-stu-id="3725e-113">**To verify the signature of a decoded, signed message**</span></span>

1.  <span data-ttu-id="3725e-114">Вызовите [**криптмсгжетпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), передав в обработчик сообщений и \_ \_ Параметр info КМСГ сведения о сертификате подписывания, \_ \_ чтобы получить [**\_ сведения о сертификате**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) подписывания из сообщения.</span><span class="sxs-lookup"><span data-stu-id="3725e-114">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the message handle and CMSG\_SIGNER\_CERT\_INFO\_PARAM to get the signer's [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) from the message.</span></span>
2.  <span data-ttu-id="3725e-115">Вызовите [**цертопенсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) , чтобы открыть временное хранилище, которое инициализируется сертификатами из сообщения.</span><span class="sxs-lookup"><span data-stu-id="3725e-115">Call [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) to open a temporary store that is initialized with the certificates from the message.</span></span>
3.  <span data-ttu-id="3725e-116">Вызовите [**цертжетсубжектцертификатефромсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) , чтобы получить [**\_ сведения о сертификате**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) подписавших из сертификатов, входящих в сообщение.</span><span class="sxs-lookup"><span data-stu-id="3725e-116">Call [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) to get the signer's [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) from the certificates included in the message.</span></span>
4.  <span data-ttu-id="3725e-117">Вызовите [**криптмсгконтрол**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), передав КМСГ \_ CTRL \_ , \_ чтобы проверить сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="3725e-117">Call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passing in CMSG\_CTRL\_VERIFY\_SIGNATURE to verify the signatures.</span></span>
5.  <span data-ttu-id="3725e-118">Вызовите [**криптмсгклосе**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) , чтобы закрыть сообщение.</span><span class="sxs-lookup"><span data-stu-id="3725e-118">Call [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) to close the message.</span></span>

<span data-ttu-id="3725e-119">Результатом этих процедур является проверка подписи и получение указателя на декодированное содержимое сообщения, полученное на шаге 4 процедуры декодирования подписанного сообщения.</span><span class="sxs-lookup"><span data-stu-id="3725e-119">The result of these procedures is that the signature is verified and a pointer is retrieved to the decoded message content obtained in step 4 of the procedure for decoding a signed message.</span></span>

<span data-ttu-id="3725e-120">Сведения о кодировании C см. в разделе [Пример программы c: подписывание, кодирование, декодирование и проверка сообщения](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).</span><span class="sxs-lookup"><span data-stu-id="3725e-120">For C coding details, see [Example C Program: Signing, Encoding, Decoding, and Verifying a Message](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).</span></span>

 

 
