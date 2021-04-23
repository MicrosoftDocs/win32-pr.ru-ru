---
description: Получает идентификатор шаблона для этого узла файловых данных.
ms.assetid: ff0662da-b4f8-4ed2-81d4-6771e91da262
title: 'Метод ID3DXFileSaveData:: GetType (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b774f71b4be111efcdbdaf8bc41b40d4b0efaa95
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694305"
---
# <a name="id3dxfilesavedatagettype-method"></a><span data-ttu-id="780f4-103">Метод ID3DXFileSaveData:: GetType</span><span class="sxs-lookup"><span data-stu-id="780f4-103">ID3DXFileSaveData::GetType method</span></span>

<span data-ttu-id="780f4-104">Получает идентификатор шаблона для этого узла файловых данных.</span><span class="sxs-lookup"><span data-stu-id="780f4-104">Retrieves the template ID of this file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="780f4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="780f4-105">Syntax</span></span>


```C++
HRESULT GetType(
  [in] GUID *type
);
```



## <a name="parameters"></a><span data-ttu-id="780f4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="780f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="780f4-107">*тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="780f4-107">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="780f4-108">Тип: **[ **GUID**](guid.md)\***</span><span class="sxs-lookup"><span data-stu-id="780f4-108">Type: **[**GUID**](guid.md)\***</span></span>

<span data-ttu-id="780f4-109">Указатель на идентификатор GUID, представляющий шаблон в этом узле данных файла.</span><span class="sxs-lookup"><span data-stu-id="780f4-109">Pointer to the GUID representing the template in this file data node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="780f4-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="780f4-110">Return value</span></span>

<span data-ttu-id="780f4-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="780f4-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="780f4-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="780f4-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="780f4-113">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DXFERR \_ бадобжект, D3DXFERR \_ бадвалуе.</span><span class="sxs-lookup"><span data-stu-id="780f4-113">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="780f4-114">Требования</span><span class="sxs-lookup"><span data-stu-id="780f4-114">Requirements</span></span>



| <span data-ttu-id="780f4-115">Требование</span><span class="sxs-lookup"><span data-stu-id="780f4-115">Requirement</span></span> | <span data-ttu-id="780f4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="780f4-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="780f4-117">Header</span><span class="sxs-lookup"><span data-stu-id="780f4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="780f4-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="780f4-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="780f4-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="780f4-119">Library</span></span><br/> | <dl> <span data-ttu-id="780f4-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="780f4-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="780f4-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="780f4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="780f4-122">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="780f4-122">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 




