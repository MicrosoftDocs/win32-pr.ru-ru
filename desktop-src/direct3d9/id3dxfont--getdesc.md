---
description: Возвращает описание текущего объекта Font. Жетдескв и DESC идентичны этому методу, за исключением того, что указатель возвращается в \_ структуру D3DXFONT дескв или D3DXFONT \_ DESC соответственно.
ms.assetid: 21bcd3e0-3659-4d64-959a-0f2d65850cb1
title: 'Метод ID3DXFont:: desc (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3310971e360fb9994a30d62349d3e7e4b764c7d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713653"
---
# <a name="id3dxfontgetdesc-method"></a><span data-ttu-id="d45fe-104">Метод ID3DXFont:: DESC</span><span class="sxs-lookup"><span data-stu-id="d45fe-104">ID3DXFont::GetDesc method</span></span>

<span data-ttu-id="d45fe-105">Возвращает описание текущего объекта Font.</span><span class="sxs-lookup"><span data-stu-id="d45fe-105">Gets a description of the current font object.</span></span> <span data-ttu-id="d45fe-106">Жетдескв и DESC идентичны этому методу, за исключением того, что указатель возвращается в структуру [**D3DXFONT \_ Дескв**](d3dxfont-desc.md) или **D3DXFONT \_ DESC** соответственно.</span><span class="sxs-lookup"><span data-stu-id="d45fe-106">GetDescW and GetDescA are identical to this method, except that a pointer is returned to a [**D3DXFONT\_DESCW**](d3dxfont-desc.md) or **D3DXFONT\_DESCA** structure, respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="d45fe-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d45fe-107">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXFONT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="d45fe-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d45fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d45fe-109">*пдеск* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d45fe-109">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d45fe-110">Тип: **[ **D3DXFONT \_ DESC**](d3dxfont-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="d45fe-110">Type: **[**D3DXFONT\_DESC**](d3dxfont-desc.md)\***</span></span>

<span data-ttu-id="d45fe-111">Указатель на структуру [**D3DXFONT \_ DESC**](d3dxfont-desc.md) , описывающую объект Font.</span><span class="sxs-lookup"><span data-stu-id="d45fe-111">Pointer to a [**D3DXFONT\_DESC**](d3dxfont-desc.md) structure that describes the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d45fe-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d45fe-112">Return value</span></span>

<span data-ttu-id="d45fe-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d45fe-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d45fe-114">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="d45fe-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d45fe-115">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="d45fe-115">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d45fe-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d45fe-116">Remarks</span></span>

<span data-ttu-id="d45fe-117">Этот метод описывает объекты шрифтов Юникода, если задан Юникод.</span><span class="sxs-lookup"><span data-stu-id="d45fe-117">This method describes Unicode font objects if UNICODE is defined.</span></span> <span data-ttu-id="d45fe-118">В противном случае вызывается метод-DESC, который возвращает указатель на структуру [**D3DXFONT \_ DESC**](d3dxfont-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="d45fe-118">Otherwise GetDescA is called, which returns a pointer to the [**D3DXFONT\_DESCA**](d3dxfont-desc.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d45fe-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d45fe-119">Requirements</span></span>



| <span data-ttu-id="d45fe-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d45fe-120">Requirement</span></span> | <span data-ttu-id="d45fe-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d45fe-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d45fe-122">Header</span><span class="sxs-lookup"><span data-stu-id="d45fe-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d45fe-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="d45fe-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="d45fe-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d45fe-124">Library</span></span><br/> | <dl> <span data-ttu-id="d45fe-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d45fe-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d45fe-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d45fe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d45fe-127">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="d45fe-127">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 




