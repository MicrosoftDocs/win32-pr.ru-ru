---
description: Задает указатель на необязательную функцию обратного вызова, которая вычисляет процент завершенных расчетов между сферами (SH) и дает вызывающему объекту возможность прервать симулятор.
ms.assetid: 0a47610d-fa4e-4094-9adb-4fd9306b8a12
title: 'Метод ID3DXPRTEngine:: Сеткаллбакк (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetCallBack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9c2cfe710bc41ff71267e381fa0bf576688f9df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703859"
---
# <a name="id3dxprtenginesetcallback-method"></a><span data-ttu-id="c26dd-103">Метод ID3DXPRTEngine:: Сеткаллбакк</span><span class="sxs-lookup"><span data-stu-id="c26dd-103">ID3DXPRTEngine::SetCallBack method</span></span>

<span data-ttu-id="c26dd-104">Задает указатель на необязательную функцию обратного вызова, которая вычисляет процент завершенных расчетов между сферами (SH) и дает вызывающему объекту возможность прервать симулятор.</span><span class="sxs-lookup"><span data-stu-id="c26dd-104">Sets a pointer to an optional callback function that computes the percentage of spherical harmonic (SH) computations completed and gives the caller the option of aborting the simulator.</span></span>

## <a name="syntax"></a><span data-ttu-id="c26dd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c26dd-105">Syntax</span></span>


```C++
HRESULT SetCallBack(
  [in] LPD3DXSHPRTSIMCB pCB,
  [in] FLOAT            Frequency,
  [in] LPVOID           lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="c26dd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c26dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c26dd-107">*ПКБ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c26dd-107">*pCB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c26dd-108">Тип: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span><span class="sxs-lookup"><span data-stu-id="c26dd-108">Type: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span></span>

<span data-ttu-id="c26dd-109">Указатель на функцию обратного вызова [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) , которая вычисляет процент завершенных вычислений sh.</span><span class="sxs-lookup"><span data-stu-id="c26dd-109">Pointer to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function that computes the percentage of SH computations completed.</span></span> <span data-ttu-id="c26dd-110">Функция обратного вызова должна быть реализована, чтобы вернуть значение S \_ ОК для сохранения запуска симулятора.</span><span class="sxs-lookup"><span data-stu-id="c26dd-110">The callback function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="c26dd-111">Любое другое значение приведет к прерыванию симулятора.</span><span class="sxs-lookup"><span data-stu-id="c26dd-111">Any other value will abort the simulator.</span></span>

</dd> <dt>

<span data-ttu-id="c26dd-112">*Частота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c26dd-112">*Frequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c26dd-113">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c26dd-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c26dd-114">Частота вызовов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="c26dd-114">Frequency of callback calls.</span></span> <span data-ttu-id="c26dd-115">Обратная частота — приблизительно столько раз, когда будет вызываться функция обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="c26dd-115">The inverse of Frequency is approximately the number of times the callback function will be called.</span></span>

</dd> <dt>

<span data-ttu-id="c26dd-116">*лпусерконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c26dd-116">*lpUserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c26dd-117">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c26dd-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c26dd-118">Указатель на определяемое пользователем значение, которое передается функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="c26dd-118">Pointer to a user-defined value which is passed to the callback function.</span></span> <span data-ttu-id="c26dd-119">Обычно используется приложением для передачи указателя на структуру данных, которая предоставляет сведения о контексте для функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="c26dd-119">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c26dd-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c26dd-120">Return value</span></span>

<span data-ttu-id="c26dd-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c26dd-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c26dd-122">Возвращаемое значение — S \_ .</span><span class="sxs-lookup"><span data-stu-id="c26dd-122">The return value is S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="c26dd-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c26dd-123">Requirements</span></span>



| <span data-ttu-id="c26dd-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c26dd-124">Requirement</span></span> | <span data-ttu-id="c26dd-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c26dd-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c26dd-126">Header</span><span class="sxs-lookup"><span data-stu-id="c26dd-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c26dd-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c26dd-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c26dd-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c26dd-128">Library</span></span><br/> | <dl> <span data-ttu-id="c26dd-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c26dd-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c26dd-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c26dd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c26dd-131">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="c26dd-131">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
