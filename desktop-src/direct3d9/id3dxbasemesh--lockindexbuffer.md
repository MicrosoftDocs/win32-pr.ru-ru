---
description: Блокирует буфер индексов и получает указатель на буфер памяти буфера индекса.
ms.assetid: c8941164-1f2a-4aed-b0bd-8130aac61da4
title: 'Метод ID3DXBaseMesh:: Локкиндексбуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 388915d0d11ff910c19a2c70b305597a79cd04bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081840"
---
# <a name="id3dxbasemeshlockindexbuffer-method"></a><span data-ttu-id="f6be7-103">Метод ID3DXBaseMesh:: Локкиндексбуффер</span><span class="sxs-lookup"><span data-stu-id="f6be7-103">ID3DXBaseMesh::LockIndexBuffer method</span></span>

<span data-ttu-id="f6be7-104">Блокирует буфер индексов и получает указатель на буфер памяти буфера индекса.</span><span class="sxs-lookup"><span data-stu-id="f6be7-104">Locks an index buffer and obtains a pointer to the index buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6be7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6be7-105">Syntax</span></span>


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="f6be7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6be7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6be7-107">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6be7-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6be7-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f6be7-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f6be7-109">Сочетание флагов блокировки (ноль или более), описывающих тип выполняемой блокировки.</span><span class="sxs-lookup"><span data-stu-id="f6be7-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="f6be7-110">Для этого метода допустимы следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="f6be7-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="f6be7-111">D3DLOCK \_ отбросить</span><span class="sxs-lookup"><span data-stu-id="f6be7-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="f6be7-112">D3DLOCK \_ без \_ "грязного" \_ обновления</span><span class="sxs-lookup"><span data-stu-id="f6be7-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="f6be7-113">D3DLOCK \_ носислокк</span><span class="sxs-lookup"><span data-stu-id="f6be7-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="f6be7-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f6be7-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="f6be7-115">Описание флагов см. в разделе [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="f6be7-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6be7-116">*ппдата* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f6be7-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f6be7-117">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f6be7-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f6be7-118">Указатель типа VOID \* на буфер, содержащий данные индекса.</span><span class="sxs-lookup"><span data-stu-id="f6be7-118">VOID\* pointer to a buffer containing the index data.</span></span> <span data-ttu-id="f6be7-119">Число индексов в этом буфере будет равно [**ID3DXBaseMesh:: жетнумфацес**](id3dxbasemesh--getnumfaces.md) \* 3.</span><span class="sxs-lookup"><span data-stu-id="f6be7-119">The count of indices in this buffer will be equal to [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* 3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6be7-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6be7-120">Return value</span></span>

<span data-ttu-id="f6be7-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f6be7-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f6be7-122">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="f6be7-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f6be7-123">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="f6be7-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6be7-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6be7-124">Remarks</span></span>

<span data-ttu-id="f6be7-125">При работе с буферами индексов вы можете выполнять несколько вызовов блокировок.</span><span class="sxs-lookup"><span data-stu-id="f6be7-125">When working with index buffers, you are allowed to make multiple lock calls.</span></span> <span data-ttu-id="f6be7-126">Однако необходимо убедиться, что количество вызовов блокировок соответствует числу вызовов Unlock.</span><span class="sxs-lookup"><span data-stu-id="f6be7-126">However, you must ensure that the number of lock calls match the number of unlock calls.</span></span> <span data-ttu-id="f6be7-127">Вызовы Дравпримитиве не будут выполнены с необработанными счетчиками блокировок в любом буфере установленного индекса.</span><span class="sxs-lookup"><span data-stu-id="f6be7-127">DrawPrimitive calls will not succeed with any outstanding lock count on any currently set index buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6be7-128">Требования</span><span class="sxs-lookup"><span data-stu-id="f6be7-128">Requirements</span></span>



| <span data-ttu-id="f6be7-129">Требование</span><span class="sxs-lookup"><span data-stu-id="f6be7-129">Requirement</span></span> | <span data-ttu-id="f6be7-130">Значение</span><span class="sxs-lookup"><span data-stu-id="f6be7-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6be7-131">Header</span><span class="sxs-lookup"><span data-stu-id="f6be7-131">Header</span></span><br/>  | <dl> <span data-ttu-id="f6be7-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6be7-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f6be7-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f6be7-133">Library</span></span><br/> | <dl> <span data-ttu-id="f6be7-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6be7-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f6be7-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6be7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6be7-136">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="f6be7-136">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
