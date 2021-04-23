---
title: uidefault - атрибут
description: Атрибут \ уидефаулт \ указывает, что элемент сведений о типе является элементом по умолчанию для вывода в пользовательском интерфейсе.
ms.assetid: e789be38-a509-437d-89c9-ebbc830e5ae2
keywords:
- атрибут уидефаулт MIDL
topic_type:
- apiref
api_name:
- uidefault
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcef39f36abad7c7cb5562b2d892761bd1bb7b5b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412816"
---
# <a name="uidefault-attribute"></a><span data-ttu-id="457f8-104">uidefault - атрибут</span><span class="sxs-lookup"><span data-stu-id="457f8-104">uidefault attribute</span></span>

<span data-ttu-id="457f8-105">Атрибут **\[ уидефаулт \]** указывает, что элемент сведений о типе является элементом по умолчанию для вывода в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="457f8-105">The **\[uidefault\]** attribute indicates that the type information member is the default member for display in the user interface.</span></span>

``` syntax
[method-attribute-list, uidefault]return-type method-name(method-parameter-list)
```

## <a name="parameters"></a><span data-ttu-id="457f8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="457f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="457f8-107">*Method — список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="457f8-107">*method-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="457f8-108">Другие атрибуты, которые применяются к методу.</span><span class="sxs-lookup"><span data-stu-id="457f8-108">Other attributes that apply to the method.</span></span>

</dd> <dt>

<span data-ttu-id="457f8-109">*Тип возвращаемого значения*</span><span class="sxs-lookup"><span data-stu-id="457f8-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="457f8-110">Тип данных, возвращаемых методом при завершении выполнения.</span><span class="sxs-lookup"><span data-stu-id="457f8-110">The type of the data that the method will return when it finishes execution.</span></span>

</dd> <dt>

<span data-ttu-id="457f8-111">*имя метода*</span><span class="sxs-lookup"><span data-stu-id="457f8-111">*method-name*</span></span> 
</dt> <dd>

<span data-ttu-id="457f8-112">Имя метода.</span><span class="sxs-lookup"><span data-stu-id="457f8-112">The name of the method.</span></span>

</dd> <dt>

<span data-ttu-id="457f8-113">*метод-Parameter-список*</span><span class="sxs-lookup"><span data-stu-id="457f8-113">*method-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="457f8-114">Ноль или более параметров для метода.</span><span class="sxs-lookup"><span data-stu-id="457f8-114">Zero or more parameters for the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="457f8-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="457f8-115">Remarks</span></span>

<span data-ttu-id="457f8-116">Применение атрибута **\[ уидефаулт \]** к члену интерфейса или DISP-интерфейсу сообщает Visual Basic во время разработки, чтобы автоматически отображать это событие или свойство пользователю.</span><span class="sxs-lookup"><span data-stu-id="457f8-116">Applying the **\[uidefault\]** attribute to a member of an interface or a dispinterface tells Visual Basic, at design-time, to automatically display this event or property to the user.</span></span> <span data-ttu-id="457f8-117">Это означает, что когда пользователь дважды щелкает объект, Visual Basic переходит к событию в исходном интерфейсе по умолчанию с атрибутом **\[ уидефаулт \]** .</span><span class="sxs-lookup"><span data-stu-id="457f8-117">This means that when the user double-clicks an object, Visual Basic jumps to the event in the default source interface that has the **\[uidefault\]** attribute.</span></span> <span data-ttu-id="457f8-118">Когда пользователь выбирает объект, браузер свойств Visual Basic отображает свойство в исходном интерфейсе по умолчанию, который имеет этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="457f8-118">When the user selects an object, Visual Basic's Properties browser displays the property in the default source interface that has this attribute.</span></span> <span data-ttu-id="457f8-119">Если событие или свойство не имеет атрибута **\[ уидефаулт \]** , Visual Basic отображает первое событие или свойство, перечисленные в интерфейсе по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="457f8-119">If no event or property has the **\[uidefault\]** attribute, Visual Basic displays the first event or property listed in the default interface.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="457f8-120">Представление типефлаг</span><span class="sxs-lookup"><span data-stu-id="457f8-120">Typeflag Representation</span></span>

<span data-ttu-id="457f8-121">Присутствие ФУНКФЛАГ \_ фуидефаулт или варфлаг \_ фуидефаулт</span><span class="sxs-lookup"><span data-stu-id="457f8-121">The presence of FUNCFLAG\_FUIDEFAULT or VARFLAG\_FUIDEFAULT</span></span>

## <a name="examples"></a><span data-ttu-id="457f8-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="457f8-122">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget]HRESULT Backcolor([out, retval] long *Value);
    [propput]HRESULT Backcolor([in] long Value);
    [propget, uidefault]HRESULT Name([out, retval] BSTR *Value);
    [propput, uidefault]HRESULT Name([in] BSTR Value);
}
[
    odl,
    dual,
    uuid(87654321-1234-1234-1234-123456789ABC),
    restricted
] 
interface IFormEvents: IDispatch
{
    [uidefault]HRESULT Click();
    HRESULT Resize();
}

[
    uuid(12345678-1234-1234-1234-987654321ABC)
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="457f8-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="457f8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="457f8-124">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="457f8-124">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="457f8-125">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="457f8-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="457f8-126">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="457f8-126">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 