---
description: В этом разделе описывается схема описания свойства, используемая системой свойств оболочки.
ms.assetid: cac93c31-d90d-4116-b846-0cf593d1d56e
title: Основные сведения о схеме описания свойства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85dbb0f20c5c4a206069e80aa308a26908bf90ee0d00cf80712a342e834411e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554564"
---
# <a name="understanding-the-property-description-schema"></a>Основные сведения о схеме описания свойства

В этом разделе описывается схема описания свойства, используемая системой свойств оболочки.

появление новых функций для Windows Vista и более поздних версий требует, чтобы существующая система свойств оболочки была расширена до:

-   Поддержка расширенной и расширяемой системы описания свойств, которая предоставляет сведения о свойствах, включая отображаемые имена, тип, тип отображения, поведение сортировки и группирования, а также другие атрибуты, необходимые для представления и работы с этими свойствами.
-   Поддерживать список типов свойств (в сочетании с пользовательским интерфейсом, который может изменять эти типы в различных представлениях, таких как ListView, панель предварительного просмотра, диалоговые окна свойств и т. д.), которые могут быть связаны с различными свойствами.
-   Укажите списки с описаниями свойств, которые определяют набор свойств, отображаемых в различных представлениях.
-   Предоставьте упрощенный интерфейс [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore), чтобы обработчики свойств могли быть написаны проще, поэтому свойства могут быть сохранены в файлах.
-   Поддержка обработчиков свойств, не являющихся файлами, для предоставления свойств в представлении.

Эти функции достигаются на архитектуре, которая предоставляет абстрактный доступ к свойствам элемента оболочки. Эта абстракция называется системой свойств оболочки.

-   [Что такое схема описания свойств?](#what-is-the-property-description-schema)
-   [Зачем использовать схему?](#why-use-a-schema)
-   [Каковы основные компоненты схемы?](#what-are-the-major-schema-parts)
-   [изменения для Windows 7](#changes-for-windows-7)
-   [Связанные темы](#related-topics)

## <a name="what-is-the-property-description-schema"></a>Что такое схема описания свойств?

Подсистема схемы состоит из следующих компонентов:

-   Один или несколько файлов схемы. пропдеск, определяющих описания свойств. Схема описания свойства определяется в коллекции файлов схемы XML (с помощью расширения файла пропдеск) во время выполнения в системе. Эти файлы загружаются с отложенной загрузкой, если они требуются для части системы свойств.
-   Кэш схемы в памяти, используемый для хранения проанализированных файлов схемы, включая все описания свойств, появившиеся в подсистеме. Нет необходимости выполнять повторное синтаксический анализ файлов конфигурации. пропдеск, описывающих схему. Дополнительные сведения см. в разделе [**псрегистерпропертисчема**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**псунрегистерпропертисчема**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema)и [**псрефрешпропертисчема**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).
-   Объект подсистемы, реализующий [**ипропертисистем**](/windows/win32/api/propsys/nn-propsys-ipropertysystem), который используется для получения описаний свойств или работы с ними.
-   Объект подсистемы, реализующий [**ипропертидескриптион**](/windows/win32/api/propsys/nn-propsys-ipropertydescription), который используется для информирования и обработки данных в зависимости от описания свойства.
-   Объект подсистемы, реализующий [**ипропертидескриптионлист**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), который используется как коллекция описаний свойств.

> [!Note]  
> Необходимо добавить `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` в корневой элемент Schema файлов пропдеск.

 

## <a name="why-use-a-schema"></a>Зачем использовать схему?

Сами по себе свойства не являются строго типизированными. Компонент может присвоить числовое значение свойству System. Author или параметру [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) Date-метка к свойству System. Music. албумтитле, и, не требуя дальнейшего применения или рекомендаций, хранилище свойств разрешит его. Итак, нам требовалось понятие «счематизе» свойств, которое приводит нас к подсистеме схемы.

## <a name="what-are-the-major-schema-parts"></a>Каковы основные компоненты схемы?

Схема описания свойства, используемая системой свойств оболочки, состоит из одного [пропертидескриптионлист](./propdesc-schema-propertydescriptionlist.md) элемента, а также атрибута *schemaVersion* , указывающего версию этого формата определения схемы. Примечание. значение должно быть "1,0".


```
<!-- schema -->
    <xs:element name="schema">
      <xs:complexType>
        <xs:sequence>
          <xs:element ref="propertyDescriptionList" minOccurs="1" maxOccurs="1"/>
        </xs:sequence>
        <xs:attribute name="schemaVersion"  type="xs:string"/>
      </xs:complexType>
    </xs:element>
```



[Пропертидескриптионлист](./propdesc-schema-propertydescriptionlist.md) состоит из одного или нескольких элементов [пропертидескриптион](./propdesc-schema-propertydescription.md) , а также атрибутов *издателя* и *продукта* .


```
<!-- propertyDescriptionList -->
    <xs:element name="propertyDescriptionList">
      <xs:complexType>
        <xs:sequence>
          <xs:element ref="propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product"   type="xs:string"/>
      </xs:complexType>
    </xs:element>
```



[Пропертидескриптион](./propdesc-schema-propertydescription.md) состоит из одного [сеарчинфо](./propdesc-schema-searchinfo.md) и нуля или одного элемента [лабелинфо](./propdesc-schema-labelinfo.md), [typeInfo](./propdesc-schema-typeinfo.md)и [displayInfo](./propdesc-schema-displayinfo.md) , а также атрибутов *форматид*, *PropID*, *пропстр* и *Name* .

Должен быть один элемент [пропертидескриптион](./propdesc-schema-propertydescription.md) для каждого уникального канонического имени свойства, которое должно быть доступно в системе. Длина строковых атрибутов ограничена 512 символами. Значения длиннее 512 символов усекаются.


```
<!-- propertyDescription -->
    <xs:element name="propertyDescription">
      <xs:complexType>
        <xs:all>
          <xs:element name="description"    type="xs:string" minOccurs="0" maxOccurs="1"/>
          <xs:element ref="searchInfo"   minOccurs="1" maxOccurs="1"/>
          <xs:element ref="labelInfo"    minOccurs="0" maxOccurs="1"/>
          <xs:element ref="typeInfo"     minOccurs="0" maxOccurs="1"/>
          <xs:element ref="displayInfo"  minOccurs="0" maxOccurs="1"/>
        </xs:all>
        <xs:attribute name="formatID"  type="upcase-uuid" use="required""/>
        <xs:attribute name="propID"    type="xs:nonNegativeInteger" use="required""/>
        <xs:attribute name="name"      type="canonical-name" use="required"/>
      </xs:complexType>
    </xs:element>
```



## <a name="changes-for-windows-7"></a>изменения для Windows 7

схема описания свойства была изменена для Windows 7. Это некритические изменения. если элемент свойства или атрибут больше не поддерживается в Windows 7, операционная система Windows 7 не учитывает элемент или атрибуты Windows Vista. аналогичным образом Windows Vista также игнорирует новые элементы или атрибуты свойств Windows 7.

однако обновление пользовательских свойств для Windows 7 рекомендуется для более эффективного и более стабильного взаимодействия с пользователем.

Ниже перечислены новые элементы и атрибуты.

-   элементы [релатедпропертинфо](./propdesc-schema-relatedpropertyinfo.md) и [relatedProperty](./propdesc-schema-relatedproperty.md)
-   элемент [Image](./propdesc-schema-image.md)
-   атрибут мнемоник элемента [сеарчинфо](./propdesc-schema-searchinfo.md)
-   атрибут мнемоник элемента [enum](./propdesc-schema-enum.md)
-   атрибут Сеарчраввалуе элемента [typeInfo](./propdesc-schema-typeinfo.md)

Изменились следующие элементы и атрибуты:

-   элементы [енумератедлист](./propdesc-schema-enumeratedlist.md), [enum](./propdesc-schema-enum.md)и [енумранже](./propdesc-schema-enumrange.md)
-   [дравконтрол](./propdesc-schema-drawcontrol.md) , элемент
-   [едитконтрол](./propdesc-schema-editcontrol.md) , элемент
-   атрибут propID элемента [пропертидескриптион](./propdesc-schema-propertydescription.md)
-   атрибут Колумниндекстипе элемента [сеарчинфо](./propdesc-schema-searchinfo.md)

Удалены следующие элементы и атрибуты:

-   [куериконтрол](./propdesc-schema-querycontrol.md) , элемент
-   атрибут, который является запрашиваемым элементом [typeInfo](./propdesc-schema-typeinfo.md)
-   атрибут Инклудеинфуллтексткуери элемента [typeInfo](./propdesc-schema-typeinfo.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[пропертидескриптион](./propdesc-schema-propertydescription.md)
</dt> <dt>

[сеарчинфо](./propdesc-schema-searchinfo.md)
</dt> <dt>

[лабелинфо](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[булеанформат](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[енумератедлист](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[дравконтрол](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[едитконтрол](./propdesc-schema-editcontrol.md)
</dt> <dt>

[филтерконтрол](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[куериконтрол](./propdesc-schema-querycontrol.md)
</dt> <dt>

[image](./propdesc-schema-image.md)
</dt> </dl>

 

 
