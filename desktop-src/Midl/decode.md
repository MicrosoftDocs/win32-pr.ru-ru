---
title: атрибут декодирования
description: Атрибут \ декодирование \ ACF указывает, что для процедуры или типа требуется поддержка отмены сериализации.
ms.assetid: 78cd855f-6731-4ef8-9097-e8da5a9b3bdc
keywords:
- декодирование атрибута MIDL
topic_type:
- apiref
api_name:
- decode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca24b3a601b9fcafd8d78a0194b6b986813f38c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337169"
---
# <a name="decode-attribute"></a><span data-ttu-id="b6e9a-104">атрибут декодирования</span><span class="sxs-lookup"><span data-stu-id="b6e9a-104">decode attribute</span></span>

<span data-ttu-id="b6e9a-105">Атрибут **\[ декодирования \]** ACF указывает, что для процедуры или типа требуется поддержка отмены сериализации.</span><span class="sxs-lookup"><span data-stu-id="b6e9a-105">The **\[decode\]** ACF attribute specifies that a procedure or a type needs de-serialization support.</span></span>

``` syntax
[ 
    decode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ decode [ , op-attribute-list] ] proc-name(...);

typedef [decode [ , type-attribute-list] ] type-name;
```

## <a name="parameters"></a><span data-ttu-id="b6e9a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6e9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6e9a-107">*Interface-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="b6e9a-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b6e9a-108">Указывает другие атрибуты, применяемые к интерфейсу в целом.</span><span class="sxs-lookup"><span data-stu-id="b6e9a-108">Specifies other attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="b6e9a-109">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="b6e9a-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b6e9a-110">Указывает имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b6e9a-110">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="b6e9a-111">*определение интерфейса*</span><span class="sxs-lookup"><span data-stu-id="b6e9a-111">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="b6e9a-112">Задает инструкции IDL, которые формируют определение интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b6e9a-112">Specifies IDL statements which form the definition of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="b6e9a-113">*Список атрибутов Op*</span><span class="sxs-lookup"><span data-stu-id="b6e9a-113">*op-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b6e9a-114">Указывает другие операционные атрибуты, которые применяются к процедуре, такой как **\[** [**кодирование**](encode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="b6e9a-114">Specifies other operational attributes that apply to the procedure such as **\[**[**encode**](encode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="b6e9a-115">*имя процесса*</span><span class="sxs-lookup"><span data-stu-id="b6e9a-115">*proc-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b6e9a-116">Указывает имя процедуры.</span><span class="sxs-lookup"><span data-stu-id="b6e9a-116">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="b6e9a-117">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="b6e9a-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b6e9a-118">Задает другие атрибуты, такие как **\[** [**кодирование**](encode.md) **\]** и **\[** [**выделение**](allocate.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="b6e9a-118">Specifies other attributes such as **\[**[**encode**](encode.md)**\]** and **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="b6e9a-119">*имя типа*</span><span class="sxs-lookup"><span data-stu-id="b6e9a-119">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b6e9a-120">Указывает тип, определенный в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="b6e9a-120">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6e9a-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6e9a-121">Remarks</span></span>

<span data-ttu-id="b6e9a-122">Атрибут **\[ декодирования \]** заставляет компилятор MIDL создавать код, который приложение может использовать для получения сериализованных данных из буфера.</span><span class="sxs-lookup"><span data-stu-id="b6e9a-122">The **\[decode\]** attribute causes the MIDL compiler to generate code that an application can use to retrieve serialized data from a buffer.</span></span> <span data-ttu-id="b6e9a-123">Атрибут **\[** [**Encoded**](encode.md) **\]** обеспечивает поддержку сериализации, создавая код для сериализации данных в буфер.</span><span class="sxs-lookup"><span data-stu-id="b6e9a-123">The **\[**[**encode**](encode.md)**\]** attribute provides serialization support, generating the code to serialize data into a buffer.</span></span>

<span data-ttu-id="b6e9a-124">Используйте атрибуты **\[** [**кодирования**](encode.md) **\]** и **\[ декодирования \]** в ACF, чтобы создать код СЕРИАЛИЗАЦИИ для процедур или типов, определенных в IDL-файле интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b6e9a-124">Use the **\[**[**encode**](encode.md)**\]** and **\[decode\]** attributes in an ACF to generate serialization code for procedures or types defined in the IDL file of an interface.</span></span> <span data-ttu-id="b6e9a-125">При использовании в качестве атрибута интерфейса **\[ декодирование \]** применяется ко всем типам и процедурам, определенным в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="b6e9a-125">When used as an interface attribute, **\[decode\]** applies to all types and procedures defined in the IDL file.</span></span> <span data-ttu-id="b6e9a-126">При использовании в качестве атрибута типа **\[ декодирование \]** применяется только к указанному типу.</span><span class="sxs-lookup"><span data-stu-id="b6e9a-126">When used as a type attribute, **\[decode\]** applies only to the specified type.</span></span> <span data-ttu-id="b6e9a-127">При использовании в качестве рабочего атрибута **\[ декодирование \]** применяется только к этой процедуре.</span><span class="sxs-lookup"><span data-stu-id="b6e9a-127">When used as an operational attribute, **\[decode\]** applies only to that procedure.</span></span>

<span data-ttu-id="b6e9a-128">Дополнительные сведения об использовании этой поддержки сериализации см. в разделе [службы сериализации](/windows/desktop/Rpc/serialization-services) и **\[** [**кодирование**](encode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="b6e9a-128">For more information about using this serialization support, see [Serialization Services](/windows/desktop/Rpc/serialization-services) and **\[**[**encode**](encode.md)**\]**.</span></span>

## <a name="see-also"></a><span data-ttu-id="b6e9a-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6e9a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6e9a-130">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="b6e9a-130">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="b6e9a-131">**allocate**</span><span class="sxs-lookup"><span data-stu-id="b6e9a-131">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="b6e9a-132">**шифровать**</span><span class="sxs-lookup"><span data-stu-id="b6e9a-132">**encode**</span></span>](encode.md)
</dt> </dl>

 

 