---
description: <folderType>Элемент указывает идентификатор GUID для папки типа. Этот элемент обязателен, если <templateInfo> элемент существует. У него нет атрибутов и дочерних элементов.
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: Элемент Фолдертипе (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6b9d5682a85126a467c051b9f1103a4ac10f2f6936cc24dd4438a5f8c75d44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862603"
---
# <a name="foldertype-element-search-connector-schema"></a>Элемент Фолдертипе (схема соединителя поиска)

<folderType>Элемент указывает идентификатор GUID для папки типа. Этот элемент обязателен, если <templateInfo> элемент существует. У него нет атрибутов и дочерних элементов.

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



 

## <a name="remarks"></a>Remarks

GUID по умолчанию — {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, общий тип папки для соединителей федеративного поиска (OpenSearch).

## <a name="example-of-a-foldertype-element"></a>Пример элемента Фолдертипе


```
<!-- templateInfo and folderType -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



