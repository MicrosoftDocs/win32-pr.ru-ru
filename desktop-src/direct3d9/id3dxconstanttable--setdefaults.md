---
description: Устанавливает константы в значения по умолчанию. Значения по умолчанию объявляются в объявлениях переменных в шейдере.
ms.assetid: 593a3a1b-cf96-4d46-9917-21068def0988
title: 'Метод ID3DXConstantTable:: SetDefaults (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetDefaults
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed49e626c979f7146b42078cf1f65fdd6716efc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821117"
---
# <a name="id3dxconstanttablesetdefaults-method"></a><span data-ttu-id="c0832-104">Метод ID3DXConstantTable:: SetDefaults</span><span class="sxs-lookup"><span data-stu-id="c0832-104">ID3DXConstantTable::SetDefaults method</span></span>

<span data-ttu-id="c0832-105">Устанавливает константы в значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c0832-105">Sets the constants to their default values.</span></span> <span data-ttu-id="c0832-106">Значения по умолчанию объявляются в объявлениях переменных в шейдере.</span><span class="sxs-lookup"><span data-stu-id="c0832-106">The default values are declared in the variable declarations in the shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0832-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0832-107">Syntax</span></span>


```C++
HRESULT SetDefaults(
  [in] LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="c0832-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0832-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0832-109">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0832-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0832-110">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="c0832-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="c0832-111">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="c0832-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0832-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0832-112">Return value</span></span>

<span data-ttu-id="c0832-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c0832-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c0832-114">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c0832-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c0832-115">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="c0832-115">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0832-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c0832-116">Requirements</span></span>



| <span data-ttu-id="c0832-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c0832-117">Requirement</span></span> | <span data-ttu-id="c0832-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c0832-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0832-119">Header</span><span class="sxs-lookup"><span data-stu-id="c0832-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c0832-120"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0832-120"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c0832-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c0832-121">Library</span></span><br/> | <dl> <span data-ttu-id="c0832-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0832-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c0832-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0832-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0832-124">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="c0832-124">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
