---
title: атрибут comm_status
description: Атрибут \ " \_ состояние связи \ ACF \" приводит к возвращению кода ошибки при возникновении ошибки взаимодействия во время выполнения функции.
ms.assetid: 3ea9ce62-8bd4-40fe-b838-bfebd52b5a15
keywords:
- comm_status атрибута MIDL
topic_type:
- apiref
api_name:
- comm_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4952d03a80dbbffb135043d024b0c0eb18966f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784314"
---
# <a name="comm_status-attribute"></a><span data-ttu-id="d9a6a-104">\_атрибут состояния связи</span><span class="sxs-lookup"><span data-stu-id="d9a6a-104">comm\_status attribute</span></span>

<span data-ttu-id="d9a6a-105">Если во время выполнения функции возникла ошибка связи, то в атрибуте ACF **\[ \_ Status \]** появляется код ошибки.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-105">The **\[comm\_status\]** ACF attribute causes an error code to be returned when a communication error occurs during the execution of a function.</span></span>

``` syntax
[comm_status [ , ACF-function-attributes ] ] 
    error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [comm_status [ , ACF-parameter-attributes ] ] error_status_t name
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="d9a6a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9a6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9a6a-107">*ACF-Function-Attributes*</span><span class="sxs-lookup"><span data-stu-id="d9a6a-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="d9a6a-108">Указывает ноль или более атрибутов функции ACF, таких как **\[ \_ состояние \]** связи и **\[** [**код**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="d9a6a-108">Specifies zero or more ACF function attributes, such as **\[comm\_status\]** and **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="d9a6a-109">Атрибуты функции заключаются в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="d9a6a-110">К функции можно применить ноль или более атрибутов.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-110">Zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="d9a6a-111">Несколько атрибутов функции разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-111">Separate multiple function attributes with commas.</span></span> <span data-ttu-id="d9a6a-112">Обратите внимание, что если **\[ \_ состояние \]** связи отображается как атрибут функции, оно не может также отображаться в качестве атрибута параметра.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-112">Note that if **\[comm\_status\]** appears as a function attribute, it cannot also appear as a parameter attribute.</span></span>

</dd> <dt>

<span data-ttu-id="d9a6a-113">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="d9a6a-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d9a6a-114">Указывает имя функции, определенное в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-114">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="d9a6a-115">*ACF-Parameter-Attributes*</span><span class="sxs-lookup"><span data-stu-id="d9a6a-115">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="d9a6a-116">Задает атрибуты, которые применяются к параметру.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-116">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="d9a6a-117">Обратите внимание, что к параметру можно применить ноль, один или несколько атрибутов.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-117">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="d9a6a-118">Несколько атрибутов параметров разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-118">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="d9a6a-119">Атрибуты параметров заключаются в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-119">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="d9a6a-120">Атрибуты параметров IDL, такие как атрибуты направления, не допускаются в ACF.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-120">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span> <span data-ttu-id="d9a6a-121">Обратите внимание, что если **\[ \_ состояние \]** связи отображается как атрибут параметра, он также не может использоваться в качестве атрибута функции.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-121">Note that if **\[comm\_status\]** appears as a parameter attribute, it cannot also appear as a function attribute.</span></span>

</dd> <dt>

<span data-ttu-id="d9a6a-122">*имя параметра*</span><span class="sxs-lookup"><span data-stu-id="d9a6a-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d9a6a-123">Задает параметр для функции, как определено в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-123">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="d9a6a-124">Каждый параметр функции должен быть указан в одной и той же последовательности, используя то же имя, которое определено в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-124">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9a6a-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9a6a-125">Remarks</span></span>

<span data-ttu-id="d9a6a-126">Атрибут **\[ \_ состояния \]** связи может использоваться как атрибут функции или как атрибут параметра, но он может использоваться только один раз для каждой функции.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-126">The **\[comm\_status\]** attribute can be used as either a function attribute or as a parameter attribute, but it can appear only once per function.</span></span> <span data-ttu-id="d9a6a-127">Его можно применить либо к функции, либо к одному параметру в каждой функции.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-127">It can be applied either to the function or to one parameter in each function.</span></span>

<span data-ttu-id="d9a6a-128">Атрибут **\[ \_ состояния \]** связи может применяться только к функциям, которые возвращают [**состояние ошибки \_ \_ t**](error-status-t.md).</span><span class="sxs-lookup"><span data-stu-id="d9a6a-128">The **\[comm\_status\]** attribute can be applied only to functions that return the type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="d9a6a-129">При возникновении ошибки связи во время выполнения функции возвращается код ошибки.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-129">When a communication error occurs during the execution of the function, an error code is returned.</span></span>

<span data-ttu-id="d9a6a-130">Если в качестве атрибута параметра используется **\[ \_ \] состояние** связи, параметр должен быть определен в IDL-файле и должен быть **\[** [**выходным**](out-idl.md) **\]** параметром типа [**\_ Status ошибки \_ t**](error-status-t.md).</span><span class="sxs-lookup"><span data-stu-id="d9a6a-130">When **\[comm\_status\]** is used as a parameter attribute, the parameter must be defined in the IDL file and must be an **\[**[**out**](out-idl.md)**\]** parameter of type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="d9a6a-131">При возникновении ошибки связи во время выполнения функции для параметра задается код ошибки.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-131">When a communication error occurs during the execution of the function, the parameter is set to the error code.</span></span> <span data-ttu-id="d9a6a-132">После успешного завершения удаленного вызова процедура задает значение.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-132">When the remote call is completed successfully, the procedure sets the value.</span></span>

<span data-ttu-id="d9a6a-133">Атрибуты состояния и состояния взаимосвязи могут отображаться **\[ в одной функции либо как атрибуты функции, либо как атрибуты параметров. \_ \]** **\[** [**\_**](fault-status.md) **\]**</span><span class="sxs-lookup"><span data-stu-id="d9a6a-133">It is possible for both the **\[comm\_status\]** and **\[**[**fault\_status**](fault-status.md)**\]** attributes to appear in a single function, either as function attributes or parameter attributes.</span></span> <span data-ttu-id="d9a6a-134">Если оба атрибута являются атрибутами функций или они применяются к одному и тому же параметру и не возникают ошибки, то функция или параметр имеют значение **\_ состояние ошибки \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-134">If both attributes are function attributes or if they apply to the same parameter and no error occurs, the function or parameter has the value **error\_status\_ok**.</span></span> <span data-ttu-id="d9a6a-135">В противном случае он будет содержать соответствующее **\[ \_ состояние \]** связи или значение **\[ \_ состояния \] сбоя** .</span><span class="sxs-lookup"><span data-stu-id="d9a6a-135">Otherwise, it contains the appropriate **\[comm\_status\]** or **\[fault\_status\]** value.</span></span> <span data-ttu-id="d9a6a-136">Так как значения, возвращаемые для **\[ \_ состояния \]** связи, отличаются от значений, возвращаемых для **\[ \_ состояния \] сбоя**, возвращаемые значения легко интерпретировать.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-136">Because values returned for **\[comm\_status\]** are different from the values returned for **\[fault\_status\]**, the returned values are readily interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="d9a6a-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9a6a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9a6a-138">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="d9a6a-138">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="d9a6a-139">**\_состояние ошибки \_ t**</span><span class="sxs-lookup"><span data-stu-id="d9a6a-139">**error\_status\_t**</span></span>](error-status-t.md)
</dt> <dt>

[<span data-ttu-id="d9a6a-140">**\_состояние сбоя**</span><span class="sxs-lookup"><span data-stu-id="d9a6a-140">**fault\_status**</span></span>](fault-status.md)
</dt> <dt>

[<span data-ttu-id="d9a6a-141">**nocode**</span><span class="sxs-lookup"><span data-stu-id="d9a6a-141">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="d9a6a-142">**заполняет**</span><span class="sxs-lookup"><span data-stu-id="d9a6a-142">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 




