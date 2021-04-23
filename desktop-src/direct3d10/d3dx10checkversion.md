---
description: Убедитесь, что версия D3DX, которая была скомпилирована с помощью, — это версия, которую вы используете.
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
ms.openlocfilehash: 3b41996f16cb97d91dc59f8d368f13b905992388
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720945"
---
# <a name="d3dx10checkversion-function"></a><span data-ttu-id="89238-103">Функция D3DX10CheckVersion</span><span class="sxs-lookup"><span data-stu-id="89238-103">D3DX10CheckVersion function</span></span>

<span data-ttu-id="89238-104">Убедитесь, что версия D3DX, которая была скомпилирована с помощью, — это версия, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="89238-104">Verify that the version of D3DX you compiled with is the version that you are running.</span></span>

## <a name="syntax"></a><span data-ttu-id="89238-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89238-105">Syntax</span></span>


```C++
HRESULT D3DX10CheckVersion(
  _In_ UINT D3DSdkVersion,
  _In_ UINT D3DX10SdkVersion
);
```



## <a name="parameters"></a><span data-ttu-id="89238-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="89238-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89238-107">*D3DSdkVersion* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="89238-107">*D3DSdkVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89238-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="89238-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="89238-109">Используйте \_ версию пакета SDK для D3D10 \_ .</span><span class="sxs-lookup"><span data-stu-id="89238-109">Use D3D10\_SDK\_VERSION.</span></span> <span data-ttu-id="89238-110">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="89238-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="89238-111">*D3DX10SdkVersion* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="89238-111">*D3DX10SdkVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89238-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="89238-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="89238-113">Используйте \_ версию пакета SDK для D3DX10 \_ .</span><span class="sxs-lookup"><span data-stu-id="89238-113">Use D3DX10\_SDK\_VERSION.</span></span> <span data-ttu-id="89238-114">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="89238-114">See remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89238-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89238-115">Return value</span></span>

<span data-ttu-id="89238-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="89238-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="89238-117">Если версия не совпадает, функция возвратит значение FALSE (число меньше или равно 0, само число не имеет смысла).</span><span class="sxs-lookup"><span data-stu-id="89238-117">If the version doesn't match, the function will return FALSE (a number less than or equal to 0, the number itself has no meaning).</span></span>

## <a name="remarks"></a><span data-ttu-id="89238-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89238-118">Remarks</span></span>

<span data-ttu-id="89238-119">Используйте эту функцию во время инициализации приложения.</span><span class="sxs-lookup"><span data-stu-id="89238-119">Use this function during the initialization of your application.</span></span>


```
HRESULT hr;
    
if( FAILED( D3DX10CheckVersion(D3D10_SDK_VERSION, D3DX10_SDK_VERSION) ) )
    return E_FAIL;
```



## <a name="requirements"></a><span data-ttu-id="89238-120">Требования</span><span class="sxs-lookup"><span data-stu-id="89238-120">Requirements</span></span>



| <span data-ttu-id="89238-121">Требование</span><span class="sxs-lookup"><span data-stu-id="89238-121">Requirement</span></span> | <span data-ttu-id="89238-122">Значение</span><span class="sxs-lookup"><span data-stu-id="89238-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89238-123">Header</span><span class="sxs-lookup"><span data-stu-id="89238-123">Header</span></span><br/>  | <dl> <span data-ttu-id="89238-124"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="89238-124"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="89238-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="89238-125">Library</span></span><br/> | <dl> <span data-ttu-id="89238-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89238-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="89238-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89238-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89238-128">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="89238-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
