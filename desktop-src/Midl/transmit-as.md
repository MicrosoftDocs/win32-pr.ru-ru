---
title: transmit_as - атрибут
description: Атрибут \ "передать \_ как \" указывает компилятору связать тип-ID, который представляет собой представляемый тип, управляемый клиентскими и серверными приложениями, с переданным типом xmit-Type.
ms.assetid: 3dd1a242-03ec-49b4-ac96-87ef186e41d2
keywords:
- transmit_as атрибута MIDL
topic_type:
- apiref
api_name:
- transmit_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ec0cba27e994f7d77d441aef7bb783cad71cbad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105661688"
---
# <a name="transmit_as-attribute"></a><span data-ttu-id="caf26-104">передать \_ как атрибут</span><span class="sxs-lookup"><span data-stu-id="caf26-104">transmit\_as attribute</span></span>

<span data-ttu-id="caf26-105">Атрибут **\[ передать \_ как \]** указывает компилятору связать \* \* \**,* который представляет собой тип, который управляется клиентскими и серверными приложениями, с переданным типом **xmit-Type.**</span><span class="sxs-lookup"><span data-stu-id="caf26-105">The **\[transmit\_as\]** attribute instructs the compiler to associate \**type-id\*\*\*,* which is a presented type that client and server applications manipulate, with a transmitted type **xmit-type.**</span></span>

``` syntax
typedef [transmit_as(xmit-type) [[ , type-attribute-list ]] ] type-specifier declarator-list; 

void __RPC_USER type-id_to_xmit (
  type-id __RPC_FAR *,
  xmit-type __RPC_FAR * __RPC_FAR *);
void __RPC_USER type-id_from_xmit (
  xmit-type __RPC_FAR *,
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_inst (
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_xmit (
  xmit-type__RPC_FAR *);
```

## <a name="parameters"></a><span data-ttu-id="caf26-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="caf26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caf26-107">*xmit — тип*</span><span class="sxs-lookup"><span data-stu-id="caf26-107">*xmit-type*</span></span> 
</dt> <dd>

<span data-ttu-id="caf26-108">Указывает тип данных, передаваемый между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="caf26-108">Specifies the data type that is transmitted between client and server.</span></span>

</dd> <dt>

<span data-ttu-id="caf26-109">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="caf26-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="caf26-110">Указывает один или несколько атрибутов, применяемых к типу.</span><span class="sxs-lookup"><span data-stu-id="caf26-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="caf26-111">К допустимым атрибутам типа относятся **\[** [**Handle**](handle.md), **\]** **\[** [**Switch \_ Type**](switch-type.md) **\]** ; указатель на **\[** [**ref**](ref.md) **\]** , **\[** [**UNIQUE**](unique.md) **\]** , **\[** [**ptr**](ptr.md), **\]** и атрибуты использования, а также параметр **\[** [](string.md) **\]** **\[** [**Ignore**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="caf26-111">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]** and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="caf26-112">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="caf26-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="caf26-113">*Описатель типа*</span><span class="sxs-lookup"><span data-stu-id="caf26-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="caf26-114">Задает [базовый тип](midl-base-types.md), [**структуру**](struct.md), [**объединение**](union.md), тип [**перечисления**](enum.md) или идентификатор типа.</span><span class="sxs-lookup"><span data-stu-id="caf26-114">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="caf26-115">Дополнительная спецификация хранилища может предшествовать *спецификатору типа*.</span><span class="sxs-lookup"><span data-stu-id="caf26-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="caf26-116">*декларатор-список*</span><span class="sxs-lookup"><span data-stu-id="caf26-116">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="caf26-117">Задает стандартные деклараторы C, такие как идентификаторы, деклараторы указателей и деклараторы массивов.</span><span class="sxs-lookup"><span data-stu-id="caf26-117">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="caf26-118">Дополнительные сведения см. в разделе [атрибуты Array и Sized-Pointer](array-and-sized-pointer-attributes.md), [**массивы**](arrays-1.md), [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="caf26-118">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="caf26-119">*Список деклараторов* состоит из одного или нескольких деклараторов, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="caf26-119">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="caf26-120">Декларатор параметра в деклараторе функции, например имя параметра, является необязательным.</span><span class="sxs-lookup"><span data-stu-id="caf26-120">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> <dt>

<span data-ttu-id="caf26-121">*Идентификатор типа*</span><span class="sxs-lookup"><span data-stu-id="caf26-121">*type-id*</span></span> 
</dt> <dd>

<span data-ttu-id="caf26-122">Указывает имя типа данных, представленного для клиентских и серверных приложений.</span><span class="sxs-lookup"><span data-stu-id="caf26-122">Specifies the name of the data type that is presented to the client and server applications.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="caf26-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="caf26-123">Remarks</span></span>

<span data-ttu-id="caf26-124">Чтобы использовать атрибут **\[ передачи \_ As \]** , пользователь должен предоставить подпрограммы, которые преобразуют данные между представленными и передаваемыми типами. Эти подпрограммы также должны освободить память, используемую для хранения преобразованных данных.</span><span class="sxs-lookup"><span data-stu-id="caf26-124">To use the **\[transmit\_as\]** attribute, the user must supply routines that convert data between the presented and the transmitted types; these routines must also free memory used to hold the converted data.</span></span> <span data-ttu-id="caf26-125">Атрибут **\[ передать \_ как \]** указывает заглушкам вызывать предоставляемые пользователем подпрограммы преобразования.</span><span class="sxs-lookup"><span data-stu-id="caf26-125">The **\[transmit\_as\]** attribute instructs the stubs to call the user-supplied conversion routines.</span></span>

<span data-ttu-id="caf26-126">Передаваемый тип *xmit-Type* должен разрешаться в базовый тип MIDL, предопределенный тип или идентификатор типа.</span><span class="sxs-lookup"><span data-stu-id="caf26-126">The transmitted type *xmit-type* must resolve to a MIDL base type, predefined type, or a type identifier.</span></span> <span data-ttu-id="caf26-127">Дополнительные сведения см. в разделе [базовые типы MIDL](midl-base-types.md).</span><span class="sxs-lookup"><span data-stu-id="caf26-127">For more information, see [MIDL Base Types](midl-base-types.md).</span></span>

<span data-ttu-id="caf26-128">Пользователь должен предоставить следующие подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="caf26-128">The user must supply the following routines.</span></span>



| <span data-ttu-id="caf26-129">Имя подпрограммы</span><span class="sxs-lookup"><span data-stu-id="caf26-129">Routine name</span></span>              | <span data-ttu-id="caf26-130">Описание</span><span class="sxs-lookup"><span data-stu-id="caf26-130">Description</span></span>                                                                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caf26-131">*Type-ID \* \* \* \_ to \_ xmit*\*</span><span class="sxs-lookup"><span data-stu-id="caf26-131">*type-id\*\*\*\_to\_xmit*\*</span></span>   | <span data-ttu-id="caf26-132">Преобразует данные из представленного типа в передаваемый тип.</span><span class="sxs-lookup"><span data-stu-id="caf26-132">Converts data from the presented type to the transmitted type.</span></span> <span data-ttu-id="caf26-133">Эта подпрограммы выделяет память для переданного типа и для любых данных, на которые ссылаются указатели в переданном типе.</span><span class="sxs-lookup"><span data-stu-id="caf26-133">This routine allocates memory for the transmitted type and for any data referenced by pointers in the transmitted type.</span></span>                            |
| <span data-ttu-id="caf26-134">*Type-ID \* \* \* \_ из \_ xmit*\*</span><span class="sxs-lookup"><span data-stu-id="caf26-134">*type-id\*\*\*\_from\_xmit*\*</span></span> | <span data-ttu-id="caf26-135">Преобразует данные переданного типа в представленный тип.</span><span class="sxs-lookup"><span data-stu-id="caf26-135">Converts data from the transmitted type to the presented type.</span></span> <span data-ttu-id="caf26-136">Эта подпрограммы отвечает за выделение памяти для данных, на которые ссылаются указатели в представленном типе.</span><span class="sxs-lookup"><span data-stu-id="caf26-136">This routine is responsible for allocating memory for data referenced by pointers in the presented type.</span></span> <span data-ttu-id="caf26-137">RPC выделяет память для самого типа.</span><span class="sxs-lookup"><span data-stu-id="caf26-137">RPC allocates memory for the type itself.</span></span> |
| <span data-ttu-id="caf26-138">*Type-ID \* \* \* \_ бесплатная \_ inst*\*</span><span class="sxs-lookup"><span data-stu-id="caf26-138">*type-id\*\*\*\_free\_inst*\*</span></span> | <span data-ttu-id="caf26-139">Освобождает память, выделенную для данных, на которые ссылаются указатели в представленном типе.</span><span class="sxs-lookup"><span data-stu-id="caf26-139">Frees memory allocated for data referenced by pointers in the presented type.</span></span> <span data-ttu-id="caf26-140">RPC освобождает память для самого типа.</span><span class="sxs-lookup"><span data-stu-id="caf26-140">RPC frees memory for the type itself.</span></span>                                                                                               |
| <span data-ttu-id="caf26-141">*Type-ID \* \* \* \_ бесплатная \_ xmit*\*</span><span class="sxs-lookup"><span data-stu-id="caf26-141">*type-id\*\*\*\_free\_xmit*\*</span></span> | <span data-ttu-id="caf26-142">Освобождает хранилище, используемое вызывающим объектом для переданного типа, и для данных, на которые ссылаются указатели в переданном типе.</span><span class="sxs-lookup"><span data-stu-id="caf26-142">Frees storage used by the caller for the transmitted type and for data referenced by pointers in the transmitted type.</span></span>                                                                                            |



 

 

<span data-ttu-id="caf26-143">Заглушка клиента вызывает *Type-ID \* \* \* \_ to \_ xmit*\* для выделения пространства для передаваемого типа и преобразования данных в объекты типа *xmit-Type.*</span><span class="sxs-lookup"><span data-stu-id="caf26-143">The client stub calls *type-id\*\*\*\_to\_xmit*\* to allocate space for the transmitted type and to translate the data into objects of type *xmit-type.*</span></span> <span data-ttu-id="caf26-144">Заглушка сервера выделяет место для исходного типа данных и вызывает метод *Type-ID \* \* \* \_ из \_ xmit*\* для преобразования данных из переданного типа в представленный тип.</span><span class="sxs-lookup"><span data-stu-id="caf26-144">The server stub allocates space for the original data type and calls *type-id\*\*\*\_from\_xmit*\* to translate the data from its transmitted type to the presented type.</span></span>

<span data-ttu-id="caf26-145">При возврате из кода приложения заглушка сервера вызывает \*Type-ID \* \* \* \_ Free \_ inst\*\*, чтобы освободить хранилище для *типа-ID* на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="caf26-145">Upon return from the application code, the server stub calls *type-id\*\*\*\_free\_inst*\* to deallocate the storage for *type-id* on the server side.</span></span> <span data-ttu-id="caf26-146">Заглушка клиента вызывает *Type-ID \* \* \* \_ Free \_ xmit*\* для освобождения хранилища *типа xmit* на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="caf26-146">The client stub calls *type-id\*\*\*\_free\_xmit*\* to deallocate the *xmit-type* storage on the client side.</span></span>

<span data-ttu-id="caf26-147">Следующие типы не могут иметь атрибут " **\[ передать \_ как \]** ":</span><span class="sxs-lookup"><span data-stu-id="caf26-147">The following types cannot have a **\[transmit\_as\]** attribute:</span></span>

-   <span data-ttu-id="caf26-148">Дескрипторы контекста (типы с **\[** атрибутом типа [**\_ дескриптора контекста**](context-handle.md) **\]** и типами, которые используются в качестве параметров атрибута **\[ \_ дескриптора \] контекста** )</span><span class="sxs-lookup"><span data-stu-id="caf26-148">Context handles (types with the **\[**[**context\_handle**](context-handle.md)**\]** type attribute and types that are used as parameters with the **\[context\_handle\]** attribute)</span></span>
-   <span data-ttu-id="caf26-149">Типы, являющиеся каналами или производными от каналов</span><span class="sxs-lookup"><span data-stu-id="caf26-149">Types that are pipes or derived from pipes</span></span>
-   <span data-ttu-id="caf26-150">Типы данных, используемые в качестве базового типа определения канала</span><span class="sxs-lookup"><span data-stu-id="caf26-150">Data types that are used as the base type of a pipe definition</span></span>
-   <span data-ttu-id="caf26-151">Параметры, которые являются указателями или разрешаются в указатели</span><span class="sxs-lookup"><span data-stu-id="caf26-151">Parameters that are pointers or resolve to pointers</span></span>
-   <span data-ttu-id="caf26-152">Параметры, которые являются согласованными, различными или открытыми массивами</span><span class="sxs-lookup"><span data-stu-id="caf26-152">Parameters that are conformant, varying, or open arrays</span></span>
-   <span data-ttu-id="caf26-153">Структуры, содержащие согласованные массивы</span><span class="sxs-lookup"><span data-stu-id="caf26-153">Structures that contain conformant arrays</span></span>
-   <span data-ttu-id="caf26-154">Предопределенный тип [**маркера \_ t**](handle-t.md), [**void**](void.md)</span><span class="sxs-lookup"><span data-stu-id="caf26-154">The predefined type [**handle\_t**](handle-t.md), [**void**](void.md)</span></span>

<span data-ttu-id="caf26-155">Передаваемые типы должны соответствовать следующим ограничениям:</span><span class="sxs-lookup"><span data-stu-id="caf26-155">Types that are transmitted must conform to the following restrictions:</span></span>

-   <span data-ttu-id="caf26-156">Они не должны быть указателями или содержать указатели.</span><span class="sxs-lookup"><span data-stu-id="caf26-156">They must not be pointers or contain pointers.</span></span>
-   <span data-ttu-id="caf26-157">Они не должны быть каналами или содержать каналы.</span><span class="sxs-lookup"><span data-stu-id="caf26-157">They must not be pipes or contain pipes.</span></span>

## <a name="examples"></a><span data-ttu-id="caf26-158">Примеры</span><span class="sxs-lookup"><span data-stu-id="caf26-158">Examples</span></span>

``` syntax
typedef struct _TREE_NODE_TYPE 
{ 
    unsigned short data; 
    struct _TREE_NODE_TYPE * left; 
    struct _TREE_NODE_TYPE * right; 
} TREE_NODE_TYPE; 
 
typedef [transmit_as(TREE_XMIT_TYPE)] TREE_NODE_TYPE * TREE_TYPE; 
 
void __RPC_USER TREE_TYPE_to_xmit( 
    TREE_TYPE __RPC_FAR * , 
    TREE_XMIT_TYPE __RPC_FAR * __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_from_xmit ( 
    TREE_XMIT_TYPE __RPC_FAR *, 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_inst( 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_xmit( 
    TREE_XMIT_TYPE __RPC_FAR *);
```

## <a name="see-also"></a><span data-ttu-id="caf26-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="caf26-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caf26-160">**массивы**</span><span class="sxs-lookup"><span data-stu-id="caf26-160">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="caf26-161">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="caf26-161">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="caf26-162">**Контекстный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="caf26-162">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="caf26-163">**перечисления**</span><span class="sxs-lookup"><span data-stu-id="caf26-163">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="caf26-164">**справиться**</span><span class="sxs-lookup"><span data-stu-id="caf26-164">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="caf26-165">**Handle \_ t**</span><span class="sxs-lookup"><span data-stu-id="caf26-165">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="caf26-166">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="caf26-166">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="caf26-167">**обращать**</span><span class="sxs-lookup"><span data-stu-id="caf26-167">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="caf26-168">**ptr**</span><span class="sxs-lookup"><span data-stu-id="caf26-168">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="caf26-169">**ref**</span><span class="sxs-lookup"><span data-stu-id="caf26-169">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="caf26-170">**Строка**</span><span class="sxs-lookup"><span data-stu-id="caf26-170">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="caf26-171">**struct**</span><span class="sxs-lookup"><span data-stu-id="caf26-171">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="caf26-172">**Тип коммутатора \_**</span><span class="sxs-lookup"><span data-stu-id="caf26-172">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="caf26-173">**определение**</span><span class="sxs-lookup"><span data-stu-id="caf26-173">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="caf26-174">**наборов**</span><span class="sxs-lookup"><span data-stu-id="caf26-174">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="caf26-175">**однозначно**</span><span class="sxs-lookup"><span data-stu-id="caf26-175">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="caf26-176">**void**</span><span class="sxs-lookup"><span data-stu-id="caf26-176">**void**</span></span>](void.md)
</dt> </dl>

 

 