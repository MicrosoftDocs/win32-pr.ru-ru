---
title: атрибут прокси-сервера
description: Атрибут \ proxy \ предотвращает регистрацию автоматизации в качестве обработчика прокси-сервера или заглушки для сдвоенного интерфейса.
ms.assetid: 88e59938-83c9-436a-931c-f4396fdcf653
keywords:
- прокси-атрибут MIDL
topic_type:
- apiref
api_name:
- proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa8c9d305b7f51a012ae26d7b1a76d2e3011fd7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487541"
---
# <a name="proxy-attribute"></a><span data-ttu-id="f6fd5-104">атрибут прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="f6fd5-104">proxy attribute</span></span>

<span data-ttu-id="f6fd5-105">Атрибут **\[ Proxy \]** предотвращает регистрацию автоматизации в качестве обработчика прокси-сервера или заглушки для сдвоенного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f6fd5-105">The **\[proxy\]** attribute prevents Automation from registering as a proxy/stub handler for a dual interface.</span></span>

``` syntax
[ 
    proxy, 
    uuid(string-uuid <>)
    [ , interface-attribute-list <>] 
] 
interface interface-name <> : base-interface <>
{
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="f6fd5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6fd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6fd5-107">*Строка UUID*</span><span class="sxs-lookup"><span data-stu-id="f6fd5-107">*string-uuid*</span></span> 
</dt> <dd>

<span data-ttu-id="f6fd5-108">Задает строку, состоящую из 8 шестнадцатеричных цифр, за которыми следует дефис, затем три группы из четырех шестнадцатеричных цифр, за которыми следует дефис, а затем 12 шестнадцатеричных цифр.</span><span class="sxs-lookup"><span data-stu-id="f6fd5-108">Specifies a string consisting of 8 hexadecimal digits followed by a hyphen, then three groups of 4 hexadecimal digits each followed by a hyphen, then 12 hexadecimal digits.</span></span> <span data-ttu-id="f6fd5-109">Строку UUID можно заключать в кавычки, за исключением случаев, когда используется параметр компилятора MIDL [**/ОСФ**](-osf.md).</span><span class="sxs-lookup"><span data-stu-id="f6fd5-109">You can enclose the UUID string in quotes, except when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6fd5-110">*Interface-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="f6fd5-110">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f6fd5-111">Задает список из нуля или нескольких атрибутов IDL, которые применяются к интерфейсу в целом.</span><span class="sxs-lookup"><span data-stu-id="f6fd5-111">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="f6fd5-112">При наличии двух или более атрибутов интерфейса они должны быть разделены запятыми.</span><span class="sxs-lookup"><span data-stu-id="f6fd5-112">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="f6fd5-113">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="f6fd5-113">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f6fd5-114">Имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f6fd5-114">Name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="f6fd5-115">*базовый интерфейс*</span><span class="sxs-lookup"><span data-stu-id="f6fd5-115">*base-interface*</span></span> 
</dt> <dd>

<span data-ttu-id="f6fd5-116">Указывает имя интерфейса, от которого этот производный интерфейс наследует функции члена, коды состояния и атрибуты интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f6fd5-116">Specifies the name of an interface from which this derived interface inherits member functions, status codes, and interface attributes.</span></span> <span data-ttu-id="f6fd5-117">Производный интерфейс не наследует определения типов.</span><span class="sxs-lookup"><span data-stu-id="f6fd5-117">The derived interface does not inherit type definitions.</span></span> <span data-ttu-id="f6fd5-118">Для этого используйте ключевое слово [**Import**](import.md) , чтобы импортировать idl-файл базового интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f6fd5-118">To do this, use the [**import**](import.md) keyword to import the IDL file of the base interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6fd5-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6fd5-119">Remarks</span></span>

<span data-ttu-id="f6fd5-120">Использование атрибута \[ **proxy** \] для сдвоенного интерфейса предотвращает создание TLB созданных заглушек.</span><span class="sxs-lookup"><span data-stu-id="f6fd5-120">Using the \[ **proxy**\] attribute for a dual interface prevents the TLB from taking over generated stubs.</span></span> <span data-ttu-id="f6fd5-121">Если этот атрибут указан, не следует отменять регистрацию прокси-сервера typelib при отмене регистрации библиотеки типов.</span><span class="sxs-lookup"><span data-stu-id="f6fd5-121">If this attribute is specified, the typelib proxy should not be unregistered when the typelib is unregistered.</span></span>

### <a name="flags"></a><span data-ttu-id="f6fd5-122">Флаги</span><span class="sxs-lookup"><span data-stu-id="f6fd5-122">Flags</span></span>

<dl> <dt>

<span data-ttu-id="f6fd5-123"><span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>\_прокси-сервер типефлаг</span><span class="sxs-lookup"><span data-stu-id="f6fd5-123"><span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>TYPEFLAG\_PROXY</span></span>
</dt> <dd>

<span data-ttu-id="f6fd5-124">Интерфейсы можно пометить с помощью \_ флага прокси-сервера типефлаг, чтобы указать, что они будут использовать библиотеку динамической компоновки прокси или заглушки.</span><span class="sxs-lookup"><span data-stu-id="f6fd5-124">Interfaces can be marked with the TYPEFLAG\_PROXY flag to indicate they will be using a proxy/stub dynamic link library.</span></span> <span data-ttu-id="f6fd5-125">Этот флаг указывает, что не следует отменять регистрацию прокси-сервера typelib при отмене регистрации библиотеки типов.</span><span class="sxs-lookup"><span data-stu-id="f6fd5-125">This flag specifies the typelib proxy should not be unregistered when the typelib is unregistered.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="f6fd5-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6fd5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6fd5-127">**Создание библиотеки типов с помощью MIDL**</span><span class="sxs-lookup"><span data-stu-id="f6fd5-127">**Generating a Type Library with MIDL**</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="f6fd5-128">**двойной**</span><span class="sxs-lookup"><span data-stu-id="f6fd5-128">**dual**</span></span>](dual.md)
</dt> <dt>

[<span data-ttu-id="f6fd5-129">**типефлагс**</span><span class="sxs-lookup"><span data-stu-id="f6fd5-129">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 