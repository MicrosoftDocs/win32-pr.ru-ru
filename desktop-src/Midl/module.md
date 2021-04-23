---
title: атрибут module
description: Оператор Module определяет группу функций, обычно набор точек входа DLL.
ms.assetid: 4dec207f-98bc-4784-a3c9-506ffe7523fe
keywords:
- атрибут модуля MIDL
topic_type:
- apiref
api_name:
- module
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1eb310c3e126caf9b25b8c015b840aea11791d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337132"
---
# <a name="module-attribute"></a><span data-ttu-id="928be-104">атрибут module</span><span class="sxs-lookup"><span data-stu-id="928be-104">module attribute</span></span>

<span data-ttu-id="928be-105">Оператор **module** определяет группу функций, обычно набор точек входа DLL.</span><span class="sxs-lookup"><span data-stu-id="928be-105">The **module** statement defines a group of functions, typically a set of DLL entry points.</span></span>

``` syntax
[
    attributes
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a><span data-ttu-id="928be-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="928be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="928be-107">*attributes*</span><span class="sxs-lookup"><span data-stu-id="928be-107">*attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="928be-108">Атрибуты \[ [**UUID**](uuid.md) \] , \[ [**Version**](version.md) \] , \[ [**helpString**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**Hidden**](hidden.md) \] и \[ [**dllname**](dllname-str-.md) \] принимаются перед оператором **module** .</span><span class="sxs-lookup"><span data-stu-id="928be-108">The \[[**uuid**](uuid.md)\], \[[**version**](version.md)\], \[[**helpstring**](helpstring.md)\], \[[**helpcontext**](helpcontext.md)\], \[[**hidden**](hidden.md)\], and \[[**dllname**](dllname-str-.md)\] attributes are accepted before a **module** statement.</span></span> <span data-ttu-id="928be-109">Дополнительные сведения об атрибутах, принятых перед определением модуля, см. в [описании атрибутов](/previous-versions/windows/desktop/automat/attribute-descriptions)в книге OLE-автоматизации.</span><span class="sxs-lookup"><span data-stu-id="928be-109">See [Attribute Descriptions](/previous-versions/windows/desktop/automat/attribute-descriptions), in the OLE Automation book, for more information on the attributes accepted before a module definition.</span></span> <span data-ttu-id="928be-110">Атрибут \[ **dllname** \] является обязательным.</span><span class="sxs-lookup"><span data-stu-id="928be-110">The \[**dllname**\] attribute is required.</span></span> <span data-ttu-id="928be-111">Если атрибут \[ **UUID** \] опущен, модуль не указывается уникальным образом в системе.</span><span class="sxs-lookup"><span data-stu-id="928be-111">If the \[**uuid**\] attribute is omitted, the module is not uniquely specified in the system.</span></span>

</dd> <dt>

<span data-ttu-id="928be-112">*ModuleName*</span><span class="sxs-lookup"><span data-stu-id="928be-112">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="928be-113">Имя модуля.</span><span class="sxs-lookup"><span data-stu-id="928be-113">The name of the module.</span></span>

</dd> <dt>

<span data-ttu-id="928be-114">*елементлист*</span><span class="sxs-lookup"><span data-stu-id="928be-114">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="928be-115">Список константных определений и прототипов функций для каждой функции в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="928be-115">List of constant definitions and function prototypes for each function in the DLL.</span></span> <span data-ttu-id="928be-116">В списке функций может присутствовать любое количество определений функций.</span><span class="sxs-lookup"><span data-stu-id="928be-116">Any number of function definitions can appear in the function list.</span></span> <span data-ttu-id="928be-117">Функция в списке функций имеет следующий вид:</span><span class="sxs-lookup"><span data-stu-id="928be-117">A function in the function list has the following form:</span></span>

<span data-ttu-id="928be-118">\[*атрибуты* \] *ReturnType* \[ *соглашение о вызовах funcname* \] (*params*);</span><span class="sxs-lookup"><span data-stu-id="928be-118">\[*attributes*\] *returntype* \[*calling convention funcname*\](*params*);</span></span>

<span data-ttu-id="928be-119">\[*атрибуты* \] [**const**](const.md) константтипе *констнаме*  =  *конствал*;</span><span class="sxs-lookup"><span data-stu-id="928be-119">\[*attributes*\] [**const**](const.md) constanttype *constname* = *constval*;</span></span>

<span data-ttu-id="928be-120">Только атрибуты \[ [**helpString**](helpstring.md) \] и \[ [**HelpContext**](helpcontext.md) \] принимаются для [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="928be-120">Only the \[[**helpstring**](helpstring.md)\] and \[[**helpcontext**](helpcontext.md)\] attributes are accepted for a [**const**](const.md).</span></span>

<span data-ttu-id="928be-121">Следующие атрибуты принимаются для функции в модуле: \[ [**helpString**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**String**](string.md) \] , \[ [**entry**](entry.md) \] , \[ [**propget**](propget.md) \] , \[ [**propput**](propput.md) \] , \[ [**propputref**](propputref.md) \] и \[ [**vararg**](vararg.md) \] .</span><span class="sxs-lookup"><span data-stu-id="928be-121">The following attributes are accepted on a function in a module: \[[**helpstring**](helpstring.md)\], \[[**helpcontext**](helpcontext.md)\], \[[**string**](string.md)\], \[[**entry**](entry.md)\], \[[**propget**](propget.md)\], \[[**propput**](propput.md)\], \[[**propputref**](propputref.md)\], and \[[**vararg**](vararg.md)\].</span></span> <span data-ttu-id="928be-122">Если \[  \] указано vararg, последний параметр должен быть надежным массивом типа **Variant** .</span><span class="sxs-lookup"><span data-stu-id="928be-122">If \[**vararg**\] is specified, the last parameter must be a safe array of **VARIANT** type.</span></span>

<span data-ttu-id="928be-123">Необязательное соглашение о вызовах может быть одним из \_ \_ : Pascal/ \_ Pascal/Pascal, \_ \_ cdecl/ \_ cdecl/cdecl или \_ \_ STDCALL/ \_ STDCALL/STDCALL.</span><span class="sxs-lookup"><span data-stu-id="928be-123">The optional calling convention can be one of \_\_pascal/\_pascal/pascal, \_\_cdecl/\_cdecl/cdecl, or \_\_stdcall/\_stdcall/stdcall.</span></span> <span data-ttu-id="928be-124">*Тип соглашения о вызове paramName* может включать до двух подчеркивания в начале.</span><span class="sxs-lookup"><span data-stu-id="928be-124">The *calling convention type paramname* can include up to two leading underscores.</span></span>

<span data-ttu-id="928be-125">Список параметров представляет собой разделенный запятыми список:</span><span class="sxs-lookup"><span data-stu-id="928be-125">The parameter list is a comma-delimited list of:</span></span>

<span data-ttu-id="928be-126">\[*атрибута*\]</span><span class="sxs-lookup"><span data-stu-id="928be-126">\[*attributes*\]</span></span>

<span data-ttu-id="928be-127">Тип может быть любым ранее объявленным типом или встроенным типом, указателем на любой тип или указателем на встроенный тип.</span><span class="sxs-lookup"><span data-stu-id="928be-127">The type can be any previously declared type or built-in type, a pointer to any type, or a pointer to a built-in type.</span></span> <span data-ttu-id="928be-128">Атрибуты в параметрах:</span><span class="sxs-lookup"><span data-stu-id="928be-128">Attributes on parameters are:</span></span>

<span data-ttu-id="928be-129">\[[**в**](in.md) \] , \[ [**out**](out-idl.md) \] , \[ [**необязательно**](optional.md) \] .</span><span class="sxs-lookup"><span data-stu-id="928be-129">\[[**in**](in.md)\], \[[**out**](out-idl.md)\], \[[**optional**](optional.md)\].</span></span>

<span data-ttu-id="928be-130">Если \[ используется [**необязательный**](optional.md) параметр \] , типы этих параметров должны быть **Variant** или **Variant** \* .</span><span class="sxs-lookup"><span data-stu-id="928be-130">If \[[**optional**](optional.md)\] is used, the types of those parameters must be **VARIANT** or **VARIANT**\*.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="928be-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="928be-131">Remarks</span></span>

<span data-ttu-id="928be-132">Выходные данные файла заголовка (h) для модулей — это последовательность прототипов функций.</span><span class="sxs-lookup"><span data-stu-id="928be-132">The header file (.h) output for modules is a series of function prototypes.</span></span> <span data-ttu-id="928be-133">Ключевое слово **module** и окружающие квадратные скобки удаляются из выходных данных файла заголовка (. h), но перед прототипами вставляется комментарий (// *ModuleName* **модуля** ).</span><span class="sxs-lookup"><span data-stu-id="928be-133">The **module** keyword and surrounding brackets are stripped from the header (.h) file output, but a comment (// **module** *modulename*) is inserted before the prototypes.</span></span> <span data-ttu-id="928be-134">Ключевое слово **extern** вставляется перед объявлениями.</span><span class="sxs-lookup"><span data-stu-id="928be-134">The keyword **extern** is inserted before the declarations.</span></span>

## <a name="examples"></a><span data-ttu-id="928be-135">Примеры</span><span class="sxs-lookup"><span data-stu-id="928be-135">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("This is not GDI.EXE"), 
    helpcontext(190), 
    dllname("MATH.DLL")
] 
module somemodule
{ 
    [helpstring("Color for the frame")] 
            unsigned long const COLOR_FRAME = 0xH80000006; 
    [helpstring("Not a rectangle but a square"), 
     entry(1)] 
            pascal double square([in] double x); 
};
```

## <a name="see-also"></a><span data-ttu-id="928be-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="928be-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="928be-137">**const**</span><span class="sxs-lookup"><span data-stu-id="928be-137">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="928be-138">Содержимое библиотеки типов</span><span class="sxs-lookup"><span data-stu-id="928be-138">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="928be-139">**dllname**</span><span class="sxs-lookup"><span data-stu-id="928be-139">**dllname**</span></span>](dllname-str-.md)
</dt> <dt>

[<span data-ttu-id="928be-140">**операции**</span><span class="sxs-lookup"><span data-stu-id="928be-140">**entry**</span></span>](entry.md)
</dt> <dt>

[<span data-ttu-id="928be-141">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="928be-141">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="928be-142">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="928be-142">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="928be-143">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="928be-143">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="928be-144">**служеб**</span><span class="sxs-lookup"><span data-stu-id="928be-144">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="928be-145">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="928be-145">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="928be-146">**propget**</span><span class="sxs-lookup"><span data-stu-id="928be-146">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="928be-147">**propput**</span><span class="sxs-lookup"><span data-stu-id="928be-147">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="928be-148">**propputref**</span><span class="sxs-lookup"><span data-stu-id="928be-148">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="928be-149">**Строка**</span><span class="sxs-lookup"><span data-stu-id="928be-149">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="928be-150">**типефлагс**</span><span class="sxs-lookup"><span data-stu-id="928be-150">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="928be-151">**UUID**</span><span class="sxs-lookup"><span data-stu-id="928be-151">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="928be-152">**vararg**</span><span class="sxs-lookup"><span data-stu-id="928be-152">**vararg**</span></span>](vararg.md)
</dt> <dt>

[<span data-ttu-id="928be-153">**Версия**</span><span class="sxs-lookup"><span data-stu-id="928be-153">**version**</span></span>](version.md)
</dt> </dl>

 

 