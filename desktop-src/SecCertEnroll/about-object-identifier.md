---
description: Тип данных идентификатора объекта кодируется в TLV-Triplet, который начинается со значения тега 0x06.
ms.assetid: 42c015c8-3de1-4482-bf27-b19c422b8cdb
title: ИДЕНТИФИКАТОР ОБЪЕКТА
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6cc81169968bfb3be5a49b0f30b8171cd904bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264483"
---
# <a name="object-identifier"></a><span data-ttu-id="20769-103">ИДЕНТИФИКАТОР ОБЪЕКТА</span><span class="sxs-lookup"><span data-stu-id="20769-103">OBJECT IDENTIFIER</span></span>

<span data-ttu-id="20769-104">Тип данных **идентификатора объекта** кодируется в TLV-Triplet, который начинается со значения **тега** 0x06.</span><span class="sxs-lookup"><span data-stu-id="20769-104">The **OBJECT IDENTIFIER** data type is encoded into a TLV triplet that begins with a **Tag** value of 0x06.</span></span> <span data-ttu-id="20769-105">Каждое целочисленное значение идентификатора объекта в точечно-десятичной кодировке кодируется в соответствии со следующими правилами:</span><span class="sxs-lookup"><span data-stu-id="20769-105">Each integer of a dotted decimal object identifier (OID) is encoded according to the following rules:</span></span>

-   <span data-ttu-id="20769-106">Первые два узла OID кодируются на один байт.</span><span class="sxs-lookup"><span data-stu-id="20769-106">The first two nodes of the OID are encoded onto a single byte.</span></span> <span data-ttu-id="20769-107">Первый узел умножается на десятичный 40, а результат добавляется к значению второго узла.</span><span class="sxs-lookup"><span data-stu-id="20769-107">The first node is multiplied by the decimal 40 and the result is added to the value of the second node.</span></span>
-   <span data-ttu-id="20769-108">Значения узлов, меньшие или равные 127, кодируются в одном байте.</span><span class="sxs-lookup"><span data-stu-id="20769-108">Node values less than or equal to 127 are encoded on one byte.</span></span>
-   <span data-ttu-id="20769-109">Значения узлов, которые больше или равны 128, кодируются в нескольких байтах.</span><span class="sxs-lookup"><span data-stu-id="20769-109">Node values greater than or equal to 128 are encoded on multiple bytes.</span></span> <span data-ttu-id="20769-110">Бит 7 самого левого байта имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="20769-110">Bit 7 of the leftmost byte is set to one.</span></span> <span data-ttu-id="20769-111">Биты 0 – 6 каждого байта содержат закодированное значение.</span><span class="sxs-lookup"><span data-stu-id="20769-111">Bits 0 through 6 of each byte contains the encoded value.</span></span>

<span data-ttu-id="20769-112">Эти моменты показаны на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="20769-112">These points are shown by the following illustration.</span></span>

![Кодировка der для типа данных идентификатора объекта](images/der-tlv-oid.png)

<span data-ttu-id="20769-114">В следующем примере показано, как атрибут **ClientID** кодируется в запросе на сертификат.</span><span class="sxs-lookup"><span data-stu-id="20769-114">The following example shows how the **ClientId** attribute is encoded in a certificate request.</span></span>

``` syntax
06 09                                ; OBJECT_ID (9 Bytes)
|  2b 06 01 04 01 82 37 15  14       ;   1.3.6.1.4.1.311.21.20 
31 4a                                ; SET (4a Bytes)
   30 48                             ; SEQUENCE (48 Bytes)
      02 01                          ; INTEGER (1 Bytes)
      |  09
      0c 23                          ; UTF8_STRING (23 Bytes)
      |  76 69 63 68 33 64 2e 6a     ;   vich3d.j
      |  64 6f 6d 63 73 63 2e 6e     ;   domcsc.n
      |  74 74 65 73 74 2e 6d 69     ;   ttest.mi
      |  63 72 6f 73 6f 66 74 2e     ;   crosoft.
      |  63 6f 6d                    ;   com
      0c 15                          ; UTF8_STRING (15 Bytes)
      |  4a 44 4f 4d 43 53 43 5c     ;   JDOMCSC\
      |  61 64 6d 69 6e 69 73 74     ;   administ
      |  72 61 74 6f 72              ;   rator
      0c 07                          ; UTF8_STRING (7 Bytes)
         63 65 72 74 72 65 71        ;   certreq
```

 

 



