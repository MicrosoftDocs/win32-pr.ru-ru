---
description: Одним из преимуществ использования списков доверия сертификатов (CTL) является возможность разработки приложений, которые могут автоматически проверять подписанные сообщения от доверенных сертификатов, не требуя от пользователя диалоговых окон.
ms.assetid: e45ea3ae-52bc-49d3-8144-f3becc254f53
title: Проверка подписанных сообщений с помощью списков CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a660bcd7e17a168b25048e61684aabc2d3ef3124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683490"
---
# <a name="verifying-signed-messages-by-using-ctls"></a><span data-ttu-id="c960b-103">Проверка подписанных сообщений с помощью списков CTL</span><span class="sxs-lookup"><span data-stu-id="c960b-103">Verifying Signed Messages by Using CTLs</span></span>

<span data-ttu-id="c960b-104">Одним из преимуществ использования [*списков доверия сертификатов*](../secgloss/c-gly.md) (CTL) является возможность разработки приложений, которые могут автоматически проверять подписанные сообщения от доверенных сертификатов, не требуя от пользователя диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="c960b-104">One of the advantages of using [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) is that applications can be designed that can automatically verify signed messages against trusted certificates without bothering the user with dialog boxes.</span></span> <span data-ttu-id="c960b-105">Он также дает администратору сети контроль над доверенными источниками.</span><span class="sxs-lookup"><span data-stu-id="c960b-105">It also gives a network administrator control sources to be trusted.</span></span>

<span data-ttu-id="c960b-106">Следующую процедуру можно использовать для проверки подписи подписанного сообщения с помощью списка доверия сертификатов.</span><span class="sxs-lookup"><span data-stu-id="c960b-106">The following procedure can be used to verify the signature of a signed message by using a CTL.</span></span>

<span data-ttu-id="c960b-107">**Проверка подписанного сообщения с помощью списка доверия сертификатов**</span><span class="sxs-lookup"><span data-stu-id="c960b-107">**To verify a signed message by using a CTL**</span></span>

1.  <span data-ttu-id="c960b-108">Декодировать сообщение следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c960b-108">Decode the message as follows:</span></span>

    1.  <span data-ttu-id="c960b-109">Получение указателя на полученное сообщение (закодированный BLOB- [*объект*](../secgloss/b-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="c960b-109">Get a pointer to the received message (the encoded [*BLOB*](../secgloss/b-gly.md)).</span></span>
    2.  <span data-ttu-id="c960b-110">Вызовите [**криптмсгопентодекоде**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), передав необходимые аргументы.</span><span class="sxs-lookup"><span data-stu-id="c960b-110">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passing the necessary arguments.</span></span>
    3.  <span data-ttu-id="c960b-111">Вызовите [**криптмсгупдате**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) один раз, передав маркер, полученный на шаге b, и указатель на данные, которые необходимо декодировать.</span><span class="sxs-lookup"><span data-stu-id="c960b-111">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) once, passing in the handle retrieved in step b and a pointer to the data that is to be decoded.</span></span> <span data-ttu-id="c960b-112">Это приводит к тому, что в зависимости от типа сообщений в сообщении будут выполняться соответствующие действия.</span><span class="sxs-lookup"><span data-stu-id="c960b-112">This causes the appropriate actions to be taken on the message, depending on the message type.</span></span>

2.  <span data-ttu-id="c960b-113">Проверка подписи декодированного подписанного сообщения и получение указателя на [**\_ контекст сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)подписавшего.</span><span class="sxs-lookup"><span data-stu-id="c960b-113">Verify the signature of the decoded, signed message, and get a pointer to the signer's [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span></span>

    <span data-ttu-id="c960b-114">Это можно сделать, вызвав [**криптмсгжетандверифисигнер**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), передав полученный в шаге 1C маркер сообщения в качестве параметра *хкриптмсг* .</span><span class="sxs-lookup"><span data-stu-id="c960b-114">This can be done by calling [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), passing the message handle retrieved in step 1c as the *hCryptMsg* parameter.</span></span> <span data-ttu-id="c960b-115">Если вызов функции возвращает **значение true**, то сигнатура была проверена, а в параметре *ппсигнер* возвращается указатель на [**\_ контекст пкцерт**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) подписи.</span><span class="sxs-lookup"><span data-stu-id="c960b-115">If the function call returns **TRUE**, the signature was verified, and a pointer to the signer's [**PCCERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) is returned in the *ppSigner* parameter.</span></span>

3.  <span data-ttu-id="c960b-116">Убедитесь, что подписавший является надежным источником, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="c960b-116">Confirm that the signer is a trusted source as follows:</span></span>

    1.  <span data-ttu-id="c960b-117">Откройте хранилище сертификатов, содержащее соответствующий список доверия сертификатов.</span><span class="sxs-lookup"><span data-stu-id="c960b-117">Open the certificate store containing the appropriate CTL.</span></span>
    2.  <span data-ttu-id="c960b-118">Получите указатель на [**\_ контекст CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) , вызвав [**цертфиндктлинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span><span class="sxs-lookup"><span data-stu-id="c960b-118">Get a pointer to the [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) by calling [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span></span>
    3.  <span data-ttu-id="c960b-119">Чтобы убедиться, что подписавший является надежным источником, вызовите [**цертфиндсубжектинктл**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl), передав указатель, полученный на предыдущем шаге, в параметре *пктлконтекст* , \_ \_ Тип субъекта сертификата CTL \_ в параметре *двсубжекттипе* и указатель на [**\_ контекст сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) , полученный на шаге 2 в параметре *пвсубжект* .</span><span class="sxs-lookup"><span data-stu-id="c960b-119">To confirm that the signer is a trusted source, call [**CertFindSubjectInCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl), passing the pointer retrieved in the previous step in the *pCtlContext* parameter, CTL\_CERT\_SUBJECT\_TYPE in the *dwSubjectType* parameter, and the pointer to the [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) retrieved in step 2 in the *pvSubject* parameter.</span></span> <span data-ttu-id="c960b-120">Если вызов функции возвращает **значение true**, то **\_ контекст сертификата** , переданный в функцию, является надежным источником в списке доверия (CTL).</span><span class="sxs-lookup"><span data-stu-id="c960b-120">If the function call returns **TRUE**, the **CERT\_CONTEXT** passed to the function is a trusted source in the CTL.</span></span>

 

 
