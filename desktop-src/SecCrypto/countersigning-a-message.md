---
description: Объясняет, как выполнить скрепляющую подпись сообщение с помощью Криптмсгкаунтерсигн.
ms.assetid: e1969b43-f50e-4c7d-a7e5-b22db4e05be2
title: Скрепляющая подпись сообщение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02091d25e7ee22f986a26b8f07abff68ebb8c11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663624"
---
# <a name="countersigning-a-message"></a><span data-ttu-id="ce9e6-103">Скрепляющая подпись сообщение</span><span class="sxs-lookup"><span data-stu-id="ce9e6-103">Countersigning a Message</span></span>

<span data-ttu-id="ce9e6-104">**Выполнить скрепляющую подпись подписанное сообщение с помощью Криптмсгкаунтерсигн**</span><span class="sxs-lookup"><span data-stu-id="ce9e6-104">**To countersign a signed message by using CryptMsgCountersign**</span></span>

1.  <span data-ttu-id="ce9e6-105">Вызовите [**криптмсгопентодекоде**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) , чтобы получить маркер подписанного сообщения.</span><span class="sxs-lookup"><span data-stu-id="ce9e6-105">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="ce9e6-106">Инициализируйте [**\_ \_ \_ информационную структуру КМСГ для кодирования подписи**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) для каунтерсигнер.</span><span class="sxs-lookup"><span data-stu-id="ce9e6-106">Initialize a [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure for the countersigner.</span></span>
3.  <span data-ttu-id="ce9e6-107">Добавьте структуру [**КМСГ для \_ \_ кодирования подписи \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) в массив каунтерсигнерс (в настоящее время поддерживается только один каунтерсигнер).</span><span class="sxs-lookup"><span data-stu-id="ce9e6-107">Add the [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure to an array of countersigners (only one countersigner is currently supported).</span></span>
4.  <span data-ttu-id="ce9e6-108">Вызовите [**криптмсгкаунтерсигн**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) , чтобы добавить подпись или подписи другой стороны.</span><span class="sxs-lookup"><span data-stu-id="ce9e6-108">Call [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) to add the countersignature or countersignatures.</span></span>

<span data-ttu-id="ce9e6-109">Если все вызовы функций выполнены успешно, то исходное сообщение теперь имеет [*подпись*](../secgloss/c-gly.md) , входящую в непроверенный атрибут.</span><span class="sxs-lookup"><span data-stu-id="ce9e6-109">If all of the function calls succeed, the original message now has a [*countersignature*](../secgloss/c-gly.md) included as an unauthenticated attribute.</span></span>

<span data-ttu-id="ce9e6-110">**Выполнить скрепляющую подпись подписанное сообщение с помощью Криптмсгкаунтерсигненкодед**</span><span class="sxs-lookup"><span data-stu-id="ce9e6-110">**To countersign a signed message by using CryptMsgCountersignEncoded**</span></span>

1.  <span data-ttu-id="ce9e6-111">Вызовите [**криптмсгопентодекоде**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) , чтобы получить маркер подписанного сообщения.</span><span class="sxs-lookup"><span data-stu-id="ce9e6-111">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="ce9e6-112">Вызовите [**криптмсгжетпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) , чтобы получить закодированные сведения о подписанном сообщении.</span><span class="sxs-lookup"><span data-stu-id="ce9e6-112">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the encoded signer information of the signed message.</span></span>
3.  <span data-ttu-id="ce9e6-113">Инициализируйте [**\_ \_ \_ информационную структуру КМСГ для кодирования подписи**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) для каунтерсигнер.</span><span class="sxs-lookup"><span data-stu-id="ce9e6-113">Initialize a [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure for the countersigner.</span></span>
4.  <span data-ttu-id="ce9e6-114">Добавьте структуру [**КМСГ для \_ \_ кодирования подписи \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) в массив каунтерсигнерс (в настоящее время поддерживается только один каунтерсигнер).</span><span class="sxs-lookup"><span data-stu-id="ce9e6-114">Add the [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure to an array of countersigners (only one countersigner is currently supported).</span></span>
5.  <span data-ttu-id="ce9e6-115">Вызовите [**криптмсгкаунтерсигненкодед**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) , чтобы создать закодированный атрибут другой стороны.</span><span class="sxs-lookup"><span data-stu-id="ce9e6-115">Call [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) to create the encoded countersignature attribute.</span></span>
6.  <span data-ttu-id="ce9e6-116">Вызовите [**криптмсгконтрол**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) , чтобы добавить атрибут подписи к исходному сообщению в качестве атрибута, не прошедшего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="ce9e6-116">Call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) to add the countersignature attribute to the original message as an unauthenticated attribute.</span></span>

<span data-ttu-id="ce9e6-117">Если все вызовы функции выполнены, к исходному сообщению добавляется атрибут [*подписи другой стороны*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ce9e6-117">If all of the function calls succeed, a [*countersignature*](../secgloss/c-gly.md) attribute is added to the original message.</span></span>

 

 
