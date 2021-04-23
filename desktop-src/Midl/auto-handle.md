---
title: атрибут auto_handle
description: Атрибут \ Auto \_ Handle \ ACF указывает заглушке автоматически устанавливать привязку для функции, которая не имеет явного параметра обработчика привязки. Примечание. Этот атрибут устарел и больше не поддерживается.
ms.assetid: a402b933-f69b-4dfe-b0c5-b034d65d4a84
keywords:
- auto_handle атрибута MIDL
topic_type:
- apiref
api_name:
- auto_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e9a4c91fac8553867536f4f5a8c3094e0f0ff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487117"
---
# <a name="auto_handle-attribute"></a><span data-ttu-id="a533b-104">\_атрибут Auto Handle</span><span class="sxs-lookup"><span data-stu-id="a533b-104">auto\_handle attribute</span></span>

<span data-ttu-id="a533b-105">Атрибут **\[ Auto \_ Handle \]** ACF указывает заглушке автоматически устанавливать привязку для функции, которая не имеет явного параметра обработчика привязки.</span><span class="sxs-lookup"><span data-stu-id="a533b-105">The **\[auto\_handle\]** ACF attribute directs the stub to automatically establish the binding for a function that does not have an explicit binding-handle parameter.</span></span>

> [!Note]  
> <span data-ttu-id="a533b-106">Этот атрибут устарел и больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a533b-106">This attribute is obsolete and no longer supported.</span></span> <span data-ttu-id="a533b-107">Рекомендуется использовать параметр [**/robust**](-robust.md) .</span><span class="sxs-lookup"><span data-stu-id="a533b-107">Use of the [**/robust**](-robust.md) switch is recommended.</span></span>

 

``` syntax
[ 
    auto_handle [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}
```

## <a name="parameters"></a><span data-ttu-id="a533b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a533b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a533b-109">*Interface-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="a533b-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a533b-110">Указывает ноль или более атрибутов, которые применяются к интерфейсу в целом, например [**код**](code.md) [**или код**](nocode.md).</span><span class="sxs-lookup"><span data-stu-id="a533b-110">Specifies zero or more attributes that apply to the interface as a whole, such as [**code**](code.md) or [**nocode**](nocode.md).</span></span> <span data-ttu-id="a533b-111">Разделяйте атрибуты интерфейса запятыми.</span><span class="sxs-lookup"><span data-stu-id="a533b-111">Separate interface attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="a533b-112">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="a533b-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a533b-113">Указывает имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a533b-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="a533b-114">*определение интерфейса*</span><span class="sxs-lookup"><span data-stu-id="a533b-114">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="a533b-115">Задает инструкции IDL, которые формируют определение интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a533b-115">Specifies IDL statements that form the definition of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a533b-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a533b-116">Remarks</span></span>

<span data-ttu-id="a533b-117">Атрибут **\[ Auto \_ Handle \]** отображается в заголовке интерфейса ACF.</span><span class="sxs-lookup"><span data-stu-id="a533b-117">The **\[auto\_handle\]** attribute appears in the interface header of the ACF.</span></span> <span data-ttu-id="a533b-118">Он также отображается в заголовке интерфейса IDL-файла при указании конфигурации компилятора MIDL Switch [**/АПП \_ config**](-app-config.md).</span><span class="sxs-lookup"><span data-stu-id="a533b-118">It also appears in the interface header of the IDL file when you specify the MIDL compiler switch [**/app\_config**](-app-config.md).</span></span>

<span data-ttu-id="a533b-119">Когда клиент вызывает функцию, которая использует автоматическую привязку и не существует привязки к серверу, заглушка автоматически устанавливает привязку.</span><span class="sxs-lookup"><span data-stu-id="a533b-119">When the client calls a function that uses automatic binding and no binding to a server exists, the stub automatically establishes the binding.</span></span> <span data-ttu-id="a533b-120">Привязка повторно используется для последующих вызовов других функций в интерфейсе, который использует автоматическую привязку.</span><span class="sxs-lookup"><span data-stu-id="a533b-120">The binding is reused for subsequent calls to other functions in the interface that use automatic binding.</span></span> <span data-ttu-id="a533b-121">Приложению клиента не нужно объявлять или выполнять обработку, связанную с маркером привязки.</span><span class="sxs-lookup"><span data-stu-id="a533b-121">The client application program does not have to declare or perform any processing relating to the binding handle.</span></span>

<span data-ttu-id="a533b-122">Если ACF отсутствует или не включает атрибут [**\[ неявного \_ обработчика \]**](implicit-handle.md) , компилятор MIDL использует **\[ автоматическую \_ обработку \]** и выдает информационное сообщение.</span><span class="sxs-lookup"><span data-stu-id="a533b-122">When the ACF is not present or does not include the [**\[implicit\_handle\]**](implicit-handle.md) attribute, the MIDL compiler uses **\[auto\_handle\]** and issues an informational message.</span></span> <span data-ttu-id="a533b-123">Компилятор MIDL также использует при необходимости **\[ автоматическую \_ обработку \]**, чтобы установить начальную привязку для [**\[ \_ маркера \] контекста**](context-handle.md).</span><span class="sxs-lookup"><span data-stu-id="a533b-123">The MIDL compiler also uses **\[auto\_handle\]**, if needed, to establish the initial binding for a [**\[context\_handle\]**](context-handle.md).</span></span>

<span data-ttu-id="a533b-124">Атрибут **\[ Auto \_ Handle \]** может возникать, только если не существует [**\[ неявного \_ обработчика \]**](implicit-handle.md) или [**\[ \_ \] атрибута неявного**](explicit-handle.md) обработчика.</span><span class="sxs-lookup"><span data-stu-id="a533b-124">The **\[auto\_handle\]** attribute can occur only if the [**\[implicit\_handle\]**](implicit-handle.md) or [**\[explicit\_handle\]**](explicit-handle.md) attribute does not occur.</span></span> <span data-ttu-id="a533b-125">Атрибут **\[ Auto \_ Handle \]** может появляться в заголовке интерфейса ACF или IDL не более одного раза.</span><span class="sxs-lookup"><span data-stu-id="a533b-125">The **\[auto\_handle\]** attribute can occur in the ACF or IDL interface header at most once.</span></span>

> [!Note]  
> <span data-ttu-id="a533b-126">Нельзя использовать автоматическую привязку (с атрибутом **\[ Auto \_ Handle \]** или по умолчанию) при обработке данных по каналам.</span><span class="sxs-lookup"><span data-stu-id="a533b-126">You cannot use automatic binding (either with the **\[auto\_handle\]** attribute, or by default) if you are processing data through pipes.</span></span>

 

## <a name="examples"></a><span data-ttu-id="a533b-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="a533b-127">Examples</span></span>

``` syntax
[
    auto_handle
] 
interface MyInterface 
{ 
    /* Interface definition goes here*/
} 
[
    auto_handle, 
    code
] 
interface MyInterface
{ 
    /* Interface definition goes here*/
}
```

## <a name="see-also"></a><span data-ttu-id="a533b-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a533b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a533b-129">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="a533b-129">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="a533b-130">**\_Конфигурация/АПП**</span><span class="sxs-lookup"><span data-stu-id="a533b-130">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="a533b-131">**приведен**</span><span class="sxs-lookup"><span data-stu-id="a533b-131">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="a533b-132">**явный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="a533b-132">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="a533b-133">**Контекстный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="a533b-133">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="a533b-134">**неявный \_ обработчик**</span><span class="sxs-lookup"><span data-stu-id="a533b-134">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="a533b-135">**nocode**</span><span class="sxs-lookup"><span data-stu-id="a533b-135">**nocode**</span></span>](nocode.md)
</dt> </dl>

 

 




