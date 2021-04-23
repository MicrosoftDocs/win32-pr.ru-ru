---
title: Метод распаковки ID3DX11DataLoader (D3DX11core. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Распаковывает закодированные данные.
ms.assetid: 68579c86-9f77-444b-86b3-746cff745be8
keywords:
- Метод распаковки Direct3D 11
- Распаковка метода Direct3D 11, интерфейс ID3DX11DataLoader
- Интерфейс ID3DX11DataLoader Direct3D 11, метод unуплотнения
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Decompress
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b515eb38fb70fc31f0bbd0d02e20dcfb9f66ea5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000520"
---
# <a name="id3dx11dataloaderdecompress-method"></a><span data-ttu-id="40581-107">ID3DX11DataLoader: метод:D екомпресс</span><span class="sxs-lookup"><span data-stu-id="40581-107">ID3DX11DataLoader::Decompress method</span></span>

> [!Note]  
> <span data-ttu-id="40581-108">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="40581-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="40581-109">Распаковывает закодированные данные.</span><span class="sxs-lookup"><span data-stu-id="40581-109">Decompresses encoded data.</span></span>

## <a name="syntax"></a><span data-ttu-id="40581-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40581-110">Syntax</span></span>


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a><span data-ttu-id="40581-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="40581-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40581-112">*ппдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="40581-112">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40581-113">Тип: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="40581-113">Type: **void\*\***</span></span>

<span data-ttu-id="40581-114">Указатель на необработанные данные для распаковки.</span><span class="sxs-lookup"><span data-stu-id="40581-114">Pointer to the raw data to decompress.</span></span>

</dd> <dt>

<span data-ttu-id="40581-115">*пкбитес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="40581-115">*pcBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40581-116">Type: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="40581-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="40581-117">Размер данных, на которые указывает Ппдата.</span><span class="sxs-lookup"><span data-stu-id="40581-117">The size of the data pointed to by ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40581-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="40581-118">Return value</span></span>

<span data-ttu-id="40581-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="40581-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="40581-120">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="40581-120">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="40581-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="40581-121">Remarks</span></span>

<span data-ttu-id="40581-122">Используйте этот метод для загрузки ресурсов из файловых систем, таких как ZIP-файлы.</span><span class="sxs-lookup"><span data-stu-id="40581-122">Use this method to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="40581-123">При загрузке из несжатого ресурса стадия распаковки не должна выполнять никаких действий.</span><span class="sxs-lookup"><span data-stu-id="40581-123">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span>

<span data-ttu-id="40581-124">[**Интерфейс ID3DX11DataLoader**](id3dx11dataloader.md) может быть унаследован и его члены переопределяются для поддержки пользовательских форматов файлов.</span><span class="sxs-lookup"><span data-stu-id="40581-124">[**ID3DX11DataLoader Interface**](id3dx11dataloader.md) can be inherited and its members redefined to support custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="40581-125">Требования</span><span class="sxs-lookup"><span data-stu-id="40581-125">Requirements</span></span>



| <span data-ttu-id="40581-126">Требование</span><span class="sxs-lookup"><span data-stu-id="40581-126">Requirement</span></span> | <span data-ttu-id="40581-127">Значение</span><span class="sxs-lookup"><span data-stu-id="40581-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40581-128">Header</span><span class="sxs-lookup"><span data-stu-id="40581-128">Header</span></span><br/>  | <dl> <span data-ttu-id="40581-129"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="40581-129"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="40581-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="40581-130">Library</span></span><br/> | <dl> <span data-ttu-id="40581-131"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40581-131"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="40581-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40581-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40581-133">ID3DX11DataLoader</span><span class="sxs-lookup"><span data-stu-id="40581-133">ID3DX11DataLoader</span></span>](id3dx11dataloader.md)
</dt> <dt>

[<span data-ttu-id="40581-134">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="40581-134">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

