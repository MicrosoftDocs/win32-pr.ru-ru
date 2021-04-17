---
description: Этот необязательный <templateInfo> элемент указывает тип папки для отображения результатов запроса через этот соединитель поиска. У этого элемента нет атрибутов и только один обязательный дочерний элемент.
ms.assetid: fe42f589-5c47-4629-94eb-78dbaffa4112
title: Элемент Темплатеинфо (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fd28780689b4d544f251bbaf1542bc379ecdaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692164"
---
# <a name="templateinfo-element-search-connector-schema"></a>Элемент Темплатеинфо (схема соединителя поиска)

Этот необязательный <templateInfo> элемент указывает тип папки для отображения результатов запроса через этот соединитель поиска. У этого элемента нет атрибутов и только один обязательный дочерний элемент.

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

Если в элементе не указан определенный тип папки <templateInfo> , Windows использует тип папки "общий соединитель поиска" {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.

## <a name="example-of-a-templateinfo-element"></a>Пример элемента Темплатеинфо


```
<!-- templateInfo -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



