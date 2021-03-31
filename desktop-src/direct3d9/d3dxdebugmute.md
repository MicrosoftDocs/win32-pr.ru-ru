---
description: Включает или выключает все выходные данные отладки D3DX.
ms.assetid: e35cbfd2-401e-47ec-9f5b-e2ed63ea1fcd
title: Функция D3DXDebugMute (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDebugMute
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9259fa43a6a64829e42cbaa661aa7223a958f22d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273783"
---
# <a name="d3dxdebugmute-function"></a><span data-ttu-id="86acb-103">Функция D3DXDebugMute</span><span class="sxs-lookup"><span data-stu-id="86acb-103">D3DXDebugMute function</span></span>

<span data-ttu-id="86acb-104">Включает или выключает все выходные данные отладки D3DX.</span><span class="sxs-lookup"><span data-stu-id="86acb-104">Turns on or off all D3DX debug output.</span></span>

## <a name="syntax"></a><span data-ttu-id="86acb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86acb-105">Syntax</span></span>


```C++
BOOL D3DXDebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a><span data-ttu-id="86acb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="86acb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86acb-107">*Отключить звук* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="86acb-107">*Mute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86acb-108">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="86acb-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="86acb-109">Если **значение — true**, выходные данные отладчика прерываются; Если **значение равно false**, выходные данные отладки включены.</span><span class="sxs-lookup"><span data-stu-id="86acb-109">If **TRUE**, debugger output is halted; if **FALSE**, debug output is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86acb-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86acb-110">Return value</span></span>

<span data-ttu-id="86acb-111">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="86acb-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="86acb-112">Возвращает предыдущее значение звука.</span><span class="sxs-lookup"><span data-stu-id="86acb-112">Returns the previous value of Mute.</span></span>

## <a name="requirements"></a><span data-ttu-id="86acb-113">Требования</span><span class="sxs-lookup"><span data-stu-id="86acb-113">Requirements</span></span>



| <span data-ttu-id="86acb-114">Требование</span><span class="sxs-lookup"><span data-stu-id="86acb-114">Requirement</span></span> | <span data-ttu-id="86acb-115">Значение</span><span class="sxs-lookup"><span data-stu-id="86acb-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86acb-116">Header</span><span class="sxs-lookup"><span data-stu-id="86acb-116">Header</span></span><br/>  | <dl> <span data-ttu-id="86acb-117"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="86acb-117"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="86acb-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="86acb-118">Library</span></span><br/> | <dl> <span data-ttu-id="86acb-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86acb-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="86acb-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86acb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86acb-121">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="86acb-121">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
