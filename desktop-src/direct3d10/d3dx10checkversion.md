---
description: Функция D3DX10CheckVersion. Убедитесь, что версия D3DX, которая была скомпилирована с помощью, является версией, которую вы используете.
ms.assetid: 57085b07-f77b-425e-a889-22c3071d7143
title: Функция D3DX10CheckVersion (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CheckVersion
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4fc8befa88fb706965a30224843745b033ea205b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105352"
---
# <a name="d3dx10checkversion-function"></a><span data-ttu-id="ca4e6-103">Функция D3DX10CheckVersion</span><span class="sxs-lookup"><span data-stu-id="ca4e6-103">D3DX10CheckVersion function</span></span>

<span data-ttu-id="ca4e6-104">Убедитесь, что версия D3DX, которая была скомпилирована с помощью, — это версия, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="ca4e6-104">Verify that the version of D3DX you compiled with is the version that you are running.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca4e6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca4e6-105">Syntax</span></span>


```C++
HRESULT D3DX10CheckVersion(
  _In_ UINT D3DSdkVersion,
  _In_ UINT D3DX10SdkVersion
);
```



## <a name="parameters"></a><span data-ttu-id="ca4e6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca4e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca4e6-107">*D3DSdkVersion* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ca4e6-107">*D3DSdkVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca4e6-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca4e6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca4e6-109">Используйте \_ версию пакета SDK для D3D10 \_ .</span><span class="sxs-lookup"><span data-stu-id="ca4e6-109">Use D3D10\_SDK\_VERSION.</span></span> <span data-ttu-id="ca4e6-110">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="ca4e6-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ca4e6-111">*D3DX10SdkVersion* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ca4e6-111">*D3DX10SdkVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca4e6-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca4e6-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca4e6-113">Используйте \_ версию пакета SDK для D3DX10 \_ .</span><span class="sxs-lookup"><span data-stu-id="ca4e6-113">Use D3DX10\_SDK\_VERSION.</span></span> <span data-ttu-id="ca4e6-114">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="ca4e6-114">See remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca4e6-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca4e6-115">Return value</span></span>

<span data-ttu-id="ca4e6-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ca4e6-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ca4e6-117">Если версия не совпадает, функция возвратит значение FALSE (число меньше или равно 0, само число не имеет смысла).</span><span class="sxs-lookup"><span data-stu-id="ca4e6-117">If the version doesn't match, the function will return FALSE (a number less than or equal to 0, the number itself has no meaning).</span></span>

## <a name="remarks"></a><span data-ttu-id="ca4e6-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="ca4e6-118">Remarks</span></span>

<span data-ttu-id="ca4e6-119">Используйте эту функцию во время инициализации приложения.</span><span class="sxs-lookup"><span data-stu-id="ca4e6-119">Use this function during the initialization of your application.</span></span>


```
HRESULT hr;
    
if( FAILED( D3DX10CheckVersion(D3D10_SDK_VERSION, D3DX10_SDK_VERSION) ) )
    return E_FAIL;
```



## <a name="requirements"></a><span data-ttu-id="ca4e6-120">Требования</span><span class="sxs-lookup"><span data-stu-id="ca4e6-120">Requirements</span></span>



| <span data-ttu-id="ca4e6-121">Требование</span><span class="sxs-lookup"><span data-stu-id="ca4e6-121">Requirement</span></span> | <span data-ttu-id="ca4e6-122">Значение</span><span class="sxs-lookup"><span data-stu-id="ca4e6-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca4e6-123">Header</span><span class="sxs-lookup"><span data-stu-id="ca4e6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ca4e6-124"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca4e6-124"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="ca4e6-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ca4e6-125">Library</span></span><br/> | <dl> <span data-ttu-id="ca4e6-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca4e6-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ca4e6-127">См. также</span><span class="sxs-lookup"><span data-stu-id="ca4e6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca4e6-128">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="ca4e6-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
