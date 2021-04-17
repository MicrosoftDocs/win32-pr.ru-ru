---
description: Используется для распаковки закодированных данных. Обычно это используется для загрузки ресурсов из файловых систем, таких как ZIP-файлы. При загрузке из несжатого ресурса стадия распаковки не должна выполнять никаких действий.
ms.assetid: 7f7e3ffd-8dac-403f-813b-d6d21d146fa7
title: 'ID3DX10DataLoader: метод:D екомпресс (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader.Decompress
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e6f711722852cba4b671cc84416055d279fd7cc6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694173"
---
# <a name="id3dx10dataloaderdecompress-method"></a><span data-ttu-id="54863-105">ID3DX10DataLoader: метод:D екомпресс</span><span class="sxs-lookup"><span data-stu-id="54863-105">ID3DX10DataLoader::Decompress method</span></span>

<span data-ttu-id="54863-106">Используется для распаковки закодированных данных.</span><span class="sxs-lookup"><span data-stu-id="54863-106">Used to decompress encoded data.</span></span> <span data-ttu-id="54863-107">Обычно это используется для загрузки ресурсов из файловых систем, таких как ZIP-файлы.</span><span class="sxs-lookup"><span data-stu-id="54863-107">Typically this would be used to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="54863-108">При загрузке из несжатого ресурса стадия распаковки не должна выполнять никаких действий.</span><span class="sxs-lookup"><span data-stu-id="54863-108">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span>

## <a name="syntax"></a><span data-ttu-id="54863-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54863-109">Syntax</span></span>


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a><span data-ttu-id="54863-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="54863-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54863-111">*ппдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="54863-111">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54863-112">Тип: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="54863-112">Type: **void\*\***</span></span>

<span data-ttu-id="54863-113">Указатель на необработанные данные для распаковки.</span><span class="sxs-lookup"><span data-stu-id="54863-113">Pointer to the raw data to decompress.</span></span>

</dd> <dt>

<span data-ttu-id="54863-114">*пкбитес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="54863-114">*pcBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54863-115">Type: **[ **size \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="54863-115">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="54863-116">Размер данных, на которые указывает Ппдата.</span><span class="sxs-lookup"><span data-stu-id="54863-116">The size of the data pointed to by ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54863-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54863-117">Return value</span></span>

<span data-ttu-id="54863-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="54863-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="54863-119">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="54863-119">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="54863-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54863-120">Remarks</span></span>

<span data-ttu-id="54863-121">[**Интерфейс ID3DX10DataLoader**](id3dx10dataloader.md) может быть унаследован и его члены переопределяются.</span><span class="sxs-lookup"><span data-stu-id="54863-121">[**ID3DX10DataLoader Interface**](id3dx10dataloader.md) can be inherited and its members redefined.</span></span> <span data-ttu-id="54863-122">Распаковку можно переопределить для поддержки собственных пользовательских форматов файлов.</span><span class="sxs-lookup"><span data-stu-id="54863-122">Decompress could be redefined to support your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="54863-123">Требования</span><span class="sxs-lookup"><span data-stu-id="54863-123">Requirements</span></span>



| <span data-ttu-id="54863-124">Требование</span><span class="sxs-lookup"><span data-stu-id="54863-124">Requirement</span></span> | <span data-ttu-id="54863-125">Значение</span><span class="sxs-lookup"><span data-stu-id="54863-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54863-126">Header</span><span class="sxs-lookup"><span data-stu-id="54863-126">Header</span></span><br/>  | <dl> <span data-ttu-id="54863-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="54863-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="54863-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="54863-128">Library</span></span><br/> | <dl> <span data-ttu-id="54863-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54863-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54863-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54863-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54863-131">ID3DX10DataLoader</span><span class="sxs-lookup"><span data-stu-id="54863-131">ID3DX10DataLoader</span></span>](id3dx10dataloader.md)
</dt> <dt>

[<span data-ttu-id="54863-132">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="54863-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
