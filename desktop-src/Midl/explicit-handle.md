---
title: атрибут explicit_handle
description: Атрибут \ Explicit \_ Handle \ ACF указывает, что каждая процедура в качестве первого параметра представляет собой примитивный маркер, такой как \_ тип t.
ms.assetid: c95d005e-dcc7-4d83-885d-91c0773c0ed8
keywords:
- explicit_handle атрибута MIDL
topic_type:
- apiref
api_name:
- explicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4fa677f1bb5a3414e6cf6dc761b83414c2d68b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105650310"
---
# <a name="explicit_handle-attribute"></a><span data-ttu-id="031d1-104">явный \_ атрибут Handle</span><span class="sxs-lookup"><span data-stu-id="031d1-104">explicit\_handle attribute</span></span>

<span data-ttu-id="031d1-105">Атрибут \[ **явного \_ Handle** \] ACF указывает, что каждая процедура имеет в качестве первого параметра, примитивный маркер, такой как тип [**\_ t**](handle-t.md) .</span><span class="sxs-lookup"><span data-stu-id="031d1-105">The \[**explicit\_handle**\] ACF attribute specifies that each procedure has, as its first parameter, a primitive handle, such as a [**handle\_t**](handle-t.md) type.</span></span>

``` syntax
[
    explicit_handle
] 
interface interface-name
{
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="031d1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="031d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="031d1-107">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="031d1-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="031d1-108">Указывает имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="031d1-108">Specifies the name of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="031d1-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="031d1-109">Remarks</span></span>

<span data-ttu-id="031d1-110">При использовании явного атрибута **\[ \_ Handle \]** каждая процедура имеет примитивный маркер в качестве первого параметра, даже если IDL-файл не содержит этот обработчик в списке параметров.</span><span class="sxs-lookup"><span data-stu-id="031d1-110">When you use the **\[explicit\_handle\]** attribute, each procedure has a primitive handle as its first parameter even if the IDL file does not contain this handle in its parameter list.</span></span> <span data-ttu-id="031d1-111">Прототипы, передаваемые в файл заголовка и подпрограммы-заглушки, содержат дополнительный параметр, а этот параметр используется в качестве маркера для направления удаленного вызова.</span><span class="sxs-lookup"><span data-stu-id="031d1-111">The prototypes emitted to the header file and stub routines contain the additional parameter, and that parameter is used as the handle for directing the remote call.</span></span>

<span data-ttu-id="031d1-112">**\[ Явный атрибут \_ Handle \]** влияет как на удаленные процедуры, так и на процедуры сериализации.</span><span class="sxs-lookup"><span data-stu-id="031d1-112">The **\[explicit\_handle\]** attribute affects both remote procedures and serialization procedures.</span></span> <span data-ttu-id="031d1-113">Для сериализации типов подпрограммы поддержки создаются с начальным параметром в виде явного (сериализации) маркера.</span><span class="sxs-lookup"><span data-stu-id="031d1-113">For type serialization, the support routines are generated with the initial parameter as an explicit (serialization) handle.</span></span> <span data-ttu-id="031d1-114">Если **\[ явный атрибут \_ Handle \]** не используется, приложение по-прежнему может указать, что операция имеет явный маркер (привязку или сериализацию), направленный на вызов.</span><span class="sxs-lookup"><span data-stu-id="031d1-114">If the **\[explicit\_handle\]** attribute is not used, the application can still specify that an operation have an explicit handle (binding or serialization) directing the call.</span></span> <span data-ttu-id="031d1-115">Для этого прототип с аргументом, содержащим тип маркера, предоставляется IDL-файлу.</span><span class="sxs-lookup"><span data-stu-id="031d1-115">To do this, a prototype with an argument containing a handle type is supplied to the IDL file.</span></span> <span data-ttu-id="031d1-116">Обратите внимание, что в режиме по умолчанию аргумент, который не является первым, можно также использовать в качестве обработчика, направляющего вызов.</span><span class="sxs-lookup"><span data-stu-id="031d1-116">Note that in default mode, an argument that does not appear first can also be used as a handle directing the call.</span></span>

<span data-ttu-id="031d1-117">Таким образом, хотя **\[ явный \_ атрибут \] Handle** является способом предоставления прототипа IDL **\[ явному \_ \]** атрибуту Handle, он не обязательно требует изменения IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="031d1-117">Therefore, while the **\[explicit\_handle\]** attribute is a way of giving the IDL prototype a primitive **\[explicit\_handle\]** attribute, it does not necessarily require a change to the IDL file.</span></span> <span data-ttu-id="031d1-118">В режиме [**/ОСФ**](-osf.md) только первый аргумент может быть использован в качестве явного типа обработчика.</span><span class="sxs-lookup"><span data-stu-id="031d1-118">In [**/osf**](-osf.md) mode only the first argument can be used as an explicit handle type.</span></span>

<span data-ttu-id="031d1-119">**\[ Явный атрибут \_ Handle \]** можно использовать как атрибут интерфейса или атрибут операции.</span><span class="sxs-lookup"><span data-stu-id="031d1-119">The **\[explicit\_handle\]** attribute can be used as either an interface attribute or an operation attribute.</span></span> <span data-ttu-id="031d1-120">Как атрибут интерфейса он влияет на все операции в интерфейсе и на все типы, требующие поддержки сериализации.</span><span class="sxs-lookup"><span data-stu-id="031d1-120">As an interface attribute, it affects all the operations in the interface and all the types that require serialization support.</span></span> <span data-ttu-id="031d1-121">Однако если он используется как атрибут операции, он влияет только на эту конкретную операцию.</span><span class="sxs-lookup"><span data-stu-id="031d1-121">If, however, it is used as an operation attribute, it affects only that particular operation.</span></span> <span data-ttu-id="031d1-122">Если метод содержит один или несколько \[ \] дескрипторов контекста, то в \[ \] качестве дескриптора привязки используется самый левый дескриптор контекста, а дополнительный неявный дескриптор не создается.</span><span class="sxs-lookup"><span data-stu-id="031d1-122">If a method contains one or more \[in\] context handles, the left most \[in\] context handle is used as the binding handle, and no additional explicit handle is created.</span></span>

## <a name="examples"></a><span data-ttu-id="031d1-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="031d1-123">Examples</span></span>

``` syntax
/* ACF File */ 
[
    explicit_handle
] 
interface iface
{ 
    // Interface definition statements.
};
```

## <a name="see-also"></a><span data-ttu-id="031d1-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="031d1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="031d1-125">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="031d1-125">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="031d1-126">**Автоматическая \_ работа**</span><span class="sxs-lookup"><span data-stu-id="031d1-126">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="031d1-127">**неявный \_ обработчик**</span><span class="sxs-lookup"><span data-stu-id="031d1-127">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="031d1-128">**/осф**</span><span class="sxs-lookup"><span data-stu-id="031d1-128">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 




