---
description: Получает данные в буфере индекса.
ms.assetid: 8e14a047-a8a6-4763-88c7-3b439044eeb4
title: 'Метод ID3DXBaseMesh:: Жетиндексбуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5b7cf57cd8f31e54cf48ae7f0cab69a40783debe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355160"
---
# <a name="id3dxbasemeshgetindexbuffer-method"></a><span data-ttu-id="d231f-103">Метод ID3DXBaseMesh:: Жетиндексбуффер</span><span class="sxs-lookup"><span data-stu-id="d231f-103">ID3DXBaseMesh::GetIndexBuffer method</span></span>

<span data-ttu-id="d231f-104">Получает данные в буфере индекса.</span><span class="sxs-lookup"><span data-stu-id="d231f-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d231f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d231f-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a><span data-ttu-id="d231f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d231f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d231f-107">*ппиб* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d231f-107">*ppIB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d231f-108">Тип: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="d231f-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="d231f-109">Адрес указателя на интерфейс [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , представляющий объект буфера индекса, связанный с сеткой.</span><span class="sxs-lookup"><span data-stu-id="d231f-109">Address of a pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing the index buffer object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d231f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d231f-110">Return value</span></span>

<span data-ttu-id="d231f-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d231f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d231f-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d231f-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d231f-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="d231f-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d231f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d231f-114">Requirements</span></span>



| <span data-ttu-id="d231f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d231f-115">Requirement</span></span> | <span data-ttu-id="d231f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d231f-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d231f-117">Header</span><span class="sxs-lookup"><span data-stu-id="d231f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d231f-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d231f-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d231f-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d231f-119">Library</span></span><br/> | <dl> <span data-ttu-id="d231f-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d231f-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d231f-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d231f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d231f-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="d231f-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
