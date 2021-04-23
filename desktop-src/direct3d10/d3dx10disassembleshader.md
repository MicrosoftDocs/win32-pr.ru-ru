---
description: Примечание. вместо использования этой устаревшей функции рекомендуется использовать API D3DDisassemble. Эта функция, которая разбивает Скомпилированный шейдер на текстовую строку, содержащую инструкции ассемблера и назначения регистрации, больше не существует.
ms.assetid: f94264f8-121a-4bb7-bf1f-cc5d2cac6cd2
title: Функция D3DX10DisassembleShader (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 13716fd5d25e2e8602379ea3864c516fa5388475
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674671"
---
# <a name="d3dx10disassembleshader-function"></a><span data-ttu-id="790a2-104">Функция D3DX10DisassembleShader</span><span class="sxs-lookup"><span data-stu-id="790a2-104">D3DX10DisassembleShader function</span></span>

> [!Note]  
> <span data-ttu-id="790a2-105">Вместо использования этой устаревшей функции рекомендуется использовать API [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .</span><span class="sxs-lookup"><span data-stu-id="790a2-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

<span data-ttu-id="790a2-106">Эта функция, которая разбивает Скомпилированный шейдер на текстовую строку, содержащую инструкции ассемблера и назначения регистрации, больше не существует.</span><span class="sxs-lookup"><span data-stu-id="790a2-106">This function -- which disassembles a compiled shader into a text string that contains assembly instructions and register assignments -- no longer exists.</span></span> <span data-ttu-id="790a2-107">Вместо этого используйте [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span><span class="sxs-lookup"><span data-stu-id="790a2-107">Instead, use [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span></span>

## <a name="syntax"></a><span data-ttu-id="790a2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="790a2-108">Syntax</span></span>


```C++
HRESULT D3DX10DisassembleShader(
  _In_  const void       *pShader,
  _In_        SIZE_T     BytecodeLength,
  _In_        BOOL       EnableColorCode,
  _In_        LPCSTR     pComments,
  _Out_       ID3D10Blob **ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="790a2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="790a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="790a2-110">*пшадер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="790a2-110">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="790a2-111">Тип: **константа \* void**</span><span class="sxs-lookup"><span data-stu-id="790a2-111">Type: **const void\***</span></span>

<span data-ttu-id="790a2-112">Указатель на [**Скомпилированный шейдер**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span><span class="sxs-lookup"><span data-stu-id="790a2-112">A pointer to the [**compiled shader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span></span>

</dd> <dt>

<span data-ttu-id="790a2-113">*Битекоделенгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="790a2-113">*BytecodeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="790a2-114">Type: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="790a2-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="790a2-115">Размер Пшадер.</span><span class="sxs-lookup"><span data-stu-id="790a2-115">The size of pShader.</span></span>

</dd> <dt>

<span data-ttu-id="790a2-116">*Енаблеколоркоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="790a2-116">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="790a2-117">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="790a2-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="790a2-118">Включить HTML-теги в выходные данные, чтобы получить цветовой код для результата.</span><span class="sxs-lookup"><span data-stu-id="790a2-118">Include HTML tags in the output to color code the result.</span></span>

</dd> <dt>

<span data-ttu-id="790a2-119">*пкомментс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="790a2-119">*pComments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="790a2-120">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="790a2-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="790a2-121">Строка комментария в верхней части шейдера, которая определяет константы и переменные шейдера.</span><span class="sxs-lookup"><span data-stu-id="790a2-121">The comment string at the top of the shader that identifies the shader constants and variables.</span></span>

</dd> <dt>

<span data-ttu-id="790a2-122">*ппдисассембли* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="790a2-122">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="790a2-123">Тип: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="790a2-123">Type: **[**ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="790a2-124">Адрес буфера (см. [**интерфейс ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)), который содержит десобранный шейдер.</span><span class="sxs-lookup"><span data-stu-id="790a2-124">Address of a buffer (see [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) which contains the disassembled shader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="790a2-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="790a2-125">Return value</span></span>

<span data-ttu-id="790a2-126">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="790a2-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="790a2-127">Возвращает один из следующих [кодов возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="790a2-127">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="790a2-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="790a2-128">Remarks</span></span>

<span data-ttu-id="790a2-129">Возвращаемый текст включает заголовок с версией компилятора HLSL, используемой для создания этого объекта, комментарии, описывающие макет памяти буферов констант, используемых шейдером, входными и выходными подписями, а также точками привязки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="790a2-129">This returned text includes a header with the version of the HLSL compiler used to generate this object, comments describing the memory layout of the constant buffers used by the shader, input and output signatures, and resource binding points.</span></span>

<span data-ttu-id="790a2-130">Ниже приведен пример разборки скомпилированного шейдера.</span><span class="sxs-lookup"><span data-stu-id="790a2-130">Here is an example of disassembling a compiled shader.</span></span> <span data-ttu-id="790a2-131">В этом примере предполагается, что вы начинаете с скомпилированного шейдера (показанного как *пвсбуф* , который можно увидеть в [примере HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span><span class="sxs-lookup"><span data-stu-id="790a2-131">The example assumes you start with a compiled shader (shown as *pVSBuf* which you can see in [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span></span>


```
LPCSTR commentString = NULL;
ID3D10Blob* pIDisassembly = NULL;
char* pDisassembly = NULL;
if( pVSBuf )
{
    D3D10DisassembleShader( (UINT*) pVSBuf->GetBufferPointer(), 
        pVSBuf->GetBufferSize(), TRUE, commentString, &pIDisassembly );
    if( pIDisassembly )
    {
        FILE* pFile = fopen( "shader.htm", "w" );
        if( pFile)
        {
            fputs( (char*)pIDisassembly->GetBufferPointer(), pFile );
            fclose( pFile );
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="790a2-132">Требования</span><span class="sxs-lookup"><span data-stu-id="790a2-132">Requirements</span></span>



| <span data-ttu-id="790a2-133">Требование</span><span class="sxs-lookup"><span data-stu-id="790a2-133">Requirement</span></span> | <span data-ttu-id="790a2-134">Значение</span><span class="sxs-lookup"><span data-stu-id="790a2-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="790a2-135">Header</span><span class="sxs-lookup"><span data-stu-id="790a2-135">Header</span></span><br/> | <dl> <span data-ttu-id="790a2-136"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="790a2-136"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="790a2-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="790a2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="790a2-138">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="790a2-138">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
