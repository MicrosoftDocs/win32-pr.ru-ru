---
description: Блокирует буфер вершин и получает указатель на память буфера вершин.
ms.assetid: afcd479c-b268-4720-b26c-88b82f1aab08
title: 'Метод ID3DXBaseMesh:: Локквертексбуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2e93e59715d9f262d7693f2bef652f8be63337f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713740"
---
# <a name="id3dxbasemeshlockvertexbuffer-method"></a><span data-ttu-id="68058-103">Метод ID3DXBaseMesh:: Локквертексбуффер</span><span class="sxs-lookup"><span data-stu-id="68058-103">ID3DXBaseMesh::LockVertexBuffer method</span></span>

<span data-ttu-id="68058-104">Блокирует буфер вершин и получает указатель на память буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="68058-104">Locks a vertex buffer and obtains a pointer to the vertex buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="68058-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68058-105">Syntax</span></span>


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="68058-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="68058-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68058-107">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68058-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68058-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68058-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68058-109">Сочетание флагов блокировки (ноль или более), описывающих тип выполняемой блокировки.</span><span class="sxs-lookup"><span data-stu-id="68058-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="68058-110">Для этого метода допустимы следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="68058-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="68058-111">D3DLOCK \_ отбросить</span><span class="sxs-lookup"><span data-stu-id="68058-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="68058-112">D3DLOCK \_ без \_ "грязного" \_ обновления</span><span class="sxs-lookup"><span data-stu-id="68058-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="68058-113">D3DLOCK \_ носислокк</span><span class="sxs-lookup"><span data-stu-id="68058-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="68058-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="68058-114">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="68058-115">D3DLOCK \_ нуверврите</span><span class="sxs-lookup"><span data-stu-id="68058-115">D3DLOCK\_NOOVERWRITE</span></span>

<span data-ttu-id="68058-116">Описание флагов см. в разделе [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="68058-116">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="68058-117">*ппдата* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="68058-117">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="68058-118">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="68058-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="68058-119">Указатель типа VOID \* на буфер, содержащий данные вершин.</span><span class="sxs-lookup"><span data-stu-id="68058-119">VOID\* pointer to a buffer containing the vertex data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68058-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68058-120">Return value</span></span>

<span data-ttu-id="68058-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="68058-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="68058-122">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="68058-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="68058-123">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="68058-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="68058-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68058-124">Remarks</span></span>

<span data-ttu-id="68058-125">При работе с буферами вершин вы можете выполнять несколько вызовов блокировки. Однако необходимо убедиться, что количество вызовов блокировок соответствует числу вызовов Unlock.</span><span class="sxs-lookup"><span data-stu-id="68058-125">When working with vertex buffers, you are allowed to make multiple lock calls; however, you must ensure that the number of lock calls match the number of unlock calls.</span></span> <span data-ttu-id="68058-126">Вызовы Дравпримитиве не будут выполнены с необработанными счетчиками блокировок в любом заданном в данный момент буфере вершин.</span><span class="sxs-lookup"><span data-stu-id="68058-126">DrawPrimitive calls will not succeed with any outstanding lock count on any currently set vertex buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="68058-127">Требования</span><span class="sxs-lookup"><span data-stu-id="68058-127">Requirements</span></span>



| <span data-ttu-id="68058-128">Требование</span><span class="sxs-lookup"><span data-stu-id="68058-128">Requirement</span></span> | <span data-ttu-id="68058-129">Значение</span><span class="sxs-lookup"><span data-stu-id="68058-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68058-130">Header</span><span class="sxs-lookup"><span data-stu-id="68058-130">Header</span></span><br/>  | <dl> <span data-ttu-id="68058-131"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="68058-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="68058-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="68058-132">Library</span></span><br/> | <dl> <span data-ttu-id="68058-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68058-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="68058-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68058-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68058-135">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="68058-135">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
