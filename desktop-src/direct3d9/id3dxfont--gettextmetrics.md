---
description: Получает характеристики шрифта, определенные в структуре ТЕКСТМЕТРИК. Этот метод поддерживает параметры компилятора ANSI и Unicode.
ms.assetid: 37788281-5bb0-45bb-b6d4-bdc4d811e3af
title: 'Метод ID3DXFont:: Жеттекстметрикс (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetTextMetrics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ce6064804d2aac2846cbea6971f145fc07759f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354763"
---
# <a name="id3dxfontgettextmetrics-method"></a><span data-ttu-id="4d4bc-104">Метод ID3DXFont:: Жеттекстметрикс</span><span class="sxs-lookup"><span data-stu-id="4d4bc-104">ID3DXFont::GetTextMetrics method</span></span>

<span data-ttu-id="4d4bc-105">Получает характеристики шрифта, определенные в структуре [**текстметрик**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) .</span><span class="sxs-lookup"><span data-stu-id="4d4bc-105">Retrieves font characteristics that are identified in a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.</span></span> <span data-ttu-id="4d4bc-106">Этот метод поддерживает параметры компилятора ANSI и Unicode.</span><span class="sxs-lookup"><span data-stu-id="4d4bc-106">This method supports ANSI and Unicode compiler settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d4bc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d4bc-107">Syntax</span></span>


```C++
BOOL GetTextMetrics(
  [out] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="4d4bc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d4bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d4bc-109">*птекстметрикс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4d4bc-109">*pTextMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d4bc-110">Тип: **[ **текстметрик**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***</span><span class="sxs-lookup"><span data-stu-id="4d4bc-110">Type: **[**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***</span></span>

<span data-ttu-id="4d4bc-111">Указатель на структуру [**текстметрик**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) , которая содержит свойства шрифта.</span><span class="sxs-lookup"><span data-stu-id="4d4bc-111">Pointer to a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure, which contains font properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d4bc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4d4bc-112">Return value</span></span>

<span data-ttu-id="4d4bc-113">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4d4bc-113">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4d4bc-114">Ненулевое значение, если функция выполнена успешно; в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="4d4bc-114">Nonzero if the function is successful; otherwise 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d4bc-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4d4bc-115">Remarks</span></span>

<span data-ttu-id="4d4bc-116">Параметр компилятора также определяет тип структуры.</span><span class="sxs-lookup"><span data-stu-id="4d4bc-116">The compiler setting also determines the structure type.</span></span> <span data-ttu-id="4d4bc-117">Если определен Юникод, функция возвращает структуру ТЕКСТМЕТРИКВ.</span><span class="sxs-lookup"><span data-stu-id="4d4bc-117">If Unicode is defined, the function returns a TEXTMETRICW structure.</span></span> <span data-ttu-id="4d4bc-118">В противном случае вызов функции возвращает структуру ТЕКСТМЕТРИКА.</span><span class="sxs-lookup"><span data-stu-id="4d4bc-118">Otherwise, the function call returns a TEXTMETRICA structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d4bc-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4d4bc-119">Requirements</span></span>



| <span data-ttu-id="4d4bc-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4d4bc-120">Requirement</span></span> | <span data-ttu-id="4d4bc-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4d4bc-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d4bc-122">Header</span><span class="sxs-lookup"><span data-stu-id="4d4bc-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4d4bc-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d4bc-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="4d4bc-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4d4bc-124">Library</span></span><br/> | <dl> <span data-ttu-id="4d4bc-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d4bc-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4d4bc-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d4bc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d4bc-127">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="4d4bc-127">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
