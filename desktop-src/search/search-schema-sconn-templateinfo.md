---
description: Этот необязательный &lt; &gt; элемент темплатеинфо указывает тип папки для отображения результатов запроса через этот соединитель поиска. У этого элемента нет атрибутов и только один обязательный дочерний элемент.
ms.assetid: fe42f589-5c47-4629-94eb-78dbaffa4112
title: Элемент Темплатеинфо (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c815d04e23f1e1af9582ad93ba08d118855676
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880383"
---
# <a name="templateinfo-element-search-connector-schema"></a>Элемент Темплатеинфо (схема соединителя поиска)

Этот необязательный &lt; &gt; элемент темплатеинфо указывает тип папки для отображения результатов запроса через этот соединитель поиска. У этого элемента нет атрибутов и только один обязательный дочерний элемент.

## <a name="syntax"></a>Синтаксис


```
<!-- templateInfo -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="templateInfo" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="folderType" minOccurs="0"/>
                    </xs:all>
                </xs:complexType>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                                                                   | Дочерние элементы                                                                     |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)](search-schema-searchconnectordescription.md) | [Элемент Фолдертипе (схема соединителя поиска)](search-schema-sconn-foldertype.md) |



 

## <a name="remarks"></a>Комментарии

если вы не укажете определенный тип папки в &lt; элементе темплатеинфо &gt; , Windows использует тип папки "общий соединитель поиска" {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.

## <a name="example-of-a-templateinfo-element"></a>Пример элемента Темплатеинфо


```
<!-- templateInfo -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



