---
title: Оператор Switch (Urlmon. h)
description: Передает управление другому блоку операторов в теле переключателя в зависимости от значения селектора.
ms.assetid: d1932ee1-d789-4536-b77d-162aacdbb115
keywords:
- Оператор Switch HLSL
topic_type:
- apiref
api_name:
- switch Statement
api_location:
- urlmon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4af131ca3a126cd6f1fd54160418bfbe70cc9cce
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119089"
---
# <a name="switch-statement"></a><span data-ttu-id="5e864-104">Оператор switch</span><span class="sxs-lookup"><span data-stu-id="5e864-104">switch Statement</span></span>

<span data-ttu-id="5e864-105">Передает управление другому блоку операторов в теле переключателя в зависимости от значения селектора.</span><span class="sxs-lookup"><span data-stu-id="5e864-105">Transfer control to a different statement block within the switch body depending on the value of a selector.</span></span>


<span data-ttu-id="5e864-106">\[*Атрибут* \] переключатель ( *селектор* ) {Case 0: { *статементблокк*;}   разбиени   вариант 1: { *статементблокк*;}   разбиени   Case n: { *статементблокк*;}   разбиени   значение по умолчанию: { *статементблокк*;}   разбиени</span><span class="sxs-lookup"><span data-stu-id="5e864-106">\[*Attribute*\] switch( *Selector* ) {   case 0 :     { *StatementBlock*; }   break;   case 1 :     { *StatementBlock*; }   break;   case n :     { *StatementBlock*; }   break;   default :     { *StatementBlock*; }   break;</span></span>



 

## <a name="parameters"></a><span data-ttu-id="5e864-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e864-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e864-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Версию*</span><span class="sxs-lookup"><span data-stu-id="5e864-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="5e864-109">Необязательный параметр, управляющий компиляцией инструкции.</span><span class="sxs-lookup"><span data-stu-id="5e864-109">An optional parameter that controls how the statement is compiled.</span></span> <span data-ttu-id="5e864-110">Если атрибут не указан, компилятор может использовать аппаратный переключатель или порождать последовательность инструкций **If** .</span><span class="sxs-lookup"><span data-stu-id="5e864-110">When no attribute is specified, the compiler may use a hardware switch or emit a series of **if** statements.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5e864-111">attribute</span><span class="sxs-lookup"><span data-stu-id="5e864-111">Attribute</span></span></th>
<th><span data-ttu-id="5e864-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5e864-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5e864-113">преобразовать в плоский формат</span><span class="sxs-lookup"><span data-stu-id="5e864-113">flatten</span></span></td>
<td><span data-ttu-id="5e864-114">Скомпилируйте оператор как ряд инструкций <strong>If</strong> , каждый с атрибутом <strong>спрямления</strong> .</span><span class="sxs-lookup"><span data-stu-id="5e864-114">Compile the statement as a series of <strong>if</strong> statements, each with the <strong>flatten</strong> attribute.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e864-115">ветвь</span><span class="sxs-lookup"><span data-stu-id="5e864-115">branch</span></span></td>
<td><span data-ttu-id="5e864-116">Скомпилируйте оператор как ряд операторов <strong>If</strong> , каждый с атрибутом <strong>branch</strong> .</span><span class="sxs-lookup"><span data-stu-id="5e864-116">Compile the statement as a series of <strong>if</strong> statements each with the <strong>branch</strong> attribute.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5e864-117">При использовании <a href="dx-graphics-hlsl-sm2.md">модели шейдеров 2. x</a> или <a href="dx-graphics-hlsl-sm3.md">Shader Model 3,0</a>каждый раз при использовании динамического ветвления используются ресурсы.</span><span class="sxs-lookup"><span data-stu-id="5e864-117">When you use <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> or <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>, each time you use dynamic branching you consume resources.</span></span> <span data-ttu-id="5e864-118">Поэтому при чрезмерном использовании динамической ветви при выборе этих профилей могут возникнуть ошибки компиляции.</span><span class="sxs-lookup"><span data-stu-id="5e864-118">So, if you use dynamic branching excessively when you target these profiles, you can receive compilation errors.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5e864-119">форцекасе</span><span class="sxs-lookup"><span data-stu-id="5e864-119">forcecase</span></span></td>
<td><span data-ttu-id="5e864-120">Принудительно использовать оператор switch на оборудовании.</span><span class="sxs-lookup"><span data-stu-id="5e864-120">Force a switch statement in the hardware.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5e864-121">Требуется 10_0 или более поздний <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">уровень</a> оборудования.</span><span class="sxs-lookup"><span data-stu-id="5e864-121">Requires <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 10_0 or later hardware.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e864-122">вызывает</span><span class="sxs-lookup"><span data-stu-id="5e864-122">call</span></span></td>
<td><span data-ttu-id="5e864-123">Тексты отдельных вариантов в коммутаторе будут перемещены в подпрограммы оборудования, а коммутатор будет являться серией вызовов подпрограмм.</span><span class="sxs-lookup"><span data-stu-id="5e864-123">The bodies of the individual cases in the switch will be moved into hardware subroutines and the switch will be a series of subroutine calls.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5e864-124">Требуется 10_0 или более поздний <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">уровень</a> оборудования.</span><span class="sxs-lookup"><span data-stu-id="5e864-124">Requires <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 10_0 or later hardware.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="5e864-125"><span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Выбора*</span><span class="sxs-lookup"><span data-stu-id="5e864-125"><span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Selector*</span></span>
</dt> <dd>

<span data-ttu-id="5e864-126">Переменная.</span><span class="sxs-lookup"><span data-stu-id="5e864-126">A variable.</span></span> <span data-ttu-id="5e864-127">Инструкции CASE внутри фигурных скобок будут проверять эту переменную, чтобы определить, соответствует ли SwitchValue их конкретному Касевалуе.</span><span class="sxs-lookup"><span data-stu-id="5e864-127">The case statements inside the curly brackets will each check this variable to see if the SwitchValue matches their particular CaseValue.</span></span>

</dd> <dt>

<span data-ttu-id="5e864-128"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*статементблокк*</span><span class="sxs-lookup"><span data-stu-id="5e864-128"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span></span>
</dt> <dd>

<span data-ttu-id="5e864-129">Одна или несколько [инструкций](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="5e864-129">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e864-130">Remarks</span><span class="sxs-lookup"><span data-stu-id="5e864-130">Remarks</span></span>


```
[branch] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



<span data-ttu-id="5e864-131">Эквивалентно следующему:</span><span class="sxs-lookup"><span data-stu-id="5e864-131">Is equivalent to:</span></span>


```
[branch] if( a == 2 )
    return 3;
else if( a == 1 )
    return 1;
else if( a == 0 )
    return 0;
else
    return 6;
```



<span data-ttu-id="5e864-132">Ниже приведены примеры использования атрибутов управления потоком форцекасе и Call.</span><span class="sxs-lookup"><span data-stu-id="5e864-132">Here are example usages of forcecase and call flow control attributes:</span></span>


```
[forcecase] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}

[call] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



## <a name="requirements"></a><span data-ttu-id="5e864-133">Требования</span><span class="sxs-lookup"><span data-stu-id="5e864-133">Requirements</span></span>



| <span data-ttu-id="5e864-134">Требование</span><span class="sxs-lookup"><span data-stu-id="5e864-134">Requirement</span></span> | <span data-ttu-id="5e864-135">Значение</span><span class="sxs-lookup"><span data-stu-id="5e864-135">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5e864-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5e864-136">Header</span></span><br/> | <dl> <span data-ttu-id="5e864-137"><dt>Urlmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e864-137"><dt>Urlmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e864-138">См. также</span><span class="sxs-lookup"><span data-stu-id="5e864-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e864-139">Управление потоком</span><span class="sxs-lookup"><span data-stu-id="5e864-139">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

