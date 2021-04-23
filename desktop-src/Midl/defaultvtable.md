---
title: defaultvtable - атрибут
description: Атрибут \ defaultvtable \ определяет интерфейс как интерфейс vtable по умолчанию.
ms.assetid: 05e50935-c630-4f9e-a7ec-3bb70a9834f1
keywords:
- атрибут defaultvtable MIDL
topic_type:
- apiref
api_name:
- defaultvtable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8086d60d0936dcf56738afadea4244a5fff758b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890584"
---
# <a name="defaultvtable-attribute"></a><span data-ttu-id="f5998-104">defaultvtable - атрибут</span><span class="sxs-lookup"><span data-stu-id="f5998-104">defaultvtable attribute</span></span>

<span data-ttu-id="f5998-105">Атрибут **\[ defaultvtable \]** определяет интерфейс как интерфейс vtable по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f5998-105">The **\[defaultvtable\]** attribute defines an interface as the default Vtable interface.</span></span>

``` syntax
[
    coclass-attribute-list, 
    defaultvtable
]
coclass coclass-name
{
    coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="f5998-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5998-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5998-107">*Список атрибутов coclass*</span><span class="sxs-lookup"><span data-stu-id="f5998-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f5998-108">Другие атрибуты, которые применяются к классу.</span><span class="sxs-lookup"><span data-stu-id="f5998-108">Other attributes that apply to the class.</span></span> <span data-ttu-id="f5998-109">Атрибуты **\[** [**Source**](source.md) **\]** и **\[** [**UUID**](uuid.md) **\]** обязательны.</span><span class="sxs-lookup"><span data-stu-id="f5998-109">The **\[**[**source**](source.md)**\]** and **\[**[**uuid**](uuid.md)**\]** attributes are required.</span></span>

</dd> <dt>

<span data-ttu-id="f5998-110">*имя класса*</span><span class="sxs-lookup"><span data-stu-id="f5998-110">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f5998-111">Имя класса.</span><span class="sxs-lookup"><span data-stu-id="f5998-111">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="f5998-112">*coclass-интерфейс-список*</span><span class="sxs-lookup"><span data-stu-id="f5998-112">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f5998-113">Список интерфейсов для класса.</span><span class="sxs-lookup"><span data-stu-id="f5998-113">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5998-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5998-114">Remarks</span></span>

<span data-ttu-id="f5998-115">Интерфейс vtable по умолчанию не может быть диспетчером интерфейса, он должен быть сдвоенным или vtable или интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="f5998-115">A default Vtable interface cannot be a dispinterface—it must be a dual or Vtable or interface.</span></span> <span data-ttu-id="f5998-116">Если интерфейс является сдвоенным интерфейсом, приемники могут предположить, что они будут принимать события через vtable.</span><span class="sxs-lookup"><span data-stu-id="f5998-116">If the interface is a dual interface, then sinks can assume that they will receive events through Vtable.</span></span>

<span data-ttu-id="f5998-117">Класс может быть как исходным интерфейсом по умолчанию, так и исходным интерфейсом vtable по умолчанию, как показано в примере.</span><span class="sxs-lookup"><span data-stu-id="f5998-117">A class can be both a default source interface and a default Vtable source interface as shown in the example.</span></span> <span data-ttu-id="f5998-118">В этом случае приемник уведомлений должен использовать IID \_ IDISPATCH для получения событий диспетчеризации и использовать идентификатор интерфейса для получения событий vtable.</span><span class="sxs-lookup"><span data-stu-id="f5998-118">In this case an advise sink should use IID\_IDISPATCH to receive dispatch events and use the interface identifier to receive Vtable events.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="f5998-119">Представление типефлаг</span><span class="sxs-lookup"><span data-stu-id="f5998-119">Typeflag Representation</span></span>

<span data-ttu-id="f5998-120">Присутствие ИМПЛТИПЕФЛАГ \_ фдефаултвтабле.</span><span class="sxs-lookup"><span data-stu-id="f5998-120">The presence of IMPLTYPEFLAG\_FDEFAULTVTABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="f5998-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="f5998-121">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget] HRESULT Backcolor([out, retval] long *Value);
    [propput] HRESULT Backcolor([in] long Value);
    [propget] HRESULT Name([out, retval] BSTR *Value);
    [propput] HRESULT Name([in] BSTR Value);}

[
    dual,
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    restricted
]
interface IFormEvents: IDispatch
{
    HRESULT Click();
    HRESULT Resize();}

    [
        uuid(1e123456-1f3c-1069-996b-123456789ABC)
    ]
    coclass Form
    {
        [default] interface IForm;
        [default, defaultvtable, source] interface IFormEvents;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="f5998-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5998-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5998-123">**кокласс**</span><span class="sxs-lookup"><span data-stu-id="f5998-123">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="f5998-124">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="f5998-124">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="f5998-125">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="f5998-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="f5998-126">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="f5998-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="f5998-127">**источника**</span><span class="sxs-lookup"><span data-stu-id="f5998-127">**source**</span></span>](source.md)
</dt> <dt>

[<span data-ttu-id="f5998-128">**UUID**</span><span class="sxs-lookup"><span data-stu-id="f5998-128">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 