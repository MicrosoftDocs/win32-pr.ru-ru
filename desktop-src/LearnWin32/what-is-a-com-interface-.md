---
title: Что такое COM-интерфейс
description: Что такое COM-интерфейс
ms.assetid: 36f27a58-cc63-4b67-bdcb-8f9a19650c6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da703569beae7a9aa2fc41bcea0214cc9aa488ad
ms.sourcegitcommit: 8eac40ea4d87a85e036ed5bbffec7b7a3dab39ec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2019
ms.locfileid: "104411471"
---
# <a name="what-is-a-com-interface"></a><span data-ttu-id="28a90-103">Что такое COM-интерфейс?</span><span class="sxs-lookup"><span data-stu-id="28a90-103">What Is a COM Interface?</span></span>

<span data-ttu-id="28a90-104">Если вы знаете C# или Java, интерфейсы должны быть привычными концепциями.</span><span class="sxs-lookup"><span data-stu-id="28a90-104">If you know C# or Java, interfaces should be a familiar concept.</span></span> <span data-ttu-id="28a90-105">*Интерфейс* определяет набор методов, которые может поддерживать объект, без диктовки каких-либо сведений о реализации.</span><span class="sxs-lookup"><span data-stu-id="28a90-105">An *interface* defines a set of methods that an object can support, without dictating anything about the implementation.</span></span> <span data-ttu-id="28a90-106">Интерфейс помечает четкие границы между кодом, который вызывает метод, и кодом, реализующим метод.</span><span class="sxs-lookup"><span data-stu-id="28a90-106">The interface marks a clear boundary between code that calls a method and the code that implements the method.</span></span> <span data-ttu-id="28a90-107">В условиях компьютерной науки вызывающий объект *отделен* от реализации.</span><span class="sxs-lookup"><span data-stu-id="28a90-107">In computer science terms, the caller is *decoupled* from the implementation.</span></span>

![Иллюстрация, демонстрирующая границу интерфейса между объектом и приложением](images/com01.png)

<span data-ttu-id="28a90-109">В C++ ближайший эквивалент интерфейса является чистым виртуальным классом, то есть классом, который содержит только чистые виртуальные методы и не имеет других членов.</span><span class="sxs-lookup"><span data-stu-id="28a90-109">In C++, the nearest equivalent to an interface is a pure virtual class—that is, a class that contains only pure virtual methods and no other members.</span></span> <span data-ttu-id="28a90-110">Ниже приведен гипотетический пример интерфейса:</span><span class="sxs-lookup"><span data-stu-id="28a90-110">Here is a hypothetical example of an interface:</span></span>

```C++
// The following is not actual COM.

// Pseudo-C++:

interface IDrawable
{
    void Draw();
};
```

<span data-ttu-id="28a90-111">Идея этого примера состоит в том, что набор объектов в некоторой графической библиотеке может быть нарисован.</span><span class="sxs-lookup"><span data-stu-id="28a90-111">The idea of this example is that a set of objects in some graphics library are drawable.</span></span> <span data-ttu-id="28a90-112">`IDrawable`Интерфейс определяет операции, которые должен поддерживать любой объект, поддерживающий рисование.</span><span class="sxs-lookup"><span data-stu-id="28a90-112">The `IDrawable` interface defines the operations that any drawable object must support.</span></span> <span data-ttu-id="28a90-113">(По соглашению имена интерфейсов начинаются с "I".) В этом примере `IDrawable` интерфейс определяет одну операцию: `Draw` .</span><span class="sxs-lookup"><span data-stu-id="28a90-113">(By convention, interface names start with "I".) In this example, the `IDrawable` interface defines a single operation: `Draw`.</span></span>

<span data-ttu-id="28a90-114">Все интерфейсы являются *абстрактными*, поэтому программа не может создать экземпляр `IDrawable` объекта таким образом.</span><span class="sxs-lookup"><span data-stu-id="28a90-114">All interfaces are *abstract*, so a program could not create an instance of an `IDrawable` object as such.</span></span> <span data-ttu-id="28a90-115">Например, следующий код не компилируется.</span><span class="sxs-lookup"><span data-stu-id="28a90-115">For example, the following code would not compile.</span></span>

```C++
IDrawable draw;
draw.Draw();
```

<span data-ttu-id="28a90-116">Вместо этого библиотека графики предоставляет объекты, *реализующие* `IDrawable` интерфейс.</span><span class="sxs-lookup"><span data-stu-id="28a90-116">Instead, the graphics library provides objects that *implement* the `IDrawable` interface.</span></span> <span data-ttu-id="28a90-117">Например, Библиотека может предоставить объект Shape для рисования фигур и растровый объект для рисования изображений.</span><span class="sxs-lookup"><span data-stu-id="28a90-117">For example, the library might provide a shape object for drawing shapes and a bitmap object for drawing images.</span></span> <span data-ttu-id="28a90-118">В C++ это делается путем наследования от общего абстрактного базового класса:</span><span class="sxs-lookup"><span data-stu-id="28a90-118">In C++, this is done by inheriting from a common abstract base class:</span></span>

```C++
class Shape : public IDrawable
{
public:
    virtual void Draw();    // Override Draw and provide implementation.
};

class Bitmap : public IDrawable
{
public:
    virtual void Draw();    // Override Draw and provide implementation.
};
```

<span data-ttu-id="28a90-119">`Shape`Классы и `Bitmap` определяют два различных типа рисуемого объекта.</span><span class="sxs-lookup"><span data-stu-id="28a90-119">The `Shape` and `Bitmap` classes define two distinct types of drawable object.</span></span> <span data-ttu-id="28a90-120">Каждый класс наследует от `IDrawable` и предоставляет собственную реализацию `Draw` метода.</span><span class="sxs-lookup"><span data-stu-id="28a90-120">Each class inherits from `IDrawable` and provides its own implementation of the `Draw` method.</span></span> <span data-ttu-id="28a90-121">Естественно, две реализации могут значительно различаться.</span><span class="sxs-lookup"><span data-stu-id="28a90-121">Naturally, the two implementations might differ considerably.</span></span> <span data-ttu-id="28a90-122">Например, `Shape::Draw` метод может расрастрировать набор строк, тогда как `Bitmap::Draw` бы Блит массив пикселей.</span><span class="sxs-lookup"><span data-stu-id="28a90-122">For example, the `Shape::Draw` method might rasterize a set of lines, while `Bitmap::Draw` would blit an array of pixels.</span></span>

<span data-ttu-id="28a90-123">Программа, использующая эту библиотеку, будет обрабатывать `Shape` `Bitmap` объекты и `IDrawable` с помощью указателей, а не `Shape` напрямую использовать или `Bitmap` указатели.</span><span class="sxs-lookup"><span data-stu-id="28a90-123">A program using this graphics library would manipulate `Shape` and `Bitmap` objects through `IDrawable` pointers, rather than using `Shape` or `Bitmap` pointers directly.</span></span>

```C++
IDrawable *pDrawable = CreateTriangleShape();

if (pDrawable)
{
    pDrawable->Draw();
}
```

<span data-ttu-id="28a90-124">Ниже приведен пример, в котором циклический перебор массива `IDrawable` указателей.</span><span class="sxs-lookup"><span data-stu-id="28a90-124">Here is an example that loops over an array of `IDrawable` pointers.</span></span> <span data-ttu-id="28a90-125">Массив может содержать разнородный ассортимент фигур, точечных рисунков и других графических объектов при условии, что каждый объект в массиве наследуется `IDrawable` .</span><span class="sxs-lookup"><span data-stu-id="28a90-125">The array might contain a heterogeneous assortment of shapes, bitmaps, and other graphics objects, as long as each object in the array inherits `IDrawable`.</span></span>

```C++
void DrawSomeShapes(IDrawable **drawableArray, size_t count)
{
    for (size_t i = 0; i < count; i++)
    {
        drawableArray[i]->Draw();
    }
}
```

<span data-ttu-id="28a90-126">Ключевой момент COM заключается в том, что вызывающий код никогда не видит тип производного класса.</span><span class="sxs-lookup"><span data-stu-id="28a90-126">A key point about COM is that the calling code never sees the type of the derived class.</span></span> <span data-ttu-id="28a90-127">Иными словами, вы никогда не объявили переменную типа `Shape` или `Bitmap` в коде.</span><span class="sxs-lookup"><span data-stu-id="28a90-127">In other words, you would never declare a variable of type `Shape` or `Bitmap` in your code.</span></span> <span data-ttu-id="28a90-128">Все операции с фигурами и точечными рисунками выполняются с помощью `IDrawable` указателей.</span><span class="sxs-lookup"><span data-stu-id="28a90-128">All operations on shapes and bitmaps are performed using `IDrawable` pointers.</span></span> <span data-ttu-id="28a90-129">Таким образом, COM обеспечивает четкое разделение между интерфейсом и реализацией.</span><span class="sxs-lookup"><span data-stu-id="28a90-129">In this way, COM maintains a strict separation between interface and implementation.</span></span> <span data-ttu-id="28a90-130">Сведения о реализации `Shape` `Bitmap` классов и могут изменяться, например, чтобы исправить ошибки или добавить новые возможности, не изменяя вызывающий код.</span><span class="sxs-lookup"><span data-stu-id="28a90-130">The implementation details of the `Shape` and `Bitmap` classes can change—for example, to fix bugs or add new capabilities—with no changes to the calling code.</span></span>

<span data-ttu-id="28a90-131">В реализации C++ интерфейсы объявляются с помощью класса или структуры.</span><span class="sxs-lookup"><span data-stu-id="28a90-131">In a C++ implementation, interfaces are declared using a class or structure.</span></span>

> [!Note]  
> <span data-ttu-id="28a90-132">Примеры кода в этом разделе предназначены для передачи общих понятий, а не реальных рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="28a90-132">The code examples in this topic are meant to convey general concepts, not real-world practice.</span></span> <span data-ttu-id="28a90-133">Определение новых COM-интерфейсов выходит за рамки этой серии, но интерфейс не определяется непосредственно в файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="28a90-133">Defining new COM interfaces is beyond the scope of this series, but you would not define an interface directly in a header file.</span></span> <span data-ttu-id="28a90-134">Вместо этого COM-интерфейс определяется с помощью языка IDL.</span><span class="sxs-lookup"><span data-stu-id="28a90-134">Instead, a COM interface is defined using a language called Interface Definition Language (IDL).</span></span> <span data-ttu-id="28a90-135">IDL-файл обрабатывается компилятором IDL, который создает заголовочный файл C++.</span><span class="sxs-lookup"><span data-stu-id="28a90-135">The IDL file is processed by an IDL compiler, which generates a C++ header file.</span></span>

```C++
class IDrawable
{
public:
    virtual void Draw() = 0;
};
```

<span data-ttu-id="28a90-136">При работе с COM важно помнить, что интерфейсы не являются объектами.</span><span class="sxs-lookup"><span data-stu-id="28a90-136">When you work with COM, it is important to remember that interfaces are not objects.</span></span> <span data-ttu-id="28a90-137">Они представляют собой коллекции методов, которые должны быть реализованы объектами.</span><span class="sxs-lookup"><span data-stu-id="28a90-137">They are collections of methods that objects must implement.</span></span> <span data-ttu-id="28a90-138">Несколько объектов могут реализовывать один и тот же интерфейс, как показано `Shape` в `Bitmap` примерах и.</span><span class="sxs-lookup"><span data-stu-id="28a90-138">Several objects can implement the same interface, as shown with the `Shape` and `Bitmap` examples.</span></span> <span data-ttu-id="28a90-139">Более того, один объект может реализовать несколько интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="28a90-139">Moreover, one object can implement several interfaces.</span></span> <span data-ttu-id="28a90-140">Например, Библиотека графики может определять интерфейс с именем `ISerializable` , который поддерживает сохранение и загрузку графических объектов.</span><span class="sxs-lookup"><span data-stu-id="28a90-140">For example, the graphics library might define an interface named `ISerializable` that supports saving and loading graphics objects.</span></span> <span data-ttu-id="28a90-141">Теперь рассмотрим следующие объявления классов:</span><span class="sxs-lookup"><span data-stu-id="28a90-141">Now consider the following class declarations:</span></span>

```C++
// An interface for serialization.
class ISerializable
{
public:
    virtual void Load(PCWSTR filename) = 0;    // Load from file.
    virtual void Save(PCWSTR filename) = 0;    // Save to file.
};

// Declarations of drawable object types.

class Shape : public IDrawable
{
    ...
};

class Bitmap : public IDrawable, public ISerializable
{
    ...
};
```

<span data-ttu-id="28a90-142">В этом примере `Bitmap` класс реализует `ISerializable` .</span><span class="sxs-lookup"><span data-stu-id="28a90-142">In this example, the `Bitmap` class implements `ISerializable`.</span></span> <span data-ttu-id="28a90-143">Программа может использовать этот метод для сохранения или загрузки точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="28a90-143">The program could use this method to save or load the bitmap.</span></span> <span data-ttu-id="28a90-144">Однако класс не `Shape` реализует `ISerializable` , поэтому он не предоставляет эту функциональность.</span><span class="sxs-lookup"><span data-stu-id="28a90-144">However, the `Shape` class does not implement `ISerializable`, so it does not expose that functionality.</span></span> <span data-ttu-id="28a90-145">На следующей диаграмме показаны отношения наследования в этом примере.</span><span class="sxs-lookup"><span data-stu-id="28a90-145">The following diagram shows the inheritance relations in this example.</span></span>

![Иллюстрация, демонстрирующая наследование интерфейса с помощью классов Shape и Bitmap, указывающих на идравабле, но только точечный рисунок, указывающий на ISerializable](images/com02.png)

<span data-ttu-id="28a90-147">В этом разделе рассматривалась концепция интерфейсов, но пока мы не видели фактический код COM.</span><span class="sxs-lookup"><span data-stu-id="28a90-147">This section has examined the conceptual basis of interfaces, but so far we have not seen actual COM code.</span></span> <span data-ttu-id="28a90-148">Начнем с первого, что должно сделать любое приложение COM: Инициализация библиотеки COM.</span><span class="sxs-lookup"><span data-stu-id="28a90-148">We'll start with the first thing that any COM application must do: Initialize the COM library.</span></span>

## <a name="next"></a><span data-ttu-id="28a90-149">Следующая</span><span class="sxs-lookup"><span data-stu-id="28a90-149">Next</span></span>

[<span data-ttu-id="28a90-150">Инициализация библиотеки COM</span><span class="sxs-lookup"><span data-stu-id="28a90-150">Initializing the COM Library</span></span>](initializing-the-com-library.md)