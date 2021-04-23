---
description: Получение описания текущего объекта Font.
ms.assetid: f08beb35-351f-4087-a2db-097843463291
title: 'Метод ID3DX10Font:: desc (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDesc
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 59a7e361ebb6254fcc49eab30ff44ab39c38fd76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664991"
---
# <a name="id3dx10fontgetdesc-method"></a><span data-ttu-id="ffb79-103">Метод ID3DX10Font:: DESC</span><span class="sxs-lookup"><span data-stu-id="ffb79-103">ID3DX10Font::GetDesc method</span></span>

<span data-ttu-id="ffb79-104">Получение описания текущего объекта Font.</span><span class="sxs-lookup"><span data-stu-id="ffb79-104">Get a description of the current font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffb79-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffb79-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DX10_FONT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="ffb79-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ffb79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffb79-107">*пдеск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ffb79-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffb79-108">Тип: **[ **D3DX10 \_ Font \_ DESC**](d3dx10-font-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="ffb79-108">Type: **[**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md)\***</span></span>

<span data-ttu-id="ffb79-109">Указатель на [**D3DX10 структуру \_ шрифта \_**](d3dx10-font-desc.md) , описывающую объект Font.</span><span class="sxs-lookup"><span data-stu-id="ffb79-109">Pointer to a [**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md) structure that describes the font object.</span></span> <span data-ttu-id="ffb79-110">Если определен Юникод, возвращается указатель на D3DX10FONT \_ дескв; в противном случае возвращается указатель на D3DX10FONT \_ DESC.</span><span class="sxs-lookup"><span data-stu-id="ffb79-110">If UNICODE is defined, a pointer to a D3DX10FONT\_DESCW is returned; otherwise a pointer to a D3DX10FONT\_DESCA is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffb79-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ffb79-111">Return value</span></span>

<span data-ttu-id="ffb79-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ffb79-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ffb79-113">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="ffb79-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ffb79-114">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="ffb79-114">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffb79-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ffb79-115">Remarks</span></span>

<span data-ttu-id="ffb79-116">Этот метод описывает объекты шрифтов Юникода, если задан Юникод.</span><span class="sxs-lookup"><span data-stu-id="ffb79-116">This method describes Unicode font objects if UNICODE is defined.</span></span> <span data-ttu-id="ffb79-117">В противном случае вызывается метод-DESC, который возвращает указатель на \_ структуру D3DX10FONT DESC.</span><span class="sxs-lookup"><span data-stu-id="ffb79-117">Otherwise GetDescA is called, which returns a pointer to the D3DX10FONT\_DESCA structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffb79-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ffb79-118">Requirements</span></span>



| <span data-ttu-id="ffb79-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ffb79-119">Requirement</span></span> | <span data-ttu-id="ffb79-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ffb79-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ffb79-121">Header</span><span class="sxs-lookup"><span data-stu-id="ffb79-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ffb79-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffb79-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ffb79-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ffb79-123">Library</span></span><br/> | <dl> <span data-ttu-id="ffb79-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ffb79-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffb79-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ffb79-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffb79-126">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="ffb79-126">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="ffb79-127">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="ffb79-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




