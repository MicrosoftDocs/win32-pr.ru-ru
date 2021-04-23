---
title: dual - атрибут
description: Двойной атрибут определяет интерфейс, который предоставляет свойства и методы через IDispatch и напрямую через VTBL.
ms.assetid: 1c214f10-57eb-4a05-99a8-a09770666a74
keywords:
- двойной атрибут MIDL
topic_type:
- apiref
api_name:
- dual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39a9e44de464f58fd1ffc0606551b9a0203ae9e9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987491"
---
# <a name="dual-attribute"></a><span data-ttu-id="3ffc2-104">dual - атрибут</span><span class="sxs-lookup"><span data-stu-id="3ffc2-104">dual attribute</span></span>

<span data-ttu-id="3ffc2-105">**Двойной** атрибут определяет интерфейс, который предоставляет свойства и методы через [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) и напрямую через VTBL.</span><span class="sxs-lookup"><span data-stu-id="3ffc2-105">The **dual** attribute identifies an interface that exposes properties and methods through [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) and directly through the VTBL.</span></span>

``` syntax
[
    uuid(uuid-number), 
    oleautomation,
    dual 
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a><span data-ttu-id="3ffc2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ffc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ffc2-107">*UUID — номер*</span><span class="sxs-lookup"><span data-stu-id="3ffc2-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="3ffc2-108">Задает универсальный уникальный идентификационный номер для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3ffc2-108">Specifies a universally unique identification number for the interface</span></span>

</dd> <dt>

<span data-ttu-id="3ffc2-109">*список необязательных атрибутов*</span><span class="sxs-lookup"><span data-stu-id="3ffc2-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3ffc2-110">Задает список из нуля или нескольких дополнительных атрибутов MIDL.</span><span class="sxs-lookup"><span data-stu-id="3ffc2-110">Specifies a list of zero or more additional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="3ffc2-111">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="3ffc2-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3ffc2-112">Имя интерфейса, к которому будет применен **двойной** атрибут.</span><span class="sxs-lookup"><span data-stu-id="3ffc2-112">The name of the interface to which the **dual** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ffc2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ffc2-113">Remarks</span></span>

<span data-ttu-id="3ffc2-114">Интерфейсы, определяемые **двойным** атрибутом, должны быть совместимы с автоматизацией и быть производными от [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span><span class="sxs-lookup"><span data-stu-id="3ffc2-114">Interfaces identified by the **dual** attribute must be compatible with Automation and be derived from [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span></span> <span data-ttu-id="3ffc2-115">Этот атрибут не разрешен в DISP-интерфейсах.</span><span class="sxs-lookup"><span data-stu-id="3ffc2-115">This attribute is not allowed on dispinterfaces.</span></span>

<span data-ttu-id="3ffc2-116">**Двойной** атрибут создает интерфейс, который является как интерфейсом [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , так и интерфейсом модели COM.</span><span class="sxs-lookup"><span data-stu-id="3ffc2-116">The **dual** attribute creates an interface that is both an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface and a Component Object Model (COM) interface.</span></span> <span data-ttu-id="3ffc2-117">Первые семь записей таблицы VTBL для сдвоенного интерфейса — семь членов **IDispatch**, а остальные — для прямого доступа к членам сдвоенного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3ffc2-117">The first seven entries of the VTBL for a dual interface are the seven members of **IDispatch**, and the remaining entries are for direct access to members of the dual interface.</span></span> <span data-ttu-id="3ffc2-118">Все параметры и возвращаемые типы, указанные для членов сдвоенного интерфейса, должны иметь совместимые с автоматизацией типы.</span><span class="sxs-lookup"><span data-stu-id="3ffc2-118">All the parameters and return types specified for members of a dual interface must be Automation-compatible types.</span></span>

<span data-ttu-id="3ffc2-119">Все члены сдвоенного интерфейса должны передавать HRESULT в качестве возвращаемого значения функции.</span><span class="sxs-lookup"><span data-stu-id="3ffc2-119">All members of a dual interface must pass an HRESULT as the function return value.</span></span> <span data-ttu-id="3ffc2-120">Элементы, такие как функции доступа к свойствам, которые должны возвращать другие значения, должны указывать последний параметр как [**out**](out-idl.md), [**retval**](retval.md), указывающий выходной параметр, возвращающий значение функции.</span><span class="sxs-lookup"><span data-stu-id="3ffc2-120">Members, such as property accessor functions, that need to return other values, should specify the last parameter as [**out**](out-idl.md), [**retval**](retval.md), indicating an output parameter that returns the value of the function.</span></span> <span data-ttu-id="3ffc2-121">Кроме того, члены, которым требуется поддержка нескольких языковых стандартов, должны передавать параметр [**LCID**](lcid.md) .</span><span class="sxs-lookup"><span data-stu-id="3ffc2-121">In addition, members that need to support multiple locales should pass an [**lcid**](lcid.md) parameter.</span></span>

<span data-ttu-id="3ffc2-122">Сдвоенный интерфейс обеспечивает как скорость прямой привязки VTBL, так и гибкость привязки [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="3ffc2-122">A dual interface provides for both the speed of direct VTBL binding and the flexibility of [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) binding.</span></span> <span data-ttu-id="3ffc2-123">По этой причине при возможности рекомендуется использовать сдвоенные интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="3ffc2-123">For this reason, dual interfaces are recommended whenever possible.</span></span>

> [!Note]  
> <span data-ttu-id="3ffc2-124">Если приложение обращается к данным объекта путем приведения *указателя мыши в* вызове интерфейса, следует проверить УКАЗАТЕЛИ таблицы VTBL в объекте на соответствие собственным указателям VTBL, чтобы убедиться, что вы подключены к соответствующему прокси-серверу.</span><span class="sxs-lookup"><span data-stu-id="3ffc2-124">If your application accesses object data by casting the *this* pointer within the interface call, you should check the VTBL pointers in the object against your own VTBL pointers to ensure that you are connected to the appropriate proxy.</span></span>

 

<span data-ttu-id="3ffc2-125">Указание **двойного** интерфейса подразумевает, что интерфейс совместим с автоматизацией, и поэтому \_ устанавливает флаги ТИПЕФЛАГ фдуал и типефлаг \_ фолеаутоматион.</span><span class="sxs-lookup"><span data-stu-id="3ffc2-125">Specifying **dual** on an interface implies that the interface is compatible with Automation, and therefore causes both the TYPEFLAG\_FDUAL and TYPEFLAG\_FOLEAUTOMATION flags to be set.</span></span>

### <a name="flags"></a><span data-ttu-id="3ffc2-126">Флаги</span><span class="sxs-lookup"><span data-stu-id="3ffc2-126">Flags</span></span>

<span data-ttu-id="3ffc2-127">ТИПЕФЛАГ \_ фдуал, типефлаг \_ фолеаутоматион</span><span class="sxs-lookup"><span data-stu-id="3ffc2-127">TYPEFLAG\_FDUAL, TYPEFLAG\_FOLEAUTOMATION</span></span>

## <a name="examples"></a><span data-ttu-id="3ffc2-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="3ffc2-128">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    oleautomation, dual
]
interface IHello : IDispatch
{
    //Diverse properties and methods defined here.
};
```

## <a name="see-also"></a><span data-ttu-id="3ffc2-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ffc2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ffc2-130">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="3ffc2-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="3ffc2-131">**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="3ffc2-131">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="3ffc2-132">**намного**</span><span class="sxs-lookup"><span data-stu-id="3ffc2-132">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="3ffc2-133">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="3ffc2-133">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="3ffc2-134">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="3ffc2-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="3ffc2-135">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="3ffc2-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="3ffc2-136">**заполняет**</span><span class="sxs-lookup"><span data-stu-id="3ffc2-136">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="3ffc2-137">**retval**</span><span class="sxs-lookup"><span data-stu-id="3ffc2-137">**retval**</span></span>](retval.md)
</dt> </dl>

 

 