---
title: Терминология схемы Active Directory
description: Следующие термины обычно используются для ссылки на схему Active Directory.
ms.assetid: 22c5756f-d663-4cb7-aab0-956b22a01e9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efca7057a79d87c45cc3e3da4b604e842143fedd
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "105654395"
---
# <a name="active-directory-schema-terminology"></a><span data-ttu-id="e7f4c-103">Терминология схемы Active Directory</span><span class="sxs-lookup"><span data-stu-id="e7f4c-103">Active Directory Schema Terminology</span></span>

<span data-ttu-id="e7f4c-104">Следующие термины обычно используются для ссылки на схему Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-104">The following terms are commonly used to refer to the Active Directory schema.</span></span>


<dl> <dt>

<span data-ttu-id="e7f4c-105"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Версию</span><span class="sxs-lookup"><span data-stu-id="e7f4c-105"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-106">Элементы данных, используемые для описания объектов, представленных классами, определенными в схеме.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-106">Data items used to describe the objects that are represented by the classes that are defined in the schema.</span></span> <span data-ttu-id="e7f4c-107">Атрибуты определяются в схеме отдельно от классов. Это позволяет применять одно определение атрибута ко многим классам.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-107">Attributes are defined in the schema separately from the classes; this allows a single attribute definition to be applied to many classes.</span></span> <span data-ttu-id="e7f4c-108">Например, [**Description**](a-description.md) — это атрибут, который можно применить к любому классу в схеме.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-108">For example, [**Description**](a-description.md) is an attribute that can be applied to any class in the schema.</span></span> <span data-ttu-id="e7f4c-109">Атрибут **Description** определен один раз в схеме, гарантируя согласованность, вместо того чтобы иметь другое определение для **описания** пользователя и **описания** принтера.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-109">The **Description** attribute is defined once in the schema, assuring consistency, rather than having a different definition for **Description** of a user and **Description** of a printer.</span></span>

> [!Note]  
> <span data-ttu-id="e7f4c-110">*Свойство* Term часто используется с *атрибутом* Term.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-110">The term *property* is frequently used interchangeably with the term *attribute*.</span></span>

 

</dd> <dt>

<span data-ttu-id="e7f4c-111"><span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Экземпляр атрибута</span><span class="sxs-lookup"><span data-stu-id="e7f4c-111"><span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Attribute Instance</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-112">Вхождение атрибута, определенного в схеме.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-112">An occurrence of an attribute that is defined in the schema.</span></span> <span data-ttu-id="e7f4c-113">Этот термин используется для различения определения атрибута и отдельного вхождения атрибута.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-113">This term is used to distinguish between the definition of an attribute and a discrete occurrence of the attribute.</span></span> <span data-ttu-id="e7f4c-114">Например, при хранении объекта пользователя для «Джеффа Иванов» с атрибутом [**Common-Name**](a-cn.md) , имеющим значение «Джефф Иванов», создается экземпляр [**Common-Name**](a-cn.md).</span><span class="sxs-lookup"><span data-stu-id="e7f4c-114">For example, storing a User object for "Jeff Smith" with the [**Common-Name**](a-cn.md) attribute set to "Jeff Smith" creates an instance of [**Common-Name**](a-cn.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7f4c-115"><span id="Class"></span><span id="class"></span><span id="CLASS"></span>См</span><span class="sxs-lookup"><span data-stu-id="e7f4c-115"><span id="Class"></span><span id="class"></span><span id="CLASS"></span>Class</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-116">Формальное описание дискретного идентифицируемого типа объекта, хранящегося в службе каталогов.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-116">A formal description of a discrete, identifiable type of object stored in the directory service.</span></span> <span data-ttu-id="e7f4c-117">Например, [**пользователь**](c-user.md), [**очередь печати**](c-printqueue.md)и [**Группа**](c-group.md) являются классами.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-117">For example, [**User**](c-user.md), [**Print-Queue**](c-printqueue.md), and [**Group**](c-group.md) are all classes.</span></span> <span data-ttu-id="e7f4c-118">Более того, существует три категории классов: [структурные классы](classes-structural.md), [абстрактные классы](classes-abstract.md)и [вспомогательные классы](classes-auxiliary.md).</span><span class="sxs-lookup"><span data-stu-id="e7f4c-118">Furthermore, there are 3 distinct categories of classes: [Structural Classes](classes-structural.md), [Abstract Classes](classes-abstract.md), and [Auxiliary Classes](classes-auxiliary.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7f4c-119"><span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Экземпляр класса</span><span class="sxs-lookup"><span data-stu-id="e7f4c-119"><span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Class Instance</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-120">Вхождение класса, определенного в схеме.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-120">An occurrence of a class that is defined in the schema.</span></span> <span data-ttu-id="e7f4c-121">Этот термин используется для различения определения класса и отдельного вхождения класса.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-121">This term is used to distinguish between the definition of a class and a discrete occurrence of the class.</span></span> <span data-ttu-id="e7f4c-122">Например, при сохранении объекта [**пользователя**](c-user.md) для «Джеффа Иванов» в службе каталогов создается экземпляр [**пользователя**](c-user.md).</span><span class="sxs-lookup"><span data-stu-id="e7f4c-122">For example, storing a [**User**](c-user.md) object for "Jeff Smith" in the directory service creates an instance of [**User**](c-user.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7f4c-123"><span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Правила содержимого</span><span class="sxs-lookup"><span data-stu-id="e7f4c-123"><span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Content Rules</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-124">Определение возможного содержимого экземпляров класса, которые хранятся в службе каталогов.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-124">The definition of the possible contents of the class instances that are stored in the directory service.</span></span> <span data-ttu-id="e7f4c-125">В службах каталогов NT (NTDS), на которых основано Active Directory, правила содержимого полностью выражаются атрибутами, которые [**должны содержать**](a-mustcontain.md) и [**могут содержать**](a-maycontain.md) атрибуты определений схемы для каждого класса.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-125">In NT Directory Services (NTDS), upon which Active Directory is based, the content rules are completely expressed by the [**Must-Contain**](a-mustcontain.md) and [**May-Contain**](a-maycontain.md) attributes of the schema definitions for each class.</span></span>

</dd> <dt>

<span data-ttu-id="e7f4c-126"><span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Рожден</span><span class="sxs-lookup"><span data-stu-id="e7f4c-126"><span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Derivation</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-127">См. раздел *наследование*.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-127">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="e7f4c-128"><span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Дерево сведений о каталоге</span><span class="sxs-lookup"><span data-stu-id="e7f4c-128"><span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Directory Information Tree</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-129">Сам каталог, представленный в виде древовидной структуры, в которой вершины являются записями каталога (экземплярами класса) и соединяющими строками отношения типа «родители-потомки» между записями.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-129">The directory itself, represented as a tree structure in which the vertices are the directory entries (class instances) and the connecting lines the parent-child relationships between the entries.</span></span>

</dd> <dt>

<span data-ttu-id="e7f4c-130"><span id="DIT"></span><span id="dit"></span>DIT</span><span class="sxs-lookup"><span data-stu-id="e7f4c-130"><span id="DIT"></span><span id="dit"></span>DIT</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-131">См. раздел *дерево сведений о каталоге*.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-131">See *Directory Information Tree*.</span></span>

</dd> <dt>

<span data-ttu-id="e7f4c-132"><span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Управление правами доступа</span><span class="sxs-lookup"><span data-stu-id="e7f4c-132"><span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Control Access Rights</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-133">Класс, описывающий право доступа, не привязанное к ресурсу, но действие.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-133">A class that describes an access right not tied to a resource, but an action.</span></span> <span data-ttu-id="e7f4c-134">Например, пользователю может быть предоставлено право создавать относительные значения ИДЕНТИФИКАТОРов.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-134">For example, a user can be granted the right to create relative ID values.</span></span>

</dd> <dt>

<span data-ttu-id="e7f4c-135"><span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Цепочк</span><span class="sxs-lookup"><span data-stu-id="e7f4c-135"><span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Inheritance</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-136">Возможность создавать новые классы объектов на основе существующих классов объектов.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-136">The ability to build new object classes from existing object classes.</span></span> <span data-ttu-id="e7f4c-137">Новый объект определяется как *подкласс* родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-137">The new object is defined as a *subclass* of the parent object.</span></span> <span data-ttu-id="e7f4c-138">Родительский объект превращается в *Суперкласс* нового объекта.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-138">The parent object becomes a *superclass* of the new object.</span></span> <span data-ttu-id="e7f4c-139">Подкласс наследует атрибуты родителя, включая правила структуры и правила содержимого.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-139">A subclass inherits the attributes of the parent, including structure rules and content rules.</span></span>

</dd> <dt>

<span data-ttu-id="e7f4c-140"><span id="LDAP"></span><span id="ldap"></span>LDAP</span><span class="sxs-lookup"><span data-stu-id="e7f4c-140"><span id="LDAP"></span><span id="ldap"></span>LDAP</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-141">См. раздел *протокол упрощенного доступа к каталогу*.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-141">See *Lightweight Directory Access Protocol*.</span></span>

</dd> <dt>

<span data-ttu-id="e7f4c-142"><span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Упрощенный протокол доступа к каталогу</span><span class="sxs-lookup"><span data-stu-id="e7f4c-142"><span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Lightweight Directory Access Protocol</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-143">Стандартный протокол связи Интернета, используемый для связи с NTDS.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-143">A standard Internet communications protocol used to communicate with the NTDS.</span></span> <span data-ttu-id="e7f4c-144">Поддерживаются LDAP версии 2 и 3.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-144">LDAP version 2 and version 3 are supported.</span></span>

</dd> <dt>

<span data-ttu-id="e7f4c-145"><span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>Дескриптор безопасности NT</span><span class="sxs-lookup"><span data-stu-id="e7f4c-145"><span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>NT Security Descriptor</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-146">См. раздел *дескриптор безопасности*.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-146">See *Security Descriptor*.</span></span>

</dd> <dt>

<span data-ttu-id="e7f4c-147"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Объектами</span><span class="sxs-lookup"><span data-stu-id="e7f4c-147"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Object</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-148">Единица хранения данных в службе каталогов.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-148">A unit of data storage in the directory service.</span></span> <span data-ttu-id="e7f4c-149">Объекты службы каталогов не следует путать с COM-объектами или другими объектно-ориентированными системными объектами, которые имеют исполняемый компонент и поведение во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-149">Directory service objects are not to be confused with COM objects or other object-oriented system objects, which have an executable component and run-time behavior.</span></span> <span data-ttu-id="e7f4c-150">Объекты службы каталогов состоят только из данных.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-150">Directory service objects consist only of data.</span></span> <span data-ttu-id="e7f4c-151">Объект службы каталогов определяется объектом [**class-schema**](c-classschema.md) и группой объектов [**Attribute-Schema**](c-attributeschema.md) , на которые ссылается объект [**class-schema**](c-classschema.md) .</span><span class="sxs-lookup"><span data-stu-id="e7f4c-151">A directory service object is defined by a [**Class-Schema**](c-classschema.md) object and a group of [**Attribute-Schema**](c-attributeschema.md) objects referenced by the [**Class-Schema**](c-classschema.md) object.</span></span>

<span data-ttu-id="e7f4c-152">Объекты схемы [**классов**](c-classschema.md) и [**атрибутов**](c-attributeschema.md) — это объекты службы каталогов, которые имеют определения в схеме, как и любые другие объекты.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-152">[**Class-Schema**](c-classschema.md) and [**Attribute-Schema**](c-attributeschema.md) objects are themselves directory service objects, and have definitions in the schema like any other objects.</span></span> <span data-ttu-id="e7f4c-153">См. раздел *класс*.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-153">See *Class*.</span></span>

</dd> <dt>

<span data-ttu-id="e7f4c-154"><span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Идентификатор объекта</span><span class="sxs-lookup"><span data-stu-id="e7f4c-154"><span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Object Identifier</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-155">Уникальные числовые значения, выданные различными центрами сертификации для уникальной идентификации элементов данных, синтаксисов и других частей распределенных приложений.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-155">Unique numeric values, issued by various issuing authorities, to uniquely identify data elements, syntaxes, and various other parts of distributed applications.</span></span> <span data-ttu-id="e7f4c-156">Идентификаторы объектов (OID) находятся в приложениях OSI, каталогах X. 500, SNMP и других приложениях, где важна уникальность.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-156">Object Identifiers (OIDs) are found in OSI applications, X.500 Directories, SNMP, and other applications where uniqueness is important.</span></span> <span data-ttu-id="e7f4c-157">OID основаны на древовидной структуре, в которой общепроизводительный центр сертификации, например ISO, выделяет ветвь дерева подразделу, который, в свою очередь, может выделять подветви.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-157">OIDs are based on a tree structure, in which a superior issuing authority, such as the ISO, allocates a branch of the tree to a sub-authority, which in turn can allocate sub-branches.</span></span>

<span data-ttu-id="e7f4c-158">Идентификаторы объектов в NTDS включают некоторые, выданные ISO для классов и атрибутов X. 500, а также некоторые, выпущенные корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-158">OIDs in the NTDS include some issued by the ISO for X.500 classes and attributes, and some issued by Microsoft.</span></span> <span data-ttu-id="e7f4c-159">Нотация OID — это пунктирная строка чисел, например "1.2.840.113556.1.5.4", которая преобразуется, как указано в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-159">OID notation is a dotted string of numbers, for example "1.2.840.113556.1.5.4", which translates as listed in the following list.</span></span> 

| <span data-ttu-id="e7f4c-160">Значение</span><span class="sxs-lookup"><span data-stu-id="e7f4c-160">Value</span></span>  | <span data-ttu-id="e7f4c-161">Описание</span><span class="sxs-lookup"><span data-stu-id="e7f4c-161">Description</span></span>                                                                                  |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7f4c-162">1</span><span class="sxs-lookup"><span data-stu-id="e7f4c-162">1</span></span>      | <span data-ttu-id="e7f4c-163">ISO — "корневой центр", выдано "1,2" в ANSI, который, в свою очередь,</span><span class="sxs-lookup"><span data-stu-id="e7f4c-163">ISO - the "root authority", issued "1.2" to ANSI, which in turn...</span></span>                           |
| <span data-ttu-id="e7f4c-164">2</span><span class="sxs-lookup"><span data-stu-id="e7f4c-164">2</span></span>      | <span data-ttu-id="e7f4c-165">ANSI... выдано "1.2.840" для США, который, в свою очередь,...</span><span class="sxs-lookup"><span data-stu-id="e7f4c-165">ANSI ...issued "1.2.840" to USA, which in turn...</span></span>                                            |
| <span data-ttu-id="e7f4c-166">840</span><span class="sxs-lookup"><span data-stu-id="e7f4c-166">840</span></span>    | <span data-ttu-id="e7f4c-167">США... выдано "1.2.840.113556" в Майкрософт...</span><span class="sxs-lookup"><span data-stu-id="e7f4c-167">USA ...issued "1.2.840.113556" to Microsoft...</span></span>                                               |
| <span data-ttu-id="e7f4c-168">113556</span><span class="sxs-lookup"><span data-stu-id="e7f4c-168">113556</span></span> | <span data-ttu-id="e7f4c-169">Microsoft... где Microsoft внутренне управляет несколькими ветвями OID в разделе "1.2.840.113556".</span><span class="sxs-lookup"><span data-stu-id="e7f4c-169">Microsoft ...where Microsoft internally manages several OID branches under "1.2.840.113556".</span></span> |
| <span data-ttu-id="e7f4c-170">1</span><span class="sxs-lookup"><span data-stu-id="e7f4c-170">1</span></span>      | <span data-ttu-id="e7f4c-171">Microsoft DS</span><span class="sxs-lookup"><span data-stu-id="e7f4c-171">Microsoft DS</span></span>                                                                                 |
| <span data-ttu-id="e7f4c-172">5</span><span class="sxs-lookup"><span data-stu-id="e7f4c-172">5</span></span>      | <span data-ttu-id="e7f4c-173">Классы NTDS</span><span class="sxs-lookup"><span data-stu-id="e7f4c-173">NTDS Classes</span></span>                                                                                 |
| <span data-ttu-id="e7f4c-174">4</span><span class="sxs-lookup"><span data-stu-id="e7f4c-174">4</span></span>      | <span data-ttu-id="e7f4c-175">Builtin-Domain</span><span class="sxs-lookup"><span data-stu-id="e7f4c-175">Builtin-Domain</span></span>                                                                               |



 

</dd> <dt>

<span data-ttu-id="e7f4c-176"><span id="OID"></span><span id="oid"></span>КОДА</span><span class="sxs-lookup"><span data-stu-id="e7f4c-176"><span id="OID"></span><span id="oid"></span>OID</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-177">См. *идентификатор объекта*.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-177">See *Object Identifier*.</span></span>

</dd> <dt>

<span data-ttu-id="e7f4c-178"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Схемы</span><span class="sxs-lookup"><span data-stu-id="e7f4c-178"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Schema</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-179">Формальное определение содержимого и структуры службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-179">A formal definition of the directory service contents and structure.</span></span> <span data-ttu-id="e7f4c-180">Схема определяет все атрибуты и классы.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-180">The schema defines all attributes and classes.</span></span> <span data-ttu-id="e7f4c-181">Для каждого класса определены [**ПОСС-старший**](a-posssuperiors.md), [**должен-содержать**](a-mustcontain.md)и [**может содержать**](a-maycontain.md) атрибуты.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-181">For each class, the [**Poss-Superiors**](a-posssuperiors.md), [**Must-Contain**](a-mustcontain.md), and [**May-Contain**](a-maycontain.md) attributes are defined.</span></span> <span data-ttu-id="e7f4c-182">[**ПОСС — старший**](a-posssuperiors.md) элемент определяет возможные структуры дерева для службы каталогов, указывая, какие классы могут быть родительскими для любого заданного класса.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-182">[**Poss-Superiors**](a-posssuperiors.md) defines the possible tree structures for the directory service by specifying what classes can be the parent for any given class.</span></span> <span data-ttu-id="e7f4c-183">[**Должен содержать**](a-mustcontain.md) и [**может содержать**](a-maycontain.md) список атрибутов для класса, который должен присутствовать для хранения класса и дополнительных атрибутов, которые могут быть заданы при необходимости.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-183">[**Must-Contain**](a-mustcontain.md) and [**May-Contain**](a-maycontain.md) list the attributes for a class that must be present to store the class and what additional attributes may optionally be present.</span></span>

</dd> <dt>

<span data-ttu-id="e7f4c-184"><span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Дескриптор безопасности</span><span class="sxs-lookup"><span data-stu-id="e7f4c-184"><span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Security Descriptor</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-185">Сведения о владении объектом и разрешениях, которые другие пользователи применяют к этому объекту.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-185">Information about the ownership of an object and the permissions that other users have on that object.</span></span> <span data-ttu-id="e7f4c-186">Свойство [**дескриптора NT-Security-**](a-ntsecuritydescriptor.md) Schema записи схемы содержит строку, представляющую дескриптор безопасности объекта.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-186">The [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md) property of a schema entry contains a string that represents the security descriptor of the object.</span></span> <span data-ttu-id="e7f4c-187">Дополнительные сведения о формате сведений в этом поле см. в разделе [Формат строки дескриптора безопасности](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span><span class="sxs-lookup"><span data-stu-id="e7f4c-187">For more information about the format of the information in this field, see [Security Descriptor String Format](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span></span>

</dd> <dt>

<span data-ttu-id="e7f4c-188"><span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Правила структуры</span><span class="sxs-lookup"><span data-stu-id="e7f4c-188"><span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Structure Rules</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-189">Определение возможной древовидной структуры или структур.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-189">The definition of the possible tree structure or structures.</span></span> <span data-ttu-id="e7f4c-190">В NTDS правила структуры полностью выражаются атрибутом ПОСС-Превосходно, присутствующим в каждом объекте [**class-schema**](c-classschema.md) .</span><span class="sxs-lookup"><span data-stu-id="e7f4c-190">In the NTDS, the structure rules are completely expressed by the Poss-superiors attribute present on each [**Class-Schema**](c-classschema.md) object.</span></span> <span data-ttu-id="e7f4c-191">См. *схему*.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-191">See *Schema*.</span></span>

</dd> <dt>

<span data-ttu-id="e7f4c-192"><span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Подкласс</span><span class="sxs-lookup"><span data-stu-id="e7f4c-192"><span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Subclass</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-193">Объект [**class-schema**](c-classschema.md) , наследующий от другого объекта [**class-schema**](c-classschema.md) .</span><span class="sxs-lookup"><span data-stu-id="e7f4c-193">A [**Class-Schema**](c-classschema.md) object that inherits from another [**Class-Schema**](c-classschema.md) object.</span></span> <span data-ttu-id="e7f4c-194">См. раздел *наследование*.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-194">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="e7f4c-195"><span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Суперкласс</span><span class="sxs-lookup"><span data-stu-id="e7f4c-195"><span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Superclass</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-196">Объект [**class-schema**](c-classschema.md) , из которого наследуются один или несколько других объектов [**-схем классов**](c-classschema.md) .</span><span class="sxs-lookup"><span data-stu-id="e7f4c-196">A [**Class-Schema**](c-classschema.md) object from which one or more other [**Class-Schema**](c-classschema.md) objects inherit.</span></span> <span data-ttu-id="e7f4c-197">См. раздел *наследование*.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-197">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="e7f4c-198"><span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Приклад</span><span class="sxs-lookup"><span data-stu-id="e7f4c-198"><span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Tree</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-199">См. раздел *дерево сведений о каталоге*.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-199">See *Directory Information Tree*.</span></span>

</dd> <dt>

<span data-ttu-id="e7f4c-200"><span id="X.500"></span><span id="x.500"></span>X. 500</span><span class="sxs-lookup"><span data-stu-id="e7f4c-200"><span id="X.500"></span><span id="x.500"></span>X.500</span></span>
</dt> <dd>

<span data-ttu-id="e7f4c-201">Семейство стандартов, разработанное совместно с ISO и ITU, ранее известное как CCITT, которое определяет именование, представление данных и протоколы связи для службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="e7f4c-201">A family of standards developed jointly by the ISO and ITU, formerly known as the CCITT, that specify the naming, data representation, and communications protocols for a directory service.</span></span>

</dd> </dl>

 

 