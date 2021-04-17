---
description: Возвращает маркер для контекста дисплея устройства (DC), для которого установлен шрифт.
ms.assetid: 57510b89-980d-42bb-a7ab-a292680a6004
title: 'Метод ID3DX10Font:: GetDC (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDC
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 93ee06df61e0285e26dba1976ea5bf09b9cb5a9b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694236"
---
# <a name="id3dx10fontgetdc-method"></a><span data-ttu-id="bc8fd-103">Метод ID3DX10Font:: GetDC</span><span class="sxs-lookup"><span data-stu-id="bc8fd-103">ID3DX10Font::GetDC method</span></span>

<span data-ttu-id="bc8fd-104">Возвращает маркер для контекста дисплея устройства (DC), для которого установлен шрифт.</span><span class="sxs-lookup"><span data-stu-id="bc8fd-104">Return a handle to a display device context (DC) that has the font set onto it.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc8fd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc8fd-105">Syntax</span></span>


```C++
HDC GetDC();
```



## <a name="parameters"></a><span data-ttu-id="bc8fd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc8fd-106">Parameters</span></span>

<span data-ttu-id="bc8fd-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="bc8fd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bc8fd-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc8fd-108">Return value</span></span>

<span data-ttu-id="bc8fd-109">Тип: **[ **HDC**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc8fd-109">Type: **[**HDC**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc8fd-110">Обработайте с КОНТРОЛЛЕРом экрана.</span><span class="sxs-lookup"><span data-stu-id="bc8fd-110">Handle to a display DC.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc8fd-111">Требования</span><span class="sxs-lookup"><span data-stu-id="bc8fd-111">Requirements</span></span>



| <span data-ttu-id="bc8fd-112">Требование</span><span class="sxs-lookup"><span data-stu-id="bc8fd-112">Requirement</span></span> | <span data-ttu-id="bc8fd-113">Значение</span><span class="sxs-lookup"><span data-stu-id="bc8fd-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc8fd-114">Header</span><span class="sxs-lookup"><span data-stu-id="bc8fd-114">Header</span></span><br/>  | <dl> <span data-ttu-id="bc8fd-115"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc8fd-115"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc8fd-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bc8fd-116">Library</span></span><br/> | <dl> <span data-ttu-id="bc8fd-117"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc8fd-117"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc8fd-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc8fd-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc8fd-119">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="bc8fd-119">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="bc8fd-120">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="bc8fd-120">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
