---
description: Задайте диапазон массива для передачи на устройство.
ms.assetid: 43f1c258-770c-4756-9033-e5667b379fe6
title: 'Метод ID3DXBaseEffect:: Сетаррайранже (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetArrayRange
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 59b981c1f2aff18d4bdb57f5726136945203f5fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157131"
---
# <a name="id3dxbaseeffectsetarrayrange-method"></a><span data-ttu-id="9bbdf-103">Метод ID3DXBaseEffect:: Сетаррайранже</span><span class="sxs-lookup"><span data-stu-id="9bbdf-103">ID3DXBaseEffect::SetArrayRange method</span></span>

<span data-ttu-id="9bbdf-104">Задайте диапазон массива для передачи на устройство.</span><span class="sxs-lookup"><span data-stu-id="9bbdf-104">Set the range of an array to pass to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bbdf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bbdf-105">Syntax</span></span>


```C++
HRESULT SetArrayRange(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Start,
  [in] UINT       Stop
);
```



## <a name="parameters"></a><span data-ttu-id="9bbdf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9bbdf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bbdf-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9bbdf-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bbdf-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="9bbdf-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="9bbdf-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="9bbdf-109">Unique identifier.</span></span> <span data-ttu-id="9bbdf-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="9bbdf-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="9bbdf-111">*Запуск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9bbdf-111">*Start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bbdf-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9bbdf-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9bbdf-113">Начальный индекс.</span><span class="sxs-lookup"><span data-stu-id="9bbdf-113">Start index.</span></span>

</dd> <dt>

<span data-ttu-id="9bbdf-114">*Завершение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9bbdf-114">*Stop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bbdf-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9bbdf-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9bbdf-116">Останавливает индекс.</span><span class="sxs-lookup"><span data-stu-id="9bbdf-116">Stop index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bbdf-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9bbdf-117">Return value</span></span>

<span data-ttu-id="9bbdf-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9bbdf-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9bbdf-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="9bbdf-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9bbdf-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="9bbdf-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bbdf-121">Требования</span><span class="sxs-lookup"><span data-stu-id="9bbdf-121">Requirements</span></span>



| <span data-ttu-id="9bbdf-122">Требование</span><span class="sxs-lookup"><span data-stu-id="9bbdf-122">Requirement</span></span> | <span data-ttu-id="9bbdf-123">Значение</span><span class="sxs-lookup"><span data-stu-id="9bbdf-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bbdf-124">Header</span><span class="sxs-lookup"><span data-stu-id="9bbdf-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9bbdf-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bbdf-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9bbdf-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9bbdf-126">Library</span></span><br/> | <dl> <span data-ttu-id="9bbdf-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9bbdf-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9bbdf-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9bbdf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bbdf-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="9bbdf-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
