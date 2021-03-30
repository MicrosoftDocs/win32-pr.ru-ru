---
description: Выделение пространства для дополнительных костей.
ms.assetid: f2acd338-f2c2-4340-a673-f36940cf31d9
title: 'Метод ID3DX10SkinInfo:: Аддбонес (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddBones
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4bf9667bd25dd717c4da96c2150e7bd7c45964f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354940"
---
# <a name="id3dx10skininfoaddbones-method"></a><span data-ttu-id="c1276-103">Метод ID3DX10SkinInfo:: Аддбонес</span><span class="sxs-lookup"><span data-stu-id="c1276-103">ID3DX10SkinInfo::AddBones method</span></span>

<span data-ttu-id="c1276-104">Выделение пространства для дополнительных костей.</span><span class="sxs-lookup"><span data-stu-id="c1276-104">Allocate space for more bones.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1276-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1276-105">Syntax</span></span>


```C++
HRESULT AddBones(
  [in] UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="c1276-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1276-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1276-107">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1276-107">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1276-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1276-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c1276-109">Число добавляемых костей.</span><span class="sxs-lookup"><span data-stu-id="c1276-109">The number of bones to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1276-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1276-110">Return value</span></span>

<span data-ttu-id="c1276-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c1276-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c1276-112">Если этот метод завершился успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c1276-112">If this method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c1276-113">Если метод завершается со сбоем, возвращаемое значение может быть следующим: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c1276-113">If the method fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1276-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c1276-114">Requirements</span></span>



| <span data-ttu-id="c1276-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c1276-115">Requirement</span></span> | <span data-ttu-id="c1276-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c1276-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1276-117">Header</span><span class="sxs-lookup"><span data-stu-id="c1276-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c1276-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1276-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c1276-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c1276-119">Library</span></span><br/> | <dl> <span data-ttu-id="c1276-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1276-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1276-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1276-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1276-122">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="c1276-122">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="c1276-123">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="c1276-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
