---
title: defaultcollelem - атрибут
description: Атрибут \ дефаултколлелем \ помечает свойство как функцию доступа для элемента коллекции по умолчанию.
ms.assetid: e409f845-3f26-4551-abda-86c4776160aa
keywords:
- атрибут дефаултколлелем MIDL
topic_type:
- apiref
api_name:
- defaultcollelem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45fdbd59ca954d955fc5598b2bc2dc7a39ee14b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069950"
---
# <a name="defaultcollelem-attribute"></a><span data-ttu-id="5665b-104">defaultcollelem - атрибут</span><span class="sxs-lookup"><span data-stu-id="5665b-104">defaultcollelem attribute</span></span>

<span data-ttu-id="5665b-105">Атрибут **\[ дефаултколлелем \]** помечает свойство как функцию доступа для элемента коллекции по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5665b-105">The **\[defaultcollelem\]** attribute flags a property as an accessor function for an element of the default collection.</span></span>

``` syntax
[property-attribute-list, defaultcollelem] return-type property-name(prop-param-list)
```

## <a name="parameters"></a><span data-ttu-id="5665b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5665b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5665b-107">*Property — список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="5665b-107">*property-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5665b-108">Другие атрибуты, которые применяются к свойству.</span><span class="sxs-lookup"><span data-stu-id="5665b-108">Other attributes that apply to the property.</span></span>

</dd> <dt>

<span data-ttu-id="5665b-109">*Тип возвращаемого значения*</span><span class="sxs-lookup"><span data-stu-id="5665b-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="5665b-110">Указывает тип возвращаемого значения функции.</span><span class="sxs-lookup"><span data-stu-id="5665b-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="5665b-111">*имя свойства*</span><span class="sxs-lookup"><span data-stu-id="5665b-111">*property-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5665b-112">Имя свойства.</span><span class="sxs-lookup"><span data-stu-id="5665b-112">The name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="5665b-113">*Prop-param-List*</span><span class="sxs-lookup"><span data-stu-id="5665b-113">*prop-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5665b-114">Список из нуля или более параметров, связанных со свойством.</span><span class="sxs-lookup"><span data-stu-id="5665b-114">A list of zero or more parameters associated with the property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5665b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5665b-115">Remarks</span></span>

<span data-ttu-id="5665b-116">Атрибут **\[ дефаултколлелем \]** используется для оптимизации кода Visual басикâ®.</span><span class="sxs-lookup"><span data-stu-id="5665b-116">The **\[defaultcollelem\]** attribute is used for Visual BasicÂ® code optimization.</span></span> <span data-ttu-id="5665b-117">Если член интерфейса или DISP помечается как функция доступа, то вызов перейдет непосредственно к этому элементу.</span><span class="sxs-lookup"><span data-stu-id="5665b-117">If a member of an interface or dispinterface is flagged as an accessor function, then the call will go directly to that member.</span></span>

<span data-ttu-id="5665b-118">Использование **\[ дефаултколлелем \]** должно соответствовать свойству.</span><span class="sxs-lookup"><span data-stu-id="5665b-118">Use of **\[defaultcollelem\]** must be consistent for a property.</span></span> <span data-ttu-id="5665b-119">Например, если атрибут используется для свойства *Get* , он также должен присутствовать в свойстве *let* .</span><span class="sxs-lookup"><span data-stu-id="5665b-119">For example, if you use the attribute on a *Get* property, it must also be present on a *Let* property.</span></span>

### <a name="typeflags-representation"></a><span data-ttu-id="5665b-120">Представление типефлагс</span><span class="sxs-lookup"><span data-stu-id="5665b-120">Typeflags Representation</span></span>

<span data-ttu-id="5665b-121">Присутствие ФУНКФЛАГ \_ фдефаултколлелем или варфлаг \_ фдефаултколлелем.</span><span class="sxs-lookup"><span data-stu-id="5665b-121">The presence of FUNCFLAG\_FDEFAULTCOLLELEM or VARFLAG\_FDEFAULTCOLLELEM.</span></span>

## <a name="examples"></a><span data-ttu-id="5665b-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="5665b-122">Examples</span></span>

``` syntax
//A form has a button on it named Button1. 
//To enable use of the property syntax and efficient use of the !
//syntax, the form describes itself in type info this way.
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is IForm"),
    restricted
]
interface IForm1: IForm
{
    [propget, defaultcollelem] HRESULT Button1(
        [out, retval] Button *Value);
}

//User code may access the button using property syntax or ! syntax.

Sub Test()
Dim f as Form1
Dim b1 As Button
Dim b2 As Button

Set f = Form1

Set b1 = f.Button1        ' Property syntax
Set b = f!Button1        ' ! syntax
End Sub
```

## <a name="see-also"></a><span data-ttu-id="5665b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5665b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5665b-124">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="5665b-124">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="5665b-125">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="5665b-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="5665b-126">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="5665b-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 