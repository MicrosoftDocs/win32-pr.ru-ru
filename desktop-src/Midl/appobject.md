---
title: appobject - атрибут
description: Атрибут \ аппобжект \ определяет компонент coclass как объект приложения, связанный с полноценным приложением EXE.
ms.assetid: f4fcdf55-7431-4d66-8a46-f741c52fbe56
keywords:
- атрибут аппобжект MIDL
topic_type:
- apiref
api_name:
- appobject
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d937d4a83306bc0c29f3c8c806bc043febec6a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412846"
---
# <a name="appobject-attribute"></a><span data-ttu-id="d399d-104">appobject - атрибут</span><span class="sxs-lookup"><span data-stu-id="d399d-104">appobject attribute</span></span>

<span data-ttu-id="d399d-105">Атрибут **\[ аппобжект \]** идентифицирует [**компонентный класс**](coclass.md) как объект приложения, связанный с полноценным приложением exe.</span><span class="sxs-lookup"><span data-stu-id="d399d-105">The **\[appobject\]** attribute identifies the [**coclass**](coclass.md) as an application object, which is associated with a full EXE application.</span></span>

``` syntax
[
    uuid(uuid-number), 
    appobject 
  [, coclass-attribute-list]
]
coclass classname 
{ 
    [coclass definition]
}
```

## <a name="parameters"></a><span data-ttu-id="d399d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d399d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d399d-107">*UUID — номер*</span><span class="sxs-lookup"><span data-stu-id="d399d-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="d399d-108">Задает универсальный уникальный идентификационный номер для [**компонентного класса**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="d399d-108">Specifies a universally unique identification number for the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="d399d-109">*Список атрибутов coclass*</span><span class="sxs-lookup"><span data-stu-id="d399d-109">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d399d-110">Указывает ноль или более атрибутов, которые применяются к оператору [**coclass**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="d399d-110">Specifies zero or more attributes that apply to the [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="d399d-111">Допустимыми атрибутами **coclass** являются [**\[ helpString \]**](helpstring.md), [**\[ HelpContext \]**](helpcontext.md), [**\[ License \]**](licensed.md), [**\[ Version \]**](version.md), [**\[ Control \]**](control.md)и [**\[ Hidden \]**](hidden.md).</span><span class="sxs-lookup"><span data-stu-id="d399d-111">Allowable **coclass** attributes are [**\[helpstring\]**](helpstring.md), [**\[helpcontext\]**](helpcontext.md), [**\[licensed\]**](licensed.md), [**\[version\]**](version.md), [**\[control\]**](control.md), and [**\[hidden\]**](hidden.md).</span></span>

</dd> <dt>

<span data-ttu-id="d399d-112">*classname*</span><span class="sxs-lookup"><span data-stu-id="d399d-112">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="d399d-113">Указывает имя, по которому объект компонента известен в библиотеке типов.</span><span class="sxs-lookup"><span data-stu-id="d399d-113">Specifies the name by which the component object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="d399d-114">*определение coclass*</span><span class="sxs-lookup"><span data-stu-id="d399d-114">*coclass definition*</span></span> 
</dt> <dd>

<span data-ttu-id="d399d-115">Указывает инструкции, составляющие определение [**класса**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="d399d-115">Specifies statements that make up the [**coclass**](coclass.md) definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d399d-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d399d-116">Remarks</span></span>

<span data-ttu-id="d399d-117">Атрибут **\[ аппобжект \]** также указывает, что функции и свойства [**компонентного класса**](coclass.md) глобально доступны в текущей библиотеке типов.</span><span class="sxs-lookup"><span data-stu-id="d399d-117">The **\[appobject\]** attribute also indicates that the functions and properties of the [**coclass**](coclass.md) are globally available in the current type library.</span></span>

<span data-ttu-id="d399d-118">Представление типефлаг для этого атрибута — ТИПЕФЛАГ \_ фаппобжект</span><span class="sxs-lookup"><span data-stu-id="d399d-118">The typeflag representation for this attribute is TYPEFLAG\_FAPPOBJECT</span></span>

## <a name="examples"></a><span data-ttu-id="d399d-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="d399d-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a><span data-ttu-id="d399d-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d399d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d399d-121">**кокласс**</span><span class="sxs-lookup"><span data-stu-id="d399d-121">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="d399d-122">**элемента**</span><span class="sxs-lookup"><span data-stu-id="d399d-122">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="d399d-123">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="d399d-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="d399d-124">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="d399d-124">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="d399d-125">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="d399d-125">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="d399d-126">**служеб**</span><span class="sxs-lookup"><span data-stu-id="d399d-126">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="d399d-127">**обладателем**</span><span class="sxs-lookup"><span data-stu-id="d399d-127">**licensed**</span></span>](licensed.md)
</dt> <dt>

[<span data-ttu-id="d399d-128">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="d399d-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="d399d-129">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="d399d-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="d399d-130">типефлагс</span><span class="sxs-lookup"><span data-stu-id="d399d-130">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="d399d-131">**Версия**</span><span class="sxs-lookup"><span data-stu-id="d399d-131">**version**</span></span>](version.md)
</dt> </dl>

 

 