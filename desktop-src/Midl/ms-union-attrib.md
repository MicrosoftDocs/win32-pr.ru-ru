---
title: ms_union - атрибут
description: '\_Для управления выравниванием ОНД неинкапсулированных объединений используется ключевое слово \ MS Union \.'
ms.assetid: 20ac2985-4552-4224-b03b-07378a2c0cdf
keywords:
- ms_union атрибута MIDL
topic_type:
- apiref
api_name:
- ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ad9b750027163aef806f5a66e51f87874a0ad2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068828"
---
# <a name="ms_union-attribute"></a><span data-ttu-id="e4c08-104">\_атрибут MS Union</span><span class="sxs-lookup"><span data-stu-id="e4c08-104">ms\_union attribute</span></span>

<span data-ttu-id="e4c08-105">Ключевое слово \[ **MS \_ Union** \] используется для управления выравниванием ОНД неинкапсулированных объединений.</span><span class="sxs-lookup"><span data-stu-id="e4c08-105">The keyword \[**ms\_union**\] is used to control the NDR alignment of nonencapsulated unions.</span></span>

``` syntax
[
    ms_union,
    ...
]
interface interface-name 
{
    ...
}

[ms_union] procedure-type procedure-name(param-list);
```

## <a name="parameters"></a><span data-ttu-id="e4c08-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4c08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4c08-107">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="e4c08-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e4c08-108">Указывает имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e4c08-108">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="e4c08-109">*тип процедуры*</span><span class="sxs-lookup"><span data-stu-id="e4c08-109">*procedure-type*</span></span> 
</dt> <dd>

<span data-ttu-id="e4c08-110">Указывает тип возвращаемого значения процедуры, к которой применяется атрибут.</span><span class="sxs-lookup"><span data-stu-id="e4c08-110">Specifies the return type of the procedure to which the attribute is being applied.</span></span>

</dd> <dt>

<span data-ttu-id="e4c08-111">*имя процедуры*</span><span class="sxs-lookup"><span data-stu-id="e4c08-111">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e4c08-112">Указывает имя процедуры.</span><span class="sxs-lookup"><span data-stu-id="e4c08-112">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="e4c08-113">*Param-List*</span><span class="sxs-lookup"><span data-stu-id="e4c08-113">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e4c08-114">Указывает список параметров процедуры, который может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="e4c08-114">Specifies the procedure's parameter list, which may be empty.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4c08-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4c08-115">Remarks</span></span>

<span data-ttu-id="e4c08-116">Никогда не используйте этот параметр или атрибут с новыми интерфейсами.</span><span class="sxs-lookup"><span data-stu-id="e4c08-116">Never use this switch or attribute with new interfaces.</span></span> <span data-ttu-id="e4c08-117">Это функция обратной совместимости. Компилятор MIDL в этой версии Microsoft RPC отражает поведение компилятора использование DCE IDL для неинкапсулированных объединений.</span><span class="sxs-lookup"><span data-stu-id="e4c08-117">This is a backward compatibility feature only.The MIDL compiler in this version of Microsoft RPC mirrors the behavior of the OSF DCE IDL compiler for nonencapsulated unions.</span></span> <span data-ttu-id="e4c08-118">Однако, поскольку более ранние версии компилятора MIDL не сделали этого, коммутатор [**/МС \_ Union**](-ms-union.md) обеспечивает совместимость с интерфейсами, созданными в предыдущих версиях компилятора MIDL.</span><span class="sxs-lookup"><span data-stu-id="e4c08-118">However, because earlier versions of the MIDL compiler did not do so, the [**/ms\_union**](-ms-union.md) switch provides compatibility with interfaces built on previous versions of the MIDL compiler.</span></span>

<span data-ttu-id="e4c08-119">Функцию **MS \_ Union** можно использовать в качестве атрибута интерфейса IDL, атрибута типа IDL или в качестве параметра командной строки ( [**/МС \_ Union**](-ms-union.md)).</span><span class="sxs-lookup"><span data-stu-id="e4c08-119">The **ms\_union** feature can be used as an IDL interface attribute, an IDL type attribute, or as a command-line switch ( [**/ms\_union**](-ms-union.md)).</span></span>

## <a name="examples"></a><span data-ttu-id="e4c08-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="e4c08-120">Examples</span></span>

``` syntax
[ms_union] long procedure (...);
```

## <a name="see-also"></a><span data-ttu-id="e4c08-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4c08-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4c08-122">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="e4c08-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e4c08-123">**\_объединение/МС**</span><span class="sxs-lookup"><span data-stu-id="e4c08-123">**/ms\_union**</span></span>](-ms-union.md)
</dt> </dl>

 

 




