---
title: Реализация файла IEnumSTATPROPSTG-Compound
description: Реализация составного файла интерфейса Иенумстатпропстг используется для перечисления свойств, в результате чего структуры СТАТПРОПСТГ, которые содержат данные статистических свойств.
ms.assetid: 8fa536f4-cce6-47e4-a860-2f43e48fa469
keywords:
- Иенумстатпропстг Стрктд STG, реализация составного файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbffce14016efdb4e2a77d60096b6776e6c2189
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987784"
---
# <a name="ienumstatpropstg-compound-file-implementation"></a><span data-ttu-id="cc4bd-104">Реализация файла IEnumSTATPROPSTG-Compound</span><span class="sxs-lookup"><span data-stu-id="cc4bd-104">IEnumSTATPROPSTG-Compound File Implementation</span></span>

<span data-ttu-id="cc4bd-105">Реализация составного файла интерфейса [**иенумстатпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) используется для перечисления свойств, в результате чего структуры [**статпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , которые содержат данные статистических свойств.</span><span class="sxs-lookup"><span data-stu-id="cc4bd-105">The compound file implementation of the [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) interface is used to enumerate properties, resulting in [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures, which contain statistical property data.</span></span> <span data-ttu-id="cc4bd-106">Реализация [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) управляет статистическими данными и связывается с текущим объектом хранилища составного файла.</span><span class="sxs-lookup"><span data-stu-id="cc4bd-106">The implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) manages the statistical data and is associated with a current compound file storage object.</span></span>

<span data-ttu-id="cc4bd-107">Конструктор в реализации COM [**иенумстатпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) создает класс, который считывает набор свойств и создает статический массив, который может использоваться совместно при вызове **Иенумстатпропстг:: Clone** .</span><span class="sxs-lookup"><span data-stu-id="cc4bd-107">The constructor in the COM implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) creates a class that reads the entire property set, and creates a static array which can be shared when **IEnumSTATPROPSTG::Clone** is called.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="cc4bd-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="cc4bd-108">When to Use</span></span>

<span data-ttu-id="cc4bd-109">Вызовите реализацию составного файла [**иенумстатпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , чтобы перечислить структуры [**статпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , содержащие данные о свойствах в текущем наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="cc4bd-109">Call the compound file implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) to enumerate the [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures that contain data about the properties within the current property set.</span></span> <span data-ttu-id="cc4bd-110">При использовании реализации составного файла интерфейсов хранилища свойств вызовите [**ипропертистораже:: Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) , чтобы вернуть указатель на **иенумстатпропстг** для управления объектом хранилища свойств и элементами внутри него.</span><span class="sxs-lookup"><span data-stu-id="cc4bd-110">When using the compound file implementation of the property storage interfaces, call [**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) to return a pointer to **IEnumSTATPROPSTG** to manage the property storage object and the elements within it.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc4bd-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc4bd-111">Remarks</span></span>

<dl> <dt>

<span data-ttu-id="cc4bd-112"><span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**Иенумстатпропстг:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="cc4bd-112"><span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**IEnumSTATPROPSTG::Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="cc4bd-113">Возвращает следующую одну или несколько структур [**статпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) (число определяется параметром *celt* ).</span><span class="sxs-lookup"><span data-stu-id="cc4bd-113">Gets the next one or more [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures (the number is specified by the *celt* parameter).</span></span> <span data-ttu-id="cc4bd-114">\_При успешном выполнении возвращает значение ОК.</span><span class="sxs-lookup"><span data-stu-id="cc4bd-114">Returns S\_OK if successful.</span></span>

</dd> <dt>

<span data-ttu-id="cc4bd-115"><span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**Иенумстатпропстг:: Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="cc4bd-115"><span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**IEnumSTATPROPSTG::Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="cc4bd-116">Пропускает количество элементов, указанное в параметре *celt*.</span><span class="sxs-lookup"><span data-stu-id="cc4bd-116">Skips the number of elements specified in *celt*.</span></span> <span data-ttu-id="cc4bd-117">Следующий элемент, который будет перечисляться с помощью вызова Next, станет элементом после пропущенных элементов.</span><span class="sxs-lookup"><span data-stu-id="cc4bd-117">The next element to be enumerated through a call to Next then becomes the element after the skipped elements.</span></span> <span data-ttu-id="cc4bd-118">Возвращает \_ значение "ОК", если значения *celt* пропущены; \_ Если пропущено менее *celt* элементов, возвращает s false.</span><span class="sxs-lookup"><span data-stu-id="cc4bd-118">Returns S\_OK if *celt* elements were skipped; returns S\_FALSE if fewer than *celt* elements were skipped.</span></span>

</dd> <dt>

<span data-ttu-id="cc4bd-119"><span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**Иенумстатпропстг:: Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="cc4bd-119"><span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**IEnumSTATPROPSTG::Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="cc4bd-120">Устанавливает курсор в начало перечисления.</span><span class="sxs-lookup"><span data-stu-id="cc4bd-120">Sets the cursor to the beginning of the enumeration.</span></span> <span data-ttu-id="cc4bd-121">В случае успеха возвращает S \_ ОК, в противном случае ВОЗВРАЩАЕТ STG \_ E \_ инвалидхандле.</span><span class="sxs-lookup"><span data-stu-id="cc4bd-121">If successful, returns S\_OK, otherwise, returns STG\_E\_INVALIDHANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="cc4bd-122"><span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**Иенумстатпропстг:: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="cc4bd-122"><span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**IEnumSTATPROPSTG::Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="cc4bd-123">Использует конструктор для [**иенумстатпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , чтобы создать копию массива.</span><span class="sxs-lookup"><span data-stu-id="cc4bd-123">Uses the constructor for the [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) to create a copy of the array.</span></span> <span data-ttu-id="cc4bd-124">Поскольку класс, создающий статический массив, фактически содержит объект, эта функция в основном добавляет к счетчику ссылок.</span><span class="sxs-lookup"><span data-stu-id="cc4bd-124">Because the class that constructs the static array actually contains the object, this function mainly adds to the reference count.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="cc4bd-125">См. также</span><span class="sxs-lookup"><span data-stu-id="cc4bd-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc4bd-126">**статпропстг**</span><span class="sxs-lookup"><span data-stu-id="cc4bd-126">**STATPROPSTG**</span></span>](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dt>

[<span data-ttu-id="cc4bd-127">**Ипропертистораже:: Enum**</span><span class="sxs-lookup"><span data-stu-id="cc4bd-127">**IPropertyStorage::Enum**</span></span>](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> </dl>

 

 