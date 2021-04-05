---
description: Описывает методику, используемую в результате.
ms.assetid: 7ba2dbb3-8039-4d1c-ad9d-130d9bf3d80a
title: Структура D3DXTECHNIQUE_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTECHNIQUE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 35dd483a983f17371d6a77e6c020b3a45d9e9360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081854"
---
# <a name="d3dxtechnique_desc-structure"></a><span data-ttu-id="5298a-103">\_Структура D3DXTECHNIQUE DESC</span><span class="sxs-lookup"><span data-stu-id="5298a-103">D3DXTECHNIQUE\_DESC structure</span></span>

<span data-ttu-id="5298a-104">Описывает методику, используемую в результате.</span><span class="sxs-lookup"><span data-stu-id="5298a-104">Describes a technique used by an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="5298a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5298a-105">Syntax</span></span>


```C++
typedef struct D3DXTECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DXTECHNIQUE_DESC, *LPD3DXTECHNIQUE_DESC;
```



## <a name="members"></a><span data-ttu-id="5298a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="5298a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5298a-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="5298a-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="5298a-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5298a-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5298a-109">Строка, содержащая имя метода.</span><span class="sxs-lookup"><span data-stu-id="5298a-109">String that contains the technique name.</span></span>

</dd> <dt>

<span data-ttu-id="5298a-110">**Соответствующий**</span><span class="sxs-lookup"><span data-stu-id="5298a-110">**Passes**</span></span>
</dt> <dd>

<span data-ttu-id="5298a-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5298a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5298a-112">Количество проходов, выполненных методом подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="5298a-112">Number of rendering passes the technique requires.</span></span> <span data-ttu-id="5298a-113">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="5298a-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5298a-114">**Заметки**</span><span class="sxs-lookup"><span data-stu-id="5298a-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="5298a-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5298a-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5298a-116">Число заметок.</span><span class="sxs-lookup"><span data-stu-id="5298a-116">The number of annotations.</span></span> <span data-ttu-id="5298a-117">См. раздел [Добавление сведений, чтобы параметры вступили в действие с \_ заметками](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="5298a-117">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5298a-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5298a-118">Remarks</span></span>

<span data-ttu-id="5298a-119">Некоторые видеоадаптеры могут визуализировать две текстуры за один проход.</span><span class="sxs-lookup"><span data-stu-id="5298a-119">Some video cards can render two textures in a single pass.</span></span> <span data-ttu-id="5298a-120">Тем не менее, если у карточки нет этой возможности, часто можно визуализировать тот же результат в двух проходах, используя одну текстуру для каждого прохода.</span><span class="sxs-lookup"><span data-stu-id="5298a-120">However, if a card does not have this capability, it is often possible to render the same effect in two passes, using one texture for each pass.</span></span>

## <a name="requirements"></a><span data-ttu-id="5298a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="5298a-121">Requirements</span></span>



| <span data-ttu-id="5298a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="5298a-122">Requirement</span></span> | <span data-ttu-id="5298a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="5298a-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5298a-124">Header</span><span class="sxs-lookup"><span data-stu-id="5298a-124">Header</span></span><br/> | <dl> <span data-ttu-id="5298a-125"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5298a-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5298a-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5298a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5298a-127">Структуры эффектов</span><span class="sxs-lookup"><span data-stu-id="5298a-127">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
