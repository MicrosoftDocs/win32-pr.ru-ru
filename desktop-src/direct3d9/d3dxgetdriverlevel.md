---
description: Возвращает уровень драйвера.
ms.assetid: e8c85201-7850-4c8d-a124-ceb76d4e24d5
title: Функция D3DXGetDriverLevel (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDriverLevel
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 83f756f6b6ab5864f14e797879be243f871fb9e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713674"
---
# <a name="d3dxgetdriverlevel-function"></a><span data-ttu-id="85bc9-103">Функция D3DXGetDriverLevel</span><span class="sxs-lookup"><span data-stu-id="85bc9-103">D3DXGetDriverLevel function</span></span>

<span data-ttu-id="85bc9-104">Возвращает уровень драйвера.</span><span class="sxs-lookup"><span data-stu-id="85bc9-104">Returns the driver level.</span></span>

## <a name="syntax"></a><span data-ttu-id="85bc9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85bc9-105">Syntax</span></span>


```C++
UINT D3DXGetDriverLevel(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="85bc9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85bc9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85bc9-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85bc9-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85bc9-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="85bc9-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="85bc9-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство.</span><span class="sxs-lookup"><span data-stu-id="85bc9-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface representing the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85bc9-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85bc9-110">Return value</span></span>

<span data-ttu-id="85bc9-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85bc9-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85bc9-112">Уровень драйвера.</span><span class="sxs-lookup"><span data-stu-id="85bc9-112">The driver level.</span></span> <span data-ttu-id="85bc9-113">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="85bc9-113">See remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="85bc9-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="85bc9-114">Remarks</span></span>

<span data-ttu-id="85bc9-115">Этот метод возвращает версию драйвера, которая является одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="85bc9-115">This method returns the driver version, which is one of the following:</span></span>

-   <span data-ttu-id="85bc9-116">700 — драйвер уровня Direct3D 7</span><span class="sxs-lookup"><span data-stu-id="85bc9-116">700 - Direct3D 7 level driver</span></span>
-   <span data-ttu-id="85bc9-117">800-драйвер уровня Direct3D 8</span><span class="sxs-lookup"><span data-stu-id="85bc9-117">800 - Direct3D 8 level driver</span></span>
-   <span data-ttu-id="85bc9-118">900-Драйвер уровня Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="85bc9-118">900 - Direct3D 9 level driver</span></span>

## <a name="requirements"></a><span data-ttu-id="85bc9-119">Требования</span><span class="sxs-lookup"><span data-stu-id="85bc9-119">Requirements</span></span>



| <span data-ttu-id="85bc9-120">Требование</span><span class="sxs-lookup"><span data-stu-id="85bc9-120">Requirement</span></span> | <span data-ttu-id="85bc9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="85bc9-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85bc9-122">Header</span><span class="sxs-lookup"><span data-stu-id="85bc9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="85bc9-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="85bc9-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="85bc9-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="85bc9-124">Library</span></span><br/> | <dl> <span data-ttu-id="85bc9-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85bc9-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="85bc9-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85bc9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85bc9-127">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="85bc9-127">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
