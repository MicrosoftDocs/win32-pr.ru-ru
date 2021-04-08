---
description: Сохраняет сжатый предварительно вычисленный радианце передаваемой (PRT) буфер на диск.
ms.assetid: cc94a83e-f755-411d-a993-4529c5d53cd5
title: Функция D3DXSavePRTCompBufferToFile (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTCompBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d06629185637ce6fa0d7d33d5454282d2bbb8ec2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000352"
---
# <a name="d3dxsaveprtcompbuffertofile-function"></a><span data-ttu-id="68fac-103">Функция D3DXSavePRTCompBufferToFile</span><span class="sxs-lookup"><span data-stu-id="68fac-103">D3DXSavePRTCompBufferToFile function</span></span>

<span data-ttu-id="68fac-104">Сохраняет сжатый предварительно вычисленный радианце передаваемой (PRT) буфер на диск.</span><span class="sxs-lookup"><span data-stu-id="68fac-104">Saves a compressed precomputed radiance transfer (PRT) buffer to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="68fac-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68fac-105">Syntax</span></span>

```cpp
HRESULT D3DXSavePRTCompBufferToFile(
  _In_ LPCSTR              pFileName,
  _In_ LPD3DXPRTCOMPBUFFER pBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="68fac-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="68fac-106">Parameters</span></span>

<span data-ttu-id="68fac-107">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68fac-107">*pFileName* \[in\]</span></span>

<span data-ttu-id="68fac-108">Тип: **[LPCSTR](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68fac-108">Type: **[LPCSTR](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68fac-109">Имя файла, в который будет сохранен сжатый буфер.</span><span class="sxs-lookup"><span data-stu-id="68fac-109">Name of the file to which the compressed buffer is to be saved.</span></span>

<span data-ttu-id="68fac-110">*pBuffer* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68fac-110">*pBuffer* \[in\]</span></span>

<span data-ttu-id="68fac-111">Тип: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="68fac-111">Type: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**</span></span>

<span data-ttu-id="68fac-112">Адрес указателя на входной объект [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="68fac-112">Address of a pointer to the input [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="68fac-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68fac-113">Return value</span></span>

<span data-ttu-id="68fac-114">Тип: **[HRESULT](../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="68fac-114">Type: **[HRESULT](../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="68fac-115">Если метод выполнен успешно, возвращается значение **D3D \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="68fac-115">If the method succeeds, then the return value is **D3D\_OK**.</span></span> <span data-ttu-id="68fac-116">В случае сбоя метода возвращаемое значение может быть **D3DERR \_ инвалидкалл**.</span><span class="sxs-lookup"><span data-stu-id="68fac-116">If the method fails, then the return value can be **D3DERR\_INVALIDCALL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="68fac-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68fac-117">Remarks</span></span>

<span data-ttu-id="68fac-118">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="68fac-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="68fac-119">Если определен Юникод, вызов функции разрешается в [D3DXSavePRTCompBufferToFileW]().</span><span class="sxs-lookup"><span data-stu-id="68fac-119">If Unicode is defined, then the function call resolves to [D3DXSavePRTCompBufferToFileW]().</span></span> <span data-ttu-id="68fac-120">В противном случае вызов функции разрешается в **D3DXSavePRTCompBufferToFileA**.</span><span class="sxs-lookup"><span data-stu-id="68fac-120">Otherwise, the function call resolves to **D3DXSavePRTCompBufferToFileA**.</span></span>

<span data-ttu-id="68fac-121">Формат файла PCA представляет собой двоичный файл в виде заголовка, а затем два или три блока данных.</span><span class="sxs-lookup"><span data-stu-id="68fac-121">The PCA file format is a binary file in the form of a header and then two or three data blocks.</span></span>

```cpp
struct PRTCompressHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
    UINT NumClusters;
    UINT NumPCA;
};
```

<span data-ttu-id="68fac-122">В случае, если *бистекс* не равен нулю, *нумсамплес* должен равняться `TexWidth * TexHeight` .</span><span class="sxs-lookup"><span data-stu-id="68fac-122">For the case of *bIsTex* being non-zero, *NumSamples* should equal `TexWidth * TexHeight`.</span></span>

<span data-ttu-id="68fac-123">Базовый блок данных, следующий за заголовком, — это `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` байты.</span><span class="sxs-lookup"><span data-stu-id="68fac-123">The basis data block that follows the header is `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` bytes.</span></span>

<span data-ttu-id="68fac-124">Ниже приведен блок данных веса PCA, который представляет собой `NumPCA * NumSamples * sizeof(float)` байты.</span><span class="sxs-lookup"><span data-stu-id="68fac-124">Following that is the PCA weights data block, which is `NumPCA * NumSamples * sizeof(float)` bytes.</span></span>

<span data-ttu-id="68fac-125">Если *нумклустерс* больше 1, то файл заканчивается блоком данных идентификаторов кластеров (байт) `NumSamples * sizeof(UINT)` .</span><span class="sxs-lookup"><span data-stu-id="68fac-125">If *NumClusters* is greater than 1, then the file ends with the cluster IDs data block of `NumSamples * sizeof(UINT)` bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="68fac-126">Требования</span><span class="sxs-lookup"><span data-stu-id="68fac-126">Requirements</span></span>

| <span data-ttu-id="68fac-127">Требование</span><span class="sxs-lookup"><span data-stu-id="68fac-127">Requirement</span></span> | <span data-ttu-id="68fac-128">Значение</span><span class="sxs-lookup"><span data-stu-id="68fac-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68fac-129">Header</span><span class="sxs-lookup"><span data-stu-id="68fac-129">Header</span></span><br/>  | <dl> <span data-ttu-id="68fac-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="68fac-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="68fac-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="68fac-131">Library</span></span><br/> | <dl> <span data-ttu-id="68fac-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68fac-132"><dt>D3dx9.lib</dt></span></span> </dl>   |

## <a name="see-also"></a><span data-ttu-id="68fac-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68fac-133">See also</span></span>

[<span data-ttu-id="68fac-134">Предварительно вычисленные функции пересылки Радианце</span><span class="sxs-lookup"><span data-stu-id="68fac-134">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
