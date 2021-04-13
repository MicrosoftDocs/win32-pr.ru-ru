---
title: Сложный тип FilterType
description: Определяет фильтр данных, используемый сеансом для фильтрации событий на основе данных событий.
ms.assetid: f2874b3f-cf3a-4dd9-b914-6adaac33cf7b
keywords:
- Журнал событий сложных типов FilterType
topic_type:
- apiref
api_name:
- FilterType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ef3d80b8cb5347c1adf0e2b21a745e4d4f5fae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493167"
---
# <a name="filtertype-complex-type"></a>Сложный тип FilterType

Определяет фильтр данных, используемый сеансом для фильтрации событий на основе данных событий.

``` syntax
<xs:complexType name="FilterType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="version"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="tid"
                type="token"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Атрибуты



| Имя    | Тип                                                              | Описание                                                                                                                                                                                                                                      |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message | [**стртаблереф**](eventmanifestschema-strtableref-simpletype.md) | Локализованное описание для фильтра. Строка сообщения ссылается на локализованную строку в разделе " [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) " манифеста.<br/>                                   |
| name    | **QName**                                                         | Имя, идентифицирующее фильтр.<br/>                                                                                                                                                                                                    |
| символ  | [**ксимболтипе**](eventmanifestschema-csymboltype-simpletype.md) | Символ, используемый для ссылки на фильтр в приложении. [**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ, чтобы создать константу для фильтра в файле заголовка, создаваемом компилятором.<br/> |
| tid     | token                                                             | Идентификатор шаблона, описывающий данные фильтра, которые сеанс передает поставщику, когда он включает поставщик.<br/>                                                                                                            |
| значение   | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Целочисленное значение, уникально идентифицирующее фильтр в списке фильтров, которые вы определяете.<br/>                                                                                                                                      |
| version | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Целочисленное значение, определяющее эту версию фильтра. Если не указано, значение равно нулю.<br/>                                                                                                                                     |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



 

 





