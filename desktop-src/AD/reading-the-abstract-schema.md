---
title: Чтение абстрактной схемы
description: В этом разделе приведен пример кода и рекомендации по чтению из абстрактной схемы, которая предоставляет подмножество данных, хранящихся в объектах attributeSchema и classSchema в контейнере схемы.
ms.assetid: f31fc0ae-048f-413c-9370-96367dc68df8
ms.tgt_platform: multiple
keywords:
- Active Directory схемы, чтение абстрактной схемы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d7fadba33bcc5e93bf2b9e89934e8b440d559b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103890379"
---
# <a name="reading-the-abstract-schema"></a><span data-ttu-id="12be1-104">Чтение абстрактной схемы</span><span class="sxs-lookup"><span data-stu-id="12be1-104">Reading the Abstract Schema</span></span>

<span data-ttu-id="12be1-105">В этом разделе приведен пример кода и рекомендации по чтению из абстрактной схемы, которая предоставляет подмножество данных, хранящихся в объектах **attributeSchema** и **classSchema** в контейнере схемы.</span><span class="sxs-lookup"><span data-stu-id="12be1-105">This topic provides a code example and guidelines for reading from the abstract schema, which provides a subset of the data stored in the **attributeSchema** and **classSchema** objects in the schema container.</span></span> <span data-ttu-id="12be1-106">Чтобы получить данные, недоступные в абстрактной схеме, прочтите данные непосредственно из контейнера схемы, как описано в разделе [чтение объектов attributeSchema и classSchema](reading-attributeschema-and-classschema-objects.md).</span><span class="sxs-lookup"><span data-stu-id="12be1-106">To retrieve data that is unavailable in the abstract schema, read the data directly from the schema container as described in [Reading attributeSchema and classSchema Objects](reading-attributeschema-and-classschema-objects.md).</span></span>

<span data-ttu-id="12be1-107">Используйте строку привязки "LDAP://schema" для привязки к указателю [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) в абстрактной схеме.</span><span class="sxs-lookup"><span data-stu-id="12be1-107">Use the "LDAP://schema" binding string to bind to an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) pointer on the abstract schema.</span></span> <span data-ttu-id="12be1-108">Этот указатель используется для перечисления записей класса, атрибута и синтаксиса в абстрактной схеме.</span><span class="sxs-lookup"><span data-stu-id="12be1-108">Use this pointer to enumerate the class, attribute, and syntax entries in the abstract schema.</span></span> <span data-ttu-id="12be1-109">Для получения отдельных записей можно также использовать метод [**иадсконтаинер. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) .</span><span class="sxs-lookup"><span data-stu-id="12be1-109">You can also use the [**IADsContainer.GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) method to retrieve individual entries.</span></span>


```C++
// Bind to the abstract schema.
IADsContainer *pAbsSchema = NULL;
hr = ADsGetObject(L"LDAP://schema",
                  IID_IADsContainer,
                  (void**)&pAbsSchema);
```




```VB
' Bind to the abstract schema.
Dim adschema As IADsContainer
Set adschema = GetObject("LDAP://schema")
```



<span data-ttu-id="12be1-110">Используйте аналогичную строку привязки "LDAP://schema/ <object> " для непосредственной привязки к записи класса или атрибута в абстрактной схеме.</span><span class="sxs-lookup"><span data-stu-id="12be1-110">Use a similar binding string, "LDAP://schema/<object>", to bind directly to a class or attribute entry in the abstract schema.</span></span> <span data-ttu-id="12be1-111">В этой строке " &lt; Object &gt; " — это атрибут **lDAPDisplayName** класса или атрибута.</span><span class="sxs-lookup"><span data-stu-id="12be1-111">In this string, "&lt;object&gt;" is the **lDAPDisplayName** of a class or attribute.</span></span> <span data-ttu-id="12be1-112">Для классов привязывается к интерфейсу [**иадскласс**](/windows/desktop/api/iads/nn-iads-iadsclass) ; для атрибутов привяжите к интерфейсу [**иадспроперти**](/windows/desktop/api/iads/nn-iads-iadsproperty) .</span><span class="sxs-lookup"><span data-stu-id="12be1-112">For classes bind to the [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) interface; for attributes, bind to [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) interface.</span></span>


```C++
// Bind to the user class entry in the abstract schema.
IADsClass *pClass;
hr = ADsGetObject(L"LDAP://schema/user",
                  IID_IADsClass,
                  (void**)&pClass);
```




```VB
Bind to the user class entry in the abstract schema.
Dim userclass As IADsClass
Set userclass = GetObject("LDAP://schema/user")
```



<span data-ttu-id="12be1-113">Кроме того, интерфейс [**iAds**](/windows/desktop/api/iads/nn-iads-iads) предоставляет свойство [**iAds. Schema**](/windows/desktop/ADSI/iads-property-methods) .</span><span class="sxs-lookup"><span data-stu-id="12be1-113">In addition, the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface provides the [**IADs.Schema**](/windows/desktop/ADSI/iads-property-methods) property.</span></span> <span data-ttu-id="12be1-114">Это свойство возвращает значение ADsPath для класса объекта в формате строки абстрактной привязки схемы.</span><span class="sxs-lookup"><span data-stu-id="12be1-114">This property returns the ADsPath for the object class in abstract schema binding string format.</span></span> <span data-ttu-id="12be1-115">При наличии указателя **iAds** для объекта можно выполнить привязку к его классу в абстрактной схеме, используя значение ADsPath, возвращенное методом **iAds. Schema**.</span><span class="sxs-lookup"><span data-stu-id="12be1-115">If you have an **IADs** pointer to an object, you can bind to its class in the abstract schema using the ADsPath returned from **IADs.Schema**.</span></span>

<span data-ttu-id="12be1-116">Для классов в следующей таблице перечислены ключевые свойства, предоставляемые абстрактной схемой.</span><span class="sxs-lookup"><span data-stu-id="12be1-116">For classes, the following table lists key properties provided by the abstract schema.</span></span>



| <span data-ttu-id="12be1-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="12be1-117">Property</span></span>                                                             | <span data-ttu-id="12be1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="12be1-118">Meaning</span></span>                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12be1-119">**Иадскласс. abstract**</span><span class="sxs-lookup"><span data-stu-id="12be1-119">**IADsClass.Abstract**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)            | <span data-ttu-id="12be1-120">Указывает, является ли этот класс абстрактным.</span><span class="sxs-lookup"><span data-stu-id="12be1-120">Indicates whether this is an abstract class.</span></span>                                                                                                                                                                                                                                            |
| [<span data-ttu-id="12be1-121">**Иадскласс. Вспомогательная**</span><span class="sxs-lookup"><span data-stu-id="12be1-121">**IADsClass.Auxiliary**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)           | <span data-ttu-id="12be1-122">Указывает, является ли это вспомогательным классом.</span><span class="sxs-lookup"><span data-stu-id="12be1-122">Indicates whether this is an auxiliary class.</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="12be1-123">**Иадскласс. Ауксдериведфром**</span><span class="sxs-lookup"><span data-stu-id="12be1-123">**IADsClass.AuxDerivedFrom**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)      | <span data-ttu-id="12be1-124">Массив вспомогательных классов, от которых наследует этот класс.</span><span class="sxs-lookup"><span data-stu-id="12be1-124">Array of auxiliary classes this class derives from.</span></span>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="12be1-125">**Иадскласс. Container**</span><span class="sxs-lookup"><span data-stu-id="12be1-125">**IADsClass.Container**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)           | <span data-ttu-id="12be1-126">Указывает, могут ли объекты этого класса содержать другие объекты, что имеет значение true, если любой класс включает этот класс в свой список **поссиблесупериорс**.</span><span class="sxs-lookup"><span data-stu-id="12be1-126">Indicates whether objects of this class can contain other objects, which is true if any class includes this class in its list of **possibleSuperiors**.</span></span>                                                                                                                                 |
| [<span data-ttu-id="12be1-127">**Иадскласс. Дериведфром**</span><span class="sxs-lookup"><span data-stu-id="12be1-127">**IADsClass.DerivedFrom**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)         | <span data-ttu-id="12be1-128">Массив классов, производным от которого является этот класс.</span><span class="sxs-lookup"><span data-stu-id="12be1-128">Array of classes that this class is derived from.</span></span>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="12be1-129">**Иадскласс. Мандаторипропертиес**</span><span class="sxs-lookup"><span data-stu-id="12be1-129">**IADsClass.MandatoryProperties**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods) | <span data-ttu-id="12be1-130">Извлекает массив обязательных свойств, которые должны быть установлены для экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="12be1-130">Retrieves an array of the mandatory properties that must be set for an instance of the class.</span></span> <span data-ttu-id="12be1-131">Возвращаемый список содержит все значения **mustContain** и **системмустконтаин** для класса и классов, от которых он производных, включая классы и вспомогательные классы.</span><span class="sxs-lookup"><span data-stu-id="12be1-131">The returned list includes all the **mustContain** and **systemMustContain** values for the class and the classes from which it is derived, including superclasses and auxiliary classes.</span></span> |
| [<span data-ttu-id="12be1-132">**Иадскласс. OID**</span><span class="sxs-lookup"><span data-stu-id="12be1-132">**IADsClass.OID**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)                 | <span data-ttu-id="12be1-133">Возвращает governsID класса.</span><span class="sxs-lookup"><span data-stu-id="12be1-133">Retrieves the governsID of the class.</span></span>                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="12be1-134">**Иадскласс. OptionalProperties**</span><span class="sxs-lookup"><span data-stu-id="12be1-134">**IADsClass.OptionalProperties**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)  | <span data-ttu-id="12be1-135">Извлекает массив необязательных свойств, которые могут быть установлены для экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="12be1-135">Retrieves an array of the optional properties that might be set for an instance of the class.</span></span> <span data-ttu-id="12be1-136">Возвращаемый список содержит все значения **mayContain** и **системмайконтаин** для класса и классов, от которых он производных, включая классы и вспомогательные классы.</span><span class="sxs-lookup"><span data-stu-id="12be1-136">The returned list includes all the **mayContain** and **systemMayContain** values for the class and the classes from which it is derived, including superclasses and auxiliary classes.</span></span>   |
| [<span data-ttu-id="12be1-137">**Иадскласс. Поссиблесупериорс**</span><span class="sxs-lookup"><span data-stu-id="12be1-137">**IADsClass.PossibleSuperiors**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)   | <span data-ttu-id="12be1-138">Извлекает массив значений **поссиблесупериорс** для класса, который указывает классы объектов, которые могут содержать объекты этого класса.</span><span class="sxs-lookup"><span data-stu-id="12be1-138">Retrieves an array of the **possibleSuperiors** values for the class, which indicates the object classes that can contain objects of this class.</span></span>                                                                                                                                        |



 

<span data-ttu-id="12be1-139">Абстрактная схема хранится в объекте **подсхемы** в контейнере схемы.</span><span class="sxs-lookup"><span data-stu-id="12be1-139">The abstract schema is stored in the **subSchema** object in the schema container.</span></span> <span data-ttu-id="12be1-140">Чтобы получить различающееся имя объекта **подсхемы** , выполните привязку к RootDSE и прочтите атрибут **субсчемасубентри** , как описано в разделе [Привязка без сервера и RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="12be1-140">To get the distinguished name of the **subSchema** object, bind to rootDSE and read the **subSchemaSubEntry** attribute, as described in [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span> <span data-ttu-id="12be1-141">Имейте в виду, что более эффективно считывать абстрактную схему путем привязки к "LDAP://schema", чем путем привязки непосредственно к объекту **подсхемы** .</span><span class="sxs-lookup"><span data-stu-id="12be1-141">Be aware that it is more efficient to read the abstract schema by binding to "LDAP://schema", than by binding directly to the **subSchema** object.</span></span>

 

 