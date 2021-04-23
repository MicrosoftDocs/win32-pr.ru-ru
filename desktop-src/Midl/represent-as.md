---
title: атрибут represent_as
description: Атрибут \ представление \_ as \ ACF связывает именованный локальный тип в целевом языке репр-Type с типом передачи с именем-Type, который передается между клиентом и сервером.
ms.assetid: ae44d220-e8f3-47a3-8f5e-a2668ac75411
keywords:
- represent_as атрибута MIDL
topic_type:
- apiref
api_name:
- represent_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17d0b8915e75bb3065b394ef76900bd8efb5e0c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068734"
---
# <a name="represent_as-attribute"></a><span data-ttu-id="d134d-104">представить \_ как атрибут</span><span class="sxs-lookup"><span data-stu-id="d134d-104">represent\_as attribute</span></span>

<span data-ttu-id="d134d-105">Атрибут **\[ представления \_ As \]** ACF связывает именованный локальный тип на целевом языке *репр-Type* с типом передачи с *именем-Type* , который передается между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="d134d-105">The **\[represent\_as\]** ACF attribute associates a named local type in the target language *repr-type* with a transfer type *named-type* that is transferred between client and server.</span></span>

``` syntax
typedef [represent_as(repr-type) [[ , type-attribute-list ]] ] named-type; 
void __RPC_USER named-type_from_local (
  repr-type __RPC_FAR * ,
  named-type __RPC_FAR * __RPC_FAR * );
void __RPC_USER named-type_to_local (
  named-type __RPC_FAR * ,
  repr-type __RPC_FAR * ); void __RPC_USER named-type _free_inst ( named-type __RPC_FAR * ); void __RPC_USER named-type _free_local ( repr-type __RPC_FAR * );
```

## <a name="parameters"></a><span data-ttu-id="d134d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d134d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d134d-107">*именованный тип*</span><span class="sxs-lookup"><span data-stu-id="d134d-107">*named-type*</span></span> 
</dt> <dd>

<span data-ttu-id="d134d-108">Указывает именованный тип данных передачи, который передается между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="d134d-108">Specifies the named transfer data type that is transferred between client and server.</span></span>

</dd> <dt>

<span data-ttu-id="d134d-109">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="d134d-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d134d-110">Указывает один или несколько атрибутов, применяемых к типу.</span><span class="sxs-lookup"><span data-stu-id="d134d-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="d134d-111">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="d134d-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="d134d-112">*репр — тип*</span><span class="sxs-lookup"><span data-stu-id="d134d-112">*repr-type*</span></span> 
</dt> <dd>

<span data-ttu-id="d134d-113">Указывает представленный локальный тип на целевом языке, который предоставляется клиентским и серверным приложениям.</span><span class="sxs-lookup"><span data-stu-id="d134d-113">Specifies the represented local type in the target language that is presented to the client and server applications.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d134d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d134d-114">Remarks</span></span>

<span data-ttu-id="d134d-115">При использовании **\[ представления "представить \_ как \]**" необходимо предоставить подпрограммы, которые выполняют преобразование между локальным типом и типами передачи и свободным объемом памяти, используемым для хранения преобразованных данных.</span><span class="sxs-lookup"><span data-stu-id="d134d-115">When using **\[represent\_as\]**, you must supply routines that convert between the local and the transfer types and that free memory used to hold the converted data.</span></span> <span data-ttu-id="d134d-116">Атрибут **\[ представить \_ как \]** указывает заглушкам вызывать предоставляемые пользователем подпрограммы преобразования.</span><span class="sxs-lookup"><span data-stu-id="d134d-116">The **\[represent\_as\]** attribute instructs the stubs to call the user-supplied conversion routines.</span></span>

<span data-ttu-id="d134d-117">Переданный тип *с именем-Type* должен разрешаться в базовый тип MIDL, предопределенный тип или в идентификатор типа.</span><span class="sxs-lookup"><span data-stu-id="d134d-117">The transferred type *named-type* must resolve to a MIDL base type, predefined type, or to a type identifier.</span></span> <span data-ttu-id="d134d-118">Дополнительные сведения см. в разделе [базовые типы MIDL](midl-base-types.md).</span><span class="sxs-lookup"><span data-stu-id="d134d-118">For more information, see [MIDL Base Types](midl-base-types.md).</span></span>

<span data-ttu-id="d134d-119">Необходимо указать следующие подпрограммы:</span><span class="sxs-lookup"><span data-stu-id="d134d-119">You must supply the following routines:</span></span>



| <span data-ttu-id="d134d-120">Имя подпрограммы</span><span class="sxs-lookup"><span data-stu-id="d134d-120">Routine name</span></span>                   | <span data-ttu-id="d134d-121">Описание</span><span class="sxs-lookup"><span data-stu-id="d134d-121">Description</span></span>                                                                                                                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d134d-122">*именованный \_ тип \* \* \* \_ из \_ локальной*\*</span><span class="sxs-lookup"><span data-stu-id="d134d-122">*named\_type\*\*\*\_from\_local*\*</span></span> | <span data-ttu-id="d134d-123">Преобразует данные локального типа в тип сети.</span><span class="sxs-lookup"><span data-stu-id="d134d-123">Converts data from the local type to the network type.</span></span> <span data-ttu-id="d134d-124">Подпрограммы выделяют память для типа данных сети, включая память для любых данных, на которые ссылаются указатели в сетевом типе данных.</span><span class="sxs-lookup"><span data-stu-id="d134d-124">The routine allocates memory for the network data type, including memory for any data referenced by pointers in the network data type.</span></span>              |
| <span data-ttu-id="d134d-125">*именованный \_ тип \* \* \* \_ в \_ локальную*\*</span><span class="sxs-lookup"><span data-stu-id="d134d-125">*named\_type\*\*\*\_to\_local*\*</span></span>   | <span data-ttu-id="d134d-126">Преобразует данные из типа сети в локальный тип.</span><span class="sxs-lookup"><span data-stu-id="d134d-126">Converts data from the network type to the local type.</span></span> <span data-ttu-id="d134d-127">Подпрограммы отвечают за выделение памяти для данных, на которые ссылаются указатели в локальном типе.</span><span class="sxs-lookup"><span data-stu-id="d134d-127">The routine is responsible for allocating memory for data referenced by pointers in the local type.</span></span> <span data-ttu-id="d134d-128">RPC выделяет память для локального типа.</span><span class="sxs-lookup"><span data-stu-id="d134d-128">RPC allocates memory for the local type itself.</span></span> |
| <span data-ttu-id="d134d-129">*именованный \_ тип \* \* \* \_ бесплатный \_ локальный*\*</span><span class="sxs-lookup"><span data-stu-id="d134d-129">*named\_type\*\*\*\_free\_local*\*</span></span> | <span data-ttu-id="d134d-130">Освобождает память, выделенную для данных, на которые ссылаются указатели в локальном типе.</span><span class="sxs-lookup"><span data-stu-id="d134d-130">Frees memory allocated for data referenced by pointers in the local type.</span></span> <span data-ttu-id="d134d-131">RPC освобождает память для самого типа</span><span class="sxs-lookup"><span data-stu-id="d134d-131">RPC frees memory for the type itself</span></span>                                                                                             |
| <span data-ttu-id="d134d-132">*именованный \_ тип \* \* \* \_ бесплатный \_ inst*\*</span><span class="sxs-lookup"><span data-stu-id="d134d-132">*named\_type\*\*\*\_free\_inst*\*</span></span>  | <span data-ttu-id="d134d-133">Освобождает память, выделенную для данных, на которые ссылаются указатели в типе сети и для самого типа сети.</span><span class="sxs-lookup"><span data-stu-id="d134d-133">Frees memory allocated for the data referenced by pointers in the network type and for the network type itself.</span></span>                                                                                            |



 

<span data-ttu-id="d134d-134">Заглушка клиента вызывает *именованный тип \* \* \* \_ из \_ локальной*\* для выделения пространства для передаваемого типа и преобразования данных из локального типа в тип сети.</span><span class="sxs-lookup"><span data-stu-id="d134d-134">The client stub calls *named-type\*\*\*\_from\_local*\* to allocate space for the transmitted type and to translate the data from the local type to the network type.</span></span> <span data-ttu-id="d134d-135">Заглушка сервера выделяет место для исходного типа данных и вызывает *именованный тип \* \* \* \_ в \_ локальную*\* для преобразования данных из типа сети в локальный тип.</span><span class="sxs-lookup"><span data-stu-id="d134d-135">The server stub allocates space for the original data type and calls *named-type\*\*\*\_to\_local*\* to translate the data from the network type to the local type.</span></span>

<span data-ttu-id="d134d-136">При возврате из кода приложения заглушки клиента и сервера вызывают *именованный тип \* \* \* \_ Free \_ inst*\* для освобождения хранилища для типа сети.</span><span class="sxs-lookup"><span data-stu-id="d134d-136">Upon return from the application code, the client and server stubs call *named-type\*\*\*\_free\_inst*\* to deallocate the storage for network type.</span></span> <span data-ttu-id="d134d-137">Заглушка клиента вызывает *именованный тип \* \* \* \_ бесплатный \_ локальный*\* для освобождения хранилища, возвращенного подпрограммой.</span><span class="sxs-lookup"><span data-stu-id="d134d-137">The client stub calls *named-type\*\*\*\_free\_local*\* to deallocate storage returned by the routine.</span></span>

<span data-ttu-id="d134d-138">Следующие типы не могут иметь атрибут **\[ представления \_ As \]** :</span><span class="sxs-lookup"><span data-stu-id="d134d-138">The following types cannot have a **\[represent\_as\]** attribute:</span></span>

-   <span data-ttu-id="d134d-139">Согласованные, различные или согласованные, независящие от изменения массивы</span><span class="sxs-lookup"><span data-stu-id="d134d-139">Conformant, varying, or conformant-varying arrays</span></span>
-   <span data-ttu-id="d134d-140">Структуры, в которых последний элемент является согласованным массивом (согласованная структура)</span><span class="sxs-lookup"><span data-stu-id="d134d-140">Structures in which the last member is a conformant array (a conformant structure)</span></span>
-   <span data-ttu-id="d134d-141">Указатели или типы, содержащие указатель</span><span class="sxs-lookup"><span data-stu-id="d134d-141">Pointers or types that contain a pointer</span></span>
-   <span data-ttu-id="d134d-142">Каналы или типы, содержащие каналы</span><span class="sxs-lookup"><span data-stu-id="d134d-142">Pipes or types that contain pipes</span></span>
-   <span data-ttu-id="d134d-143">Типы, используемые в качестве базового типа для канала</span><span class="sxs-lookup"><span data-stu-id="d134d-143">Types that are used as the base type for a pipe</span></span>
-   <span data-ttu-id="d134d-144">Стандартные типы. [**обрабатывает \_ t**](handle-t.md), [**void**](void.md)</span><span class="sxs-lookup"><span data-stu-id="d134d-144">Predefined types [**handle\_t**](handle-t.md), [**void**](void.md)</span></span>
-   <span data-ttu-id="d134d-145">Типы, имеющие атрибут [**\[ Handle \]**](handle.md)</span><span class="sxs-lookup"><span data-stu-id="d134d-145">Types that have the [**\[handle\]**](handle.md) attribute</span></span>

## <a name="examples"></a><span data-ttu-id="d134d-146">Примеры</span><span class="sxs-lookup"><span data-stu-id="d134d-146">Examples</span></span>

``` syntax
//these data types defined in .IDL or elsewhere
typedef struct  _lbox 
{ 
    long         data; 
    struct _lbox *next; 
} lbox; 
typedef [ref] lbox *PBOX_LOC; 
typedef long LONG4[4]; 
 
//in .ACF file :
interface iface
{
    typedef  [ represent_as(PBOX_LOC) ]  LONG4; 
}
```

## <a name="see-also"></a><span data-ttu-id="d134d-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d134d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d134d-148">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="d134d-148">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="d134d-149">**массивы**</span><span class="sxs-lookup"><span data-stu-id="d134d-149">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="d134d-150">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="d134d-150">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="d134d-151">**Handle \_ t**</span><span class="sxs-lookup"><span data-stu-id="d134d-151">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="d134d-152">**определение**</span><span class="sxs-lookup"><span data-stu-id="d134d-152">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="d134d-153">**void**</span><span class="sxs-lookup"><span data-stu-id="d134d-153">**void**</span></span>](void.md)
</dt> </dl>

 

 




