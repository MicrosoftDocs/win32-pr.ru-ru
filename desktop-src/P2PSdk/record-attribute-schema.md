---
description: Записи могут иметь атрибуты, зависящие от приложения, которые представляют собой последовательность пар имен или значений, представленных в виде XML-строки в элементе Псзаттрибутес в структуре одноранговой \_ записи.
ms.assetid: 2991af9b-da32-4915-b4d6-575e3faac04e
title: Схема атрибута записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefa8c4c8b00b09e9c8cb988088af645e9f9c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664261"
---
# <a name="record-attribute-schema"></a><span data-ttu-id="68db2-103">Схема атрибута записи</span><span class="sxs-lookup"><span data-stu-id="68db2-103">Record Attribute Schema</span></span>

<span data-ttu-id="68db2-104">Записи могут иметь атрибуты, зависящие от приложения, которые представляют собой последовательность пар имен или значений, представленных в виде XML-строки в элементе **псзаттрибутес** в структуре [**одноранговой \_ записи**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="68db2-104">Records can have application-specific attributes that are a sequence of name or value pairs represented as an XML string in the **pszAttributes** member of the [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span> <span data-ttu-id="68db2-105">Атрибуты используются для фильтрации поиска записей, инициированного вызовами метода [**пирграупсеарчрекордс**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords), который принимает фильтр поиска XML, заданный в [формате запроса поиска записей](record-search-query-format.md) в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="68db2-105">The attributes are used to filter a record search initiated by calls to [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords), which takes an XML search filter specified in [Record Search Query Format](record-search-query-format.md) as a parameter.</span></span>

<span data-ttu-id="68db2-106">Атрибут записи может иметь один из следующих трех типов:</span><span class="sxs-lookup"><span data-stu-id="68db2-106">A record attribute can be one of the following three types:</span></span>

-   <span data-ttu-id="68db2-107">**int** — это целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="68db2-107">**int** is an integer value.</span></span>
-   <span data-ttu-id="68db2-108">**Date** — это значение DateTime, представленное в виде одного из стандартных форматов, описанных в разделе [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .</span><span class="sxs-lookup"><span data-stu-id="68db2-108">**date** is a datetime value represented as one of the standard formats described at [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime).</span></span>
-   <span data-ttu-id="68db2-109">**строка** является строковым значением в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="68db2-109">**string** is a Unicode string value.</span></span>

<span data-ttu-id="68db2-110">В следующем списке указаны имена атрибутов, зарезервированные для одноранговой инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="68db2-110">The following list identifies the specific attribute names that are reserved by the Peer Infrastructure:</span></span>

-   <span data-ttu-id="68db2-111">**пирластмодифиедби**</span><span class="sxs-lookup"><span data-stu-id="68db2-111">**peerlastmodifiedby**</span></span>
-   <span data-ttu-id="68db2-112">**пиркреаторид**</span><span class="sxs-lookup"><span data-stu-id="68db2-112">**peercreatorid**</span></span>
-   <span data-ttu-id="68db2-113">**пирластмодификатионтиме**</span><span class="sxs-lookup"><span data-stu-id="68db2-113">**peerlastmodificationtime**</span></span>
-   <span data-ttu-id="68db2-114">**пиррекордид**</span><span class="sxs-lookup"><span data-stu-id="68db2-114">**peerrecordid**</span></span>
-   <span data-ttu-id="68db2-115">**пиррекордтипе**</span><span class="sxs-lookup"><span data-stu-id="68db2-115">**peerrecordtype**</span></span>
-   <span data-ttu-id="68db2-116">**пиркреатионтиме**</span><span class="sxs-lookup"><span data-stu-id="68db2-116">**peercreationtime**</span></span>
-   <span data-ttu-id="68db2-117">**пирластмодификатионтиме**</span><span class="sxs-lookup"><span data-stu-id="68db2-117">**peerlastmodificationtime**</span></span>

## <a name="example-of-defining-record-attributes"></a><span data-ttu-id="68db2-118">Пример определения атрибутов записи</span><span class="sxs-lookup"><span data-stu-id="68db2-118">Example of Defining Record Attributes</span></span>

<span data-ttu-id="68db2-119">В следующем примере схемы показано, как определить атрибуты записи:</span><span class="sxs-lookup"><span data-stu-id="68db2-119">The following schema example shows you how to define record attributes:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <xs:simpleType name="alphanum">
       <xs:restriction base="xs:string">
          <xs:pattern value="\c+" />
       </xs:restriction>
   </xs:simpleType>
   <xs:complexType name="attributeType">
       <xs:simpleContent>
          <xs:extension base="xs:string">
                <xs:attribute name="name" type="alphanum" />
                <xs:attribute name="type">
                    <xs:simpleType>
                        <xs:restriction base="alphanum">
                           <xs:enumeration value="string"/>
                           <xs:enumeration value="date"/>
                           <xs:enumeration value="int"/>
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
           </xs:extension>
       </xs:simpleContent>
    </xs:complexType>
    <xs:element name="attributes">
       <xs:complexType>
           <xs:sequence>
                <xs:element name="attribute" type="attributeType" minOccurs="0" maxOccurs="unbounded" />
           </xs:sequence>
       </xs:complexType>
    </xs:element>
</xs:schema>  
```

> [!Note]  
> <span data-ttu-id="68db2-120">Имена атрибутов должны быть последовательностями из буквенно-цифровых символов.</span><span class="sxs-lookup"><span data-stu-id="68db2-120">Attribute names must be sequences of alphanumeric characters.</span></span> <span data-ttu-id="68db2-121">В именах атрибутов нельзя использовать специальные символы, такие как дефисы ("-") и символы подчеркивания (" \_ ").</span><span class="sxs-lookup"><span data-stu-id="68db2-121">Special characters like hyphens ("-") and underscores ("\_") are not allowed in an attribute name.</span></span>

 

<span data-ttu-id="68db2-122">В следующем примере последовательности атрибутов XML содержатся пользовательские атрибуты **AuthenticationType** и **аусекспирес** , отображаемые в элементе **псзаттрибутес** [**одноранговой \_ записи**](/windows/desktop/api/P2P/ns-p2p-peer_record).</span><span class="sxs-lookup"><span data-stu-id="68db2-122">The following example of an XML attribute sequence contains the custom **AuthenticationType** and **AuthExpires** attributes that appear in the **pszAttributes** member of [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record).</span></span>

``` syntax
<attributes>
  <attribute name="AuthenticationType" type="string">Kerberos</attribute><attribute name="AuthExpires" type="date">2002-01-31</attribute>
<attributes>
```

 

 



