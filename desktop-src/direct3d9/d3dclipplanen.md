---
description: Определяет битовые шаблоны, обеспечивающие определенные пользователем обтравочные плоскости. Эти макросы определяются в качестве удобства при задании значений для \_ состояния визуализации D3DRS клиппланинабле.
ms.assetid: 5bca2401-a3fb-4b1c-bb59-621b15da10f1
title: Макрос D3DCLIPPLANEn (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPPLANEn
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4508f1654a357eb80b3847b7562e230c6a9be4d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424354"
---
# <a name="d3dclipplanen-macro"></a><span data-ttu-id="a20e3-104">Макрос D3DCLIPPLANEn</span><span class="sxs-lookup"><span data-stu-id="a20e3-104">D3DCLIPPLANEn macro</span></span>

<span data-ttu-id="a20e3-105">Определяет битовые шаблоны, обеспечивающие определенные пользователем обтравочные плоскости.</span><span class="sxs-lookup"><span data-stu-id="a20e3-105">Defines bit patterns that enable user-defined clipping planes.</span></span> <span data-ttu-id="a20e3-106">Эти макросы определяются в качестве удобства при задании значений для \_ состояния визуализации D3DRS клиппланинабле.</span><span class="sxs-lookup"><span data-stu-id="a20e3-106">These macros are defined as a convenience when setting values for the D3DRS\_CLIPPLANEENABLE render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="a20e3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a20e3-107">Syntax</span></span>


```C++
void D3DCLIPPLANEn(void);
```



## <a name="parameters"></a><span data-ttu-id="a20e3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a20e3-108">Parameters</span></span>

<span data-ttu-id="a20e3-109">Этот макрос не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a20e3-109">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a20e3-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a20e3-110">Return value</span></span>

<span data-ttu-id="a20e3-111">Этот макрос не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a20e3-111">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a20e3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a20e3-112">Remarks</span></span>

<span data-ttu-id="a20e3-113">Определяемые пользователем отрезкиные плоскости включаются, если значение, заданное в \_ состоянии прорисовки D3DRS клиппланинабле, содержит один или несколько наборов битов (то есть не равен 0).</span><span class="sxs-lookup"><span data-stu-id="a20e3-113">User-defined clipping planes are enabled when the value set in the D3DRS\_CLIPPLANEENABLE render state contains one or more set bits (that is, is not 0).</span></span> <span data-ttu-id="a20e3-114">Значение состояния визуализации не имеет значения; система не интерпретирует это значение как число.</span><span class="sxs-lookup"><span data-stu-id="a20e3-114">The value of the render-state is not important; the system does not interpret the value as a number.</span></span> <span data-ttu-id="a20e3-115">Вместо этого значение включает плоскость обрезки, для которой установлен соответствующий бит.</span><span class="sxs-lookup"><span data-stu-id="a20e3-115">Rather, the value enables the clipping plane whose corresponding bit is set.</span></span> <span data-ttu-id="a20e3-116">Бит 0 управляет состоянием первой плоскости обрезки (с индексом 0), битом 1 второй плоскости и т. д.</span><span class="sxs-lookup"><span data-stu-id="a20e3-116">Bit 0 controls the state of the first clipping plane (at index 0), bit 1 the second plane, and so on.</span></span>

<span data-ttu-id="a20e3-117">Битовые шаблоны, создаваемые этими макросами, можно комбинировать с помощью логической операции или для одновременного включения нескольких обтравочных плоскостей.</span><span class="sxs-lookup"><span data-stu-id="a20e3-117">The bit patterns that these macros create can be combined by using a logical OR operation to simultaneously enable multiple clipping planes.</span></span> <span data-ttu-id="a20e3-118">Пропуск одного из этих макросов в сочетании эффективно отключает плоскость обрезки в этом индексе.</span><span class="sxs-lookup"><span data-stu-id="a20e3-118">Omitting one of these macros from the combination effectively disables the clipping plane at that index.</span></span>

## <a name="requirements"></a><span data-ttu-id="a20e3-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a20e3-119">Requirements</span></span>



| <span data-ttu-id="a20e3-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a20e3-120">Requirement</span></span> | <span data-ttu-id="a20e3-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a20e3-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a20e3-122">Header</span><span class="sxs-lookup"><span data-stu-id="a20e3-122">Header</span></span><br/> | <dl> <span data-ttu-id="a20e3-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a20e3-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a20e3-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a20e3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a20e3-125">Макросы</span><span class="sxs-lookup"><span data-stu-id="a20e3-125">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




