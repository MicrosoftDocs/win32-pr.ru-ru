---
description: Сохраняет предварительно вычисленный буфер радианценой пересылки (PRT) на диск.
ms.assetid: 1fca69bd-6729-45af-981f-b7480c741bc2
title: Функция D3DXSavePRTBufferToFile (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b796ee24be44bf65be7df938bdfe85d6784cc5f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694134"
---
# <a name="d3dxsaveprtbuffertofile-function"></a><span data-ttu-id="0fd13-103">Функция D3DXSavePRTBufferToFile</span><span class="sxs-lookup"><span data-stu-id="0fd13-103">D3DXSavePRTBufferToFile function</span></span>

<span data-ttu-id="0fd13-104">Сохраняет предварительно вычисленный буфер радианценой пересылки (PRT) на диск.</span><span class="sxs-lookup"><span data-stu-id="0fd13-104">Saves a precomputed radiance transfer (PRT) buffer to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd13-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0fd13-105">Syntax</span></span>

```cpp
HRESULT D3DXSavePRTBufferToFile(
  _In_ LPCSTR          pFileName,
  _In_ LPD3DXPRTBUFFER pBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="0fd13-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0fd13-106">Parameters</span></span>

<span data-ttu-id="0fd13-107">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0fd13-107">*pFileName* \[in\]</span></span>

<span data-ttu-id="0fd13-108">Тип: **[LPCSTR](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0fd13-108">Type: **[LPCSTR](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0fd13-109">Имя файла, в который будет сохранен буфер.</span><span class="sxs-lookup"><span data-stu-id="0fd13-109">Name of the file to which the buffer is to be saved.</span></span>

<span data-ttu-id="0fd13-110">*pBuffer* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0fd13-110">*pBuffer* \[in\]</span></span>

<span data-ttu-id="0fd13-111">Тип: **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="0fd13-111">Type: **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="0fd13-112">Адрес указателя на входной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="0fd13-112">Address of a pointer to the input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="0fd13-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0fd13-113">Return value</span></span>

<span data-ttu-id="0fd13-114">Тип: **[HRESULT](../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="0fd13-114">Type: **[HRESULT](../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="0fd13-115">Если метод выполнен успешно, возвращается значение **D3D \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="0fd13-115">If the method succeeds, the return value is **D3D\_OK**.</span></span> <span data-ttu-id="0fd13-116">В случае сбоя метода возвращаемое значение может быть **D3DERR \_ инвалидкалл**.</span><span class="sxs-lookup"><span data-stu-id="0fd13-116">If the method fails, the return value can be **D3DERR\_INVALIDCALL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fd13-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0fd13-117">Remarks</span></span>

<span data-ttu-id="0fd13-118">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="0fd13-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="0fd13-119">Если определен Юникод, вызов функции разрешается в [D3DXSavePRTBufferToFileW]().</span><span class="sxs-lookup"><span data-stu-id="0fd13-119">If Unicode is defined, then the function call resolves to [D3DXSavePRTBufferToFileW]().</span></span> <span data-ttu-id="0fd13-120">В противном случае вызов функции разрешается в **D3DXSavePRTBufferToFileA**.</span><span class="sxs-lookup"><span data-stu-id="0fd13-120">Otherwise, the function call resolves to **D3DXSavePRTBufferToFileA**.</span></span>

<span data-ttu-id="0fd13-121">Формат файла PRT представляет собой двоичный файл в виде заголовка, а затем блок данных.</span><span class="sxs-lookup"><span data-stu-id="0fd13-121">The PRT file format is a binary file in the form of a header and then a data block.</span></span>

```cpp
struct PRTHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
};
```

<span data-ttu-id="0fd13-122">В случае, если *бистекс* не равен нулю, *нумсамплес* должен равняться `TexWidth * TexHeight` .</span><span class="sxs-lookup"><span data-stu-id="0fd13-122">For the case of *bIsTex* being non-zero, *NumSamples* should equal `TexWidth * TexHeight`.</span></span>

<span data-ttu-id="0fd13-123">Блок данных, следующий за заголовком, — это `NumSamples * NumCoeffs * NumChannels * sizeof(float)` байты.</span><span class="sxs-lookup"><span data-stu-id="0fd13-123">The data block that follows the header is `NumSamples * NumCoeffs * NumChannels * sizeof(float)` bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fd13-124">Требования</span><span class="sxs-lookup"><span data-stu-id="0fd13-124">Requirements</span></span>

| <span data-ttu-id="0fd13-125">Требование</span><span class="sxs-lookup"><span data-stu-id="0fd13-125">Requirement</span></span> | <span data-ttu-id="0fd13-126">Значение</span><span class="sxs-lookup"><span data-stu-id="0fd13-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd13-127">Header</span><span class="sxs-lookup"><span data-stu-id="0fd13-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0fd13-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fd13-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0fd13-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0fd13-129">Library</span></span><br/> | <dl> <span data-ttu-id="0fd13-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0fd13-130"><dt>D3dx9.lib</dt></span></span> </dl>   |

## <a name="see-also"></a><span data-ttu-id="0fd13-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0fd13-131">See also</span></span>

[<span data-ttu-id="0fd13-132">Предварительно вычисленные функции пересылки Радианце</span><span class="sxs-lookup"><span data-stu-id="0fd13-132">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
