---
title: Warning pragma, директива
description: Директива pragma, которая изменяет поведение предупреждающих сообщений компилятора.
ms.assetid: 69488014-36e3-4c87-8b65-6123b5e87bcb
keywords:
- предупреждение директивы pragma HLSL
topic_type:
- apiref
api_name:
- warning pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7599886b47830b33c69f11c0c341c7775c644dd3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103986958"
---
# <a name="warning-pragma-directive"></a><span data-ttu-id="d9ac4-104">Warning pragma, директива</span><span class="sxs-lookup"><span data-stu-id="d9ac4-104">warning pragma Directive</span></span>

<span data-ttu-id="d9ac4-105">Директива pragma, которая изменяет поведение предупреждающих сообщений компилятора.</span><span class="sxs-lookup"><span data-stu-id="d9ac4-105">Pragma directive that modifies the behavior of compiler warning messages.</span></span>



| <span data-ttu-id="d9ac4-106">\#pragma warning ( *warning-спецификатор* : *warning-number-list* \[ ; *warning — описатель* : *warning-number-list*... \] )</span><span class="sxs-lookup"><span data-stu-id="d9ac4-106">\#pragma warning( *warning-specifier* : *warning-number-list* \[; *warning-specifier* : *warning-number-list*...\] )</span></span> |
|----------------------------------------------------------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="d9ac4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9ac4-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9ac4-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="d9ac4-108">Item</span></span></th>
<th><span data-ttu-id="d9ac4-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d9ac4-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9ac4-110"><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>описатель "предупреждение"</em></span><span class="sxs-lookup"><span data-stu-id="d9ac4-110"><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>warning-specifier</em></span></span><br/></td>
<td><span data-ttu-id="d9ac4-111">Поведение, заданное для указанных предупреждений.</span><span class="sxs-lookup"><span data-stu-id="d9ac4-111">Behavior to set for the specified warnings.</span></span> <span data-ttu-id="d9ac4-112">Этот параметр может принимать одно из значений, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d9ac4-112">This parameter can take one of the values listed in the following table.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d9ac4-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d9ac4-113">Value</span></span></th>
<th><span data-ttu-id="d9ac4-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d9ac4-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9ac4-115">once</span><span class="sxs-lookup"><span data-stu-id="d9ac4-115">once</span></span></td>
<td><span data-ttu-id="d9ac4-116">Отображение сообщения предупреждений с указанными числами только один раз.</span><span class="sxs-lookup"><span data-stu-id="d9ac4-116">Display the message of the warnings with the specified numbers only once.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9ac4-117">default</span><span class="sxs-lookup"><span data-stu-id="d9ac4-117">default</span></span></td>
<td><span data-ttu-id="d9ac4-118">Сброс поведения предупреждений с указанными значениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d9ac4-118">Reset the behavior of the warnings with the specified numbers to their default value.</span></span> <span data-ttu-id="d9ac4-119">Это также влияет на отключение предупреждения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d9ac4-119">This also has the effect of turning a warning on that is off by default.</span></span> <span data-ttu-id="d9ac4-120">Предупреждение будет создано на уровне по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d9ac4-120">The warning will be generated at its default level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9ac4-121">1, 2, 3, 4</span><span class="sxs-lookup"><span data-stu-id="d9ac4-121">1, 2, 3, 4</span></span></td>
<td><span data-ttu-id="d9ac4-122">Применить указанный уровень к предупреждениям с указанными числами.</span><span class="sxs-lookup"><span data-stu-id="d9ac4-122">Apply the specified level to the warnings with the specified numbers.</span></span> <span data-ttu-id="d9ac4-123">Это также влияет на отключение предупреждения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d9ac4-123">This also has the effect of turning a warning on that is off by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9ac4-124">disable</span><span class="sxs-lookup"><span data-stu-id="d9ac4-124">disable</span></span></td>
<td><span data-ttu-id="d9ac4-125">Не выдавать предупреждения с указанными числами.</span><span class="sxs-lookup"><span data-stu-id="d9ac4-125">Do not issue the warnings with the specified numbers.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9ac4-126">Ошибка</span><span class="sxs-lookup"><span data-stu-id="d9ac4-126">error</span></span></td>
<td><span data-ttu-id="d9ac4-127">Сообщать о предупреждениях с указанными числами как об ошибках.</span><span class="sxs-lookup"><span data-stu-id="d9ac4-127">Report the warnings with the specified numbers as errors.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9ac4-128"><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>Список "warning-number-list"</em></span><span class="sxs-lookup"><span data-stu-id="d9ac4-128"><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>warning-number-list</em></span></span></p></td>
<td><p><span data-ttu-id="d9ac4-129">Разделенный пробелами список номеров предупреждений для изменения поведения.</span><span class="sxs-lookup"><span data-stu-id="d9ac4-129">White space-delimited list of the numbers of the warnings to modify the behavior of.</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="d9ac4-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="d9ac4-130">Remarks</span></span>

<span data-ttu-id="d9ac4-131">Можно указать любое количество уникальных изменений поведения предупреждений в пределах одной и той же директивы pragma warning, разделяя изменения точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="d9ac4-131">You can specify any number of distinct warning behavior changes within the same warning pragma by separating the changes with semicolons.</span></span>

<span data-ttu-id="d9ac4-132">Компилятор добавит 4000 к любому номеру предупреждения, который находится в диапазоне от 0 до 999.</span><span class="sxs-lookup"><span data-stu-id="d9ac4-132">The compiler will add 4000 to any warning number that is between 0 and 999.</span></span> <span data-ttu-id="d9ac4-133">Для номеров предупреждений больше 4699 (связанных с созданием кода) прагма-директива warning действует только при размещении внешних определений функций.</span><span class="sxs-lookup"><span data-stu-id="d9ac4-133">For warning numbers greater than 4699, (those associated with code generation) the warning pragma has effect only when placed outside function definitions.</span></span> <span data-ttu-id="d9ac4-134">Директива pragma пропускается, если она указывает число больше 4699 и используется внутри функции.</span><span class="sxs-lookup"><span data-stu-id="d9ac4-134">The pragma is ignored if it specifies a number greater than 4699 and is used inside a function.</span></span>

<span data-ttu-id="d9ac4-135">Прагма-директива HLSL warning не поддерживает функцию **Push** и **POP** предупреждения pragma, входящей в компилятор C++.</span><span class="sxs-lookup"><span data-stu-id="d9ac4-135">The HLSL warning pragma does not support the **push** and **pop** functionality of the warning pragma included in the C++ compiler.</span></span>

## <a name="examples"></a><span data-ttu-id="d9ac4-136">Примеры</span><span class="sxs-lookup"><span data-stu-id="d9ac4-136">Examples</span></span>

<span data-ttu-id="d9ac4-137">В следующем примере отключаются предупреждения 4507 и 4034, отображается предупреждение 4385 и выводится предупреждение 4164 в качестве ошибки.</span><span class="sxs-lookup"><span data-stu-id="d9ac4-137">The following example disables warnings 4507 and 4034, displays warning 4385 once once, and reports warning 4164 as an error.</span></span>


```
#pragma warning( disable : 4507 34; once : 4385; error : 164 )
```



<span data-ttu-id="d9ac4-138">Предыдущий пример функционально эквивалентен следующему:</span><span class="sxs-lookup"><span data-stu-id="d9ac4-138">The preceding example is functionally equivalent to the following:</span></span>


```
#pragma warning( disable : 4507 34 )
#pragma warning( once : 4385 )
#pragma warning( error : 164 )
```



## <a name="see-also"></a><span data-ttu-id="d9ac4-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9ac4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9ac4-140">Директивы препроцессора (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d9ac4-140">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="d9ac4-141">\#Директива pragma (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d9ac4-141">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





