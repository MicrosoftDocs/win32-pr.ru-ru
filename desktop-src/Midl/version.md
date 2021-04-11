---
title: атрибут version
description: Атрибут интерфейса \ Version \ определяет определенную версию в нескольких версиях интерфейса RPC. С помощью атрибута Version вы гарантируете, что только совместимые версии клиентского и серверного программного обеспечения могут быть привязаны.
ms.assetid: 66ac5cf3-2230-44fd-aaf6-8013e4a4ae81
keywords:
- атрибут версии MIDL
topic_type:
- apiref
api_name:
- version
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bacbf7478ebfb745e5fc9b5e50959d0f1587dedf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069026"
---
# <a name="version-attribute"></a><span data-ttu-id="e4895-105">атрибут version</span><span class="sxs-lookup"><span data-stu-id="e4895-105">version attribute</span></span>

<span data-ttu-id="e4895-106">Атрибут интерфейса **\[ версии \]** определяет определенную версию для нескольких версий интерфейса RPC.</span><span class="sxs-lookup"><span data-stu-id="e4895-106">The **\[version\]** interface attribute identifies a particular version among multiple versions of an RPC interface.</span></span> <span data-ttu-id="e4895-107">С помощью атрибута Version вы гарантируете, что только совместимые версии клиентского и серверного программного обеспечения могут быть привязаны.</span><span class="sxs-lookup"><span data-stu-id="e4895-107">With the version attribute, you ensure that only compatible versions of client and server software are allowed to bind.</span></span>

``` syntax
version ( major-value[[. minor-value]] )
```

## <a name="parameters"></a><span data-ttu-id="e4895-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4895-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4895-109">*основной ценности*</span><span class="sxs-lookup"><span data-stu-id="e4895-109">*major-value*</span></span> 
</dt> <dd>

<span data-ttu-id="e4895-110">Задает короткое целое число без знака от 0 до 65 535 включительно, представляющее основной номер версии.</span><span class="sxs-lookup"><span data-stu-id="e4895-110">Specifies a short unsigned integer between zero and 65,535, inclusive, that represents the major version number.</span></span>

</dd> <dt>

<span data-ttu-id="e4895-111">*вспомогательное значение*</span><span class="sxs-lookup"><span data-stu-id="e4895-111">*minor-value*</span></span> 
</dt> <dd>

<span data-ttu-id="e4895-112">Задает короткое целое число без знака от 0 до 65 535 включительно, представляющее дополнительный номер версии.</span><span class="sxs-lookup"><span data-stu-id="e4895-112">Specifies a short unsigned integer between zero and 65,535, inclusive, that represents the minor version number.</span></span> <span data-ttu-id="e4895-113">Значение дополнительного номера версии является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e4895-113">The minor version value is optional.</span></span> <span data-ttu-id="e4895-114">Если указано значение, дополнительный номер версии отделяется от основного номера версии на символ точки (.).</span><span class="sxs-lookup"><span data-stu-id="e4895-114">If present, the minor version value is separated from the major version number by a period character (.).</span></span> <span data-ttu-id="e4895-115">Если значение не указано, дополнительный номер версии равен нулю.</span><span class="sxs-lookup"><span data-stu-id="e4895-115">If not specified, the minor version value is zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4895-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4895-116">Remarks</span></span>

<span data-ttu-id="e4895-117">Компилятор MIDL не поддерживает несколько версий COM-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e4895-117">The MIDL compiler does not support multiple versions of a COM interface.</span></span> <span data-ttu-id="e4895-118">В результате список атрибутов интерфейса, включающий **\[** атрибут [**объекта**](object.md) , **\]** не может включать атрибут **\[ \] Version** .</span><span class="sxs-lookup"><span data-stu-id="e4895-118">As a result, an interface attribute list that includes the **\[**[**object**](object.md)**\]** attribute cannot include the **\[version\]** attribute.</span></span> <span data-ttu-id="e4895-119">Чтобы создать новую версию существующего COM-интерфейса, используйте наследование интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e4895-119">To create a new version of an existing COM interface, use interface inheritance.</span></span> <span data-ttu-id="e4895-120">Производный COM-интерфейс имеет другой UUID, но наследует функции-члены интерфейса, коды состояния и атрибуты интерфейса базового интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e4895-120">A derived COM interface has a different UUID but inherits the interface member functions, status codes, and interface attributes of the base interface.</span></span>

<span data-ttu-id="e4895-121">В сочетании со значением **\[** [**UUID**](uuid.md) **\]** значение **\[ версии \]** однозначно определяет интерфейс.</span><span class="sxs-lookup"><span data-stu-id="e4895-121">In combination with the **\[**[**uuid**](uuid.md)**\]** value, the **\[version\]** value uniquely identifies the interface.</span></span> <span data-ttu-id="e4895-122">Библиотека времени выполнения передает значения **\[ версии \]** и **\[ UUID \]** на сервер, когда клиент вызывает удаленную функцию.</span><span class="sxs-lookup"><span data-stu-id="e4895-122">The run-time library passes the **\[version\]** and **\[uuid\]** values to the server when the client calls a remote function.</span></span> <span data-ttu-id="e4895-123">Клиент может выполнить привязку к серверу для данного интерфейса, если:</span><span class="sxs-lookup"><span data-stu-id="e4895-123">A client can bind to a server for a given interface if:</span></span>

-   <span data-ttu-id="e4895-124">Значение **\[ UUID \]** одинаково.</span><span class="sxs-lookup"><span data-stu-id="e4895-124">The **\[uuid\]** value is the same.</span></span>
-   <span data-ttu-id="e4895-125">Основной номер версии совпадает.</span><span class="sxs-lookup"><span data-stu-id="e4895-125">The major version number is the same.</span></span>
-   <span data-ttu-id="e4895-126">Дополнительный номер версии клиента меньше или равен дополнительному номеру версии сервера.</span><span class="sxs-lookup"><span data-stu-id="e4895-126">The client's minor version number is less than or equal to the server's minor version number.</span></span>

<span data-ttu-id="e4895-127">Это преимущество и преимущество пользователей в обеспечении совместимости с более широкими версиями Версионсâ, что позволяет изменять интерфейс таким образом, чтобы изменился только дополнительный номер версии.</span><span class="sxs-lookup"><span data-stu-id="e4895-127">It is to your benefit and your users' benefit to retain upward compatibility among versionsÂ that is, to modify the interface so that only the minor version number changes.</span></span> <span data-ttu-id="e4895-128">При добавлении новых типов данных, которые не используются существующими функциями, а также при добавлении новых функций без изменения спецификации интерфейса для существующих функций, можно обеспечить совместимость с более широкими характеристиками.</span><span class="sxs-lookup"><span data-stu-id="e4895-128">You can retain upward compatibility when you add new data types that are not used by existing functions and when you add new functions without changing the interface specification for existing functions.</span></span>

<span data-ttu-id="e4895-129">Измените основной номер версии, если применяется одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="e4895-129">Change the major version number if any one of the following conditions apply:</span></span>

-   <span data-ttu-id="e4895-130">При изменении типа данных, используемого существующей функцией.</span><span class="sxs-lookup"><span data-stu-id="e4895-130">If you change a data type that is used by an existing function.</span></span>
-   <span data-ttu-id="e4895-131">При изменении спецификации интерфейса для существующей функции (например, при добавлении или удалении параметра).</span><span class="sxs-lookup"><span data-stu-id="e4895-131">If you change the interface specification for an existing function (such as adding or removing a parameter).</span></span>
-   <span data-ttu-id="e4895-132">При добавлении обратных вызовов, вызванных существующими функциями.</span><span class="sxs-lookup"><span data-stu-id="e4895-132">If you add callbacks that are called by existing functions.</span></span>

<span data-ttu-id="e4895-133">Измените дополнительный номер версии, если выполняются все перечисленные ниже условия.</span><span class="sxs-lookup"><span data-stu-id="e4895-133">Change the minor version number if all of the following conditions apply:</span></span>

-   <span data-ttu-id="e4895-134">При добавлении определений типов или констант, которые не используются ни одной из существующих функций или обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="e4895-134">If you add type definitions or constants that are not used by any existing functions or callbacks.</span></span>
-   <span data-ttu-id="e4895-135">Если вы не изменяете существующие функции и добавляете в интерфейс новые функции.</span><span class="sxs-lookup"><span data-stu-id="e4895-135">If you do not change any existing functions and you add new functions to the interface.</span></span>
-   <span data-ttu-id="e4895-136">При добавлении обратных вызовов, которые не вызываются ни одной из существующих функций, а новые обратные вызовы следуют всем существующим функциям.</span><span class="sxs-lookup"><span data-stu-id="e4895-136">If you add callbacks that are not called by any existing functions and the new callbacks follow any existing functions.</span></span>

<span data-ttu-id="e4895-137">Если изменения в интерфейсе соответствуют перенаправленным вверх изменениям интерфейса, используйте следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="e4895-137">If your modifications qualify as an upward-compatible change to the interface, use the following procedure.</span></span>

<span data-ttu-id="e4895-138">**Изменение файла интерфейса (IDL)**</span><span class="sxs-lookup"><span data-stu-id="e4895-138">**To modify the interface (IDL) file**</span></span>

1.  <span data-ttu-id="e4895-139">Добавьте новые константы и определения типов в файл интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e4895-139">Add new constant and type definitions to the interface file.</span></span>
2.  <span data-ttu-id="e4895-140">Добавьте функции обратного вызова в конец файла интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e4895-140">Add callback functions to the end of the interface file.</span></span>
3.  <span data-ttu-id="e4895-141">Добавьте новые функции в конец файла интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e4895-141">Add new functions to the end of the interface file.</span></span>

<span data-ttu-id="e4895-142">Атрибут **\[ Version \]** может встречаться в заголовке интерфейса не более одного раза.</span><span class="sxs-lookup"><span data-stu-id="e4895-142">The **\[version\]** attribute can occur at most once in the interface header.</span></span>

<span data-ttu-id="e4895-143">Если отсутствует атрибут Version, то в интерфейсе используется версия по умолчанию 0,0.</span><span class="sxs-lookup"><span data-stu-id="e4895-143">When the version attribute is not present, the interface has a default version of 0.0.</span></span>

<span data-ttu-id="e4895-144">Символ точки между основным и дополнительным номерами является разделителем и не представляет десятичную запятую.</span><span class="sxs-lookup"><span data-stu-id="e4895-144">The period character between the major and minor numbers is a delimiter and does not represent a decimal point.</span></span> <span data-ttu-id="e4895-145">Дополнительный номер обрабатывается как целое число.</span><span class="sxs-lookup"><span data-stu-id="e4895-145">The minor number is treated as an integer.</span></span> <span data-ttu-id="e4895-146">Начальные нули не являются значимыми.</span><span class="sxs-lookup"><span data-stu-id="e4895-146">Leading zeroes are not significant.</span></span> <span data-ttu-id="e4895-147">Нули в конце являются значимыми.</span><span class="sxs-lookup"><span data-stu-id="e4895-147">Trailing zeroes are significant.</span></span>

<span data-ttu-id="e4895-148">Например, параметр версии 1,11 представляет собой основное значение одного и незначительного значения одиннадцати.</span><span class="sxs-lookup"><span data-stu-id="e4895-148">For example, the version setting 1.11 represents a major value of one and a minor value of eleven.</span></span> <span data-ttu-id="e4895-149">Версия 1,11 не представляет значение в диапазоне от 1,1 до 1,2.</span><span class="sxs-lookup"><span data-stu-id="e4895-149">Version 1.11 does not represent a value between 1.1 and 1.2.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4895-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4895-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4895-151">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="e4895-151">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e4895-152">**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="e4895-152">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="e4895-153">**объектами**</span><span class="sxs-lookup"><span data-stu-id="e4895-153">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="e4895-154">**UUID**</span><span class="sxs-lookup"><span data-stu-id="e4895-154">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 




