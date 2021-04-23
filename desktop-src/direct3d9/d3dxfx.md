---
description: Параметры для сохранения и создания эффектов.
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe1e5e57b5fac94c1fb24d35cf1826057b75c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139243"
---
# <a name="d3dxfx"></a><span data-ttu-id="c5010-103">D3DXFX</span><span class="sxs-lookup"><span data-stu-id="c5010-103">D3DXFX</span></span>

<span data-ttu-id="c5010-104">Параметры для сохранения и создания эффектов.</span><span class="sxs-lookup"><span data-stu-id="c5010-104">Options for saving and creating effects.</span></span>

<span data-ttu-id="c5010-105">Константы в следующей таблице определены в d3dx9effect. h.</span><span class="sxs-lookup"><span data-stu-id="c5010-105">The constants in the following table are defined in d3dx9effect.h.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c5010-106">Флаги сохранения и восстановления состояния эффектов</span><span class="sxs-lookup"><span data-stu-id="c5010-106">Effect State Save and Restore Flags</span></span></td>
<td><span data-ttu-id="c5010-107">Описание</span><span class="sxs-lookup"><span data-stu-id="c5010-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5010-108">D3DXFX_DONOTSAVESTATE</span><span class="sxs-lookup"><span data-stu-id="c5010-108">D3DXFX_DONOTSAVESTATE</span></span></td>
<td><span data-ttu-id="c5010-109">Состояние не сохраняется при вызове <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> или Restored при вызове <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c5010-109">No state is saved when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> or restored when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c5010-110">D3DXFX_DONOTSAVESAMPLERSTATE</span><span class="sxs-lookup"><span data-stu-id="c5010-110">D3DXFX_DONOTSAVESAMPLERSTATE</span></span></td>
<td><span data-ttu-id="c5010-111">Статеблокк сохраняет состояние при вызове <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> и восстанавливает состояние при вызове <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c5010-111">A stateblock saves state when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> and restores state when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5010-112">D3DXFX_DONOTSAVESHADERSTATE</span><span class="sxs-lookup"><span data-stu-id="c5010-112">D3DXFX_DONOTSAVESHADERSTATE</span></span></td>
<td><span data-ttu-id="c5010-113">Статеблокк сохраняет состояние (за исключением шейдеров и констант шейдера) при вызове метода <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> и восстанавливает состояние при вызове <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c5010-113">A stateblock saves state (except shaders and shader constants) when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> and restores state when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c5010-114">Флаги создания эффектов</span><span class="sxs-lookup"><span data-stu-id="c5010-114">Effect Creation Flags</span></span></td>
<td><span data-ttu-id="c5010-115">Описание</span><span class="sxs-lookup"><span data-stu-id="c5010-115">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5010-116">D3DXFX_NOT_CLONEABLE</span><span class="sxs-lookup"><span data-stu-id="c5010-116">D3DXFX_NOT_CLONEABLE</span></span></td>
<td><span data-ttu-id="c5010-117">Результат будет не клонирован и не будет содержать двоичные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="c5010-117">The effect will be non-cloneable and will not contain any shader binary data.</span></span> <span data-ttu-id="c5010-118"><a href="id3dxbaseeffect--getpassdesc.md"><strong>Жетпассдеск</strong></a> не будет возвращать указатели функций шейдера.</span><span class="sxs-lookup"><span data-stu-id="c5010-118"><a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> will not return shader function pointers.</span></span> <span data-ttu-id="c5010-119">Установка этого флага сокращает использование памяти на 50%, так как устраняет необходимость сохранения копии шейдеров в памяти системой влияния.</span><span class="sxs-lookup"><span data-stu-id="c5010-119">Setting this flag reduces effect memory usage by about 50% because it eliminates the need for the effect system to keep a copy of the shaders in memory.</span></span> <span data-ttu-id="c5010-120">Этот флаг используется <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>и <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c5010-120">This flag is used by <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>, and <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c5010-121">D3DXFX_LARGEADDRESSAWARE</span><span class="sxs-lookup"><span data-stu-id="c5010-121">D3DXFX_LARGEADDRESSAWARE</span></span></td>
<td><span data-ttu-id="c5010-122">Разрешает выделение ресурса влияния в адресном пространстве уппдер компьютера.</span><span class="sxs-lookup"><span data-stu-id="c5010-122">Enables the allocation of an effect resource into the uppder address space of a machine.</span></span> <span data-ttu-id="c5010-123">Одно важное ограничение заключается в том, что нельзя использовать строки и обрабатывать взаимозаменяемые.</span><span class="sxs-lookup"><span data-stu-id="c5010-123">One important limitation is that you cannot use strings and handles interchangeably.</span></span> <span data-ttu-id="c5010-124">Например, следующее перестанет работать.</span><span class="sxs-lookup"><span data-stu-id="c5010-124">For example, the following would no longer work.</span></span> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>g_pEffect->SetMatrix( &quot;g_mWorldViewProjection&quot;, &mWorldViewProjection );</code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c5010-125">Вместо этого метод, такой как [<strong>жетпараметербинаме</strong>](id3dxbaseeffect--getparameterbyname.md) , должен использоваться для хранения маркера параметра, который затем используется для передачи переменных в результат.</span><span class="sxs-lookup"><span data-stu-id="c5010-125">Instead, a method such as [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) must be used to store the handle of the parameter, which is then used to pass variables to the effect.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c5010-126">Константы в следующей таблице не определены по умолчанию и должны определяться разработчиком.</span><span class="sxs-lookup"><span data-stu-id="c5010-126">The constants in the following table are not defined by default and must be defined by the developer.</span></span>



|                                |                                                                                                                                                                                                                                      |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5010-127">Определение препроцессора эффектов \#</span><span class="sxs-lookup"><span data-stu-id="c5010-127">Effect Preprocessor \#define's</span></span> | <span data-ttu-id="c5010-128">Описание</span><span class="sxs-lookup"><span data-stu-id="c5010-128">Description</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="c5010-129">D3DXFX \_ ларжеаддресс \_</span><span class="sxs-lookup"><span data-stu-id="c5010-129">D3DXFX\_LARGEADDRESS\_HANDLE</span></span>   | <span data-ttu-id="c5010-130">Определите это значение перед включением d3dx9. h, чтобы приложение не было скомпилировано при попытке передать строки в параметры D3DXHANDLE.</span><span class="sxs-lookup"><span data-stu-id="c5010-130">Define this value before including d3dx9.h so that your application fails to compile when attempting to pass strings into D3DXHANDLE parameters.</span></span> <span data-ttu-id="c5010-131">Это поможет убедиться в том, что в среду выполнения передаются допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="c5010-131">This will aid in making sure that valid information is being passed to the runtime.</span></span> |
| <span data-ttu-id="c5010-132">Флаги компоновщика эффектов</span><span class="sxs-lookup"><span data-stu-id="c5010-132">Effect Linker Flags</span></span>            | <span data-ttu-id="c5010-133">Описание</span><span class="sxs-lookup"><span data-stu-id="c5010-133">Description</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="c5010-134">с \_ \_ учетом большого адреса</span><span class="sxs-lookup"><span data-stu-id="c5010-134">LARGE\_ADDRESS\_AWARE</span></span>          | <span data-ttu-id="c5010-135">Установка флага компоновщика "большой \_ адрес \_ " с учетом значения 1 позволит приложению распределять ресурсы за пределы 2 ГБ при необходимости.</span><span class="sxs-lookup"><span data-stu-id="c5010-135">Setting the linker flag LARGE\_ADDRESS\_AWARE = 1 will will allow the application to allocate resources past the 2GB address limit when needed.</span></span>                                                                                      |



 

<span data-ttu-id="c5010-136">Система эффектов использует блоки состояний для автоматического сохранения и восстановления состояния.</span><span class="sxs-lookup"><span data-stu-id="c5010-136">The effect system uses state blocks to save and restore state automatically.</span></span> <span data-ttu-id="c5010-137">Дополнительные сведения о блоках состояния см. в разделе [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md).</span><span class="sxs-lookup"><span data-stu-id="c5010-137">For more information about state blocks, see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5010-138">См. также</span><span class="sxs-lookup"><span data-stu-id="c5010-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5010-139">Константы эффектов</span><span class="sxs-lookup"><span data-stu-id="c5010-139">Effect Constants</span></span>](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 



