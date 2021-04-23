---
title: лицензированный атрибут
description: Атрибут \ Licensed указывает, что компонент, к которому он применяется, имеет лицензию и должен быть создан с помощью IClassFactory2.
ms.assetid: c4789ea2-8ff6-423e-8b69-22a7a5392854
keywords:
- лицензированный атрибут MIDL
topic_type:
- apiref
api_name:
- licensed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f24d8b6136cab86615e74838737bbda543b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069873"
---
# <a name="licensed-attribute"></a><span data-ttu-id="522c1-104">лицензированный атрибут</span><span class="sxs-lookup"><span data-stu-id="522c1-104">licensed attribute</span></span>

<span data-ttu-id="522c1-105">Атрибут **\[ Licensed \]** указывает, что [**компонент**](coclass.md) , к которому он применяется, имеет лицензию и должен быть создан с помощью [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2).</span><span class="sxs-lookup"><span data-stu-id="522c1-105">The **\[licensed\]** attribute indicates that the [**coclass**](coclass.md) to which it applies is licensed, and must be instantiated using [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2).</span></span>

``` syntax
[
    licensed
    [ , attribute-list ] 
]
coclass classname 
{
  coclass-definition
};
```

## <a name="parameters"></a><span data-ttu-id="522c1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="522c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="522c1-107">*Список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="522c1-107">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="522c1-108">Указывает ноль или более атрибутов, которые применяются к оператору [**coclass**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="522c1-108">Specifies zero or more attributes that apply to the [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="522c1-109">Допустимыми атрибутами **coclass** являются **\[** [**helpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[ License \]**, **\[** [**Version**](version.md) **\]** , **\[** [**Control**](control.md) **\]** и **\[** [**Hidden**](hidden.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="522c1-109">Allowable **coclass** attributes are **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[licensed\]**, **\[**[**version**](version.md)**\]**, **\[**[**control**](control.md)**\]**, and **\[**[**hidden**](hidden.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="522c1-110">*classname*</span><span class="sxs-lookup"><span data-stu-id="522c1-110">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="522c1-111">Указывает имя, по которому объект компонента известен в библиотеке типов.</span><span class="sxs-lookup"><span data-stu-id="522c1-111">Specifies the name by which the component object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="522c1-112">*определение кокласса*</span><span class="sxs-lookup"><span data-stu-id="522c1-112">*coclass-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="522c1-113">Указывает инструкции, составляющие определение [**класса**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="522c1-113">Specifies statements that make up the [**coclass**](coclass.md) definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="522c1-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="522c1-114">Remarks</span></span>

<span data-ttu-id="522c1-115">Лицензирование — это функция COM, которая обеспечивает контроль над созданием объектов.</span><span class="sxs-lookup"><span data-stu-id="522c1-115">Licensing is a feature of COM that provides control over object creation.</span></span> <span data-ttu-id="522c1-116">Лицензированные объекты могут создаваться только клиентами, которым разрешено их использовать.</span><span class="sxs-lookup"><span data-stu-id="522c1-116">Licensed objects can be created only by clients that are authorized to use them.</span></span> <span data-ttu-id="522c1-117">Лицензирование реализуется в COM через интерфейс [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) и с помощью поддержки лицензионного ключа, который может быть передан во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="522c1-117">Licensing is implemented in COM through the [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) interface and by support for a license key that can be passed at run time.</span></span>

### <a name="flags"></a><span data-ttu-id="522c1-118">Флаги</span><span class="sxs-lookup"><span data-stu-id="522c1-118">Flags</span></span>

<span data-ttu-id="522c1-119">ТИПЕФЛАГ \_ флиценсед</span><span class="sxs-lookup"><span data-stu-id="522c1-119">TYPEFLAG\_FLICENSED</span></span>

## <a name="examples"></a><span data-ttu-id="522c1-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="522c1-120">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    licensed, 
    helpstring("A meaningfulcomment"
]
coclass MyClass
{
    // coclass definition statements
};
```

## <a name="see-also"></a><span data-ttu-id="522c1-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="522c1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="522c1-122">**кокласс**</span><span class="sxs-lookup"><span data-stu-id="522c1-122">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="522c1-123">Содержимое библиотеки типов</span><span class="sxs-lookup"><span data-stu-id="522c1-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="522c1-124">**элемента**</span><span class="sxs-lookup"><span data-stu-id="522c1-124">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="522c1-125">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="522c1-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="522c1-126">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="522c1-126">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="522c1-127">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="522c1-127">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="522c1-128">**служеб**</span><span class="sxs-lookup"><span data-stu-id="522c1-128">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="522c1-129">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="522c1-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="522c1-130">типефлагс</span><span class="sxs-lookup"><span data-stu-id="522c1-130">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="522c1-131">**Версия**</span><span class="sxs-lookup"><span data-stu-id="522c1-131">**version**</span></span>](version.md)
</dt> </dl>

 

 