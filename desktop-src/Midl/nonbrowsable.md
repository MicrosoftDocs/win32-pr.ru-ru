---
title: nonbrowsable - атрибут
description: Используйте атрибут \ неотображаемый \, чтобы пометить интерфейс или член disp-интерфейса, который не должен отображаться в браузере свойств.
ms.assetid: 94e868cc-8d9c-4b8a-ac18-1ea513a103da
keywords:
- неотображаемый атрибут MIDL
topic_type:
- apiref
api_name:
- nonbrowsable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e24c39511df9637c352245b98b237fe8fd451eb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987408"
---
# <a name="nonbrowsable-attribute"></a><span data-ttu-id="db6ff-104">nonbrowsable - атрибут</span><span class="sxs-lookup"><span data-stu-id="db6ff-104">nonbrowsable attribute</span></span>

<span data-ttu-id="db6ff-105">Используйте **\[ неотображаемый \]** атрибут, чтобы пометить интерфейс или член disp-интерфейса, который не должен отображаться в браузере свойств.</span><span class="sxs-lookup"><span data-stu-id="db6ff-105">Use the **\[nonbrowsable\]** attribute to tag an interface or dispinterface member that should not be displayed in a properties browser.</span></span>

``` syntax
[property-attribute-list, nonbrowsable]return-type property-name(prop-param-list)
```

## <a name="parameters"></a><span data-ttu-id="db6ff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="db6ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db6ff-107">*Property — список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="db6ff-107">*property-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="db6ff-108">Другие атрибуты, которые применяются к свойству.</span><span class="sxs-lookup"><span data-stu-id="db6ff-108">Other attributes that apply to the property.</span></span>

</dd> <dt>

<span data-ttu-id="db6ff-109">*Тип возвращаемого значения*</span><span class="sxs-lookup"><span data-stu-id="db6ff-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="db6ff-110">Тип данных, возвращаемых методом.</span><span class="sxs-lookup"><span data-stu-id="db6ff-110">The type of the data returned by the method.</span></span>

</dd> <dt>

<span data-ttu-id="db6ff-111">*имя свойства*</span><span class="sxs-lookup"><span data-stu-id="db6ff-111">*property-name*</span></span> 
</dt> <dd>

<span data-ttu-id="db6ff-112">Имя свойства или метода.</span><span class="sxs-lookup"><span data-stu-id="db6ff-112">The name of the property or method.</span></span>

</dd> <dt>

<span data-ttu-id="db6ff-113">*Prop-param-List*</span><span class="sxs-lookup"><span data-stu-id="db6ff-113">*prop-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="db6ff-114">Ноль или более параметров, которые должны быть переданы в метод.</span><span class="sxs-lookup"><span data-stu-id="db6ff-114">Zero or more parameters to be passed to the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db6ff-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db6ff-115">Remarks</span></span>

<span data-ttu-id="db6ff-116">Некоторые свойства не должны отображаться в обозревателе свойств.</span><span class="sxs-lookup"><span data-stu-id="db6ff-116">Certain properties should not be displayed in a properties browser.</span></span> <span data-ttu-id="db6ff-117">Это может быть вызвано тем, что получение значения займет очень много времени.</span><span class="sxs-lookup"><span data-stu-id="db6ff-117">This may be because retrieving the value would take a very long time.</span></span> <span data-ttu-id="db6ff-118">В этом примере пользователь не пытается получить свойство *Count* , которое возвращает число строк в динамическом наборе. Это число может представлять результаты очень большого запроса.</span><span class="sxs-lookup"><span data-stu-id="db6ff-118">The example prevents the user from attempting to retrieve the *Count* property, which returns the number of rows in the dynaset.This number may represent the results of a very large query.</span></span>

<span data-ttu-id="db6ff-119">Другие свойства могут иметь непредвиденные эффекты в браузере.</span><span class="sxs-lookup"><span data-stu-id="db6ff-119">Other properties may have unexpected effects on the browser.</span></span> <span data-ttu-id="db6ff-120">Например, рассмотрим элемент управления со свойством «OnSelected», чтобы определить, выбран ли элемент управления.</span><span class="sxs-lookup"><span data-stu-id="db6ff-120">For example, consider a control with the property "IsSelected" to tell whether the control is selected.</span></span> <span data-ttu-id="db6ff-121">Если параметру "IsFalse" присвоено значение false, обозреватель свойств, основанный на выборе, будет просматривать другой объект.</span><span class="sxs-lookup"><span data-stu-id="db6ff-121">If "IsSelected" is set to false, a selection-based properties browser will browse a different object.</span></span>

<span data-ttu-id="db6ff-122">Обратите внимание, что свойство, помеченное **\[ \] как недоступное для просмотра** , по-прежнему будет отображаться в обозревателе объектов, в котором не отображаются значения свойств.</span><span class="sxs-lookup"><span data-stu-id="db6ff-122">Note that a property tagged as **\[nonbrowsable\]** will still appear in an object browser, which does not show property values.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="db6ff-123">Представление типефлаг</span><span class="sxs-lookup"><span data-stu-id="db6ff-123">Typeflag Representation</span></span>

<span data-ttu-id="db6ff-124">Присутствие ФУНКФЛАГ \_ фнонбровсабле или варфлаг \_ фнонбровсабле.</span><span class="sxs-lookup"><span data-stu-id="db6ff-124">The presence of FUNCFLAG\_FNONBROWSABLE or VARFLAG\_FNONBROWSABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="db6ff-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="db6ff-125">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IDynaset:IDispatch
{
    [propget, nonbrowsable]HRESULT Count([out, retval] long *Value);
}
```

## <a name="see-also"></a><span data-ttu-id="db6ff-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db6ff-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db6ff-127">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="db6ff-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="db6ff-128">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="db6ff-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="db6ff-129">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="db6ff-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 