---
description: Получение характеристик шрифта.
ms.assetid: ef7e0d18-492b-476b-945a-bfc0232a939a
title: 'Метод ID3DX10Font:: Жеттекстметрикс (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetTextMetrics
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72decdcf0a9573f7ad8ba0f4e363df6df3599477
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547943"
---
# <a name="id3dx10fontgettextmetrics-method"></a><span data-ttu-id="1d7a5-103">Метод ID3DX10Font:: Жеттекстметрикс</span><span class="sxs-lookup"><span data-stu-id="1d7a5-103">ID3DX10Font::GetTextMetrics method</span></span>

<span data-ttu-id="1d7a5-104">Получение характеристик шрифта.</span><span class="sxs-lookup"><span data-stu-id="1d7a5-104">Retrieve font characteristics.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d7a5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d7a5-105">Syntax</span></span>


```C++
BOOL GetTextMetrics(
  [in] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="1d7a5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d7a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d7a5-107">*птекстметрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1d7a5-107">*pTextMetrics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d7a5-108">Тип: **текстметрик \***</span><span class="sxs-lookup"><span data-stu-id="1d7a5-108">Type: **TEXTMETRIC\***</span></span>

<span data-ttu-id="1d7a5-109">Указатель на структуру [текстметрик](/previous-versions//ms534202(v=vs.85)) , которая содержит свойства шрифта.</span><span class="sxs-lookup"><span data-stu-id="1d7a5-109">Pointer to a [TEXTMETRIC](/previous-versions//ms534202(v=vs.85)) structure, which contains font properties.</span></span> <span data-ttu-id="1d7a5-110">Если определен Юникод, функция возвращает структуру ТЕКСТМЕТРИКВ.</span><span class="sxs-lookup"><span data-stu-id="1d7a5-110">If Unicode is defined, the function returns a TEXTMETRICW structure.</span></span> <span data-ttu-id="1d7a5-111">В противном случае функция возвращает структуру ТЕКСТМЕТРИКА.</span><span class="sxs-lookup"><span data-stu-id="1d7a5-111">Otherwise, the function returns a TEXTMETRICA structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d7a5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d7a5-112">Return value</span></span>

<span data-ttu-id="1d7a5-113">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d7a5-113">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d7a5-114">Ненулевое значение, если функция выполнена успешно; в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="1d7a5-114">Nonzero if the function is successful; otherwise 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d7a5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="1d7a5-115">Requirements</span></span>



| <span data-ttu-id="1d7a5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="1d7a5-116">Requirement</span></span> | <span data-ttu-id="1d7a5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1d7a5-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d7a5-118">Header</span><span class="sxs-lookup"><span data-stu-id="1d7a5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1d7a5-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d7a5-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1d7a5-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1d7a5-120">Library</span></span><br/> | <dl> <span data-ttu-id="1d7a5-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d7a5-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d7a5-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d7a5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d7a5-123">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="1d7a5-123">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="1d7a5-124">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="1d7a5-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
