---
description: Записи могут иметь атрибуты, зависящие от приложения, которые представляют собой последовательность пар имен или значений, представленных в виде XML-строки в элементе Псзаттрибутес в структуре одноранговой \_ записи.
ms.assetid: 2991af9b-da32-4915-b4d6-575e3faac04e
title: Схема атрибута записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3597369d7214b51b94a74b777315bb2ce2beb280232be5fb29571376ad3fc93e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612315"
---
# <a name="record-attribute-schema"></a>Схема атрибута записи

Записи могут иметь атрибуты, зависящие от приложения, которые представляют собой последовательность пар имен или значений, представленных в виде XML-строки в элементе **псзаттрибутес** в структуре [**одноранговой \_ записи**](/windows/desktop/api/P2P/ns-p2p-peer_record) . Атрибуты используются для фильтрации поиска записей, инициированного вызовами метода [**пирграупсеарчрекордс**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords), который принимает фильтр поиска XML, заданный в [формате запроса поиска записей](record-search-query-format.md) в качестве параметра.

Атрибут записи может иметь один из следующих трех типов:

-   **int** — это целочисленное значение.
-   **Date** — это значение DateTime, представленное в виде одного из стандартных форматов, описанных в разделе [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .
-   **строка** является строковым значением в Юникоде.

В следующем списке указаны имена атрибутов, зарезервированные для одноранговой инфраструктуры.

-   **пирластмодифиедби**
-   **пиркреаторид**
-   **пирластмодификатионтиме**
-   **пиррекордид**
-   **пиррекордтипе**
-   **пиркреатионтиме**
-   **пирластмодификатионтиме**

## <a name="example-of-defining-record-attributes"></a>Пример определения атрибутов записи

В следующем примере схемы показано, как определить атрибуты записи:

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
> Имена атрибутов должны быть последовательностями из буквенно-цифровых символов. В именах атрибутов нельзя использовать специальные символы, такие как дефисы ("-") и символы подчеркивания (" \_ ").

 

В следующем примере последовательности атрибутов XML содержатся пользовательские атрибуты **AuthenticationType** и **аусекспирес** , отображаемые в элементе **псзаттрибутес** [**одноранговой \_ записи**](/windows/desktop/api/P2P/ns-p2p-peer_record).

``` syntax
<attributes>
  <attribute name="AuthenticationType" type="string">Kerberos</attribute><attribute name="AuthExpires" type="date">2002-01-31</attribute>
<attributes>
```

 

 



