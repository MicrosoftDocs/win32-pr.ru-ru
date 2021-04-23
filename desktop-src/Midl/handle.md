---
title: атрибут Handle
description: Атрибут \ Handle \ указывает определяемый пользователем или \ 0034; настроенный \ 0034; Тип обработчика.
ms.assetid: db5c6ea6-6081-4cea-9265-5e2f67fd8c14
keywords:
- обработчик с атрибутом MIDL
topic_type:
- apiref
api_name:
- handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d4560de53bf3f24238e9ff96e01c74716729749
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890640"
---
# <a name="handle-attribute"></a><span data-ttu-id="7e21e-104">атрибут Handle</span><span class="sxs-lookup"><span data-stu-id="7e21e-104">handle attribute</span></span>

<span data-ttu-id="7e21e-105">Атрибут \[ **Handle** \] указывает определяемый пользователем или настроенный тип маркера.</span><span class="sxs-lookup"><span data-stu-id="7e21e-105">The \[**handle**\] attribute specifies a user-defined or "customized" handle type.</span></span>

``` syntax
typedef [handle] typename;  
handle_t __RPC_USER typename_bind (typename);
void __RPC_USER typename_unbind (typename, handle_t);
```

## <a name="parameters"></a><span data-ttu-id="7e21e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e21e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e21e-107">*имени*</span><span class="sxs-lookup"><span data-stu-id="7e21e-107">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="7e21e-108">Задает имя определяемого пользователем типа обработчика привязки.</span><span class="sxs-lookup"><span data-stu-id="7e21e-108">Specifies the name of the user-defined binding-handle type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e21e-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e21e-109">Remarks</span></span>

<span data-ttu-id="7e21e-110">Пользовательские дескрипторы позволяют разработчикам проектировать дескрипторы, имеющие смысл для приложения.</span><span class="sxs-lookup"><span data-stu-id="7e21e-110">User-defined handles permit developers to design handles that are meaningful to the application.</span></span> <span data-ttu-id="7e21e-111">Определяемый пользователем обработчик может быть определен только в объявлении типа, а не в деклараторе функции.</span><span class="sxs-lookup"><span data-stu-id="7e21e-111">A user-defined handle can only be defined in a type declaration, not in a function declarator.</span></span>

<span data-ttu-id="7e21e-112">Параметр типа, определенного \[  \] атрибутом Handle, используется для определения привязки для вызова и передается вызываемой процедуре.</span><span class="sxs-lookup"><span data-stu-id="7e21e-112">A parameter of a type defined by the \[**handle**\] attribute is used to determine the binding for the call and is transmitted to the called procedure.</span></span>

<span data-ttu-id="7e21e-113">Пользователь должен предоставить подпрограммы привязки и отмены привязки для преобразования между примитивными и определяемыми пользователем типами маркеров.</span><span class="sxs-lookup"><span data-stu-id="7e21e-113">The user must provide binding and unbinding routines to convert between primitive and user-defined handle types.</span></span> <span data-ttu-id="7e21e-114">При наличии определяемого пользователем маркера типа *TypeName* пользователь должен предоставить подпрограммы с именем typeName  \_ **BIND** и *TypeName* \_ **Unbind**.</span><span class="sxs-lookup"><span data-stu-id="7e21e-114">Given a user-defined handle of type *typename*, the user must supply the routines *typename*\_**bind** and *typename*\_**unbind**.</span></span> <span data-ttu-id="7e21e-115">Например, если определяемый пользователем тип Handle имеет имя МИХАНДЛЕ, подпрограммы именуются МИХАНДЛЕ \_ **BIND** и михандле \_ **Unbind**.</span><span class="sxs-lookup"><span data-stu-id="7e21e-115">For example, if the user-defined handle type is named MYHANDLE, the routines are named MYHANDLE\_**bind** and MYHANDLE\_**unbind**.</span></span>

<span data-ttu-id="7e21e-116">В случае успешного выполнения  \_ подпрограммы **привязки** TypeName должны возвращать допустимый маркер привязки типа "примитив".</span><span class="sxs-lookup"><span data-stu-id="7e21e-116">If successful, the *typename*\_**bind** routine should return a valid primitive binding handle.</span></span> <span data-ttu-id="7e21e-117">В случае неудачи подпрограммы должны возвращать **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7e21e-117">If unsuccessful, the routine should return a **NULL**.</span></span> <span data-ttu-id="7e21e-118">Если подпрограммы возвращает **значение NULL**,  \_ подпрограммы **отмены привязки** typeName не будут вызываться.</span><span class="sxs-lookup"><span data-stu-id="7e21e-118">If the routine returns **NULL**, the *typename*\_**unbind** routine will not be called.</span></span> <span data-ttu-id="7e21e-119">Если подпрограммы привязки возвращают недопустимый маркер привязки, отличный от **null**, то поведение заглушки не определено.</span><span class="sxs-lookup"><span data-stu-id="7e21e-119">If the binding routine returns an invalid binding handle different from **NULL**, the stub behavior is undefined.</span></span>

<span data-ttu-id="7e21e-120">Если у удаленной процедуры есть определяемый пользователем обработчик в качестве параметра или неявный обработчик, заглушка клиента вызывает подпрограммы привязки перед вызовом удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="7e21e-120">When the remote procedure has a user-defined handle as a parameter or as an implicit handle, the client stubs call the binding routine before calling the remote procedure.</span></span> <span data-ttu-id="7e21e-121">Заглушка клиента вызывает подпрограммы отмены привязки после удаленного вызова.</span><span class="sxs-lookup"><span data-stu-id="7e21e-121">The client stubs call the unbinding routine after the remote call.</span></span>

<span data-ttu-id="7e21e-122">В DCE IDL параметр с \[  \] атрибутом Handle должен быть первым параметром в списке аргументов удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="7e21e-122">In DCE IDL, a parameter with the \[**handle**\] attribute must appear as the first parameter in the remote procedure argument list.</span></span> <span data-ttu-id="7e21e-123">Последующие параметры, включая другие \[ атрибуты **Handle** \] , обрабатываются как обычные параметры.</span><span class="sxs-lookup"><span data-stu-id="7e21e-123">Subsequent parameters, including other \[**handle**\] attributes, are treated as ordinary parameters.</span></span> <span data-ttu-id="7e21e-124">Корпорация Майкрософт поддерживает расширение для устройства DCE IDL, которое позволяет \[ отобразить параметр пользовательского **обработчика** \] в позициях, отличных от первого параметра.</span><span class="sxs-lookup"><span data-stu-id="7e21e-124">Microsoft supports an extension to DCE IDL that allows the user-defined \[**handle**\] parameter to appear in positions other than the first parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="7e21e-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="7e21e-125">Examples</span></span>

``` syntax
typedef [handle] struct 
{ 
    char machine[8]; 
    char nmpipe[256]; 
} h_service; 
 
handle_t __RPC_USER h_service_bind(h_service); 
void __RPC_USER h_service_unbind(h_service, handle_t);
```

## <a name="see-also"></a><span data-ttu-id="7e21e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e21e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e21e-127">Привязка и дескрипторы</span><span class="sxs-lookup"><span data-stu-id="7e21e-127">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="7e21e-128">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="7e21e-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="7e21e-129">**неявный \_ обработчик**</span><span class="sxs-lookup"><span data-stu-id="7e21e-129">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="7e21e-130">**определение**</span><span class="sxs-lookup"><span data-stu-id="7e21e-130">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 