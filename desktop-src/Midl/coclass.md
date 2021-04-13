---
title: coclass - атрибут
description: Оператор CoClass предоставляет список поддерживаемых интерфейсов для объекта компонента.
ms.assetid: 2c636327-ad18-4087-b495-d1aa84a07f48
keywords:
- атрибут coclass MIDL
topic_type:
- apiref
api_name:
- coclass
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba95b38675869637c679a2409a82fb812709ec8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412897"
---
# <a name="coclass-attribute"></a><span data-ttu-id="120f9-104">coclass - атрибут</span><span class="sxs-lookup"><span data-stu-id="120f9-104">coclass attribute</span></span>

<span data-ttu-id="120f9-105">Оператор **coclass** предоставляет список поддерживаемых интерфейсов для объекта компонента.</span><span class="sxs-lookup"><span data-stu-id="120f9-105">The **coclass** statement provides a listing of the supported interfaces for a component object.</span></span>

``` syntax
[
    coclass-attribute-list
]
coclass classname
{
    [
        interface-attributes
    ] 
    [interface | dispinterface] interfacename 
    {
  . . . 
    }
}
```

## <a name="parameters"></a><span data-ttu-id="120f9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="120f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="120f9-107">*Список атрибутов coclass*</span><span class="sxs-lookup"><span data-stu-id="120f9-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="120f9-108">Атрибут **\[** [**UUID**](uuid.md) **\]** является обязательным для **компонентного класса**.</span><span class="sxs-lookup"><span data-stu-id="120f9-108">The **\[**[**uuid**](uuid.md)**\]** attribute is required on a **coclass**.</span></span> <span data-ttu-id="120f9-109">Это тот же **\[ UUID \]** , который зарегистрирован в качестве идентификатора CLSID в системной базе данных регистрации.</span><span class="sxs-lookup"><span data-stu-id="120f9-109">This is the same **\[uuid\]** that is registered as a CLSID in the system registration database.</span></span> <span data-ttu-id="120f9-110">Атрибуты **\[** [**helpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**License**](licensed.md) **\]** , **\[** [**Version**](version.md) **\]** , **\[** [**Control**](control.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** и **\[** [**аппобжект**](appobject.md) **\]** принимаются, но не являются обязательными, перед определением **компонентного класса** .</span><span class="sxs-lookup"><span data-stu-id="120f9-110">The **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**licensed**](licensed.md)**\]**, **\[**[**version**](version.md)**\]**, **\[**[**control**](control.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, and **\[**[**appobject**](appobject.md)**\]** attributes are accepted, but not required, before a **coclass** definition.</span></span>

</dd> <dt>

<span data-ttu-id="120f9-111">*classname*</span><span class="sxs-lookup"><span data-stu-id="120f9-111">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="120f9-112">Имя, по которому известен общий объект в библиотеке типов.</span><span class="sxs-lookup"><span data-stu-id="120f9-112">Name by which the common object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="120f9-113">*атрибуты интерфейса*</span><span class="sxs-lookup"><span data-stu-id="120f9-113">*interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="120f9-114">Необязательные атрибуты для интерфейса или DISP.</span><span class="sxs-lookup"><span data-stu-id="120f9-114">Optional attributes for the interface or dispinterface.</span></span> <span data-ttu-id="120f9-115">Атрибуты **\[** [**Source**](source.md) **\]** , **\[** [**Default**](default.md) **\]** и **\[** [**Restricted**](restricted.md) **\]** принимаются в интерфейсе или DISP в **компонентном классе**.</span><span class="sxs-lookup"><span data-stu-id="120f9-115">The **\[**[**source**](source.md)**\]**, **\[**[**default**](default.md)**\]**, and **\[**[**restricted**](restricted.md)**\]** attributes are accepted on an interface or dispinterface within a **coclass**.</span></span>

</dd> <dt>

<span data-ttu-id="120f9-116">*InterfaceName*</span><span class="sxs-lookup"><span data-stu-id="120f9-116">*interfacename*</span></span> 
</dt> <dd>

<span data-ttu-id="120f9-117">Либо интерфейс, объявленный с помощью ключевого слова [**Interface**](interface.md) , либо disp-интерфейс, объявленный с ключевым словом [**DISP**](dispinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="120f9-117">Either an interface declared with the [**interface**](interface.md) keyword, or a dispinterface declared with the [**dispinterface**](dispinterface.md) keyword.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="120f9-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="120f9-118">Remarks</span></span>

<span data-ttu-id="120f9-119">Объектная модель компонента Microsoft определяет класс как реализацию, которая разрешает **QueryInterface** между наборами интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="120f9-119">The Microsoft Component Object Model defines a class as an implementation that allows **QueryInterface** between a set of interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="120f9-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="120f9-120">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("A class"), 
    helpcontext(2481), appobject
] 
coclass myapp 
{ 
    [source] interface IMydocfuncs : IUnknown; 
    dispinterface DMydocfuncs; 
}; 
 
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
coclass mycoclass 
{ 
    [restricted] interface iface1; 
    interface iface2; 
}
```

## <a name="see-also"></a><span data-ttu-id="120f9-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="120f9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="120f9-122">**appobject**</span><span class="sxs-lookup"><span data-stu-id="120f9-122">**appobject**</span></span>](appobject.md)
</dt> <dt>

[<span data-ttu-id="120f9-123">**элемента**</span><span class="sxs-lookup"><span data-stu-id="120f9-123">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="120f9-124">**параметры**</span><span class="sxs-lookup"><span data-stu-id="120f9-124">**default**</span></span>](default.md)
</dt> <dt>

[<span data-ttu-id="120f9-125">**интерфейса**</span><span class="sxs-lookup"><span data-stu-id="120f9-125">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="120f9-126">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="120f9-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="120f9-127">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="120f9-127">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="120f9-128">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="120f9-128">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="120f9-129">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="120f9-129">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="120f9-130">**служеб**</span><span class="sxs-lookup"><span data-stu-id="120f9-130">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="120f9-131">**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="120f9-131">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="120f9-132">**обладателем**</span><span class="sxs-lookup"><span data-stu-id="120f9-132">**licensed**</span></span>](licensed.md)
</dt> <dt>

[<span data-ttu-id="120f9-133">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="120f9-133">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="120f9-134">**зона**</span><span class="sxs-lookup"><span data-stu-id="120f9-134">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="120f9-135">**источника**</span><span class="sxs-lookup"><span data-stu-id="120f9-135">**source**</span></span>](source.md)
</dt> <dt>

[<span data-ttu-id="120f9-136">типефлагс</span><span class="sxs-lookup"><span data-stu-id="120f9-136">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="120f9-137">**UUID**</span><span class="sxs-lookup"><span data-stu-id="120f9-137">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="120f9-138">**Версия**</span><span class="sxs-lookup"><span data-stu-id="120f9-138">**version**</span></span>](version.md)
</dt> </dl>

 

 