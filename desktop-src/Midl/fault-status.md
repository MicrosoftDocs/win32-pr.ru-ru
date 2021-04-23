---
title: атрибут fault_status
description: Атрибут \ Fault \_ Status \ ACF указывает, что код ошибки типа \_ Status ошибки \_ t указывает на сбой удаленной процедуры, а не на другие типы проблем, например ошибки связи.
ms.assetid: 9da7bd3d-cef0-4ad4-b2a4-3f8aa156e8e0
keywords:
- fault_status атрибута MIDL
topic_type:
- apiref
api_name:
- fault_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 134d9772e167fe63e133d569b9985a7735668d3c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783612"
---
# <a name="fault_status-attribute"></a><span data-ttu-id="55e67-104">\_атрибут состояния сбоя</span><span class="sxs-lookup"><span data-stu-id="55e67-104">fault\_status attribute</span></span>

<span data-ttu-id="55e67-105">Атрибут **\[ Fault \_ Status \]** ACF указывает, что код ошибки с типом [**Status ошибки \_ \_ t**](error-status-t.md) указывает на сбой удаленной процедуры, а не на другие типы проблем, например ошибки связи.</span><span class="sxs-lookup"><span data-stu-id="55e67-105">The **\[fault\_status\]** ACF attribute specifies that an error code of type [**error\_status\_t**](error-status-t.md) indicates a failure of the remote procedure, rather than other types of problems such as communication errors.</span></span>

``` syntax
[fault_status [ , ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] parameter-name
    , ... );

[ [ ACF-function-attributes ] ] function-name(
    [fault_status [ , ACF-parameter-attributes ] ] parameter-name
    , ... );
```

## <a name="parameters"></a><span data-ttu-id="55e67-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="55e67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55e67-107">*ACF-Function-Attributes*</span><span class="sxs-lookup"><span data-stu-id="55e67-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="55e67-108">Указывает ноль или более атрибутов функции ACF, таких как **\[ \_ состояние \] сбоя** и **\[** [**код**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="55e67-108">Specifies zero or more ACF function attributes such as **\[fault\_status\]** and **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="55e67-109">Атрибуты функции заключаются в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="55e67-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="55e67-110">Обратите внимание, что к функции можно применить ноль или более атрибутов.</span><span class="sxs-lookup"><span data-stu-id="55e67-110">Note that zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="55e67-111">Несколько атрибутов функции разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="55e67-111">Separate multiple function attributes with commas.</span></span> <span data-ttu-id="55e67-112">Также обратите внимание, что если **\[ \_ состояние \] ошибки** отображается как атрибут функции, он также не может использоваться в качестве атрибута параметра.</span><span class="sxs-lookup"><span data-stu-id="55e67-112">Also note that if **\[fault\_status\]** appears as a function attribute, it cannot also appear as a parameter attribute.</span></span>

</dd> <dt>

<span data-ttu-id="55e67-113">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="55e67-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="55e67-114">Указывает имя функции, определенное в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="55e67-114">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="55e67-115">*ACF-Parameter-Attributes*</span><span class="sxs-lookup"><span data-stu-id="55e67-115">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="55e67-116">Задает атрибуты, которые применяются к параметру.</span><span class="sxs-lookup"><span data-stu-id="55e67-116">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="55e67-117">Обратите внимание, что к параметру можно применить ноль или более атрибутов.</span><span class="sxs-lookup"><span data-stu-id="55e67-117">Note that zero or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="55e67-118">Атрибуты параметров заключаются в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="55e67-118">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="55e67-119">Несколько атрибутов параметров разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="55e67-119">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="55e67-120">Атрибуты параметров IDL, такие как атрибуты направления, не допускаются в ACF.</span><span class="sxs-lookup"><span data-stu-id="55e67-120">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span> <span data-ttu-id="55e67-121">Обратите внимание, что если **\[ \_ состояние \] ошибки** отображается как атрибут параметра, он также не может использоваться в качестве атрибута функции.</span><span class="sxs-lookup"><span data-stu-id="55e67-121">Note that if **\[fault\_status\]** appears as a parameter attribute, it cannot also appear as a function attribute.</span></span>

</dd> <dt>

<span data-ttu-id="55e67-122">*имя параметра*</span><span class="sxs-lookup"><span data-stu-id="55e67-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="55e67-123">Задает параметр для функции, как определено в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="55e67-123">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="55e67-124">Каждый параметр функции должен быть указан в одной и той же последовательности, используя то же имя, которое определено в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="55e67-124">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55e67-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55e67-125">Remarks</span></span>

<span data-ttu-id="55e67-126">Атрибут **\[ \_ состояния \] сбоя** может использоваться как атрибут функции или как атрибут параметра, но он может использоваться только один раз для каждой функции.</span><span class="sxs-lookup"><span data-stu-id="55e67-126">The **\[fault\_status\]** attribute can be used as either a function attribute or as a parameter attribute, but it can appear only once per function.</span></span> <span data-ttu-id="55e67-127">Его можно применить либо к самой функции, либо к одному параметру в каждой функции.</span><span class="sxs-lookup"><span data-stu-id="55e67-127">It can be applied either to the function itself or to one parameter in each function.</span></span>

<span data-ttu-id="55e67-128">Атрибут **\[ \_ состояния \] сбоя** может применяться только к функциям, которые возвращают [**состояние ошибки \_ типа \_ t**](error-status-t.md).</span><span class="sxs-lookup"><span data-stu-id="55e67-128">The **\[fault\_status\]** attribute can be applied only to functions that return the type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="55e67-129">При сбое удаленной процедуры, которая вызывает возвращение PDU сбоя, возвращается код ошибки.</span><span class="sxs-lookup"><span data-stu-id="55e67-129">When the remote procedure fails in a way that causes a fault PDU to be returned, an error code is returned.</span></span>

<span data-ttu-id="55e67-130">Если в качестве атрибута параметра используется **\[ \_ состояние \] сбоя** , параметр должен быть **\[** [**выходным**](out-idl.md) **\]** параметром типа [**\_ Status ошибки \_ t**](error-status-t.md).</span><span class="sxs-lookup"><span data-stu-id="55e67-130">When **\[fault\_status\]** is used as a parameter attribute, the parameter must be an **\[**[**out**](out-idl.md)**\]** parameter of type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="55e67-131">При возникновении ошибки сервера параметру присваивается код ошибки.</span><span class="sxs-lookup"><span data-stu-id="55e67-131">If a server error occurs, the parameter is set to the error code.</span></span> <span data-ttu-id="55e67-132">После успешного завершения удаленного вызова процедура задает значение.</span><span class="sxs-lookup"><span data-stu-id="55e67-132">When the remote call is successfully completed, the procedure sets the value.</span></span>

<span data-ttu-id="55e67-133">Параметр, связанный с атрибутом **\[ \_ состояния \] сбоя** , не обязательно должен быть указан в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="55e67-133">The parameter associated with the **\[fault\_status\]** attribute does not have to be specified in the IDL file.</span></span> <span data-ttu-id="55e67-134">Если параметр не указан, то новый [**выходной**](out-idl.md) параметр типа [**\_ Status ошибки \_ t**](error-status-t.md) создается после последнего параметра, определенного в IDL-файле устройства DCE.</span><span class="sxs-lookup"><span data-stu-id="55e67-134">When the parameter is not specified, a new [**out**](out-idl.md) parameter of type [**error\_status\_t**](error-status-t.md) is generated following the last parameter defined in the DCE IDL file.</span></span>

<span data-ttu-id="55e67-135">Атрибуты состояния **\[ сбоя \_ \]** и **\[** [**\_ состояния**](comm-status.md) взаимосвязи могут **\]** отображаться в одной функции либо как атрибуты функции, либо как атрибуты параметров.</span><span class="sxs-lookup"><span data-stu-id="55e67-135">It is possible for both the **\[fault\_status\]** and **\[**[**comm\_status**](comm-status.md)**\]** attributes to appear in a single function, either as function attributes or parameter attributes.</span></span> <span data-ttu-id="55e67-136">Если оба атрибута являются атрибутами функций или они применяются к одному и тому же параметру и не возникают ошибки, то функция или параметр имеют **значение \_ состояние ошибки \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="55e67-136">If both attributes are function attributes, or if they apply to the same parameter and no error occurs, the function or parameter has the value **error\_status\_ok**.</span></span> <span data-ttu-id="55e67-137">В противном случае он содержит соответствующее значение кода состояния.</span><span class="sxs-lookup"><span data-stu-id="55e67-137">Otherwise, it contains the appropriate status code value.</span></span> <span data-ttu-id="55e67-138">Так как значения, возвращаемые для **\[ \_ состояния \] сбоя** , отличаются от значений, возвращаемых для **\[ \_ состояния \]** связи, возвращаемые значения легко интерпретировать.</span><span class="sxs-lookup"><span data-stu-id="55e67-138">Because values returned for **\[fault\_status\]** are different from the values returned for **\[comm\_status\]**, the returned values are readily interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="55e67-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55e67-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55e67-140">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="55e67-140">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="55e67-141">**\_состояние связи**</span><span class="sxs-lookup"><span data-stu-id="55e67-141">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="55e67-142">**\_состояние ошибки \_ t**</span><span class="sxs-lookup"><span data-stu-id="55e67-142">**error\_status\_t**</span></span>](error-status-t.md)
</dt> <dt>

[<span data-ttu-id="55e67-143">**nocode**</span><span class="sxs-lookup"><span data-stu-id="55e67-143">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="55e67-144">**заполняет**</span><span class="sxs-lookup"><span data-stu-id="55e67-144">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 




