---
description: Получает идентификатор шаблона в этом объекте данных файла.
ms.assetid: abc53dda-d3ed-461b-b3d8-a64845c44c81
title: 'Метод ID3DXFileData:: GetType (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 566052c06d5f7e55629a26442dd774a2f80fd647
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424457"
---
# <a name="id3dxfiledatagettype-method"></a><span data-ttu-id="d138d-103">Метод ID3DXFileData:: GetType</span><span class="sxs-lookup"><span data-stu-id="d138d-103">ID3DXFileData::GetType method</span></span>

<span data-ttu-id="d138d-104">Получает идентификатор шаблона в этом объекте данных файла.</span><span class="sxs-lookup"><span data-stu-id="d138d-104">Retrieves the template ID in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d138d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d138d-105">Syntax</span></span>


```C++
HRESULT GetType(
  [in] const GUID *pType
);
```



## <a name="parameters"></a><span data-ttu-id="d138d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d138d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d138d-107">*птипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d138d-107">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d138d-108">Тип: **константа [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="d138d-108">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="d138d-109">Указатель на идентификатор GUID, представляющий шаблон в этом объекте данных файла.</span><span class="sxs-lookup"><span data-stu-id="d138d-109">Pointer to the GUID representing the template in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d138d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d138d-110">Return value</span></span>

<span data-ttu-id="d138d-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d138d-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d138d-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="d138d-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d138d-113">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DXFERR \_ бадвалуе.</span><span class="sxs-lookup"><span data-stu-id="d138d-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="d138d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d138d-114">Requirements</span></span>



| <span data-ttu-id="d138d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d138d-115">Requirement</span></span> | <span data-ttu-id="d138d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d138d-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d138d-117">Header</span><span class="sxs-lookup"><span data-stu-id="d138d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d138d-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="d138d-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="d138d-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d138d-119">Library</span></span><br/> | <dl> <span data-ttu-id="d138d-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d138d-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d138d-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d138d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d138d-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="d138d-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 




