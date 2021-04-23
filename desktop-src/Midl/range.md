---
title: range - атрибут
description: Атрибут \ Range \ позволяет указать диапазон допустимых значений для аргументов или полей, значения которых задаются во время выполнения. При использовании с типом канала атрибут указывает допустимый диапазон для количества элементов в фрагментах канала.
ms.assetid: 1609fea5-e82c-4389-b4f4-2cd8d0622cde
keywords:
- атрибут Range MIDL
topic_type:
- apiref
api_name:
- range
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e095d420afc433c1f01a63dff51868e57efc50f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105661691"
---
# <a name="range-attribute"></a><span data-ttu-id="6d472-105">range - атрибут</span><span class="sxs-lookup"><span data-stu-id="6d472-105">range attribute</span></span>

<span data-ttu-id="6d472-106">Атрибут **\[ Range \]** позволяет указать диапазон допустимых значений для аргументов или полей, значения которых задаются во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="6d472-106">The **\[range\]** attribute lets you specify a range of allowable values for arguments or fields whose values are set at run time.</span></span> <span data-ttu-id="6d472-107">При использовании с типом канала атрибут указывает допустимый диапазон для количества элементов в фрагментах канала.</span><span class="sxs-lookup"><span data-stu-id="6d472-107">When used with a pipe type, the attribute specifies the allowable range for the count of elements in the pipe chunks.</span></span>

``` syntax
[range(low-val,high-val)] type-specifier declarator
```

## <a name="parameters"></a><span data-ttu-id="6d472-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d472-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d472-109">*Low-Val*</span><span class="sxs-lookup"><span data-stu-id="6d472-109">*low-val*</span></span> 
</dt> <dd>

<span data-ttu-id="6d472-110">Наименьшее допустимое значение, которое может храниться в параметре или поле.</span><span class="sxs-lookup"><span data-stu-id="6d472-110">The lowest allowable value that the parameter or field can hold.</span></span>

</dd> <dt>

<span data-ttu-id="6d472-111">*Функция High-Val*</span><span class="sxs-lookup"><span data-stu-id="6d472-111">*high-val*</span></span> 
</dt> <dd>

<span data-ttu-id="6d472-112">Наибольшее допустимое значение, которое может храниться в параметре или поле.</span><span class="sxs-lookup"><span data-stu-id="6d472-112">The highest allowable value that the parameter or field can hold.</span></span>

</dd> <dt>

<span data-ttu-id="6d472-113">*Описатель типа*</span><span class="sxs-lookup"><span data-stu-id="6d472-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="6d472-114">Целочисленный тип, отличный от [**Hyper**](hyper.md) или [**\_ \_ Int64**](--int64.md), идентификатор типа для целочисленного типа, тип [**перечисления**](enum.md) или имя типа канала.</span><span class="sxs-lookup"><span data-stu-id="6d472-114">An integral type other than [**hyper**](hyper.md) or [**\_\_int64**](--int64.md), a type identifier to an integral type, an [**enum**](enum.md) type, or a pipe type name.</span></span>

</dd> <dt>

<span data-ttu-id="6d472-115">*declarator*</span><span class="sxs-lookup"><span data-stu-id="6d472-115">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="6d472-116">Стандартный декларатор C, например идентификатор.</span><span class="sxs-lookup"><span data-stu-id="6d472-116">A standard C declarator, such as an identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d472-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d472-117">Remarks</span></span>

<span data-ttu-id="6d472-118">Используйте атрибут **\[ Range \]** , чтобы изменить значение конфиденциальных параметров или полей, например, используемых для размера или длины с помощью согласованных или изменяемых массивов, или всякий раз, когда требуется проверить значение параметра или поля в диапазоне допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="6d472-118">Use the **\[range\]** attribute to modify the meaning of sensitive parameters or fields, such as those used for size or length, with conformant or varying arrays; or whenever you want to check a parameter or field value against a range of valid values.</span></span> <span data-ttu-id="6d472-119">Атрибут применим к параметрам верхнего уровня, а также к параметрам и полям более низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="6d472-119">The attribute is applicable to top-level parameters as well as lower-level parameters and fields.</span></span> <span data-ttu-id="6d472-120">Добавление атрибута **\[ Range \]** к типу не приводит к изменению его формата связи, поэтому не влияет на обратную совместимость.</span><span class="sxs-lookup"><span data-stu-id="6d472-120">Adding the **\[range\]** attribute to a type does not change its wire format, thus does not affect backward compatibility.</span></span>

<span data-ttu-id="6d472-121">Атрибут **\[ Range \]** можно также использовать для согласованных данных, таких как буферы или массивы, с атрибутом соответствия.</span><span class="sxs-lookup"><span data-stu-id="6d472-121">The **\[range\]** attribute can also be used on conformant data such as buffers or arrays with a conformance attribute.</span></span> <span data-ttu-id="6d472-122">Результатом является ограничение всех размеров соответствия для согласованных данных в указанный диапазон.</span><span class="sxs-lookup"><span data-stu-id="6d472-122">The effect is to limit all conformance sizes for the conformant data to the specified range.</span></span> <span data-ttu-id="6d472-123">Если согласованные данные являются многомерным массивом, каждое измерение массива ограничено указанным диапазоном.</span><span class="sxs-lookup"><span data-stu-id="6d472-123">If the conformant data is a multi-dimensional array, each array dimension is limited to the specified range.</span></span>

<span data-ttu-id="6d472-124">Использование **\[ диапазона \]** для согласованных данных требует, чтобы целевой объект компиляции был "целевой NT60 или выше.</span><span class="sxs-lookup"><span data-stu-id="6d472-124">Use of **\[range\]** on conformant data requires that the compilation target be â€“target NT60 or higher.</span></span>

<span data-ttu-id="6d472-125">Обратите внимание, что при компиляции IDL-файла необходимо использовать параметр компилятора [**/robust**](-robust.md) , чтобы создать код заглушки, который выполняет эти проверки.</span><span class="sxs-lookup"><span data-stu-id="6d472-125">Note that you must use the [**/robust**](-robust.md) compiler option when you compile your IDL file in order to generate the stub code that will perform these checks.</span></span> <span data-ttu-id="6d472-126">Без параметра **/robust** компилятор MIDL игнорирует этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="6d472-126">Without the **/robust** switch, the MIDL compiler ignores this attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="6d472-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="6d472-127">Examples</span></span>

``` syntax
HRESULT Method1(
    [in, range(0,100)] ULONG m,
    [in, range(0,100)] ULONG n,
    [size_is(m,n)] ULONG **pplong);

void InPipe(
    [in, range(0, MAX_CHUNK) LONG_PIPE pipe_date);
```

## <a name="see-also"></a><span data-ttu-id="6d472-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d472-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d472-129">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="6d472-129">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="6d472-130">массивах</span><span class="sxs-lookup"><span data-stu-id="6d472-130">arrays</span></span>](/windows/desktop/Rpc/arrays)
</dt> <dt>

[<span data-ttu-id="6d472-131">**первый \_ —**</span><span class="sxs-lookup"><span data-stu-id="6d472-131">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="6d472-132">**Последний \_ —**</span><span class="sxs-lookup"><span data-stu-id="6d472-132">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="6d472-133">**Длина \_ равна**</span><span class="sxs-lookup"><span data-stu-id="6d472-133">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="6d472-134">**Максимальное \_ число**</span><span class="sxs-lookup"><span data-stu-id="6d472-134">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="6d472-135">**/robust**</span><span class="sxs-lookup"><span data-stu-id="6d472-135">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="6d472-136">**размер \_ равен**</span><span class="sxs-lookup"><span data-stu-id="6d472-136">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="6d472-137">**параметр \_ имеет**</span><span class="sxs-lookup"><span data-stu-id="6d472-137">**switch\_is**</span></span>](switch-is.md)
</dt> </dl>

 

 