---
description: '&lt;Элемент фолдертипе &gt; указывает идентификатор GUID для типа папки. Этот элемент необходим, если &lt; &gt; существует элемент темплатеинфо. У него нет атрибутов и дочерних элементов.'
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: Элемент Фолдертипе (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b693a1ff7007e6d63e108d16abe77ee421b3821a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882463"
---
# <a name="foldertype-element-search-connector-schema"></a>Элемент Фолдертипе (схема соединителя поиска)

&lt;Элемент фолдертипе &gt; указывает идентификатор GUID для типа папки. Этот элемент необходим, если &lt; &gt; существует элемент темплатеинфо. У него нет атрибутов и дочерних элементов.

## <a name="syntax"></a>Синтаксис


```
<!-- folderType -->
    <xs:element name="templateInfo" minOccurs="0">
      <xs:complexType>
        <xs:all>
          <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
      </xs:complexType>
    </xs:element>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                                         | Дочерние элементы |
|----------------------------------------------------------------------------------------|----------------|
| [Элемент Темплатеинфо (схема соединителя поиска)](search-schema-sconn-templateinfo.md) |                |



 

## <a name="remarks"></a>Комментарии

GUID по умолчанию — {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, общий тип папки для соединителей федеративного поиска (OpenSearch).

## <a name="example-of-a-foldertype-element"></a>Пример элемента Фолдертипе


```
<!-- templateInfo and folderType -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



