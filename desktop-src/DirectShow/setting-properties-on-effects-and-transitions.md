---
description: Задание свойств для эффектов и переходов
ms.assetid: ce773140-7e50-4b72-8cb5-e34cba51644d
title: Задание свойств для эффектов и переходов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ddd129eb9d4ab24ebef6f5c760a4211f26c9a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672935"
---
# <a name="setting-properties-on-effects-and-transitions"></a><span data-ttu-id="38745-103">Задание свойств для эффектов и переходов</span><span class="sxs-lookup"><span data-stu-id="38745-103">Setting Properties on Effects and Transitions</span></span>

<span data-ttu-id="38745-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="38745-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="38745-105">Многие эффекты и переходы [служб редактирования DirectShow](directshow-editing-services.md) поддерживают свойства, управляющие их поведением.</span><span class="sxs-lookup"><span data-stu-id="38745-105">Many [DirectShow Editing Services](directshow-editing-services.md) effects and transitions support properties that control their behavior.</span></span> <span data-ttu-id="38745-106">Приложение может задать значение свойства с помощью интерфейса [**ипропертисеттер**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="38745-106">An application can set the value of a property using the [**IPropertySetter**](ipropertysetter.md) interface.</span></span> <span data-ttu-id="38745-107">Базовый результат или объект перехода должен поддерживать интерфейс **IDispatch** для установки свойств.</span><span class="sxs-lookup"><span data-stu-id="38745-107">The underlying effect or transition object must support **IDispatch** for setting the properties.</span></span> <span data-ttu-id="38745-108">С помощью видеоэффектов и переходов приложение может задать диапазон значений, которые изменяются со временем.</span><span class="sxs-lookup"><span data-stu-id="38745-108">With video effects and transitions, the application can set a range of values that change over time.</span></span> <span data-ttu-id="38745-109">(Например, можно задать переход на очистку, чтобы перемещаться назад и вперед по кадру.) При использовании звуковых эффектов значение свойства является статическим и не может меняться со временем.</span><span class="sxs-lookup"><span data-stu-id="38745-109">(For example, you can set a wipe transition to move back and forth across the frame.) With audio effects, the value of the property is static and cannot change over time.</span></span> <span data-ttu-id="38745-110">Единственным исключением является действие [конверта тома](volume-envelope-effect.md) , которое поддерживает динамическое свойство для уровня громкости.</span><span class="sxs-lookup"><span data-stu-id="38745-110">The only exception is the [Volume Envelope](volume-envelope-effect.md) effect, which supports a dynamic property for the volume level.</span></span>

<span data-ttu-id="38745-111">Чтобы задать свойство, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="38745-111">To set a property, perform the following steps.</span></span>

1.  <span data-ttu-id="38745-112">Создайте экземпляр метода задания свойства (CLSID \_ пропертисеттер).</span><span class="sxs-lookup"><span data-stu-id="38745-112">Create an instance of the property setter (CLSID\_PropertySetter).</span></span>
2.  <span data-ttu-id="38745-113">Заполните структуры [**Декстер \_ param**](dexter-param.md) и [**Декстер \_ value**](dexter-value.md) данными свойства.</span><span class="sxs-lookup"><span data-stu-id="38745-113">Fill [**DEXTER\_PARAM**](dexter-param.md) and [**DEXTER\_VALUE**](dexter-value.md) structures with the property data.</span></span> <span data-ttu-id="38745-114">Эти структуры обсуждаются ниже.</span><span class="sxs-lookup"><span data-stu-id="38745-114">These structures are discussed below.</span></span>
3.  <span data-ttu-id="38745-115">Передайте структуры [**\_ значений**](dexter-value.md) [**Декстер \_**](dexter-param.md) и Декстер в метод [**ипропертисеттер:: аддпроп**](ipropertysetter-addprop.md) .</span><span class="sxs-lookup"><span data-stu-id="38745-115">Pass the [**DEXTER\_PARAM**](dexter-param.md) and [**DEXTER\_VALUE**](dexter-value.md) structures to the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method.</span></span>
4.  <span data-ttu-id="38745-116">Повторите шаги 2 и 3 для каждого свойства, которое необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="38745-116">Repeat steps 2 and 3 for each property you want to set.</span></span>
5.  <span data-ttu-id="38745-117">Передайте указатель интерфейса [**ипропертисеттер**](ipropertysetter.md) в метод [**Иамтимелинеобж:: сетпропертисеттер**](iamtimelineobj-setpropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="38745-117">Pass the [**IPropertySetter**](ipropertysetter.md) interface pointer to the [**IAMTimelineObj::SetPropertySetter**](iamtimelineobj-setpropertysetter.md) method.</span></span>

<span data-ttu-id="38745-118">Структура [**\_ param Декстер**](dexter-param.md) указывает, какое свойство задается.</span><span class="sxs-lookup"><span data-stu-id="38745-118">The [**DEXTER\_PARAM**](dexter-param.md) structure specifies which property is being set.</span></span> <span data-ttu-id="38745-119">Он содержит следующие члены.</span><span class="sxs-lookup"><span data-stu-id="38745-119">It contains the following members.</span></span>

-   <span data-ttu-id="38745-120">**Name**: имя свойства.</span><span class="sxs-lookup"><span data-stu-id="38745-120">**Name**: Name of the property</span></span>
-   <span data-ttu-id="38745-121">**DISPID**: reserved, должен быть равен нулю</span><span class="sxs-lookup"><span data-stu-id="38745-121">**dispID**: Reserved, must be zero</span></span>
-   <span data-ttu-id="38745-122">**nзначения**: число значений</span><span class="sxs-lookup"><span data-stu-id="38745-122">**nValues**: Number of values</span></span>

<span data-ttu-id="38745-123">\_Структура значения Декстер задает значение свойства в определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="38745-123">The DEXTER\_VALUE structure specifies the value of a property at a given time.</span></span> <span data-ttu-id="38745-124">Он содержит следующие члены.</span><span class="sxs-lookup"><span data-stu-id="38745-124">It contains the following members.</span></span>

-   <span data-ttu-id="38745-125">**v**: тип Variant, указывающий новое значение для свойства.</span><span class="sxs-lookup"><span data-stu-id="38745-125">**v**: VARIANT type that specifies a new value for the property.</span></span> <span data-ttu-id="38745-126">Элемент **VT** в этом варианте определяет тип данных свойства.</span><span class="sxs-lookup"><span data-stu-id="38745-126">The **vt** member of this VARIANT defines the data type of the property.</span></span> <span data-ttu-id="38745-127">Дополнительные сведения о типе **варианта** см. в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="38745-127">For more information on the **VARIANT** type, see the Windows SDK.</span></span>
-   <span data-ttu-id="38745-128">**RT**: время ссылки, когда свойство принимает это значение относительно времени начала действия или перехода.</span><span class="sxs-lookup"><span data-stu-id="38745-128">**rt**: Reference time when the property assumes this value, relative to the starting time of the effect or transition.</span></span> <span data-ttu-id="38745-129">Время начала действия или перехода задается относительно времени начала родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="38745-129">The start time of the effect or transition is relative to the start time of its parent object.</span></span>
-   <span data-ttu-id="38745-130">**двинтерп**: флаг, указывающий, каким образом свойство меняет предыдущее значение на новое значение.</span><span class="sxs-lookup"><span data-stu-id="38745-130">**dwInterp**: Flag that specifies how the property changes from the previous value to the new value.</span></span> <span data-ttu-id="38745-131">При использовании \_ флага перехода декстерф свойство немедленно переходит к новому значению в указанное время.</span><span class="sxs-lookup"><span data-stu-id="38745-131">With the DEXTERF\_JUMP flag, the property jumps instantly to the new value at the specified time.</span></span> <span data-ttu-id="38745-132">При использовании \_ флага интерполяции декстерф свойство линейно передается из предыдущего значения.</span><span class="sxs-lookup"><span data-stu-id="38745-132">With the DEXTERF\_INTERPOLATE flag, the property is interpolated linearly from the previous value.</span></span>

<span data-ttu-id="38745-133">Если присвоить элементу **VT** значение VT \_ BSTR, метод задания свойств выполняет все необходимые преобразования.</span><span class="sxs-lookup"><span data-stu-id="38745-133">If you set the **vt** member to VT\_BSTR, the property setter makes any necessary conversions.</span></span> <span data-ttu-id="38745-134">Для значений с плавающей запятой включите начальный ноль перед десятичной запятой.</span><span class="sxs-lookup"><span data-stu-id="38745-134">For floating-point values, include the leading zero before the decimal place.</span></span> <span data-ttu-id="38745-135">Например, 0,3, а не. 3.</span><span class="sxs-lookup"><span data-stu-id="38745-135">For example, 0.3, not .3.</span></span>

> [!Note]  
> <span data-ttu-id="38745-136">Приложения не должны полагаться на преобразование из **BSTR** s в числовые значения.</span><span class="sxs-lookup"><span data-stu-id="38745-136">Applications should avoid relying on the conversion from **BSTR** s to numeric values.</span></span> <span data-ttu-id="38745-137">Если свойство имеет числовое значение, возможно использование соответствующего числового типа **Variant** .</span><span class="sxs-lookup"><span data-stu-id="38745-137">If the property has a numeric value, use the appropriate numeric **VARIANT** type is possible.</span></span>

 

<span data-ttu-id="38745-138">Значение свойства может изменяться со временем, поэтому метод [**ипропертисеттер:: аддпроп**](ipropertysetter-addprop.md) принимает одну структуру [**\_ param Декстер**](dexter-param.md) и указатель на массив [**декстерных структур \_ значений**](dexter-value.md) .</span><span class="sxs-lookup"><span data-stu-id="38745-138">The value of a property can change over time, so the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method takes a single [**DEXTER\_PARAM**](dexter-param.md) structure and a pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span> <span data-ttu-id="38745-139">Массив определяет набор значений, основанных на времени для свойства.</span><span class="sxs-lookup"><span data-stu-id="38745-139">The array defines a set of time-based values for the property.</span></span> <span data-ttu-id="38745-140">Элементы массива должны быть в порядке возрастания времени, а элемент **nзначения** \_ структуры param Декстер должен равняться длине массива.</span><span class="sxs-lookup"><span data-stu-id="38745-140">The members of the array must be in ascending time order, and the **nValues** member of the DEXTER\_PARAM structure must equal the length of the array.</span></span>

<span data-ttu-id="38745-141">В следующем примере кода создаются данные свойства для перехода на [очистку SMPTE](smpte-wipe-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="38745-141">The following code example creates property data for the [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span> <span data-ttu-id="38745-142">Он устанавливает для кода очистки значение 120, при котором создается очистка овала.</span><span class="sxs-lookup"><span data-stu-id="38745-142">It sets the wipe code to 120, which creates an oval wipe.</span></span> <span data-ttu-id="38745-143">Он устанавливает время ссылки равным нулю, указывая начало перехода.</span><span class="sxs-lookup"><span data-stu-id="38745-143">It sets the reference time to zero, indicating the start of the transition.</span></span>


```C++
IPropertySetter     *pProp;   // Property setter
IAMTimelineObj      *pTransObj;  // Transition object
// Create an SMPTE Wipe transition object. (Not shown)

hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER,
    IID_IPropertySetter, (void**) &pProp);

// Error checking is omitted for clarity...

DEXTER_PARAM param;
DEXTER_VALUE *pValue = (DEXTER_VALUE*)CoTaskMemAlloc(sizeof(DEXTER_VALUE));

// Initialize the parameter. 
param.Name = SysAllocString(L"MaskNum");
param.dispID = 0;
param.nValues = 1;

// Initialize the value.
pValue->v.vt = VT_I4;
pValue->v.lVal = 120; // Oval
pValue->rt = 0;
pValue->dwInterp = DEXTERF_JUMP;

pProp->AddProp(param, pValue);

// Free allocated resources.
SysFreeString(param.Name);
VariantClear(&(pValue->v));
CoTaskMemFree(pValue);

// Set the property on the transition.
pTransObj->SetPropertySetter(pProp);
pProp->Release();
```



<span data-ttu-id="38745-144">**Динамическое изменение свойств**</span><span class="sxs-lookup"><span data-stu-id="38745-144">**Dynamically Changing Properties**</span></span>

<span data-ttu-id="38745-145">После отрисовки проекта редактирования видео можно изменить свойства эффектов или объекта перехода во время работы графа.</span><span class="sxs-lookup"><span data-stu-id="38745-145">After you render a video editing project, it is possible to modify an effect or transition object's properties while the graph is running.</span></span> <span data-ttu-id="38745-146">Однако это возможно только в том случае, если задать свойства для этого объекта до того, как приложение будет называться [**ирендеренгине:: коннектфронтенд**](irenderengine-connectfrontend.md).</span><span class="sxs-lookup"><span data-stu-id="38745-146">However, this is possible only if you set properties on that object before the application called [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span> <span data-ttu-id="38745-147">Если это так, можно вызвать [**иамтимелинеобж:: жетпропертисеттер**](iamtimelineobj-getpropertysetter.md) для действия или перехода, очистить или изменить свойства, и изменения будут выполняться динамически при выполнении графа.</span><span class="sxs-lookup"><span data-stu-id="38745-147">If so, you can call [**IAMTimelineObj::GetPropertySetter**](iamtimelineobj-getpropertysetter.md) on the effect or transition, clear or modify the properties, and the changes will happen dynamically as the graph is running.</span></span> <span data-ttu-id="38745-148">В процессе изменения могут возникать визуальные аномалии, поэтому рекомендуется только для предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="38745-148">There may be visual anomalies while the change occurs, so this is recommended only for preview.</span></span> <span data-ttu-id="38745-149">Не изменяйте свойства при записи проекта в файл.</span><span class="sxs-lookup"><span data-stu-id="38745-149">Do not change the properties while you are writing the project to a file.</span></span>

<span data-ttu-id="38745-150">Если вы не устанавливали какие-либо свойства для объекта Effect или Transition перед вызовом **коннектфронтенд**, вы не сможете добавить свойства в него во время работы графа.</span><span class="sxs-lookup"><span data-stu-id="38745-150">If you did not set any properties on the effect or transition object before you called **ConnectFrontEnd**, you cannot add properties to it while the graph is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38745-151">См. также</span><span class="sxs-lookup"><span data-stu-id="38745-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38745-152">Работа с эффектами и переходами</span><span class="sxs-lookup"><span data-stu-id="38745-152">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



