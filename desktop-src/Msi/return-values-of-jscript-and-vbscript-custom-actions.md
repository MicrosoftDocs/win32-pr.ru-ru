---
description: Пользовательские действия, написанные на JScript или Visual Basic, Scripting Edition (VBScript) могут вызывать необязательную функцию. Эти функции должны возвращать одно из значений, приведенных в следующей таблице.
ms.assetid: f05d0b94-e79e-440e-9f2b-99fe0e9e2646
title: Возвращаемые значения настраиваемых действий JScript и VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae96ecba320914b7b00dfa718deffdd56ae7eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662706"
---
# <a name="return-values-of-jscript-and-vbscript-custom-actions"></a><span data-ttu-id="28b86-104">Возвращаемые значения настраиваемых действий JScript и VBScript</span><span class="sxs-lookup"><span data-stu-id="28b86-104">Return Values of JScript and VBScript Custom Actions</span></span>

<span data-ttu-id="28b86-105">Пользовательские действия, написанные на JScript или Visual Basic, Scripting Edition (VBScript) могут вызывать необязательную функцию.</span><span class="sxs-lookup"><span data-stu-id="28b86-105">Custom actions written in JScript or Visual Basic, Scripting Edition (VBScript) can call an optional function.</span></span> <span data-ttu-id="28b86-106">Эти функции должны возвращать одно из значений, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="28b86-106">These functions must return one of the values shown in the following table.</span></span>



| <span data-ttu-id="28b86-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28b86-107">Return value</span></span>              | <span data-ttu-id="28b86-108">Значение</span><span class="sxs-lookup"><span data-stu-id="28b86-108">Value</span></span>        | <span data-ttu-id="28b86-109">Описание</span><span class="sxs-lookup"><span data-stu-id="28b86-109">Description</span></span>                                                                                                |
|---------------------------|--------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28b86-110">мсидоактионстатусноактион</span><span class="sxs-lookup"><span data-stu-id="28b86-110">msiDoActionStatusNoAction</span></span> | <span data-ttu-id="28b86-111">0</span><span class="sxs-lookup"><span data-stu-id="28b86-111">0</span></span>            | <span data-ttu-id="28b86-112">Действие не выполнено.</span><span class="sxs-lookup"><span data-stu-id="28b86-112">Action not executed.</span></span>                                                                                       |
| <span data-ttu-id="28b86-113">мсидоактионстатуссукцесс</span><span class="sxs-lookup"><span data-stu-id="28b86-113">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="28b86-114">ИДОК = 1</span><span class="sxs-lookup"><span data-stu-id="28b86-114">IDOK = 1</span></span>     | <span data-ttu-id="28b86-115">Действие успешно выполнено.</span><span class="sxs-lookup"><span data-stu-id="28b86-115">Action completed successfully.</span></span>                                                                             |
| <span data-ttu-id="28b86-116">мсидоактионстатусусерексит</span><span class="sxs-lookup"><span data-stu-id="28b86-116">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="28b86-117">ИДКАНЦЕЛ = 2</span><span class="sxs-lookup"><span data-stu-id="28b86-117">IDCANCEL = 2</span></span> | <span data-ttu-id="28b86-118">Преждевременное завершение пользователем.</span><span class="sxs-lookup"><span data-stu-id="28b86-118">Premature termination by user.</span></span>                                                                             |
| <span data-ttu-id="28b86-119">мсидоактионстатусфаилуре</span><span class="sxs-lookup"><span data-stu-id="28b86-119">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="28b86-120">ИДАБОРТ = 3</span><span class="sxs-lookup"><span data-stu-id="28b86-120">IDABORT = 3</span></span>  | <span data-ttu-id="28b86-121">Неустранимая ошибка.</span><span class="sxs-lookup"><span data-stu-id="28b86-121">Unrecoverable error.</span></span> <span data-ttu-id="28b86-122">Возвращается при возникновении ошибки во время синтаксического анализа или выполнения JScript или VBScript.</span><span class="sxs-lookup"><span data-stu-id="28b86-122">Returned if there is an error during parsing or execution of the JScript or VBScript.</span></span> |
| <span data-ttu-id="28b86-123">мсидоактионстатуссуспенд</span><span class="sxs-lookup"><span data-stu-id="28b86-123">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="28b86-124">ИДРЕТРИ = 4</span><span class="sxs-lookup"><span data-stu-id="28b86-124">IDRETRY = 4</span></span>  | <span data-ttu-id="28b86-125">Приостановленная последовательность будет возобновлена позже.</span><span class="sxs-lookup"><span data-stu-id="28b86-125">Suspended sequence to be resumed later.</span></span>                                                                    |
| <span data-ttu-id="28b86-126">мсидоактионстатусфинишед</span><span class="sxs-lookup"><span data-stu-id="28b86-126">msiDoActionStatusFinished</span></span> | <span data-ttu-id="28b86-127">ИДИГНОРЕ = 5</span><span class="sxs-lookup"><span data-stu-id="28b86-127">IDIGNORE = 5</span></span> | <span data-ttu-id="28b86-128">Пропустить оставшиеся действия.</span><span class="sxs-lookup"><span data-stu-id="28b86-128">Skip remaining actions.</span></span> <span data-ttu-id="28b86-129">Не является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="28b86-129">Not an error.</span></span>                                                                      |



 

<span data-ttu-id="28b86-130">Обратите внимание, что установщик Windows преобразует возвращаемые значения из всех действий при записи возвращаемого значения в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="28b86-130">Note that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="28b86-131">Например, если возвращаемое значение действия отображается как 1 (одно) в файле журнала, это означает, что действие вернуло Мсидоактионстатуссукцесс.</span><span class="sxs-lookup"><span data-stu-id="28b86-131">For example, if the action return value appears as 1 (one) in the log file, this means that the action returned msiDoActionStatusSuccess.</span></span> <span data-ttu-id="28b86-132">Дополнительные сведения об этом переводе см. в разделе [ведение журнала возвращаемых значений действий](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="28b86-132">For more information about this translation see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="28b86-133">Чтобы вернуть значение, отличное от "успешно" из настраиваемого действия скрипта, необходимо использовать цель функции для настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="28b86-133">To return a value other than success from a script custom action, you must use a function target for the custom action.</span></span> <span data-ttu-id="28b86-134">Целевая функция указывается в столбце Target [таблицы CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="28b86-134">The target function is specified in the Target column of the [CustomAction Table](customaction-table.md).</span></span>

<span data-ttu-id="28b86-135">В следующем примере скрипта показано, как вернуть значение Success или Failure из настраиваемого действия VBScript.</span><span class="sxs-lookup"><span data-stu-id="28b86-135">The following script example shows you how to return success or failure from a VBScript custom action.</span></span>


```VB
Function MyVBScriptCA()

    If Session.Property("CustomErrorStatus") <> "0" Then
        'return error
        MyVBScriptCA = 3
        Exit Function
    End If

    ' return success
    MyVBScriptCA = 1
    Exit Function

End Function
```



<span data-ttu-id="28b86-136">Если этот сценарий VBScript был внедрен в [двоичную таблицу](binary-table.md) установочного пакета как MyCA.vbs, для скрипта будет использоваться следующая запись [CustomAction](customaction-table.md) :</span><span class="sxs-lookup"><span data-stu-id="28b86-136">If this VBScript were embedded in the [Binary table](binary-table.md) of the installation package as MyCA.vbs, the [CustomAction Table](customaction-table.md) entry for the script would be the following:</span></span>



| <span data-ttu-id="28b86-137">Действие</span><span class="sxs-lookup"><span data-stu-id="28b86-137">Action</span></span>         | <span data-ttu-id="28b86-138">Тип</span><span class="sxs-lookup"><span data-stu-id="28b86-138">Type</span></span> | <span data-ttu-id="28b86-139">Источник</span><span class="sxs-lookup"><span data-stu-id="28b86-139">Source</span></span>   | <span data-ttu-id="28b86-140">Назначение</span><span class="sxs-lookup"><span data-stu-id="28b86-140">Target</span></span>       |
|----------------|------|----------|--------------|
| <span data-ttu-id="28b86-141">микустомактион</span><span class="sxs-lookup"><span data-stu-id="28b86-141">MyCustomAction</span></span> | <span data-ttu-id="28b86-142">6</span><span class="sxs-lookup"><span data-stu-id="28b86-142">6</span></span>    | <span data-ttu-id="28b86-143">MyCA.vbs</span><span class="sxs-lookup"><span data-stu-id="28b86-143">MyCA.vbs</span></span> | <span data-ttu-id="28b86-144">мивбскриптка</span><span class="sxs-lookup"><span data-stu-id="28b86-144">MyVBScriptCA</span></span> |



 

 

 



