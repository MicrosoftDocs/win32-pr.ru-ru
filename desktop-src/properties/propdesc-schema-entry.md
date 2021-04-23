---
description: В этом разделе описывается схема описания свойства, используемая системой свойств оболочки.
ms.assetid: cac93c31-d90d-4116-b846-0cf593d1d56e
title: Основные сведения о схеме описания свойства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51d9e7c2b6fb4b599f977c0c49ad1cb2514fe8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080559"
---
# <a name="understanding-the-property-description-schema"></a><span data-ttu-id="f07d4-103">Основные сведения о схеме описания свойства</span><span class="sxs-lookup"><span data-stu-id="f07d4-103">Understanding the Property Description Schema</span></span>

<span data-ttu-id="f07d4-104">В этом разделе описывается схема описания свойства, используемая системой свойств оболочки.</span><span class="sxs-lookup"><span data-stu-id="f07d4-104">This topic introduces the property description schema used by the Shell property system.</span></span>

<span data-ttu-id="f07d4-105">В новых функциях Windows Vista и более поздних версий требуется, чтобы существующая система свойств оболочки была расширена до:</span><span class="sxs-lookup"><span data-stu-id="f07d4-105">The introduction of new features for Windows Vista and later required that the existing Shell property system be extended to:</span></span>

-   <span data-ttu-id="f07d4-106">Поддержка расширенной и расширяемой системы описания свойств, которая предоставляет сведения о свойствах, включая отображаемые имена, тип, тип отображения, поведение сортировки и группирования, а также другие атрибуты, необходимые для представления и работы с этими свойствами.</span><span class="sxs-lookup"><span data-stu-id="f07d4-106">Support a rich and extensible property description system that provides information about properties including display names, type, display type, sort and group behavior, and other attributes needed to present and operate over the properties.</span></span>
-   <span data-ttu-id="f07d4-107">Поддерживать список типов свойств (в сочетании с пользовательским интерфейсом, который может изменять эти типы в различных представлениях, таких как ListView, панель предварительного просмотра, диалоговые окна свойств и т. д.), которые могут быть связаны с различными свойствами.</span><span class="sxs-lookup"><span data-stu-id="f07d4-107">Support a stock list of property types (combined with UI that can edit those types in different views like the listview, preview pane, property dialogs, and so on) that can be associated with various properties.</span></span>
-   <span data-ttu-id="f07d4-108">Укажите списки с описаниями свойств, которые определяют набор свойств, отображаемых в различных представлениях.</span><span class="sxs-lookup"><span data-stu-id="f07d4-108">Supply property description lists, which define the set of properties displayed in various views.</span></span>
-   <span data-ttu-id="f07d4-109">Предоставьте упрощенный интерфейс [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore), чтобы обработчики свойств могли быть написаны проще, поэтому свойства могут быть сохранены в файлах.</span><span class="sxs-lookup"><span data-stu-id="f07d4-109">Provide a simplified interface, [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore), so property handlers can be written more easily and so properties can be persisted to files.</span></span>
-   <span data-ttu-id="f07d4-110">Поддержка обработчиков свойств, не являющихся файлами, для предоставления свойств в представлении.</span><span class="sxs-lookup"><span data-stu-id="f07d4-110">Support for non-file property handlers to expose properties in the view.</span></span>

<span data-ttu-id="f07d4-111">Эти функции достигаются на архитектуре, которая предоставляет абстрактный доступ к свойствам элемента оболочки.</span><span class="sxs-lookup"><span data-stu-id="f07d4-111">These features are achieved on an architecture that provides abstract access to the properties of a Shell item.</span></span> <span data-ttu-id="f07d4-112">Эта абстракция называется системой свойств оболочки.</span><span class="sxs-lookup"><span data-stu-id="f07d4-112">This abstraction is called the Shell property system.</span></span>

-   [<span data-ttu-id="f07d4-113">Что такое схема описания свойств?</span><span class="sxs-lookup"><span data-stu-id="f07d4-113">What Is the Property Description Schema?</span></span>](#what-is-the-property-description-schema)
-   [<span data-ttu-id="f07d4-114">Зачем использовать схему?</span><span class="sxs-lookup"><span data-stu-id="f07d4-114">Why Use a Schema?</span></span>](#why-use-a-schema)
-   [<span data-ttu-id="f07d4-115">Каковы основные компоненты схемы?</span><span class="sxs-lookup"><span data-stu-id="f07d4-115">What Are the Major Schema Parts?</span></span>](#what-are-the-major-schema-parts)
-   [<span data-ttu-id="f07d4-116">Изменения для Windows 7</span><span class="sxs-lookup"><span data-stu-id="f07d4-116">Changes for Windows 7</span></span>](#changes-for-windows-7)
-   [<span data-ttu-id="f07d4-117">См. также</span><span class="sxs-lookup"><span data-stu-id="f07d4-117">Related topics</span></span>](#related-topics)

## <a name="what-is-the-property-description-schema"></a><span data-ttu-id="f07d4-118">Что такое схема описания свойств?</span><span class="sxs-lookup"><span data-stu-id="f07d4-118">What Is the Property Description Schema?</span></span>

<span data-ttu-id="f07d4-119">Подсистема схемы состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="f07d4-119">The schema subsystem consists of the following:</span></span>

-   <span data-ttu-id="f07d4-120">Один или несколько файлов схемы. пропдеск, определяющих описания свойств.</span><span class="sxs-lookup"><span data-stu-id="f07d4-120">One or more .propdesc schema files that define property descriptions.</span></span> <span data-ttu-id="f07d4-121">Схема описания свойства определяется в коллекции файлов схемы XML (с помощью расширения файла пропдеск) во время выполнения в системе.</span><span class="sxs-lookup"><span data-stu-id="f07d4-121">The property description schema is defined in a collection of XML schema files (using the .propdesc file extension) at runtime on the system.</span></span> <span data-ttu-id="f07d4-122">Эти файлы загружаются с отложенной загрузкой, если они требуются для части системы свойств.</span><span class="sxs-lookup"><span data-stu-id="f07d4-122">These files are lazy-loaded when a part of the property system requires them.</span></span>
-   <span data-ttu-id="f07d4-123">Кэш схемы в памяти, используемый для хранения проанализированных файлов схемы, включая все описания свойств, появившиеся в подсистеме.</span><span class="sxs-lookup"><span data-stu-id="f07d4-123">An in-memory schema cache used to store the parsed schema files, which include all property descriptions introduced to the subsystem.</span></span> <span data-ttu-id="f07d4-124">Нет необходимости выполнять повторное синтаксический анализ файлов конфигурации. пропдеск, описывающих схему.</span><span class="sxs-lookup"><span data-stu-id="f07d4-124">There is no need to reparse the .propdesc config files that describe the schema.</span></span> <span data-ttu-id="f07d4-125">Дополнительные сведения см. в разделе [**псрегистерпропертисчема**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**псунрегистерпропертисчема**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema)и [**псрефрешпропертисчема**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).</span><span class="sxs-lookup"><span data-stu-id="f07d4-125">For more information, see [**PSRegisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**PSUnregisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema), and [**PSRefreshPropertySchema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).</span></span>
-   <span data-ttu-id="f07d4-126">Объект подсистемы, реализующий [**ипропертисистем**](/windows/win32/api/propsys/nn-propsys-ipropertysystem), который используется для получения описаний свойств или работы с ними.</span><span class="sxs-lookup"><span data-stu-id="f07d4-126">A subsystem object that implements [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem), which is used to obtain or work with property descriptions.</span></span>
-   <span data-ttu-id="f07d4-127">Объект подсистемы, реализующий [**ипропертидескриптион**](/windows/win32/api/propsys/nn-propsys-ipropertydescription), который используется для информирования и обработки данных в зависимости от описания свойства.</span><span class="sxs-lookup"><span data-stu-id="f07d4-127">A subsystem object that implements [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription), which is used to inform and operate based on a property description.</span></span>
-   <span data-ttu-id="f07d4-128">Объект подсистемы, реализующий [**ипропертидескриптионлист**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), который используется как коллекция описаний свойств.</span><span class="sxs-lookup"><span data-stu-id="f07d4-128">A subsystem object that implements [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), which is used as a collection of property descriptions.</span></span>

> [!Note]  
> <span data-ttu-id="f07d4-129">Необходимо добавить `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` в корневой элемент Schema файлов пропдеск.</span><span class="sxs-lookup"><span data-stu-id="f07d4-129">You must add `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` to the root schema element of your .propdesc files.</span></span>

 

## <a name="why-use-a-schema"></a><span data-ttu-id="f07d4-130">Зачем использовать схему?</span><span class="sxs-lookup"><span data-stu-id="f07d4-130">Why Use a Schema?</span></span>

<span data-ttu-id="f07d4-131">Сами по себе свойства не являются строго типизированными.</span><span class="sxs-lookup"><span data-stu-id="f07d4-131">Properties, by themselves, are not type-safe.</span></span> <span data-ttu-id="f07d4-132">Компонент может присвоить числовое значение свойству System. Author или параметру [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) Date-метка к свойству System. Music. албумтитле, и, не требуя дальнейшего применения или рекомендаций, хранилище свойств разрешит его.</span><span class="sxs-lookup"><span data-stu-id="f07d4-132">A component can assign a numerical value to the System.Author property, or a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) date-stamp to the System.Music.AlbumTitle property, and, without any further enforcement or guidance, the property stores will allow it.</span></span> <span data-ttu-id="f07d4-133">Итак, нам требовалось понятие «счематизе» свойств, которое приводит нас к подсистеме схемы.</span><span class="sxs-lookup"><span data-stu-id="f07d4-133">So, we needed a notion to "schematize" the properties, which brings us to the schema subsystem.</span></span>

## <a name="what-are-the-major-schema-parts"></a><span data-ttu-id="f07d4-134">Каковы основные компоненты схемы?</span><span class="sxs-lookup"><span data-stu-id="f07d4-134">What Are the Major Schema Parts?</span></span>

<span data-ttu-id="f07d4-135">Схема описания свойства, используемая системой свойств оболочки, состоит из одного [пропертидескриптионлист](./propdesc-schema-propertydescriptionlist.md) элемента, а также атрибута *schemaVersion* , указывающего версию этого формата определения схемы.</span><span class="sxs-lookup"><span data-stu-id="f07d4-135">The property description schema used by the Shell property system is composed of a single [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) element, as well as a *schemaVersion* attribute, which indicates the version of this schema definition format.</span></span> <span data-ttu-id="f07d4-136">Примечание. значение должно быть "1,0".</span><span class="sxs-lookup"><span data-stu-id="f07d4-136">Note: value must be "1.0".</span></span>


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



<span data-ttu-id="f07d4-137">[Пропертидескриптионлист](./propdesc-schema-propertydescriptionlist.md) состоит из одного или нескольких элементов [пропертидескриптион](./propdesc-schema-propertydescription.md) , а также атрибутов *издателя* и *продукта* .</span><span class="sxs-lookup"><span data-stu-id="f07d4-137">The [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) is composed of one or more [propertyDescription](./propdesc-schema-propertydescription.md) elements, as well as *publisher* and *product* attributes.</span></span>


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



<span data-ttu-id="f07d4-138">[Пропертидескриптион](./propdesc-schema-propertydescription.md) состоит из одного [сеарчинфо](./propdesc-schema-searchinfo.md) и нуля или одного элемента [лабелинфо](./propdesc-schema-labelinfo.md), [typeInfo](./propdesc-schema-typeinfo.md)и [displayInfo](./propdesc-schema-displayinfo.md) , а также атрибутов *форматид*, *PropID*, *пропстр* и *Name* .</span><span class="sxs-lookup"><span data-stu-id="f07d4-138">A [propertyDescription](./propdesc-schema-propertydescription.md) is composed of one [searchInfo](./propdesc-schema-searchinfo.md) and zero or one [labelInfo](./propdesc-schema-labelinfo.md), [typeInfo](./propdesc-schema-typeinfo.md), and [displayInfo](./propdesc-schema-displayinfo.md) elements, as well as *formatID*, *propID*, *propstr*, and *name* attributes.</span></span>

<span data-ttu-id="f07d4-139">Должен быть один элемент [пропертидескриптион](./propdesc-schema-propertydescription.md) для каждого уникального канонического имени свойства, которое должно быть доступно в системе.</span><span class="sxs-lookup"><span data-stu-id="f07d4-139">There should be one [propertyDescription](./propdesc-schema-propertydescription.md) element for every unique canonical property name that is intended to be available in the system.</span></span> <span data-ttu-id="f07d4-140">Длина строковых атрибутов ограничена 512 символами.</span><span class="sxs-lookup"><span data-stu-id="f07d4-140">The string attributes have a limit of 512 characters.</span></span> <span data-ttu-id="f07d4-141">Значения длиннее 512 символов усекаются.</span><span class="sxs-lookup"><span data-stu-id="f07d4-141">Values longer than 512 characters are truncated.</span></span>


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



## <a name="changes-for-windows-7"></a><span data-ttu-id="f07d4-142">Изменения для Windows 7</span><span class="sxs-lookup"><span data-stu-id="f07d4-142">Changes for Windows 7</span></span>

<span data-ttu-id="f07d4-143">Схема описания свойства была изменена для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f07d4-143">The property description schema has been changed for Windows 7.</span></span> <span data-ttu-id="f07d4-144">Это некритические изменения.</span><span class="sxs-lookup"><span data-stu-id="f07d4-144">These are non-breaking changes.</span></span> <span data-ttu-id="f07d4-145">Если элемент свойства или атрибут больше не поддерживается в Windows 7, операционная система Windows 7 не учитывает элементы или атрибуты Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f07d4-145">If a property element or attribute is no longer supported in Windows 7, the Windows 7 operating system ignores the Windows Vista element or attributes.</span></span> <span data-ttu-id="f07d4-146">Аналогичным образом Windows Vista также игнорирует новые элементы или атрибуты свойств Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f07d4-146">Similarly, Windows Vista ignores new Windows 7 property elements or attributes as well.</span></span>

<span data-ttu-id="f07d4-147">Однако обновление пользовательских свойств для Windows 7 рекомендуется для более эффективного и более стабильного взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="f07d4-147">However, updating custom properties for Windows 7 is recommended for a better and more consistent user experience.</span></span>

<span data-ttu-id="f07d4-148">Ниже перечислены новые элементы и атрибуты.</span><span class="sxs-lookup"><span data-stu-id="f07d4-148">The following are new elements and attributes:</span></span>

-   <span data-ttu-id="f07d4-149">элементы [релатедпропертинфо](./propdesc-schema-relatedpropertyinfo.md) и [relatedProperty](./propdesc-schema-relatedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="f07d4-149">[relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) and [relatedProperty](./propdesc-schema-relatedproperty.md) elements</span></span>
-   <span data-ttu-id="f07d4-150">элемент [Image](./propdesc-schema-image.md)</span><span class="sxs-lookup"><span data-stu-id="f07d4-150">[image](./propdesc-schema-image.md) element</span></span>
-   <span data-ttu-id="f07d4-151">атрибут мнемоник элемента [сеарчинфо](./propdesc-schema-searchinfo.md)</span><span class="sxs-lookup"><span data-stu-id="f07d4-151">mnemonics attribute of the [searchInfo](./propdesc-schema-searchinfo.md) element</span></span>
-   <span data-ttu-id="f07d4-152">атрибут мнемоник элемента [enum](./propdesc-schema-enum.md)</span><span class="sxs-lookup"><span data-stu-id="f07d4-152">mnemonics attribute of the [enum](./propdesc-schema-enum.md) element</span></span>
-   <span data-ttu-id="f07d4-153">атрибут Сеарчраввалуе элемента [typeInfo](./propdesc-schema-typeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="f07d4-153">searchRawValue attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>

<span data-ttu-id="f07d4-154">Изменились следующие элементы и атрибуты:</span><span class="sxs-lookup"><span data-stu-id="f07d4-154">The following elements and attributes have changed:</span></span>

-   <span data-ttu-id="f07d4-155">элементы [енумератедлист](./propdesc-schema-enumeratedlist.md), [enum](./propdesc-schema-enum.md)и [енумранже](./propdesc-schema-enumrange.md)</span><span class="sxs-lookup"><span data-stu-id="f07d4-155">[enumeratedList](./propdesc-schema-enumeratedlist.md), [enum](./propdesc-schema-enum.md), and [enumRange](./propdesc-schema-enumrange.md) elements</span></span>
-   <span data-ttu-id="f07d4-156">[дравконтрол](./propdesc-schema-drawcontrol.md) , элемент</span><span class="sxs-lookup"><span data-stu-id="f07d4-156">[drawControl](./propdesc-schema-drawcontrol.md) element</span></span>
-   <span data-ttu-id="f07d4-157">[едитконтрол](./propdesc-schema-editcontrol.md) , элемент</span><span class="sxs-lookup"><span data-stu-id="f07d4-157">[editControl](./propdesc-schema-editcontrol.md) element</span></span>
-   <span data-ttu-id="f07d4-158">атрибут propID элемента [пропертидескриптион](./propdesc-schema-propertydescription.md)</span><span class="sxs-lookup"><span data-stu-id="f07d4-158">propID attribute of the [propertyDescription](./propdesc-schema-propertydescription.md) element</span></span>
-   <span data-ttu-id="f07d4-159">атрибут Колумниндекстипе элемента [сеарчинфо](./propdesc-schema-searchinfo.md)</span><span class="sxs-lookup"><span data-stu-id="f07d4-159">columnIndexType attribute of the [searchInfo](./propdesc-schema-searchinfo.md) element</span></span>

<span data-ttu-id="f07d4-160">Удалены следующие элементы и атрибуты:</span><span class="sxs-lookup"><span data-stu-id="f07d4-160">The following elements and attributes have been removed:</span></span>

-   <span data-ttu-id="f07d4-161">[куериконтрол](./propdesc-schema-querycontrol.md) , элемент</span><span class="sxs-lookup"><span data-stu-id="f07d4-161">[queryControl](./propdesc-schema-querycontrol.md) element</span></span>
-   <span data-ttu-id="f07d4-162">атрибут, который является запрашиваемым элементом [typeInfo](./propdesc-schema-typeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="f07d4-162">isQueryable attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>
-   <span data-ttu-id="f07d4-163">атрибут Инклудеинфуллтексткуери элемента [typeInfo](./propdesc-schema-typeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="f07d4-163">includeInFullTextQuery attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>

## <a name="related-topics"></a><span data-ttu-id="f07d4-164">См. также</span><span class="sxs-lookup"><span data-stu-id="f07d4-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f07d4-165">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="f07d4-165">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="f07d4-166">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="f07d4-166">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="f07d4-167">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="f07d4-167">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="f07d4-168">typeInfo</span><span class="sxs-lookup"><span data-stu-id="f07d4-168">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="f07d4-169">displayInfo</span><span class="sxs-lookup"><span data-stu-id="f07d4-169">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="f07d4-170">stringFormat</span><span class="sxs-lookup"><span data-stu-id="f07d4-170">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="f07d4-171">булеанформат</span><span class="sxs-lookup"><span data-stu-id="f07d4-171">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="f07d4-172">numberFormat</span><span class="sxs-lookup"><span data-stu-id="f07d4-172">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="f07d4-173">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="f07d4-173">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="f07d4-174">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="f07d4-174">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="f07d4-175">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="f07d4-175">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="f07d4-176">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="f07d4-176">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="f07d4-177">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="f07d4-177">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="f07d4-178">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="f07d4-178">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="f07d4-179">image</span><span class="sxs-lookup"><span data-stu-id="f07d4-179">image</span></span>](./propdesc-schema-image.md)
</dt> </dl>

 

 
