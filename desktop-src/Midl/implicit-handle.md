---
title: атрибут implicit_handle
description: Атрибут \ неявный \_ Handle \ ACF задает маркер, используемый для функций, которые не включают явный маркер в качестве параметра процедуры.
ms.assetid: 09c17473-87b5-4fd6-beb9-3d9b7bc82d8c
keywords:
- implicit_handle атрибута MIDL
topic_type:
- apiref
api_name:
- implicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22f410fa048a27e1f7626690e6308de4c1a31c2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889464"
---
# <a name="implicit_handle-attribute"></a><span data-ttu-id="e17bc-104">неявный \_ атрибут Handle</span><span class="sxs-lookup"><span data-stu-id="e17bc-104">implicit\_handle attribute</span></span>

<span data-ttu-id="e17bc-105">Атрибут **\[ неявный \_ Handle \]** ACF задает маркер, используемый для функций, которые не включают явный маркер в качестве параметра процедуры.</span><span class="sxs-lookup"><span data-stu-id="e17bc-105">The **\[implicit\_handle\]** ACF attribute specifies the handle used for functions that do not include an explicit handle as a procedure parameter.</span></span>

``` syntax
implicit_handle(handle-type handle-name)
```

## <a name="parameters"></a><span data-ttu-id="e17bc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e17bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e17bc-107">*Handle-Type*</span><span class="sxs-lookup"><span data-stu-id="e17bc-107">*handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="e17bc-108">Задает тип данных Handle, например, базовый [**тип или определяемый \_ пользователем тип Handle.**](handle-t.md)</span><span class="sxs-lookup"><span data-stu-id="e17bc-108">Specifies the handle data type, such as the base type [**handle\_t**](handle-t.md) or a user-defined handle type.</span></span>

</dd> <dt>

<span data-ttu-id="e17bc-109">*имя обработчика*</span><span class="sxs-lookup"><span data-stu-id="e17bc-109">*handle-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e17bc-110">Задает имя маркера.</span><span class="sxs-lookup"><span data-stu-id="e17bc-110">Specifies the name of the handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e17bc-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e17bc-111">Remarks</span></span>

<span data-ttu-id="e17bc-112">Маркер, заданный **\[ неявным \_ \]** атрибутом Handle, используется различными способами в зависимости от характера процедуры.</span><span class="sxs-lookup"><span data-stu-id="e17bc-112">The handle specified by the **\[implicit\_handle\]** attribute is used in different ways depending on the nature of the procedure.</span></span> <span data-ttu-id="e17bc-113">Если процедура является удаленной, то маркер будет использоваться в качестве маркера привязки для удаленного вызова.</span><span class="sxs-lookup"><span data-stu-id="e17bc-113">If the procedure is remote, the handle will be used as the binding handle for the remote call.</span></span> <span data-ttu-id="e17bc-114">Неявный обработчик также может использоваться для установления начальной привязки для функции, использующей маркер контекста.</span><span class="sxs-lookup"><span data-stu-id="e17bc-114">The implicit handle may also be used to establish an initial binding for a function that uses a context handle.</span></span> <span data-ttu-id="e17bc-115">Если процедура является процедурой сериализации, то этот маркер используется в качестве маркера сериализации, управляющего операцией.</span><span class="sxs-lookup"><span data-stu-id="e17bc-115">If the procedure is a serializing procedure, the handle is used as a serializing handle controlling the operation.</span></span> <span data-ttu-id="e17bc-116">В случае сериализации типа этот маркер используется в качестве маркера сериализации для всех сериализованных типов.</span><span class="sxs-lookup"><span data-stu-id="e17bc-116">In the case of type serialization, the handle is used as the serialization handle for all the serialized types.</span></span>

<span data-ttu-id="e17bc-117">Атрибут **\[ неявного \_ дескриптора \]** задает глобальную переменную, которая содержит дескриптор, используемый любой функцией, требующей неявные дескрипторы.</span><span class="sxs-lookup"><span data-stu-id="e17bc-117">The **\[implicit\_handle\]** attribute specifies a global variable that contains a handle used by any function needing implicit handles.</span></span>

<span data-ttu-id="e17bc-118">Неявный тип маркера привязки должен быть либо [**обработчиком \_ t**](handle-t.md) (или типом, основанным на **Handle \_ t**), либо определяемым пользователем типом Handle, указанным с помощью атрибута [**Handle**](handle.md) .</span><span class="sxs-lookup"><span data-stu-id="e17bc-118">The implicit binding handle type must be either [**handle\_t**](handle-t.md) (or a type based on **handle\_t**) or a user-defined handle type specified with the [**handle**](handle.md) attribute.</span></span> <span data-ttu-id="e17bc-119">Неявный обработчик сериализации должен быть типом, основанным на **Handle \_ t**.</span><span class="sxs-lookup"><span data-stu-id="e17bc-119">The implicit serializing handle must be a type based on **handle\_t**.</span></span>

<span data-ttu-id="e17bc-120">Если неявный тип обработчика не определен в IDL-файле или в файлах, включенных и импортированных IDL-файлом для компьютера MIDL, необходимо предоставить файл, содержащий определение типа Handle, при компиляции заглушек.</span><span class="sxs-lookup"><span data-stu-id="e17bc-120">If the implicit handle type is not defined in the IDL file or in any files included and imported by the IDL file for the MIDL computer, you must supply the file containing the handle-type definition when you compile the stubs.</span></span> <span data-ttu-id="e17bc-121">Используйте инструкцию [**include**](include.md) ACF, чтобы включить файл, содержащий определение типа Handle.</span><span class="sxs-lookup"><span data-stu-id="e17bc-121">Use the ACF [**include**](include.md) statement to include the file containing the handle-type definition.</span></span>

<span data-ttu-id="e17bc-122">**\[ Неявный атрибут \_ Handle \]** может встречаться не чаще одного раза.</span><span class="sxs-lookup"><span data-stu-id="e17bc-122">The **\[implicit\_handle\]** attribute can occur once, at most.</span></span> <span data-ttu-id="e17bc-123">**\[ Неявный атрибут \_ Handle \]** может происходить только в том случае, если атрибуты [**\[ Auto \_ Handle \]**](auto-handle.md) и [**\[ explicit \_ Handle \]**](explicit-handle.md) не выполняются.</span><span class="sxs-lookup"><span data-stu-id="e17bc-123">The **\[implicit\_handle\]** attribute can occur only if the [**\[auto\_handle\]**](auto-handle.md) and [**\[explicit\_handle\]**](explicit-handle.md) attributes do not occur.</span></span>

## <a name="examples"></a><span data-ttu-id="e17bc-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="e17bc-124">Examples</span></span>

``` syntax
/* ACF file */ 
[
    implicit_handle(handle_t hMyHandle)
] 
interface iface
{ 
    // Attribute configuration statements
}
```

## <a name="see-also"></a><span data-ttu-id="e17bc-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e17bc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e17bc-126">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="e17bc-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="e17bc-127">**Автоматическая \_ работа**</span><span class="sxs-lookup"><span data-stu-id="e17bc-127">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="e17bc-128">**явный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="e17bc-128">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="e17bc-129">**Handle \_ t**</span><span class="sxs-lookup"><span data-stu-id="e17bc-129">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="e17bc-130">**относится**</span><span class="sxs-lookup"><span data-stu-id="e17bc-130">**include**</span></span>](include.md)
</dt> </dl>

 

 




