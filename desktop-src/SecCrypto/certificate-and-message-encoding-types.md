---
description: Для многих функций требуются типы кодирования сертификатов или сообщений.
ms.assetid: 97b25435-aec2-4fdb-a4c6-89ec2e26f51d
title: Типы кодировки сертификатов и сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3193b321d27892f8df9535ef81b8a988bf558e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497274"
---
# <a name="certificate-and-message-encoding-types"></a><span data-ttu-id="eda97-103">Типы кодировки сертификатов и сообщений</span><span class="sxs-lookup"><span data-stu-id="eda97-103">Certificate and Message Encoding Types</span></span>

<span data-ttu-id="eda97-104">Для многих функций требуются [*типы кодирования*](../secgloss/m-gly.md)сертификатов или сообщений.</span><span class="sxs-lookup"><span data-stu-id="eda97-104">Many of the functions require certificate or [*message encoding types*](../secgloss/m-gly.md).</span></span> <span data-ttu-id="eda97-105">Этот тип кодирования, возможно **, содержит как сертификаты, так** и типы кодирования сообщений.</span><span class="sxs-lookup"><span data-stu-id="eda97-105">This encoding type is a **DWORD**, possibly containing both the certificate and message encoding types.</span></span> <span data-ttu-id="eda97-106">Тип кодирования сертификата хранится в младшем слове.</span><span class="sxs-lookup"><span data-stu-id="eda97-106">The certificate encoding type is stored in the low-order word.</span></span> <span data-ttu-id="eda97-107">Тип кодирования сообщений хранится в слове в высоком порядке.</span><span class="sxs-lookup"><span data-stu-id="eda97-107">The message encoding type is stored in the high-order word.</span></span> <span data-ttu-id="eda97-108">Некоторым функциям или полям структуры требуется только один из типов кодирования, но всегда допустимо указывать оба типа кодировки.</span><span class="sxs-lookup"><span data-stu-id="eda97-108">Some functions or structure fields require only one of the encoding types, but it is always acceptable to specify both encoding types.</span></span> <span data-ttu-id="eda97-109">Пример, в котором указываются оба типа кодирования, см. в разделе [ \# включения и \# Определение](-includes-and--defines.md).</span><span class="sxs-lookup"><span data-stu-id="eda97-109">For an example specifying both encoding types, see [\#includes and \#defines](-includes-and--defines.md).</span></span>

<span data-ttu-id="eda97-110">Для указания требуемых типов кодировки используется следующее соглашение об именовании параметров.</span><span class="sxs-lookup"><span data-stu-id="eda97-110">The following parameter naming convention is used to indicate the encoding types required.</span></span>



| <span data-ttu-id="eda97-111">Имя</span><span class="sxs-lookup"><span data-stu-id="eda97-111">Name</span></span>                       | <span data-ttu-id="eda97-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eda97-112">Comments</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eda97-113">*двмсгандцертенкодингтипе*</span><span class="sxs-lookup"><span data-stu-id="eda97-113">*dwMsgAndCertEncodingType*</span></span> | <span data-ttu-id="eda97-114">Требуются оба типа кодирования.</span><span class="sxs-lookup"><span data-stu-id="eda97-114">Both encoding types are required.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="eda97-115">*двмсженкодингтипе*</span><span class="sxs-lookup"><span data-stu-id="eda97-115">*dwMsgEncodingType*</span></span>        | <span data-ttu-id="eda97-116">Требуется только тип кодирования сообщений.</span><span class="sxs-lookup"><span data-stu-id="eda97-116">Only the message encoding type is required.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="eda97-117">*двцертенкодингтипе*</span><span class="sxs-lookup"><span data-stu-id="eda97-117">*dwCertEncodingType*</span></span>       | <span data-ttu-id="eda97-118">Требуется только тип кодирования сертификата.</span><span class="sxs-lookup"><span data-stu-id="eda97-118">Only the certificate encoding type is required.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="eda97-119">*двенкодингтипе*</span><span class="sxs-lookup"><span data-stu-id="eda97-119">*dwEncodingType*</span></span>           | <span data-ttu-id="eda97-120">Требуется указать тип сообщения или кодировки сертификата.</span><span class="sxs-lookup"><span data-stu-id="eda97-120">Either a message or certificate encoding type is required.</span></span> <span data-ttu-id="eda97-121">Если слово низкого порядка, содержащее тип кодирования сертификата, отлично от нуля, то используется.</span><span class="sxs-lookup"><span data-stu-id="eda97-121">If the low-order word containing the certificate encoding type is nonzero, then it is used.</span></span> <span data-ttu-id="eda97-122">В противном случае используется слово высокого порядка, содержащее тип кодирования сообщений.</span><span class="sxs-lookup"><span data-stu-id="eda97-122">Otherwise, the high-order word containing the message encoding type is used.</span></span> <span data-ttu-id="eda97-123">Если указаны оба значения, используется тип кодирования сертификата в слове нижнего порядка.</span><span class="sxs-lookup"><span data-stu-id="eda97-123">If both are specified, the certificate encoding type in the low-order word is used.</span></span> |



 

<span data-ttu-id="eda97-124">В следующей таблице показаны определенные типы кодировки.</span><span class="sxs-lookup"><span data-stu-id="eda97-124">Currently defined encoding types are shown in the following table.</span></span>



| <span data-ttu-id="eda97-125">Тип кодировки</span><span class="sxs-lookup"><span data-stu-id="eda97-125">Encoding type</span></span>          | <span data-ttu-id="eda97-126">Значение</span><span class="sxs-lookup"><span data-stu-id="eda97-126">Value</span></span>      |
|------------------------|------------|
| <span data-ttu-id="eda97-127">\_ \_ Шифрование кодировки ASN</span><span class="sxs-lookup"><span data-stu-id="eda97-127">CRYPT\_ASN\_ENCODING</span></span>   | <span data-ttu-id="eda97-128">0x00000001</span><span class="sxs-lookup"><span data-stu-id="eda97-128">0x00000001</span></span> |
| <span data-ttu-id="eda97-129">\_ \_ Кодировка X509 ASN</span><span class="sxs-lookup"><span data-stu-id="eda97-129">X509\_ASN\_ENCODING</span></span>    | <span data-ttu-id="eda97-130">0x00000001</span><span class="sxs-lookup"><span data-stu-id="eda97-130">0x00000001</span></span> |
| <span data-ttu-id="eda97-131">\_ \_ Кодировка PKCS 7 ASN \_</span><span class="sxs-lookup"><span data-stu-id="eda97-131">PKCS\_7\_ASN\_ENCODING</span></span> | <span data-ttu-id="eda97-132">0x00010000</span><span class="sxs-lookup"><span data-stu-id="eda97-132">0x00010000</span></span> |



 

 

 
