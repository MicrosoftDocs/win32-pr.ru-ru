---
description: Извлекает дочерний объект в этом объекте данных файла.
ms.assetid: d8f367dd-8858-48ae-9de5-17de1538aadf
title: Метод ID3DXFileEnumObject::-Child (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b5b8d535a9060e80318d4043af6362810023b9d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703876"
---
# <a name="id3dxfileenumobjectgetchild-method"></a><span data-ttu-id="9cc8d-103">Метод ID3DXFileEnumObject:: Child</span><span class="sxs-lookup"><span data-stu-id="9cc8d-103">ID3DXFileEnumObject::GetChild method</span></span>

<span data-ttu-id="9cc8d-104">Извлекает дочерний объект в этом объекте данных файла.</span><span class="sxs-lookup"><span data-stu-id="9cc8d-104">Retrieves a child object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cc8d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9cc8d-105">Syntax</span></span>


```C++
HRESULT GetChild(
  [in]  SIZE_T        id,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="9cc8d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9cc8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cc8d-107">*идентификатор* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="9cc8d-107">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cc8d-108">Type: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9cc8d-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9cc8d-109">ИДЕНТИФИКАТОР получаемого дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="9cc8d-109">ID of the child object to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="9cc8d-110">*ппобж* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9cc8d-110">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cc8d-111">Тип: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="9cc8d-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="9cc8d-112">Адрес указателя для получения указателя интерфейса дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="9cc8d-112">Address of a pointer to receive the child object's interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cc8d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9cc8d-113">Return value</span></span>

<span data-ttu-id="9cc8d-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9cc8d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9cc8d-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="9cc8d-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9cc8d-116">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DXFERR \_ бадвалуе, D3DXFERR \_ номореобжектс.</span><span class="sxs-lookup"><span data-stu-id="9cc8d-116">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_NOMOREOBJECTS.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cc8d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="9cc8d-117">Requirements</span></span>



| <span data-ttu-id="9cc8d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="9cc8d-118">Requirement</span></span> | <span data-ttu-id="9cc8d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9cc8d-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9cc8d-120">Header</span><span class="sxs-lookup"><span data-stu-id="9cc8d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="9cc8d-121"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cc8d-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="9cc8d-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9cc8d-122">Library</span></span><br/> | <dl> <span data-ttu-id="9cc8d-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9cc8d-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="9cc8d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9cc8d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cc8d-125">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="9cc8d-125">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
