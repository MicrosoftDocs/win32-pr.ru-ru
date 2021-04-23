---
title: Метод ID3DX11EffectScalarVariable-bool (D3dx11effect. h)
description: Получить логическую переменную.
ms.assetid: 9d2789af-c59f-4d2d-87c6-9f36286e8a15
keywords:
- Метод "Cool bool" Direct3D 11
- Метод ID3DX11EffectScalarVariable с методомического bool Direct3D 11, интерфейс
- Интерфейс ID3DX11EffectScalarVariable Direct3D 11, методического bool
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetBool
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 754dd8856876ca441e83267250dcfad4f4011c69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821452"
---
# <a name="id3dx11effectscalarvariablegetbool-method"></a><span data-ttu-id="479d7-106">Метод ID3DX11EffectScalarVariable::</span><span class="sxs-lookup"><span data-stu-id="479d7-106">ID3DX11EffectScalarVariable::GetBool method</span></span>

<span data-ttu-id="479d7-107">Получить логическую переменную.</span><span class="sxs-lookup"><span data-stu-id="479d7-107">Get a boolean variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="479d7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="479d7-108">Syntax</span></span>


```C++
HRESULT GetBool(
   BOOL *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="479d7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="479d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="479d7-110">*pValue*</span><span class="sxs-lookup"><span data-stu-id="479d7-110">*pValue*</span></span> 
</dt> <dd>

<span data-ttu-id="479d7-111">Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="479d7-111">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="479d7-112">Указатель на переменную.</span><span class="sxs-lookup"><span data-stu-id="479d7-112">A pointer to the variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="479d7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="479d7-113">Return value</span></span>

<span data-ttu-id="479d7-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="479d7-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="479d7-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="479d7-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="479d7-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="479d7-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="479d7-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="479d7-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="479d7-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="479d7-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="479d7-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="479d7-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="479d7-120">Требования</span><span class="sxs-lookup"><span data-stu-id="479d7-120">Requirements</span></span>



| <span data-ttu-id="479d7-121">Требование</span><span class="sxs-lookup"><span data-stu-id="479d7-121">Requirement</span></span> | <span data-ttu-id="479d7-122">Значение</span><span class="sxs-lookup"><span data-stu-id="479d7-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="479d7-123">Header</span><span class="sxs-lookup"><span data-stu-id="479d7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="479d7-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="479d7-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="479d7-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="479d7-125">Library</span></span><br/> | <dl> <span data-ttu-id="479d7-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="479d7-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="479d7-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="479d7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="479d7-128">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="479d7-128">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

