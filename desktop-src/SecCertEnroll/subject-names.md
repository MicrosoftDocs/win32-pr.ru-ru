---
description: Поле subject запроса на сертификат PKCS \# 10 содержит различающееся имя сущности, запрашивающей сертификат.
ms.assetid: 6c35ce42-07be-4d47-a14e-ed5a361dbe33
title: Имена субъектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 226c294e75477a3960cd0ad824a98b3556c34322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663626"
---
# <a name="subject-names"></a><span data-ttu-id="3299f-103">Имена субъектов</span><span class="sxs-lookup"><span data-stu-id="3299f-103">Subject Names</span></span>

<span data-ttu-id="3299f-104">Поле **subject** запроса на сертификат PKCS \# 10 содержит различающееся имя сущности, запрашивающей сертификат.</span><span class="sxs-lookup"><span data-stu-id="3299f-104">The **subject** field of a PKCS \#10 certificate request contains the distinguished name of the entity requesting the certificate.</span></span>

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}
```

<span data-ttu-id="3299f-105">Различающееся имя состоит из последовательности относительных различающихся имен (Рднс).</span><span class="sxs-lookup"><span data-stu-id="3299f-105">The distinguished name consists of a sequence of relative distinguished names (RDNs).</span></span> <span data-ttu-id="3299f-106">Каждый RDN состоит из набора атрибутов, и каждый атрибут состоит из идентификатора объекта и значения.</span><span class="sxs-lookup"><span data-stu-id="3299f-106">Each RDN consists of a set of attributes, and each attribute consists of an object identifier and a value.</span></span> <span data-ttu-id="3299f-107">Тип данных значения определяется структурой **директористринг** .</span><span class="sxs-lookup"><span data-stu-id="3299f-107">The data type of the value is identified by the **DirectoryString** structure.</span></span>

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       EncodedObjectID,
   value      ANY 
}

DirectoryString ::= CHOICE 
{
   teletexString           TeletexString (SIZE (1..MAX)),
   printableString         PrintableString (SIZE (1..MAX)),
   universalString         UniversalString (SIZE (1..MAX)),
   utf8String              UTF8String (SIZE (1..MAX)),
   bmpString               BMPString (SIZE (1..MAX)) 
}
```

<span data-ttu-id="3299f-108">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="3299f-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="3299f-109">Создание имени субъекта</span><span class="sxs-lookup"><span data-stu-id="3299f-109">Creating a Subject Name</span></span>](creating-a-subject-name.md)
-   [<span data-ttu-id="3299f-110">Кодирование имени субъекта</span><span class="sxs-lookup"><span data-stu-id="3299f-110">Encoding a Subject Name</span></span>](encoding-a-subject-name.md)

## <a name="related-topics"></a><span data-ttu-id="3299f-111">См. также</span><span class="sxs-lookup"><span data-stu-id="3299f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3299f-112">Запросы</span><span class="sxs-lookup"><span data-stu-id="3299f-112">Requests</span></span>](/windows/desktop/SecCrypto/requests)
</dt> </dl>

 

 
