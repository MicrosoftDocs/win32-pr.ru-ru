---
description: Включение или отключение сообщений отладки.
ms.assetid: 5c2aa3cf-ee6a-40fd-b300-67cb6ce691b6
title: Функция D3DX10DebugMute (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DebugMute
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6f331e3f074a4b77a1f1a7f1a8117cf660940f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713861"
---
# <a name="d3dx10debugmute-function"></a><span data-ttu-id="3f2a9-103">Функция D3DX10DebugMute</span><span class="sxs-lookup"><span data-stu-id="3f2a9-103">D3DX10DebugMute function</span></span>

<span data-ttu-id="3f2a9-104">Включение или отключение сообщений отладки.</span><span class="sxs-lookup"><span data-stu-id="3f2a9-104">Enable or disable debug messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f2a9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f2a9-105">Syntax</span></span>


```C++
HRESULT D3DX10DebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a><span data-ttu-id="3f2a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f2a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f2a9-107">*Отключить звук* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3f2a9-107">*Mute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f2a9-108">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f2a9-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3f2a9-109">Задайте значение **true** , чтобы включить сообщения отладки. Задайте значение **false** , чтобы отключить сообщения отладки.</span><span class="sxs-lookup"><span data-stu-id="3f2a9-109">Set to **TRUE** to enable debug messages; set to **FALSE** to disable debug messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f2a9-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f2a9-110">Return value</span></span>

<span data-ttu-id="3f2a9-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3f2a9-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3f2a9-112">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3f2a9-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3f2a9-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f2a9-113">Remarks</span></span>

<span data-ttu-id="3f2a9-114">Эта функция используется для отключения сообщений об ошибках для API-интерфейсов D3DX10 во время отладки. Использование этой функции должно быть защищено \_ параметром компилятора debug D3D10.</span><span class="sxs-lookup"><span data-stu-id="3f2a9-114">Use this function to disable error messages for D3DX10 APIs during debug; the use of this function should be guarded by the D3D10\_DEBUG compiler switch.</span></span>


```
#ifdef D3D10_DEBUG
  BOOL WINAPI D3DX10DebugMute(BOOL Mute);  
#endif
```



<span data-ttu-id="3f2a9-115">Состояние по умолчанию — **true** для отладочной сборки.</span><span class="sxs-lookup"><span data-stu-id="3f2a9-115">The default state is **TRUE** for a debug build.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f2a9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3f2a9-116">Requirements</span></span>



| <span data-ttu-id="3f2a9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3f2a9-117">Requirement</span></span> | <span data-ttu-id="3f2a9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3f2a9-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f2a9-119">Header</span><span class="sxs-lookup"><span data-stu-id="3f2a9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3f2a9-120"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f2a9-120"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="3f2a9-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3f2a9-121">Library</span></span><br/> | <dl> <span data-ttu-id="3f2a9-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f2a9-122"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3f2a9-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f2a9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f2a9-124">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="3f2a9-124">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
