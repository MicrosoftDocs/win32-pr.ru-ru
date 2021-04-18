---
description: Извлекает объект данных с указанным GUID.
ms.assetid: c3d598bd-0646-4f99-8517-4475ef7cd8c9
title: 'Метод ID3DXFileEnumObject:: Жетдатаобжектбид (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 82a74ca4ff472d678ded92aa01f2c2406560955e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713799"
---
# <a name="id3dxfileenumobjectgetdataobjectbyid-method"></a><span data-ttu-id="e7af3-103">Метод ID3DXFileEnumObject:: Жетдатаобжектбид</span><span class="sxs-lookup"><span data-stu-id="e7af3-103">ID3DXFileEnumObject::GetDataObjectById method</span></span>

<span data-ttu-id="e7af3-104">Извлекает объект данных с указанным GUID.</span><span class="sxs-lookup"><span data-stu-id="e7af3-104">Retrieves the data object that has the specified GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7af3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7af3-105">Syntax</span></span>


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID        rguid,
  [out] LPD3DXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="e7af3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7af3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7af3-107">*ргуид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e7af3-107">*rguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7af3-108">Тип: **[рефгуид](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="e7af3-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="e7af3-109">Ссылка на запрошенный GUID.</span><span class="sxs-lookup"><span data-stu-id="e7af3-109">Reference to the requested GUID.</span></span>

</dd> <dt>

<span data-ttu-id="e7af3-110">*ппдатаобж* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e7af3-110">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7af3-111">Тип: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7af3-111">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)\***</span></span>

<span data-ttu-id="e7af3-112">Адрес указателя на интерфейс [**ID3DXFileData**](id3dxfiledata.md) , представляющий возвращаемый объект данных файла.</span><span class="sxs-lookup"><span data-stu-id="e7af3-112">Address of a pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7af3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7af3-113">Return value</span></span>

<span data-ttu-id="e7af3-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e7af3-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e7af3-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="e7af3-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e7af3-116">В случае сбоя метода возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадвалуе, дксфилирр \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="e7af3-116">If the method fails, the return value can be one of the following:DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7af3-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7af3-117">Remarks</span></span>

<span data-ttu-id="e7af3-118">Получите идентификатор GUID ргуид текущего файлового объекта данных с помощью метода [**ID3DXFileData:: GetId**](id3dxfiledata--getid.md) .</span><span class="sxs-lookup"><span data-stu-id="e7af3-118">Obtain the GUID rguid of the current file data object with the [**ID3DXFileData::GetId**](id3dxfiledata--getid.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7af3-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e7af3-119">Requirements</span></span>



| <span data-ttu-id="e7af3-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e7af3-120">Requirement</span></span> | <span data-ttu-id="e7af3-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e7af3-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7af3-122">Header</span><span class="sxs-lookup"><span data-stu-id="e7af3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e7af3-123"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7af3-123"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="e7af3-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e7af3-124">Library</span></span><br/> | <dl> <span data-ttu-id="e7af3-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7af3-125"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e7af3-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7af3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7af3-127">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="e7af3-127">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
