---
description: <folderType>Элемент указывает идентификатор GUID для типа папки. Этот элемент обязателен <templateInfo> , если элемент существует, в противном случае — необязательный. Этот элемент не имеет атрибутов и не содержит дочерних элементов.
title: Элемент Фолдертипе (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 240550F0-B6AC-470e-8BF1-DB5A4068226B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8d35f09a10cc88ae3873a507b6fa7000812503890240ce0b808ffecc84f23fd8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883954"
---
# <a name="foldertype-element-library-schema"></a>Элемент Фолдертипе (схема библиотеки)

<folderType>Элемент указывает идентификатор GUID для типа папки. Этот элемент обязателен <templateInfo> , если элемент существует, в противном случае — необязательный. Этот элемент не имеет атрибутов и не содержит дочерних элементов.

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



| Родительский элемент                                                           | Дочерние элементы |
|--------------------------------------------------------------------------|----------------|
| [Элемент Темплатеинфо (схема библиотеки)](schema-library-templateinfo.md) |                |



 

## <a name="remarks"></a>Remarks

задание типа папки определяет столбцы и сведения, отображаемые в Windows Explorer по умолчанию. Идентификаторы типов папок ([**фолдертипеид**](foldertypeid.md)) являются идентификаторами GUID, определенными в шлгуид. h. В следующей таблице перечислены идентификаторы GUID общих типов папок.



| Тип папки      | GUID                                   |
|------------------|----------------------------------------|
| Универсальная библиотека  | {5f4eab9a-6833-4f61-899d-31cf46979d49} |
| Библиотеки пользователей  | {C4D98F09-6124-4fe0-9942-826416082DA9} |
| Папка документов | {7D49D726-3C21-4F05-99AA-FDC2C9474656} |
| Папка "рисунки"  | {B3690E58-E961-423B-B687-386EBFD83239} |
| Папка "видео"    | {5fa96407-7e77-483c-ac93-691d05850de8} |
| Папка "игры"     | {b689b0d0-76d3-4cbb-87f7-585d0e0ce070} |
| Папка "Музыка"     | {94d6ddcc-4a68-4175-a374-bd584a510b78} |
| Контакты         | {DE2B70EC-9BF7-4A93-BD3D-243F7881D492} |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Элемент Иконреференце (схема библиотеки)](schema-library-iconreference.md)
</dt> <dt>

[Элемент Ислибрарипиннед (схема библиотеки)](schema-library-islibrarypinned.md)
</dt> <dt>

[Элемент Либраридескриптион (схема библиотеки)](schema-librarydescription.md)
</dt> <dt>

[Элемент Name (схема библиотеки)](schema-library-name.md)
</dt> <dt>

[Элемент ownerSID (схема библиотеки)](schema-library-ownersid.md)
</dt> <dt>

[Элемент Пропертисторе (схема библиотеки)](schema-library-propertystore.md)
</dt> <dt>

[Элемент Сеарчконнектордескриптион (схема библиотеки)](schema-library-searchconnectordescription.md)
</dt> <dt>

[Элемент Сеарчконнектордескриптионлист (схема библиотеки)](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[Элемент Темплатеинфо (схема библиотеки)](schema-library-templateinfo.md)
</dt> <dt>

[Элемент Version (схема библиотеки)](schema-library-version.md)
</dt> </dl>

 

 



