---
description: Запускает активный метод.
ms.assetid: 6598d77b-8b53-4f2d-aa43-adf358ad486d
title: 'Метод ID3DXEffect:: Begin (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.Begin
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1912698fbb6d6ac13f119161c4d05926f05d245b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273811"
---
# <a name="id3dxeffectbegin-method"></a><span data-ttu-id="63524-103">Метод ID3DXEffect:: Begin</span><span class="sxs-lookup"><span data-stu-id="63524-103">ID3DXEffect::Begin method</span></span>

<span data-ttu-id="63524-104">Запускает активный метод.</span><span class="sxs-lookup"><span data-stu-id="63524-104">Starts an active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="63524-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63524-105">Syntax</span></span>


```C++
HRESULT Begin(
  [out] UINT  *pPasses,
  [in]  DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="63524-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="63524-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63524-107">*ппассес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="63524-107">*pPasses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63524-108">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="63524-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="63524-109">Указатель на возвращаемое значение, указывающее количество проходов, необходимых для отрисовки текущего метода.</span><span class="sxs-lookup"><span data-stu-id="63524-109">Pointer to a value returned that indicates the number of passes needed to render the current technique.</span></span>

</dd> <dt>

<span data-ttu-id="63524-110">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63524-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63524-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63524-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63524-112">Параметр DWORD, определяющий сохранение и восстановление состояния, измененного в результате действия.</span><span class="sxs-lookup"><span data-stu-id="63524-112">DWORD that determines if state modified by an effect is saved and restored.</span></span> <span data-ttu-id="63524-113">Значение по умолчанию 0 указывает, что **ID3DXEffect:: Begin** и [**ID3DXEffect:: end**](id3dxeffect--end.md) сохранит и восстановит все состояния, измененные этим действием (включая константы в пикселях и шейдере вершин).</span><span class="sxs-lookup"><span data-stu-id="63524-113">The default value 0 specifies that **ID3DXEffect::Begin** and [**ID3DXEffect::End**](id3dxeffect--end.md) will save and restore all state modified by the effect (including pixel and vertex shader constants).</span></span> <span data-ttu-id="63524-114">Допустимые флаги можно увидеть на странице [Флаги сохранения и восстановления состояния влияния](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="63524-114">Valid flags can be seen at [Effect State Save and Restore Flags](d3dxfx.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63524-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63524-115">Return value</span></span>

<span data-ttu-id="63524-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="63524-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="63524-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="63524-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="63524-118">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="63524-118">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="63524-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63524-119">Remarks</span></span>

<span data-ttu-id="63524-120">Приложение устанавливает один активный метод в системе эффектов, вызывая **ID3DXEffect:: Begin**.</span><span class="sxs-lookup"><span data-stu-id="63524-120">An application sets one active technique in the effect system by calling **ID3DXEffect::Begin**.</span></span> <span data-ttu-id="63524-121">Система влияния отвечает, записывая все состояния конвейера, которые могут быть изменены методом в блоке состояния.</span><span class="sxs-lookup"><span data-stu-id="63524-121">The effect system responds by capturing all the pipeline state that can be changed by the technique in a state block.</span></span> <span data-ttu-id="63524-122">Приложение сигнализирует об окончании приемки, вызвав [**ID3DXEffect:: end**](id3dxeffect--end.md), который использует блок состояния для восстановления исходного состояния.</span><span class="sxs-lookup"><span data-stu-id="63524-122">An application signals the end of a technique by calling [**ID3DXEffect::End**](id3dxeffect--end.md), which uses the state block to restore the original state.</span></span> <span data-ttu-id="63524-123">Таким образом, система эффектов выполняет сохранение состояния, когда прием становится активным, и восстанавливает состояние при завершении метода.</span><span class="sxs-lookup"><span data-stu-id="63524-123">The effect system, therefore, takes care of saving state when a technique becomes active and restoring state when a technique ends.</span></span> <span data-ttu-id="63524-124">Если вы решили отключить эту функцию сохранения и восстановления, см. раздел [D3DXFX \_ донотсавесамплерстате](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="63524-124">If you choose to disable this save and restore functionality, see [D3DXFX\_DONOTSAVESAMPLERSTATE](d3dxfx.md).</span></span>

<span data-ttu-id="63524-125">В паре **ID3DXEffect:: Begin** и [**ID3DXEffect:: end**](id3dxeffect--end.md) приложение использует [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md) для установки активного прохода, [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) , если после активации прохода возникли какие либо изменения состояния, и [**ID3DXEffect:: ендпасс**](id3dxeffect--endpass.md) , чтобы завершить активный проход.</span><span class="sxs-lookup"><span data-stu-id="63524-125">Within the **ID3DXEffect::Begin** and [**ID3DXEffect::End**](id3dxeffect--end.md) pair, an application uses [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) to set the active pass, [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) if any state changes occurred after the pass was activated, and [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) to end the active pass.</span></span>

## <a name="requirements"></a><span data-ttu-id="63524-126">Требования</span><span class="sxs-lookup"><span data-stu-id="63524-126">Requirements</span></span>



| <span data-ttu-id="63524-127">Требование</span><span class="sxs-lookup"><span data-stu-id="63524-127">Requirement</span></span> | <span data-ttu-id="63524-128">Значение</span><span class="sxs-lookup"><span data-stu-id="63524-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="63524-129">Header</span><span class="sxs-lookup"><span data-stu-id="63524-129">Header</span></span><br/>  | <dl> <span data-ttu-id="63524-130"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="63524-130"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="63524-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="63524-131">Library</span></span><br/> | <dl> <span data-ttu-id="63524-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63524-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="63524-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63524-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63524-134">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="63524-134">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
