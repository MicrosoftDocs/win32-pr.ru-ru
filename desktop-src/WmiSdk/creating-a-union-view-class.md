---
description: Класс представления Union — это логическое объединение экземпляров исходного класса. Класс представления Union включает все экземпляры исходных классов, если только экземпляры не будут ограничены путем включения предложения WHERE в исходный запрос.
ms.assetid: 54a9804d-644d-4ab6-a3d5-c9c4f7761967
ms.tgt_platform: multiple
title: Создание класса представления Union
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2ff9327645828c3db78a82811831f058cc27f202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703004"
---
# <a name="creating-a-union-view-class"></a><span data-ttu-id="05e1b-104">Создание класса представления Union</span><span class="sxs-lookup"><span data-stu-id="05e1b-104">Creating a Union View Class</span></span>

<span data-ttu-id="05e1b-105">Класс представления Union — это логическое объединение экземпляров исходного класса.</span><span class="sxs-lookup"><span data-stu-id="05e1b-105">A union view class is a logical union of source class instances.</span></span> <span data-ttu-id="05e1b-106">Класс представления Union включает все экземпляры исходных классов, если только экземпляры не будут ограничены путем включения предложения WHERE в исходный запрос.</span><span class="sxs-lookup"><span data-stu-id="05e1b-106">A union view class includes all the instances of the source classes unless you limit the instances by including a WHERE clause on the source query.</span></span>

<span data-ttu-id="05e1b-107">Классы представлений Union полезны, когда необходимо просмотреть экземпляры схожих или идентичных классов, расположенных в разных пространствах имен или на разных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="05e1b-107">Union view classes are useful when you want to see instances of similar or identical classes that are located in different namespaces or on different computers.</span></span> <span data-ttu-id="05e1b-108">Например, можно создать класс Union, содержащий экземпляры различных дисков для мониторинга.</span><span class="sxs-lookup"><span data-stu-id="05e1b-108">For example, you can create a union class that contains instances of different disk drives to monitor.</span></span>

<span data-ttu-id="05e1b-109">Свойства класса представления Union также можно основывать на свойствах, отсутствующих во всех экземплярах исходного класса.</span><span class="sxs-lookup"><span data-stu-id="05e1b-109">You can also base the properties of a union view class on properties not present in all of the source class instances.</span></span> <span data-ttu-id="05e1b-110">Если экземпляры исходного класса имеют разные свойства, свойства экземпляров класса Union имеют значение **null**.</span><span class="sxs-lookup"><span data-stu-id="05e1b-110">If the source class instances do not have the same property, the properties of union class instances have a value of **NULL**.</span></span> <span data-ttu-id="05e1b-111">Например, если на одном жестком диске есть свойство **температуры** , а другое — нет, то можно по-прежнему создать объединение между ними.</span><span class="sxs-lookup"><span data-stu-id="05e1b-111">For example, if one hard disk drive has a **temperature** property but another does not, you can still create a union between the two.</span></span>

<span data-ttu-id="05e1b-112">В следующей процедуре описывается создание класса представления Union.</span><span class="sxs-lookup"><span data-stu-id="05e1b-112">The following procedure describes how to create a union view class.</span></span>

<span data-ttu-id="05e1b-113">**Создание класса представления Union**</span><span class="sxs-lookup"><span data-stu-id="05e1b-113">**To create a union view class**</span></span>

1.  <span data-ttu-id="05e1b-114">Начните определение класса с квалификатором строки [**объединения**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="05e1b-114">Begin your class definition with the [**Union**](qualifiers-specific-to-the-view-provider.md) string qualifier.</span></span>

    <span data-ttu-id="05e1b-115">Квалификаторы [**жоинон**](qualifiers-specific-to-the-view-provider.md), **Association** и **Union** являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="05e1b-115">The [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association**, and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="05e1b-116">Создайте запросы, определяющие исходные классы, используемые в классе представления с квалификатором [**виевсаурцес**](viewsources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="05e1b-116">Create the queries that define source classes used in the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
3.  <span data-ttu-id="05e1b-117">Определите имена и расположение пространств имен, в которых исходные классы находятся с квалификатором [**виевспацес**](viewspaces-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="05e1b-117">Define the names and location of the namespaces in which the source classes are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="05e1b-118">Определите свойства, которые сопоставляются со свойствами в исходных классах с квалификатором [**пропертисаурцес**](propertysources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="05e1b-118">Define the properties that map to the properties in the source classes with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="05e1b-119">При необходимости можно пометить любые свойства как принадлежащие исходному классу с помощью квалификатора [**хиддендефаулт**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="05e1b-119">If necessary, you can tag any of the properties as belonging to a source class by using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

5.  <span data-ttu-id="05e1b-120">Определите ключевые свойства исходных классов для класса представления Union.</span><span class="sxs-lookup"><span data-stu-id="05e1b-120">Define the key properties of the source classes of your union view class.</span></span>

    <span data-ttu-id="05e1b-121">Каждый исходный класс должен иметь одинаковое число ключевых свойств, совпадающих с [**Цимтипе**](swbemproperty-cimtype.md).</span><span class="sxs-lookup"><span data-stu-id="05e1b-121">Each source class must have the same number of key properties matched by [**CIMType**](swbemproperty-cimtype.md).</span></span> <span data-ttu-id="05e1b-122">Кроме того, ключи класса представления Union должны уникальным образом идентифицировать все исходные экземпляры.</span><span class="sxs-lookup"><span data-stu-id="05e1b-122">Also, the keys of your union view class must uniquely identify all source instances.</span></span> <span data-ttu-id="05e1b-123">В некоторых случаях может потребоваться указать системные свойства, чтобы убедиться, что экземпляры уникальны.</span><span class="sxs-lookup"><span data-stu-id="05e1b-123">In some cases, you might need to specify system properties to ensure that instances are unique.</span></span> <span data-ttu-id="05e1b-124">Например, при создании представления из объединения двух идентичных классов в двух разных пространствах имен можно включить свойство [**\_ \_ Namespace**](--namespace.md) в качестве ключа в класс представления, чтобы различать два экземпляра.</span><span class="sxs-lookup"><span data-stu-id="05e1b-124">For example, if you create a view from the union of two identical classes in two different namespaces, you could include the [**\_\_Namespace**](--namespace.md) property as a key in the view class to differentiate between the two instances.</span></span> <span data-ttu-id="05e1b-125">Если для создания представления используются два схожих класса из одного пространства имен, то для различения этих двух классов можно использовать свойство **\_ \_ Class** .</span><span class="sxs-lookup"><span data-stu-id="05e1b-125">If you use two similar classes from the same namespace to create a view, you could use the **\_\_Class** property to distinguish between the two.</span></span> <span data-ttu-id="05e1b-126">Переименуйте все системные свойства в представлении, чтобы избежать конфликта с системными свойствами класса представления.</span><span class="sxs-lookup"><span data-stu-id="05e1b-126">Rename any system properties in the view so you can avoid a conflict with the system properties of the view class.</span></span>

6.  <span data-ttu-id="05e1b-127">Определите все необходимые методы с помощью квалификатора [**месодсаурце**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="05e1b-127">Define any methods you want using the [**MethodSource**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

    <span data-ttu-id="05e1b-128">В отличие от других классов представлений, можно создавать методы для изменения представления объединения.</span><span class="sxs-lookup"><span data-stu-id="05e1b-128">Unlike other view classes, you can create methods to modify a union view.</span></span>

<span data-ttu-id="05e1b-129">В следующем примере кода описывается класс представления Union.</span><span class="sxs-lookup"><span data-stu-id="05e1b-129">The following code example describes a union view class.</span></span>

``` syntax
[Union, ViewSources{"SELECT Description, DeviceID, __Namespace, FileSystem, FreeSpace, VolumeName FROM LocalDisk", 
    "SELECT Description, DeviceID, __Namespace, FileSystem, FreeSpace, VolumeName FROM RemoteDisk"}, 
    ViewSpaces{"\\\\.\\Root\\LocalNamespace","\\\\.\\Root\\RemoteNamespace"}, 
    dynamic: ToInstance, provider("MS_VIEW_INSTANCE_PROVIDER")]

class UnionOfDrives

{
    [PropertySources{"Description", "Description"}] string des;
    [PropertySources{"DeviceID", "DeviceID"}, key] String did;
    [PropertySources{"__Namespace", "__Namespace"}, key] String KEYID;
    [PropertySources{"FileSystem", "FileSystem"}] String fsystem ;
    [PropertySources{"FreeSpace", "FreeSpace"}] uint64 fspace;
    [PropertySources{"VolumeName", "VolumeName"}] String vname;
};
```

 

 



