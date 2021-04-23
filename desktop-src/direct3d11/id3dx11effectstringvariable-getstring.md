---
title: Метод ID3DX11EffectStringVariable GetString (D3dx11effect. h)
description: Получите строку.
ms.assetid: ce96ae18-d316-41ba-9b2a-eac084b86098
keywords:
- Метод GetString Direct3D 11
- Метод GetString Direct3D 11, интерфейс ID3DX11EffectStringVariable
- Интерфейс ID3DX11EffectStringVariable Direct3D 11, метод GetString
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetString
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d15666bd70bf00395b7052b7820981dd8d0dcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986816"
---
# <a name="id3dx11effectstringvariablegetstring-method"></a><span data-ttu-id="33a9b-106">Метод ID3DX11EffectStringVariable:: GetString</span><span class="sxs-lookup"><span data-stu-id="33a9b-106">ID3DX11EffectStringVariable::GetString method</span></span>

<span data-ttu-id="33a9b-107">Получите строку.</span><span class="sxs-lookup"><span data-stu-id="33a9b-107">Get the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="33a9b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33a9b-108">Syntax</span></span>


```C++
HRESULT GetString(
   LPCSTR *ppString
);
```



## <a name="parameters"></a><span data-ttu-id="33a9b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="33a9b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33a9b-110">*ппстринг*</span><span class="sxs-lookup"><span data-stu-id="33a9b-110">*ppString*</span></span> 
</dt> <dd>

<span data-ttu-id="33a9b-111">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="33a9b-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="33a9b-112">Указатель на строку.</span><span class="sxs-lookup"><span data-stu-id="33a9b-112">A pointer to the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33a9b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="33a9b-113">Return value</span></span>

<span data-ttu-id="33a9b-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="33a9b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="33a9b-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="33a9b-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="33a9b-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="33a9b-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="33a9b-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="33a9b-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="33a9b-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="33a9b-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="33a9b-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="33a9b-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="33a9b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="33a9b-120">Requirements</span></span>



| <span data-ttu-id="33a9b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="33a9b-121">Requirement</span></span> | <span data-ttu-id="33a9b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="33a9b-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33a9b-123">Header</span><span class="sxs-lookup"><span data-stu-id="33a9b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="33a9b-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="33a9b-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="33a9b-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="33a9b-125">Library</span></span><br/> | <dl> <span data-ttu-id="33a9b-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="33a9b-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33a9b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33a9b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33a9b-128">ID3DX11EffectStringVariable</span><span class="sxs-lookup"><span data-stu-id="33a9b-128">ID3DX11EffectStringVariable</span></span>](id3dx11effectstringvariable.md)
</dt> </dl>

 

