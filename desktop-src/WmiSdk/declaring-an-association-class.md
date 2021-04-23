---
description: Класс ассоциации — это особый тип класса, который определяет связь между двумя другими классами.
ms.assetid: 21fd6e39-5dd3-41b8-a2f5-0135a6637ce8
ms.tgt_platform: multiple
title: Объявление класса ассоциации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ce578ca912290fd026f225799793f89685aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081276"
---
# <a name="declaring-an-association-class"></a><span data-ttu-id="e3b8c-103">Объявление класса ассоциации</span><span class="sxs-lookup"><span data-stu-id="e3b8c-103">Declaring an Association Class</span></span>

<span data-ttu-id="e3b8c-104">Класс ассоциации — это особый тип класса, который определяет связь между двумя другими классами.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-104">An association class is a special type of class that defines a relationship between two other classes.</span></span>

<span data-ttu-id="e3b8c-105">В следующей процедуре описывается создание класса ассоциации с помощью MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-105">The following procedure describes how to create an association class using MOF code.</span></span>

<span data-ttu-id="e3b8c-106">**Создание класса взаимосвязей с помощью MOF-кода**</span><span class="sxs-lookup"><span data-stu-id="e3b8c-106">**To create an association class using MOF code**</span></span>

1.  <span data-ttu-id="e3b8c-107">Назначьте квалификатор **ассоциации** вашему классу.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-107">Assign the **Association** qualifier to your class.</span></span>

    <span data-ttu-id="e3b8c-108">Несмотря на то, что можно создать класс со ссылками на объекты или классы, использование квалификатора **ассоциации** не только делает ясно, что класс является классом ассоциации, но, как вариант, рекомендуется гарантировать, что ваш класс полностью функционирует как класс ассоциации.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-108">Although it is possible to create a class with references to objects or classes, using the **Association** qualifier not only makes it clear that your class is an association class, but, as a best practice, ensures that your class fully functions as an association class.</span></span>

2.  <span data-ttu-id="e3b8c-109">Создайте две ссылки в классе, описывающие два экземпляра объектов, которые необходимо связать вместе с помощью **ссылочного** типа.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-109">Create two references within the class describing the two object instances you wish to associate together using the **ref** type.</span></span>

    <span data-ttu-id="e3b8c-110">Ссылки привязывают два объекта в ассоциации, путем того, как они содержат пути к объектам.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-110">The references bind the two objects in the association by containing paths to the objects.</span></span> <span data-ttu-id="e3b8c-111">Хотя это и не является обязательным, используйте свойства ссылки как ключевые свойства.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-111">Although not required, use the reference properties as key properties as well.</span></span>

    <span data-ttu-id="e3b8c-112">Несмотря на то, что можно создавать полные или относительные ссылки на пространства имен, Инструментарий WMI имеет ограниченную поддержку ссылок между пространствами имен.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-112">Although you can create fully qualified or namespace-relative references, WMI has only limited support for cross-namespace references.</span></span> <span data-ttu-id="e3b8c-113">В частности, только статически определенные объекты могут ссылаться друг на друга по границам пространства имен. динамически поддерживаемые объекты не могут ссылаться друг на друга.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-113">Specifically, only statically defined objects can reference each other across namespace boundaries; dynamically supported objects cannot reference each other.</span></span>

    <span data-ttu-id="e3b8c-114">При необходимости используйте квалификаторы **хасклассреф** и **классреф** в сочетании с типом ссылки на **объект** , чтобы ссылаться на класс.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-114">If necessary, use the **HasClassRef** and **Classref** qualifiers in conjunction with the **object ref** type to reference a class.</span></span>

    <span data-ttu-id="e3b8c-115">Инструментарий WMI поддерживает **одну ссылочную точку ссылки на** экземпляр и другую точку ссылки на **объект** класса.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-115">WMI supports having one **ref** reference point to an instance, and the other **object** reference point to a class.</span></span> <span data-ttu-id="e3b8c-116">В этом случае класс ассоциации описывает ассоциацию, которая привязывает экземпляры к классам.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-116">In this case, your association class would describe an association that binds instances to classes.</span></span>

    <span data-ttu-id="e3b8c-117">В следующем примере кода описывается синтаксис для использования **хасклассреф** и **классреф** с типом **объекта** .</span><span class="sxs-lookup"><span data-stu-id="e3b8c-117">The following code example describes the syntax for using **HasClassRef** and **Classref** with an **object** type.</span></span>

    ``` syntax
    [HasClassRefs, Association]
    class SomeAssocClass
    {
         [key, classref{ "MyEndpoint", "OtherContainer" }]
         object ref ep1;
         [key] object ref ep2;
    }; 
    ```

    <span data-ttu-id="e3b8c-118">В предыдущем примере ссылка **EP1** может указывать на определения класса либо для класса **MyEndpoint** , либо для класса **осерконтаинер** .</span><span class="sxs-lookup"><span data-stu-id="e3b8c-118">In the previous example, the **ep1** reference can point to the class definitions for either the **MyEndpoint** class or the **OtherContainer** class.</span></span> <span data-ttu-id="e3b8c-119">Обратите внимание, что хотя ссылочный класс должен быть слабо типизирован, нельзя слабо ввести сам квалификатор **классреф** . Это существенно снизит эффективность обработчика запросов WMI.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-119">Note that while you must weakly type the reference class, you cannot weakly type the **Classref** qualifier itself; doing so would severely reduce the efficiency of the WMI query engine.</span></span> <span data-ttu-id="e3b8c-120">Нестрогая типизация — это создание ссылки, которая может содержать любой тип данных, с помощью ключевого слова **Object** и **ссылочного** типа данных.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-120">Weak typing is creating a reference that can contain any data type by using the **object** keyword and **ref** data type.</span></span> <span data-ttu-id="e3b8c-121">Чтобы успешно использовать **хасклассреф**, необходимо задать соответствующие разновидности квалификаторов для распространения на все экземпляры и подклассы.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-121">To successfully use **HasClassRef**, you must set the relevant qualifier flavors to propagate to all instances and subclasses.</span></span>

3.  <span data-ttu-id="e3b8c-122">При необходимости создайте любые другие свойства.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-122">Create any other properties as necessary.</span></span>

    <span data-ttu-id="e3b8c-123">В следующем примере кода показано, что инструментарий WMI в настоящее время не поддерживает классы взаимосвязей с меньшей или более чем двумя ссылочными свойствами.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-123">The following code example shows that WMI does not currently support association classes having less or more than two reference properties.</span></span>

    ``` syntax
    [Association : ToInstance] 
    class MyAssocClass
    {
        ClassX ref PathToClassX ;
        ClassY ref PathToClassY ;
    };
    ```

4.  <span data-ttu-id="e3b8c-124">По завершении Скомпилируйте MOF-код с помощью компилятора MOF.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-124">When finished, compile your MOF code with the MOF compiler.</span></span>

    <span data-ttu-id="e3b8c-125">Дополнительные сведения см. в разделе [Компиляция MOF-файлов](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="e3b8c-125">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="e3b8c-126">В примере кода на шаге 3 определяется класс ассоциации **мяссоккласс** .</span><span class="sxs-lookup"><span data-stu-id="e3b8c-126">The code example in Step 3 defines the **MyAssocClass** association class.</span></span> <span data-ttu-id="e3b8c-127">Класс **мяссоккласс** определяет связь между **класскс** и **классом**.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-127">The **MyAssocClass** class defines a relationship between **ClassX** and **ClassY**.</span></span> <span data-ttu-id="e3b8c-128">Свойства **пастокласскс** и **пастокласси** содержат пути к объектам для экземпляров классов, которые должны быть связаны.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-128">The **PathToClassX** and **PathToClassY** properties contain object paths to the instances of the classes to be associated.</span></span> <span data-ttu-id="e3b8c-129">Ключевое слово **тоинстанце** является одним из нескольких флагов разновидностей, которые WMI определяет для предоставления сведений об использовании квалификатора.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-129">The keyword **ToInstance** is one of several flavor flags that WMI defines to provide information about the use of a qualifier.</span></span> <span data-ttu-id="e3b8c-130">Ключевое слово **тоинстанце** указывает, что WMI должен распространить квалификатор **ассоциации** на все экземпляры класса Association.</span><span class="sxs-lookup"><span data-stu-id="e3b8c-130">The **ToInstance** keyword indicates that WMI should propagate the **Association** qualifier to all instances of the association class.</span></span> <span data-ttu-id="e3b8c-131">Установив квалификатор этого экземпляра, клиентское программное обеспечение может определить, что экземпляр принадлежит к классу ассоциации, без необходимости извлечения определения класса для поиска квалификатора **ассоциации** .</span><span class="sxs-lookup"><span data-stu-id="e3b8c-131">By checking this instance qualifier, the client software can determine that an instance belongs to an association class, without having to retrieve the class definition to look for the **Association** qualifier.</span></span> <span data-ttu-id="e3b8c-132">Дополнительные сведения см. в разделе [Описание квалификатора с флагом квалификатора](describing-a-qualifier-with-a-qualifier-flavor.md) и [ссылками](references.md).</span><span class="sxs-lookup"><span data-stu-id="e3b8c-132">For more information, see [Describing a Qualifier With a Qualifier Flavor](describing-a-qualifier-with-a-qualifier-flavor.md) and [References](references.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3b8c-133">См. также</span><span class="sxs-lookup"><span data-stu-id="e3b8c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3b8c-134">Разработка классов MOF-файл (MOF)</span><span class="sxs-lookup"><span data-stu-id="e3b8c-134">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



