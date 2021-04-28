---
description: 'Метод ID3DXFileEnumObject:: Child — получает дочерний объект в этом объекте данных файла.'
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
ms.openlocfilehash: b26cf058b31d1016c68cccf3dde6ade9f84cde1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090362"
---
# <a name="id3dxfileenumobjectgetchild-method"></a><span data-ttu-id="cf9ee-103">Метод ID3DXFileEnumObject:: Child</span><span class="sxs-lookup"><span data-stu-id="cf9ee-103">ID3DXFileEnumObject::GetChild method</span></span>

<span data-ttu-id="cf9ee-104">Извлекает дочерний объект в этом объекте данных файла.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-104">Retrieves a child object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf9ee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf9ee-105">Syntax</span></span>


```C++
HRESULT GetChild(
  [in]  SIZE_T        id,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="cf9ee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf9ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf9ee-107">*идентификатор* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="cf9ee-107">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf9ee-108">Type: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cf9ee-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cf9ee-109">ИДЕНТИФИКАТОР получаемого дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-109">ID of the child object to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ee-110">*ппобж* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cf9ee-110">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf9ee-111">Тип: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="cf9ee-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="cf9ee-112">Адрес указателя для получения указателя интерфейса дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-112">Address of a pointer to receive the child object's interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf9ee-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf9ee-113">Return value</span></span>

<span data-ttu-id="cf9ee-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cf9ee-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cf9ee-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="cf9ee-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="cf9ee-116">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DXFERR \_ бадвалуе, D3DXFERR \_ номореобжектс.</span><span class="sxs-lookup"><span data-stu-id="cf9ee-116">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_NOMOREOBJECTS.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf9ee-117">Требования</span><span class="sxs-lookup"><span data-stu-id="cf9ee-117">Requirements</span></span>



| <span data-ttu-id="cf9ee-118">Требование</span><span class="sxs-lookup"><span data-stu-id="cf9ee-118">Requirement</span></span> | <span data-ttu-id="cf9ee-119">Значение</span><span class="sxs-lookup"><span data-stu-id="cf9ee-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf9ee-120">Header</span><span class="sxs-lookup"><span data-stu-id="cf9ee-120">Header</span></span><br/>  | <dl> <span data-ttu-id="cf9ee-121"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf9ee-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="cf9ee-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cf9ee-122">Library</span></span><br/> | <dl> <span data-ttu-id="cf9ee-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf9ee-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="cf9ee-124">См. также</span><span class="sxs-lookup"><span data-stu-id="cf9ee-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf9ee-125">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="cf9ee-125">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
