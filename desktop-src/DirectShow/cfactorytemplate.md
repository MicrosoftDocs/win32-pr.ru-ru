---
description: Предоставляет шаблон для создания фабрик классов.
ms.assetid: 3dbe6402-15f8-4490-9fe2-bebaa4e79170
title: Класс Кфакторитемплате (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be5ca9b8319eeddf777cbf0071c1930f21524369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657567"
---
# <a name="cfactorytemplate-class"></a><span data-ttu-id="140c7-103">Класс Кфакторитемплате</span><span class="sxs-lookup"><span data-stu-id="140c7-103">CFactoryTemplate class</span></span>

<span data-ttu-id="140c7-104">Предоставляет шаблон для создания фабрик классов.</span><span class="sxs-lookup"><span data-stu-id="140c7-104">Provides a template for creating class factories.</span></span>

<span data-ttu-id="140c7-105">В DirectShow фабрики классов специализированы с помощью класса **кфакторитемплате** , также называемого *шаблоном фабрики*.</span><span class="sxs-lookup"><span data-stu-id="140c7-105">In DirectShow, class factories are specialized using the **CFactoryTemplate** class, also called the *factory template*.</span></span> <span data-ttu-id="140c7-106">Каждая фабрика классов содержит указатель на шаблон фабрики.</span><span class="sxs-lookup"><span data-stu-id="140c7-106">Each class factory holds a pointer to a factory template.</span></span> <span data-ttu-id="140c7-107">Шаблон фабрики содержит сведения об объекте COM, включая идентификатор класса (CLSID) объекта и указатель на функцию, которая создает объект.</span><span class="sxs-lookup"><span data-stu-id="140c7-107">The factory template contains information about a COM object, including the object's class identifier (CLSID) and a pointer to a function that creates the object.</span></span>

<span data-ttu-id="140c7-108">В библиотеке DLL объявите глобальный массив шаблонов фабрики с именем *g \_ Templates*.</span><span class="sxs-lookup"><span data-stu-id="140c7-108">In your DLL, declare a global array of factory templates named *g\_Templates*.</span></span> <span data-ttu-id="140c7-109">Включите один шаблон фабрики для каждого объекта в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="140c7-109">Include one factory template for each object in the DLL.</span></span> <span data-ttu-id="140c7-110">Когда функция [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) создает новую фабрику классов, она ищет в массиве шаблон с соответствующим идентификатором CLSID.</span><span class="sxs-lookup"><span data-stu-id="140c7-110">When the [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) function makes a new class factory, it searches the array for a template with a matching CLSID.</span></span> <span data-ttu-id="140c7-111">При условии, что он находит один, он создает фабрику класса, содержащую указатель на соответствующий шаблон.</span><span class="sxs-lookup"><span data-stu-id="140c7-111">Assuming it finds one, it creates a class factory that holds a pointer to the matching template.</span></span> <span data-ttu-id="140c7-112">Когда клиент вызывает метод **IClassFactory:: CreateInstance**, фабрика класса вызывает функцию создания экземпляра, определенную в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="140c7-112">When the client calls **IClassFactory::CreateInstance**, the class factory calls the instantiation function defined in the template.</span></span>

<span data-ttu-id="140c7-113">Дополнительные сведения см. [в разделе Создание библиотеки DLL фильтра DirectShow](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="140c7-113">For more information, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>



| <span data-ttu-id="140c7-114">Открытые переменные члена</span><span class="sxs-lookup"><span data-stu-id="140c7-114">Public Member Variables</span></span>                                                   | <span data-ttu-id="140c7-115">Описание</span><span class="sxs-lookup"><span data-stu-id="140c7-115">Description</span></span>                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="140c7-116">**\_имя m**</span><span class="sxs-lookup"><span data-stu-id="140c7-116">**m\_Name**</span></span>](cfactorytemplate-m-name.md)                                | <span data-ttu-id="140c7-117">Имя фильтра.</span><span class="sxs-lookup"><span data-stu-id="140c7-117">Name of the filter.</span></span>                                                        |
| [<span data-ttu-id="140c7-118">**m \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="140c7-118">**m\_ClsID**</span></span>](cfactorytemplate-m-clsid.md)                              | <span data-ttu-id="140c7-119">Указатель на идентификатор CLSID объекта.</span><span class="sxs-lookup"><span data-stu-id="140c7-119">Pointer to the CLSID of the object.</span></span>                                        |
| [<span data-ttu-id="140c7-120">**m \_ лпфннев**</span><span class="sxs-lookup"><span data-stu-id="140c7-120">**m\_lpfnNew**</span></span>](cfactorytemplate-m-lpfnnew.md)                          | <span data-ttu-id="140c7-121">Указатель на функцию, которая создает экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="140c7-121">Pointer to a function that creates an instance of the object.</span></span>              |
| [<span data-ttu-id="140c7-122">**m \_ лпфнинит**</span><span class="sxs-lookup"><span data-stu-id="140c7-122">**m\_lpfnInit**</span></span>](cfactorytemplate-m-lpfninit.md)                        | <span data-ttu-id="140c7-123">Указатель на функцию, которая вызывается из точки входа библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="140c7-123">Pointer to a function that gets called from the DLL entry point.</span></span>           |
| [<span data-ttu-id="140c7-124">**m \_ памовиесетуп \_ Фильтр**</span><span class="sxs-lookup"><span data-stu-id="140c7-124">**m\_pAMovieSetup\_Filter**</span></span>](cfactorytemplate-m-pamoviesetup-filter.md) | <span data-ttu-id="140c7-125">Указатель на структуру [**\_ фильтра амовиесетуп**](amoviesetup-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="140c7-125">Pointer to an [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure.</span></span> |
| <span data-ttu-id="140c7-126">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="140c7-126">Public Methods</span></span>                                                            | <span data-ttu-id="140c7-127">Описание</span><span class="sxs-lookup"><span data-stu-id="140c7-127">Description</span></span>                                                                |
| [<span data-ttu-id="140c7-128">**Идентификатор класса**</span><span class="sxs-lookup"><span data-stu-id="140c7-128">**IsClassID**</span></span>](cfactorytemplate-isclassid.md)                           | <span data-ttu-id="140c7-129">Определяет, соответствует ли CLSID этому шаблону класса.</span><span class="sxs-lookup"><span data-stu-id="140c7-129">Determines whether a CLSID matches this class template.</span></span>                    |
| [<span data-ttu-id="140c7-130">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="140c7-130">**CreateInstance**</span></span>](cfactorytemplate-createinstance.md)                 | <span data-ttu-id="140c7-131">Вызывает функцию создания объекта для класса.</span><span class="sxs-lookup"><span data-stu-id="140c7-131">Calls the object-creation function for the class.</span></span>                          |



 

## <a name="requirements"></a><span data-ttu-id="140c7-132">Требования</span><span class="sxs-lookup"><span data-stu-id="140c7-132">Requirements</span></span>



| <span data-ttu-id="140c7-133">Требование</span><span class="sxs-lookup"><span data-stu-id="140c7-133">Requirement</span></span> | <span data-ttu-id="140c7-134">Значение</span><span class="sxs-lookup"><span data-stu-id="140c7-134">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="140c7-135">Header</span><span class="sxs-lookup"><span data-stu-id="140c7-135">Header</span></span><br/>  | <dl> <span data-ttu-id="140c7-136"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="140c7-136"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="140c7-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="140c7-137">Library</span></span><br/> | <dl> <span data-ttu-id="140c7-138"><dt>Стрмбасе. lib; </dt> <dt>Стрмбасд. lib</dt></span><span class="sxs-lookup"><span data-stu-id="140c7-138"><dt>Strmbase.lib; </dt> <dt>Strmbasd.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="140c7-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="140c7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="140c7-140">Ссылка на базовый класс</span><span class="sxs-lookup"><span data-stu-id="140c7-140">Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 

