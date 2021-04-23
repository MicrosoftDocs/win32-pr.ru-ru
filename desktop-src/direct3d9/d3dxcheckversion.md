---
description: Убедитесь, что версия D3DX, которая была скомпилирована с помощью, — это версия, которую вы используете.
ms.assetid: a4e745dd-d573-4e8f-9516-f6a7475f5cc5
title: Функция D3DXCheckVersion (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b392d706e54780924115471906096f6b63d1a80
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647858"
---
# <a name="d3dxcheckversion-function"></a><span data-ttu-id="d9c41-103">Функция D3DXCheckVersion</span><span class="sxs-lookup"><span data-stu-id="d9c41-103">D3DXCheckVersion function</span></span>

<span data-ttu-id="d9c41-104">Убедитесь, что версия D3DX, которая была скомпилирована с помощью, — это версия, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="d9c41-104">Verify that the version of D3DX you compiled with is the version that you are running.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9c41-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9c41-105">Syntax</span></span>


```C++
BOOL D3DXCheckVersion(
  _In_ UINT D3DSDKVersion,
  _In_ UINT D3DXSDKVersion
);
```



## <a name="parameters"></a><span data-ttu-id="d9c41-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9c41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9c41-107">*D3DSDKVersion* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9c41-107">*D3DSDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9c41-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9c41-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9c41-109">Используйте \_ версию пакета SDK для D3D \_ .</span><span class="sxs-lookup"><span data-stu-id="d9c41-109">Use D3D\_SDK\_VERSION.</span></span> <span data-ttu-id="d9c41-110">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="d9c41-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d9c41-111">*D3DXSDKVersion* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9c41-111">*D3DXSDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9c41-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9c41-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9c41-113">Используйте \_ версию пакета SDK для D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="d9c41-113">Use D3DX\_SDK\_VERSION.</span></span> <span data-ttu-id="d9c41-114">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="d9c41-114">See remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9c41-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9c41-115">Return value</span></span>

<span data-ttu-id="d9c41-116">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9c41-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9c41-117">Возвращает **значение true** , если версия D3DX, с которой выполнялась компиляция, является версией, с которой вы работаете; в противном случае возвращается **значение false** .</span><span class="sxs-lookup"><span data-stu-id="d9c41-117">Returns **TRUE** if the version of D3DX you compiled against is the version you are running with; otherwise, **FALSE** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9c41-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9c41-118">Remarks</span></span>

<span data-ttu-id="d9c41-119">Используйте эту функцию во время инициализации приложения следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d9c41-119">Use this function during the initialization of your application like this:</span></span>


```
HRESULT CD3DXMyApplication::Initialize(HINSTANCE hInstance, 
  LPCSTR szWindowName, LPCSTR szClassName, UINT uWidth, UINT uHeight)
{
    HRESULT hr;
    
    if (!D3DXCheckVersion(D3D_SDK_VERSION, D3DX_SDK_VERSION))
        return E_FAIL;
    
    ...
}
```



<span data-ttu-id="d9c41-120">Используйте [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) , чтобы убедиться, что установлена правильная среда выполнения.</span><span class="sxs-lookup"><span data-stu-id="d9c41-120">Use [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) to verify that the correct runtime is installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9c41-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d9c41-121">Requirements</span></span>



| <span data-ttu-id="d9c41-122">Требование</span><span class="sxs-lookup"><span data-stu-id="d9c41-122">Requirement</span></span> | <span data-ttu-id="d9c41-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d9c41-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9c41-124">Header</span><span class="sxs-lookup"><span data-stu-id="d9c41-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d9c41-125"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9c41-125"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="d9c41-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d9c41-126">Library</span></span><br/> | <dl> <span data-ttu-id="d9c41-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9c41-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d9c41-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9c41-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9c41-129">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="d9c41-129">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
