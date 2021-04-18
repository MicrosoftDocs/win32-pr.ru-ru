---
description: Удалить кость.
ms.assetid: efb88108-5c76-47c8-b8ce-1ba29cb18ba4
title: 'Метод ID3DX10SkinInfo:: Ремовебоне (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemoveBone
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 49fd24c5661bbedb7fb839171fa4a835f07e446a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713704"
---
# <a name="id3dx10skininforemovebone-method"></a><span data-ttu-id="09319-103">Метод ID3DX10SkinInfo:: Ремовебоне</span><span class="sxs-lookup"><span data-stu-id="09319-103">ID3DX10SkinInfo::RemoveBone method</span></span>

<span data-ttu-id="09319-104">Удалить кость.</span><span class="sxs-lookup"><span data-stu-id="09319-104">Remove a bone.</span></span>

## <a name="syntax"></a><span data-ttu-id="09319-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09319-105">Syntax</span></span>


```C++
HRESULT RemoveBone(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="09319-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="09319-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09319-107">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="09319-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09319-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="09319-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="09319-109">Индекс, указывающий удаляемую кость.</span><span class="sxs-lookup"><span data-stu-id="09319-109">An index that specifies which bone to remove.</span></span> <span data-ttu-id="09319-110">Значение должно находиться в диапазоне от 0 до значения, возвращаемого [**ID3DX10SkinInfo:: жетнумбонес**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="09319-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09319-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="09319-111">Return value</span></span>

<span data-ttu-id="09319-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="09319-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="09319-113">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="09319-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="09319-114">Если метод завершается со сбоем, возвращаемое значение может быть следующим: E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="09319-114">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="09319-115">Требования</span><span class="sxs-lookup"><span data-stu-id="09319-115">Requirements</span></span>



| <span data-ttu-id="09319-116">Требование</span><span class="sxs-lookup"><span data-stu-id="09319-116">Requirement</span></span> | <span data-ttu-id="09319-117">Значение</span><span class="sxs-lookup"><span data-stu-id="09319-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09319-118">Header</span><span class="sxs-lookup"><span data-stu-id="09319-118">Header</span></span><br/>  | <dl> <span data-ttu-id="09319-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="09319-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="09319-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="09319-120">Library</span></span><br/> | <dl> <span data-ttu-id="09319-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09319-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09319-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09319-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09319-123">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="09319-123">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="09319-124">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="09319-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
