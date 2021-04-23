---
description: Задает объявление вершины.
ms.assetid: cbb802ac-f0ba-41e6-8c67-a787982f975f
title: 'Метод ID3DXSkinInfo:: Сетдекларатион (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 821801647ca1aee3deabe69d911bd1cab5f7eb4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354050"
---
# <a name="id3dxskininfosetdeclaration-method"></a><span data-ttu-id="88dda-103">Метод ID3DXSkinInfo:: Сетдекларатион</span><span class="sxs-lookup"><span data-stu-id="88dda-103">ID3DXSkinInfo::SetDeclaration method</span></span>

<span data-ttu-id="88dda-104">Задает объявление вершины.</span><span class="sxs-lookup"><span data-stu-id="88dda-104">Sets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="88dda-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88dda-105">Syntax</span></span>


```C++
HRESULT SetDeclaration(
  [in] const D3DVERTEXELEMENT9 *pDeclaration
);
```



## <a name="parameters"></a><span data-ttu-id="88dda-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="88dda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88dda-107">*пдекларатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="88dda-107">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88dda-108">Тип: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="88dda-108">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="88dda-109">Указатель на массив элементов [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .</span><span class="sxs-lookup"><span data-stu-id="88dda-109">Pointer to an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88dda-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88dda-110">Return value</span></span>

<span data-ttu-id="88dda-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="88dda-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="88dda-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="88dda-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="88dda-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="88dda-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="88dda-114">Требования</span><span class="sxs-lookup"><span data-stu-id="88dda-114">Requirements</span></span>



| <span data-ttu-id="88dda-115">Требование</span><span class="sxs-lookup"><span data-stu-id="88dda-115">Requirement</span></span> | <span data-ttu-id="88dda-116">Значение</span><span class="sxs-lookup"><span data-stu-id="88dda-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="88dda-117">Header</span><span class="sxs-lookup"><span data-stu-id="88dda-117">Header</span></span><br/>  | <dl> <span data-ttu-id="88dda-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="88dda-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="88dda-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="88dda-119">Library</span></span><br/> | <dl> <span data-ttu-id="88dda-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88dda-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="88dda-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88dda-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88dda-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="88dda-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="88dda-123">**ID3DXSkinInfo:: onдекларация**</span><span class="sxs-lookup"><span data-stu-id="88dda-123">**ID3DXSkinInfo::GetDeclaration**</span></span>](id3dxskininfo--getdeclaration.md)
</dt> </dl>

 

 




