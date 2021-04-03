---
description: Возвращает количество дочерних объектов в этом объекте данных файла.
ms.assetid: 4409819f-a346-40b1-8e12-86e8128ece47
title: 'Метод ID3DXFileEnumObject:: Children (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChildren
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cafa79844e89602d3b88756e04ca460f611516dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821205"
---
# <a name="id3dxfileenumobjectgetchildren-method"></a><span data-ttu-id="92b53-103">Метод ID3DXFileEnumObject:: Children</span><span class="sxs-lookup"><span data-stu-id="92b53-103">ID3DXFileEnumObject::GetChildren method</span></span>

<span data-ttu-id="92b53-104">Возвращает количество дочерних объектов в этом объекте данных файла.</span><span class="sxs-lookup"><span data-stu-id="92b53-104">Retrieves the number of child objects in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b53-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92b53-105">Syntax</span></span>


```C++
HRESULT GetChildren(
  [in] SIZE_T *puiChildren
);
```



## <a name="parameters"></a><span data-ttu-id="92b53-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92b53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92b53-107">*пуичилдрен* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="92b53-107">*puiChildren* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92b53-108">Type: **[ **size \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="92b53-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="92b53-109">Адрес указателя для получения числа дочерних объектов в этом объекте данных файла.</span><span class="sxs-lookup"><span data-stu-id="92b53-109">Address of a pointer to receive the number of child objects in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92b53-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92b53-110">Return value</span></span>

<span data-ttu-id="92b53-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="92b53-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="92b53-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="92b53-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="92b53-113">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DXFERR \_ бадвалуе.</span><span class="sxs-lookup"><span data-stu-id="92b53-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="92b53-114">Требования</span><span class="sxs-lookup"><span data-stu-id="92b53-114">Requirements</span></span>



| <span data-ttu-id="92b53-115">Требование</span><span class="sxs-lookup"><span data-stu-id="92b53-115">Requirement</span></span> | <span data-ttu-id="92b53-116">Значение</span><span class="sxs-lookup"><span data-stu-id="92b53-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92b53-117">Header</span><span class="sxs-lookup"><span data-stu-id="92b53-117">Header</span></span><br/>  | <dl> <span data-ttu-id="92b53-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="92b53-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="92b53-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="92b53-119">Library</span></span><br/> | <dl> <span data-ttu-id="92b53-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92b53-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="92b53-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92b53-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b53-122">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="92b53-122">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
