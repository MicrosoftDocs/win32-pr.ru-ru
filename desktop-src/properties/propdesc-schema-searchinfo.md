---
description: Указывает, как настроить подсистему поиска Windows относительно заданного определения свойства.
ms.assetid: 1cb0b630-323c-41cf-8aaf-db3028b2e369
title: сеарчинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee94585aaa66a761e527ac6ada1c33b0d23966d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662758"
---
# <a name="searchinfo"></a><span data-ttu-id="43115-103">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="43115-103">searchInfo</span></span>

<span data-ttu-id="43115-104">Указывает, как настроить подсистему поиска Windows относительно заданного определения свойства.</span><span class="sxs-lookup"><span data-stu-id="43115-104">Specifies how to configure the Windows search engine with respect to a given property definition.</span></span> <span data-ttu-id="43115-105">Если элемент [сеарчинфо]() не предоставлен, свойство не включается в подсистему поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="43115-105">If no [searchInfo]() element is provided, then the property is not included in the Windows search engine.</span></span> <span data-ttu-id="43115-106">Этот элемент был изменен для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="43115-106">This element has changed for Windows 7.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="43115-107">Синтаксис для Windows 7</span><span class="sxs-lookup"><span data-stu-id="43115-107">Syntax for Windows 7</span></span>


```
<!-- searchInfo for Windows 7-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                    <xs:enumeration value="OnDiskAll"/>
                    <xs:enumeration value="OnDiskVector"/>
                    <xs:enumeration value="OnDemand"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="512"/>
        <xs:attribute name="mnemonics" type="xs:string"/>                            
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-windows-vista"></a><span data-ttu-id="43115-108">Синтаксис для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43115-108">Syntax for Windows Vista</span></span>


```
<!-- searchInfo for Windows Vista-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="128"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="43115-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="43115-109">Element Information</span></span>



| <span data-ttu-id="43115-110">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="43115-110">Parent Element</span></span>                                                   | <span data-ttu-id="43115-111">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="43115-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="43115-112">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="43115-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="43115-113">Нет</span><span class="sxs-lookup"><span data-stu-id="43115-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="43115-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="43115-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="43115-115">Атрибут</span><span class="sxs-lookup"><span data-stu-id="43115-115">Attribute</span></span></th>
<th><span data-ttu-id="43115-116">Описание</span><span class="sxs-lookup"><span data-stu-id="43115-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43115-117">ининвертединдекс</span><span class="sxs-lookup"><span data-stu-id="43115-117">inInvertedIndex</span></span></td>
<td><span data-ttu-id="43115-118">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="43115-118">Public.</span></span> <span data-ttu-id="43115-119">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="43115-119">Optional.</span></span> <span data-ttu-id="43115-120">Указывает, должно ли значение свойства храниться в инвертированном индексе.</span><span class="sxs-lookup"><span data-stu-id="43115-120">Indicates whether the property value should be stored in the inverted index.</span></span> <span data-ttu-id="43115-121">Это позволяет конечным пользователям выполнять полнотекстовые запросы по значениям этого свойства.</span><span class="sxs-lookup"><span data-stu-id="43115-121">This lets end users perform full-text queries over the values of this property.</span></span> <span data-ttu-id="43115-122">Значение по умолчанию — &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="43115-122">The default is &quot;false&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43115-123">Столбец</span><span class="sxs-lookup"><span data-stu-id="43115-123">isColumn</span></span></td>
<td><span data-ttu-id="43115-124">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="43115-124">Public.</span></span> <span data-ttu-id="43115-125">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="43115-125">Optional.</span></span> <span data-ttu-id="43115-126">Указывает, должно ли свойство храниться в базе данных Windows Search в виде столбца, чтобы независимые поставщики программного обеспечения могли создавать запросы на основе предикатов (например, &quot; SELECT \*, где &quot; System. title &quot; = ' ККК ' &quot; ).</span><span class="sxs-lookup"><span data-stu-id="43115-126">Indicates whether the property should also be stored in the Windows search database as a column, so that independent software vendors (ISVs) can create predicate-based queries (for example, &quot;Select \* Where &quot;System.Title&quot;='qqq'&quot;).</span></span> <span data-ttu-id="43115-127">Если создатель схемы хочет разрешить конечным пользователям (или разработчикам) создавать запросы на основе предикатов для свойств, необходимо задать для этого свойства значение &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="43115-127">If the schema creator wants to enable end users (or developers) to create predicate based queries on the properties, then this needs to be set to &quot;true&quot;.</span></span> <span data-ttu-id="43115-128">Значение по умолчанию — &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="43115-128">The default is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43115-129">исколумнспарсе</span><span class="sxs-lookup"><span data-stu-id="43115-129">isColumnSparse</span></span></td>
<td><span data-ttu-id="43115-130">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="43115-130">Public.</span></span> <span data-ttu-id="43115-131">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="43115-131">Optional.</span></span> <span data-ttu-id="43115-132">Значение по умолчанию — &quot;true&quot;.</span><span class="sxs-lookup"><span data-stu-id="43115-132">The default is &quot;true&quot;.</span></span> <span data-ttu-id="43115-133">Если свойство является многозначным, этот атрибут всегда имеет &quot; значение true &quot; .</span><span class="sxs-lookup"><span data-stu-id="43115-133">If the property is multi-valued, this attribute is always &quot;true&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43115-134">колумниндекстипе</span><span class="sxs-lookup"><span data-stu-id="43115-134">columnIndexType</span></span></td>
<td><span data-ttu-id="43115-135">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="43115-135">Public.</span></span> <span data-ttu-id="43115-136">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="43115-136">Optional.</span></span> <span data-ttu-id="43115-137">Для оптимизации сортировки и группирования механизм Windows Search может создавать вторичные индексы для свойств, имеющих &quot; значение IsTrue = true &quot; .</span><span class="sxs-lookup"><span data-stu-id="43115-137">To optimize sorting and grouping, the Windows search engine can create secondary indexes for properties that have isColumn=&quot;true&quot;.</span></span> <span data-ttu-id="43115-138">Этот атрибут полезен только в том случае, если в Windows Vista Ининвертединдекс имеет &quot; значение true &quot; или если &quot; в Windows 7 истинен столбец «IsTrue» &quot; .</span><span class="sxs-lookup"><span data-stu-id="43115-138">This attribute is only useful when inInvertedIndex is &quot;true&quot; in Windows Vista or when isColumn is &quot;true&quot; in Windows 7.</span></span> <span data-ttu-id="43115-139">Если свойство планируется часто сортировать для пользователей, необходимо указать этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="43115-139">If the property tends to be sorted frequently by users, this attribute should be specified.</span></span> <span data-ttu-id="43115-140">Значение по умолчанию в Windows Vista — &quot; нотиндексед &quot; .</span><span class="sxs-lookup"><span data-stu-id="43115-140">The default value in Windows Vista is &quot;NotIndexed&quot;.</span></span> <span data-ttu-id="43115-141">Значение по умолчанию в Windows 7 — &quot; OnDemand &quot; .</span><span class="sxs-lookup"><span data-stu-id="43115-141">The default value in Windows 7 is &quot;OnDemand&quot;.</span></span> <span data-ttu-id="43115-142">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="43115-142">The following values are valid.</span></span>
<ul>
<li><span data-ttu-id="43115-143"><strong>Нотиндексед</strong>: никогда не создавайте индекс значения.</span><span class="sxs-lookup"><span data-stu-id="43115-143"><strong>NotIndexed</strong>: Never build a value index.</span></span></li>
<li><span data-ttu-id="43115-144">На <strong>диске</strong>: для этого свойства по умолчанию строится индекс значения.</span><span class="sxs-lookup"><span data-stu-id="43115-144"><strong>OnDisk</strong>: Build a value index by default for this property.</span></span></li>
<li><span data-ttu-id="43115-145"><strong>Ондискалл</strong> (только Windows 7 и более поздние версии): создайте индекс значения по умолчанию для этого свойства и, если это свойство Vector, а также индекс значения для всех сцепленных векторных значений.</span><span class="sxs-lookup"><span data-stu-id="43115-145"><strong>OnDiskAll</strong> (Windows 7 and later only): Build a value index by default for this property, and if it is a vector property, also a value index for all concatenated vector values.</span></span></li>
<li><span data-ttu-id="43115-146"><strong>Ондисквектор</strong> (только Windows 7 и более поздние версии): для сцепленных векторных значений по умолчанию создается индекс значения.</span><span class="sxs-lookup"><span data-stu-id="43115-146"><strong>OnDiskVector</strong> (Windows 7 and later only): Build a value index by default for the concatenated vector values.</span></span></li>
<li><span data-ttu-id="43115-147"><strong>OnDemand</strong> (только для Windows 7 и более поздних версий): только индексы значений сборки по запросу, то есть только при первом использовании для запроса.</span><span class="sxs-lookup"><span data-stu-id="43115-147"><strong>OnDemand</strong> (Windows 7 and later only): Only build value indices by demand, that is, only first time they are used for a query.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43115-148">maxSize</span><span class="sxs-lookup"><span data-stu-id="43115-148">maxSize</span></span></td>
<td><span data-ttu-id="43115-149">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="43115-149">Public.</span></span> <span data-ttu-id="43115-150">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="43115-150">Optional.</span></span> <span data-ttu-id="43115-151">Максимальный размер (в байтах), допустимый для определенного свойства, хранящегося в базе данных поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="43115-151">The maximum size, in bytes, allowed for a certain property that is stored in the Windows search database.</span></span> <span data-ttu-id="43115-152">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="43115-152">The default is:</span></span>
<ul>
<li><span data-ttu-id="43115-153"><strong>Windows Vista</strong>: 128 байт</span><span class="sxs-lookup"><span data-stu-id="43115-153"><strong>Windows Vista</strong>: 128 bytes</span></span></li>
<li><span data-ttu-id="43115-154"><strong>Windows 7 и более поздние версии</strong>: 512 байт</span><span class="sxs-lookup"><span data-stu-id="43115-154"><strong>Windows 7 and later</strong>: 512 bytes</span></span></li>
</ul>
<span data-ttu-id="43115-155">Обратите внимание, что этот максимальный размер измеряется в байтах, а не в символах.</span><span class="sxs-lookup"><span data-stu-id="43115-155">Note that this maximum size is measured in bytes, not characters.</span></span> <span data-ttu-id="43115-156">Максимальное количество символов зависит от их кодировки.</span><span class="sxs-lookup"><span data-stu-id="43115-156">The maximum number of characters depends on their encoding.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43115-157">назначенные клавиши</span><span class="sxs-lookup"><span data-stu-id="43115-157">mnemonics</span></span></td>
<td><span data-ttu-id="43115-158"><strong>Windows 7 и более поздние версии.</strong></span><span class="sxs-lookup"><span data-stu-id="43115-158"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="43115-159">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="43115-159">Public.</span></span> <span data-ttu-id="43115-160">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="43115-160">Optional.</span></span> <span data-ttu-id="43115-161">Список назначенных значений, которые можно использовать для ссылки на свойство в поисковых запросах.</span><span class="sxs-lookup"><span data-stu-id="43115-161">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="43115-162">Список отделяется символом "|".</span><span class="sxs-lookup"><span data-stu-id="43115-162">The list is delimited with the '|' character.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
