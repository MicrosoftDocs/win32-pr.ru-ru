---
description: Примечание. вместо использования этой устаревшей функции рекомендуется использовать API D3DDisassemble. Эта функция, которая разбивает скомпилированный результат на текстовую строку, содержащую инструкции ассемблера и назначения регистров, является устаревшей.
ms.assetid: 218ac120-33ce-44db-84a7-99fef3281f07
title: Функция D3DX10DisassembleEffect (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleEffect
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 67fe19365616e779bd17ab689550b34737288317
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000434"
---
# <a name="d3dx10disassembleeffect-function"></a><span data-ttu-id="155bf-104">Функция D3DX10DisassembleEffect</span><span class="sxs-lookup"><span data-stu-id="155bf-104">D3DX10DisassembleEffect function</span></span>

> [!Note]  
> <span data-ttu-id="155bf-105">Вместо использования этой устаревшей функции рекомендуется использовать API [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .</span><span class="sxs-lookup"><span data-stu-id="155bf-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

<span data-ttu-id="155bf-106">Эта функция, которая разбивает скомпилированный результат на текстовую строку, содержащую инструкции ассемблера и назначения регистров, является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="155bf-106">This function -- which disassembles a compiled effect into a text string that contains assembly instructions and register assignments -- has been deprecated.</span></span> <span data-ttu-id="155bf-107">Вместо этого используйте [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span><span class="sxs-lookup"><span data-stu-id="155bf-107">Instead, use [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span></span>

## <a name="syntax"></a><span data-ttu-id="155bf-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="155bf-108">Syntax</span></span>


```C++
HRESULT D3DX10DisassembleEffect(
  _In_  ID3D10Effect *pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ ID3D10Blob   **ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="155bf-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="155bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="155bf-110">*пеффект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="155bf-110">*pEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="155bf-111">Тип: **[ **ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***</span><span class="sxs-lookup"><span data-stu-id="155bf-111">Type: **[**ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***</span></span>

<span data-ttu-id="155bf-112">Указатель на интерфейс Effect (см. [**интерфейс ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)).</span><span class="sxs-lookup"><span data-stu-id="155bf-112">A pointer to the effect interface (see [**ID3D10Effect Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)).</span></span>

</dd> <dt>

<span data-ttu-id="155bf-113">*Енаблеколоркоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="155bf-113">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="155bf-114">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="155bf-114">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="155bf-115">Включить HTML-теги в выходные данные, чтобы получить цветовой код для результата.</span><span class="sxs-lookup"><span data-stu-id="155bf-115">Include HTML tags in the output to color code the result.</span></span>

</dd> <dt>

<span data-ttu-id="155bf-116">*ппдисассембли* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="155bf-116">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="155bf-117">Тип: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="155bf-117">Type: **[**ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="155bf-118">Адрес буфера (см. [**интерфейс ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)), который содержит разсобранный результат.</span><span class="sxs-lookup"><span data-stu-id="155bf-118">Address of a buffer (see [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) which contains the disassembled effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="155bf-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="155bf-119">Return value</span></span>

<span data-ttu-id="155bf-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="155bf-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="155bf-121">Возвращает один из следующих [кодов возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="155bf-121">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="155bf-122">Требования</span><span class="sxs-lookup"><span data-stu-id="155bf-122">Requirements</span></span>



| <span data-ttu-id="155bf-123">Требование</span><span class="sxs-lookup"><span data-stu-id="155bf-123">Requirement</span></span> | <span data-ttu-id="155bf-124">Значение</span><span class="sxs-lookup"><span data-stu-id="155bf-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="155bf-125">Header</span><span class="sxs-lookup"><span data-stu-id="155bf-125">Header</span></span><br/> | <dl> <span data-ttu-id="155bf-126"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="155bf-126"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="155bf-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="155bf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="155bf-128">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="155bf-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
