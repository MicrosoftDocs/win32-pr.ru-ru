---
title: закодировать атрибут
description: Атрибут \ Encoded \ ACF указывает, что для процедуры или типа данных требуется поддержка сериализации.
ms.assetid: 2661021d-8a26-4216-935b-ca40b6f8b9ec
keywords:
- кодирование атрибута MIDL
topic_type:
- apiref
api_name:
- encode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2a35c6d6910229a9e14026f6727db5c3176050
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987390"
---
# <a name="encode-attribute"></a><span data-ttu-id="22ad1-104">закодировать атрибут</span><span class="sxs-lookup"><span data-stu-id="22ad1-104">encode attribute</span></span>

<span data-ttu-id="22ad1-105">Атрибут **\[ Encoded \]** ACF указывает, что для процедуры или типа данных требуется поддержка сериализации.</span><span class="sxs-lookup"><span data-stu-id="22ad1-105">The **\[encode\]** ACF attribute specifies that a procedure or a data type needs serialization support.</span></span>

``` syntax
[ 
    encode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ encode [ , op-attribute-list] ] proc-name

typedef [encode [ , type-attribute-list] ] type-name
```

## <a name="parameters"></a><span data-ttu-id="22ad1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="22ad1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22ad1-107">*Interface-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="22ad1-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="22ad1-108">Указывает другие атрибуты, применяемые к интерфейсу в целом.</span><span class="sxs-lookup"><span data-stu-id="22ad1-108">Specifies other attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="22ad1-109">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="22ad1-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="22ad1-110">Указывает имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="22ad1-110">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="22ad1-111">*определение интерфейса*</span><span class="sxs-lookup"><span data-stu-id="22ad1-111">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="22ad1-112">Задает инструкции IDL, которые формируют определение интерфейса.</span><span class="sxs-lookup"><span data-stu-id="22ad1-112">Specifies IDL statements which form the definition of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="22ad1-113">*Список атрибутов Op*</span><span class="sxs-lookup"><span data-stu-id="22ad1-113">*op-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="22ad1-114">Указывает другие операционные атрибуты, которые применяются к такой процедуре, как **\[** [**декодирование**](decode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="22ad1-114">Specifies other operational attributes that apply to the procedure such as **\[**[**decode**](decode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="22ad1-115">*имя процесса*</span><span class="sxs-lookup"><span data-stu-id="22ad1-115">*proc-name*</span></span> 
</dt> <dd>

<span data-ttu-id="22ad1-116">Указывает имя процедуры.</span><span class="sxs-lookup"><span data-stu-id="22ad1-116">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="22ad1-117">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="22ad1-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="22ad1-118">Задает другие атрибуты, применяемые к типу, например **\[** [**декодированию**](decode.md) **\]** и **\[** [**выделению**](allocate.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="22ad1-118">Specifies other attributes that apply to the type such as **\[**[**decode**](decode.md)**\]** and **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="22ad1-119">*имя типа*</span><span class="sxs-lookup"><span data-stu-id="22ad1-119">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="22ad1-120">Указывает тип, определенный в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="22ad1-120">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22ad1-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="22ad1-121">Remarks</span></span>

<span data-ttu-id="22ad1-122">Атрибут **\[ Encoded \]** заставляет компилятор MIDL создавать код, который приложение может использовать для сериализации данных в буфер.</span><span class="sxs-lookup"><span data-stu-id="22ad1-122">The **\[encode\]** attribute causes the MIDL compiler to generate code that an application can use to serialize data into a buffer.</span></span> <span data-ttu-id="22ad1-123">Атрибут **\[** [**декодирования**](decode.md) **\]** создает код для распаковки данных из буфера.</span><span class="sxs-lookup"><span data-stu-id="22ad1-123">The **\[**[**decode**](decode.md)**\]** attribute generates the code for unmarshaling data from a buffer.</span></span>

<span data-ttu-id="22ad1-124">Используйте атрибуты **\[ кодирования \]** и **\[** [**декодирования**](decode.md) **\]** в ACF, чтобы создать код СЕРИАЛИЗАЦИИ для процедур или типов, определенных в IDL-файле интерфейса.</span><span class="sxs-lookup"><span data-stu-id="22ad1-124">Use the **\[encode\]** and **\[**[**decode**](decode.md)**\]** attributes in an ACF to generate serialization code for procedures or types defined in the IDL file of an interface.</span></span> <span data-ttu-id="22ad1-125">При использовании в качестве атрибута интерфейса **\[ кодировка \]** применяется ко всем типам и процедурам, определенным в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="22ad1-125">When used as an interface attribute, **\[encode\]** applies to all the types and procedures defined in the IDL file.</span></span> <span data-ttu-id="22ad1-126">При использовании в качестве рабочего атрибута **\[ кодировка \]** применяется только к указанной процедуре.</span><span class="sxs-lookup"><span data-stu-id="22ad1-126">When used as an operational attribute, **\[encode\]** applies only to the specified procedure.</span></span> <span data-ttu-id="22ad1-127">При использовании в качестве атрибута типа **\[ кодировка \]** применяется только к указанному типу.</span><span class="sxs-lookup"><span data-stu-id="22ad1-127">When used as a type attribute, **\[encode\]** applies only to the specified type.</span></span>

<span data-ttu-id="22ad1-128">Когда к процедуре применяется атрибут **\[ Encoded \]** или **\[** [**дешифровки**](decode.md) **\]** , компилятор MIDL создает заглушку сериализации таким же образом, как удаленные заглушки создаются для удаленных подпрограмм.</span><span class="sxs-lookup"><span data-stu-id="22ad1-128">When the **\[encode\]** or **\[**[**decode**](decode.md)**\]** attribute is applied to a procedure, the MIDL compiler generates a serialization stub in a similar fashion as remote stubs are generated for remote routines.</span></span> <span data-ttu-id="22ad1-129">Процедура может быть либо удаленной, либо процедурой сериализации, но не может быть одновременно.</span><span class="sxs-lookup"><span data-stu-id="22ad1-129">A procedure can be either a remote or a serializing procedure, but it cannot be both.</span></span> <span data-ttu-id="22ad1-130">Прототип созданной подпрограммы отправляется в ЗАГЛУШКу. H-файл, когда заглушка перемещается в файл ЗАГЛУШКи \_ c. c.</span><span class="sxs-lookup"><span data-stu-id="22ad1-130">The prototype of the generated routine is sent to the STUB.H file while the stub itself goes into the STUB\_C.C file.</span></span>

<span data-ttu-id="22ad1-131">Компилятор MIDL создает две функции для каждого типа, к которому применяется атрибут **\[ \] кодирования** , и одну дополнительную функцию для каждого типа, **\[** к которому применяется атрибут [**декодирования**](decode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="22ad1-131">The MIDL compiler generates two functions for each type the **\[encode\]** attribute applies to, and one additional function for each type the **\[**[**decode**](decode.md)**\]** attribute applies to.</span></span> <span data-ttu-id="22ad1-132">Например, для определяемого пользователем типа с именем MyType компилятор создает код для \_ функций шифрования MyType, MyType \_ и MyType \_ алигнсизе.</span><span class="sxs-lookup"><span data-stu-id="22ad1-132">For example, for a user-defined type named MyType, the compiler generates code for the MyType\_Encode, MyType\_Decode, and MyType\_AlignSize functions.</span></span> <span data-ttu-id="22ad1-133">Для этих функций компилятор записывает прототипы в ЗАГЛУШКу. H и исходный код для ЗАГЛУШЕК \_ к.к.</span><span class="sxs-lookup"><span data-stu-id="22ad1-133">For these functions, the compiler writes prototypes to STUB.H and source code to STUB\_C.C.</span></span>

<span data-ttu-id="22ad1-134">Дополнительные сведения о дескрипторах сериализации и кодировании или декодировании данных см. в разделе [службы сериализации](/windows/desktop/Rpc/serialization-services).</span><span class="sxs-lookup"><span data-stu-id="22ad1-134">For additional information about serialization handles and encoding or decoding data, see [Serialization Services](/windows/desktop/Rpc/serialization-services).</span></span>

## <a name="examples"></a><span data-ttu-id="22ad1-135">Примеры</span><span class="sxs-lookup"><span data-stu-id="22ad1-135">Examples</span></span>

``` syntax
/* 
    ACF file example; 
    Assumes MyType1, MyType2, MyType3, MyProc1, MyProc2, MyProc3 defined 
    in IDL file  
    MyType1, MyType2, MyProc1, MyProc2 have encode and decode 
    serialization support 
    MyType3 and MyProc3 have encode serialization support only 
*/ 
[ 
    encode, 
    implicit_handle(handle_t bh) 
]    
interface regress 
{ 
    typedef [ decode ] MyType1; 
    typedef [ encode, decode ] MyType2; 
    [ decode ] MyProcc1(); 
    [ encode ] MyProc2(); 
}
```

## <a name="see-also"></a><span data-ttu-id="22ad1-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22ad1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22ad1-137">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="22ad1-137">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="22ad1-138">**allocate**</span><span class="sxs-lookup"><span data-stu-id="22ad1-138">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="22ad1-139">**декодировать**</span><span class="sxs-lookup"><span data-stu-id="22ad1-139">**decode**</span></span>](decode.md)
</dt> </dl>

 

 