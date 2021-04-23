---
title: interface - атрибут
description: Ключевое слово interface указывает имя интерфейса. Имя интерфейса должно быть указано как в IDL-файле, так и в ACF.
ms.assetid: 239b782e-57de-493c-b2f4-310d1859a9ae
keywords:
- атрибут интерфейса MIDL
topic_type:
- apiref
api_name:
- interface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852c29b2ba7b43e9d8b15863e60db8ad2fbde33f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890508"
---
# <a name="interface-attribute"></a><span data-ttu-id="2cefc-105">interface - атрибут</span><span class="sxs-lookup"><span data-stu-id="2cefc-105">interface attribute</span></span>

<span data-ttu-id="2cefc-106">Ключевое слово **Interface** указывает имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2cefc-106">The **interface** keyword specifies the name of the interface.</span></span> <span data-ttu-id="2cefc-107">Имя интерфейса должно быть указано как в IDL-файле, так и в ACF.</span><span class="sxs-lookup"><span data-stu-id="2cefc-107">The interface name must be provided in both the IDL file and the ACF.</span></span>

``` syntax
[ 
    interface-attribute-list 
] 
interface interface-name [ : base-interface ]
{
}

typedef interface interface-name declarator-list
```

## <a name="parameters"></a><span data-ttu-id="2cefc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cefc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cefc-109">*Interface-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="2cefc-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2cefc-110">Задает атрибуты, применяемые к интерфейсу в целом.</span><span class="sxs-lookup"><span data-stu-id="2cefc-110">Specifies attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="2cefc-111">Допустимыми атрибутами интерфейса для IDL-файла являются **\[** [**Конечная точка**](endpoint.md) **\]** , **\[** [**Локальная**](local.md) **\]** , **\[** [**объект**](object.md) **\]** , **\[** [**указатель \_ по умолчанию**](pointer-default.md) **\]** , **\[** [**UUID**](uuid.md) **\]** и **\[** [**версия**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2cefc-111">Valid interface attributes for an IDL file include **\[**[**endpoint**](endpoint.md)**\]**, **\[**[**local**](local.md)**\]**, **\[**[**object**](object.md)**\]**, **\[**[**pointer\_default**](pointer-default.md)**\]**, **\[**[**uuid**](uuid.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span> <span data-ttu-id="2cefc-112">Допустимые атрибуты интерфейса для ACF включают **\[** [**кодирование**](encode.md) **\]** , **\[** [**декодирование**](decode.md) **\]** , **\[** [**автоматическую \_ обработку**](auto-handle.md) **\]** или **\[** [**неявный \_ маркер**](implicit-handle.md) **\]** , а также **\[** [**код**](code.md) **\]** или код **\[** [](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2cefc-112">Valid interface attributes for an ACF include **\[**[**encode**](encode.md)**\]**, **\[**[**decode**](decode.md)**\]**, either **\[**[**auto\_handle**](auto-handle.md)**\]** or **\[**[**implicit\_handle**](implicit-handle.md)**\]**, and either **\[**[**code**](code.md)**\]** or **\[**[**nocode**](nocode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="2cefc-113">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="2cefc-113">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="2cefc-114">Указывает имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2cefc-114">Specifies the name of the interface.</span></span> <span data-ttu-id="2cefc-115">Имя интерфейса должно быть уникальным именем и должно начинаться с буквы или символа подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="2cefc-115">The interface name must be a unique name and must start with an alphabetic or underscore character.</span></span>

</dd> <dt>

<span data-ttu-id="2cefc-116">*базовый интерфейс*</span><span class="sxs-lookup"><span data-stu-id="2cefc-116">*base-interface*</span></span> 
</dt> <dd>

<span data-ttu-id="2cefc-117">Указывает имя интерфейса, от которого этот производный интерфейс наследует функции члена, коды состояния и атрибуты интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2cefc-117">Specifies the name of an interface from which this derived interface inherits member functions, status codes, and interface attributes.</span></span> <span data-ttu-id="2cefc-118">Производный интерфейс не наследует определения типов.</span><span class="sxs-lookup"><span data-stu-id="2cefc-118">The derived interface does not inherit type definitions.</span></span> <span data-ttu-id="2cefc-119">Для этого используйте ключевое слово [**Import**](import.md) , чтобы импортировать idl-файл базового интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2cefc-119">To do this, use the [**import**](import.md) keyword to import the IDL file of the base interface.</span></span>

</dd> <dt>

<span data-ttu-id="2cefc-120">*декларатор-список*</span><span class="sxs-lookup"><span data-stu-id="2cefc-120">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2cefc-121">Задает стандартные деклараторы C, такие как идентификаторы, деклараторы указателей и деклараторы массивов.</span><span class="sxs-lookup"><span data-stu-id="2cefc-121">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="2cefc-122">Дополнительные сведения см. в разделе [атрибуты Array и Sized-Pointer](array-and-sized-pointer-attributes.md), [**массивы**](arrays-1.md). и [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="2cefc-122">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="2cefc-123">*Список деклараторов* состоит из одного или нескольких деклараторов, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="2cefc-123">The *declarator-list* consists of one or more declarators, separated by commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2cefc-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2cefc-124">Remarks</span></span>

<span data-ttu-id="2cefc-125">Имена интерфейсов в IDL-файле и ACF должны совпадать, за исключением случаев, когда используется параметр компилятора MIDL [**/АКФ**](-acf.md).</span><span class="sxs-lookup"><span data-stu-id="2cefc-125">The interface names in the IDL file and ACF must be the same, except when you use the MIDL compiler switch [**/acf**](-acf.md).</span></span>

<span data-ttu-id="2cefc-126">Имя интерфейса образует первую часть имени структур данных интерфейсного обработчика, которые являются параметрами функций времени выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="2cefc-126">The interface name forms the first part of the name of interface-handle data structures that are parameters to the RPC run-time functions.</span></span> <span data-ttu-id="2cefc-127">Дополнительные сведения см. в разделе [**RPC \_ if \_ Handle**](/windows/desktop/Rpc/rpc-if-handle).</span><span class="sxs-lookup"><span data-stu-id="2cefc-127">For more information, see [**RPC\_IF\_HANDLE**](/windows/desktop/Rpc/rpc-if-handle).</span></span>

<span data-ttu-id="2cefc-128">Если заголовок интерфейса содержит **\[** атрибут [**объекта**](object.md) **\]** , указывающий на COM-интерфейс, он должен также включать атрибут **\[** [**UUID**](uuid.md) **\]** и указывать базовый COM-интерфейс, от которого он является производным.</span><span class="sxs-lookup"><span data-stu-id="2cefc-128">If the interface header includes the **\[**[**object**](object.md)**\]** attribute to indicate a COM interface, it must also include the **\[**[**uuid**](uuid.md)**\]** attribute and must specify the base COM interface from which it is derived.</span></span> <span data-ttu-id="2cefc-129">Дополнительные сведения о COM-интерфейсах см. в разделе **\[** [**Object**](object.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2cefc-129">For more information about COM interfaces, see **\[**[**object**](object.md)**\]**.</span></span>

<span data-ttu-id="2cefc-130">Можно также использовать ключевое слово **Interface** с ключевым словом [**typedef**](typedef.md) для определения типа данных интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2cefc-130">You can also use the **interface** keyword with the [**typedef**](typedef.md) keyword to define an interface data type.</span></span>

## <a name="examples"></a><span data-ttu-id="2cefc-131">Примеры</span><span class="sxs-lookup"><span data-stu-id="2cefc-131">Examples</span></span>

``` syntax
/* use of interface keyword in IDL file for an RPC interface */ 
[ 
    uuid (00000000-0000-0000-0000-000000000000), 
    version (1.0) 
] 
interface remote_if_2 
{  
    // Interface definition statements.
} 
 
/* use of interface keyword in ACF for an RPC interface */ 
[
    implicit_handle( handle_t xa_bhandle ) 
] 
interface remote_if_2 
{ 
    // Attribute configuration statements.
} 
 
/* use of interface keyword in IDL file for a COM interface */ 
[ 
    object, uuid (00000000-0000-0000-0000-000000000000) 
] 
interface IDerivedInterface : IBaseInterface 
{  
    import "base.idl" 
    Save(); 
} 
 
/* use of interface keyword to define an interface pointer type */ 
typedef interface IStorage *LPSTORAGE;
```

## <a name="see-also"></a><span data-ttu-id="2cefc-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2cefc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cefc-133">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="2cefc-133">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="2cefc-134">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="2cefc-134">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="2cefc-135">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="2cefc-135">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="2cefc-136">**Языковые**</span><span class="sxs-lookup"><span data-stu-id="2cefc-136">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="2cefc-137">**объектами**</span><span class="sxs-lookup"><span data-stu-id="2cefc-137">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="2cefc-138">**Указатель \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="2cefc-138">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="2cefc-139">**RPC \_ if \_ Handle**</span><span class="sxs-lookup"><span data-stu-id="2cefc-139">**RPC\_IF\_HANDLE**</span></span>](/windows/desktop/Rpc/rpc-if-handle)
</dt> <dt>

[<span data-ttu-id="2cefc-140">**определение**</span><span class="sxs-lookup"><span data-stu-id="2cefc-140">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="2cefc-141">**UUID**</span><span class="sxs-lookup"><span data-stu-id="2cefc-141">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="2cefc-142">**Версия**</span><span class="sxs-lookup"><span data-stu-id="2cefc-142">**version**</span></span>](version.md)
</dt> </dl>

 

 