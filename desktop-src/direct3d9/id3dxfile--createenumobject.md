---
description: Создает объект перечислителя, который будет считывать x-файл.
ms.assetid: 86d05eab-601c-4beb-9dbe-c23fa524871c
title: 'Метод ID3DXFile:: Креатинумобжект (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a58a3341bacf9b323cc5753f8e9e51c4b703b966
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713806"
---
# <a name="id3dxfilecreateenumobject-method"></a><span data-ttu-id="cffc0-103">Метод ID3DXFile:: Креатинумобжект</span><span class="sxs-lookup"><span data-stu-id="cffc0-103">ID3DXFile::CreateEnumObject method</span></span>

<span data-ttu-id="cffc0-104">Создает объект перечислителя, который будет считывать x-файл.</span><span class="sxs-lookup"><span data-stu-id="cffc0-104">Creates an enumerator object that will read a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="cffc0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cffc0-105">Syntax</span></span>


```C++
HRESULT CreateEnumObject(
  [out] LPCVOID               pvSource,
  [in]  D3DXF_FILELOADOPTIONS loadflags,
  [out] ID3DXFileEnumObject   **ppEnumObj
);
```



## <a name="parameters"></a><span data-ttu-id="cffc0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cffc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cffc0-107">*пвсаурце* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cffc0-107">*pvSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cffc0-108">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cffc0-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cffc0-109">Источник данных.</span><span class="sxs-lookup"><span data-stu-id="cffc0-109">The data source.</span></span> <span data-ttu-id="cffc0-110">Любое из следующих:</span><span class="sxs-lookup"><span data-stu-id="cffc0-110">Either:</span></span>

-   <span data-ttu-id="cffc0-111">Имя файла</span><span class="sxs-lookup"><span data-stu-id="cffc0-111">A file name</span></span>
-   <span data-ttu-id="cffc0-112">Структура [**\_ филелоадмемори D3DXF**](d3dxf-fileloadmemory.md)</span><span class="sxs-lookup"><span data-stu-id="cffc0-112">A [**D3DXF\_FILELOADMEMORY**](d3dxf-fileloadmemory.md) structure</span></span>
-   <span data-ttu-id="cffc0-113">Структура [**\_ филелоадресаурце D3DXF**](d3dxf-fileloadresource.md)</span><span class="sxs-lookup"><span data-stu-id="cffc0-113">A [**D3DXF\_FILELOADRESOURCE**](d3dxf-fileloadresource.md) structure</span></span>

<span data-ttu-id="cffc0-114">В зависимости от значения лоадфлагс.</span><span class="sxs-lookup"><span data-stu-id="cffc0-114">Depending on the value of loadflags.</span></span>

</dd> <dt>

<span data-ttu-id="cffc0-115">*лоадфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cffc0-115">*loadflags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cffc0-116">Тип: **[D3DXF \_ филелоадоптионс](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="cffc0-116">Type: **[D3DXF\_FILELOADOPTIONS](d3dxf.md)**</span></span>

<span data-ttu-id="cffc0-117">Значение, указывающее источник данных.</span><span class="sxs-lookup"><span data-stu-id="cffc0-117">Value that specifies the source of the data.</span></span> <span data-ttu-id="cffc0-118">Это значение может быть одним из флагов [ \_ филелоадоптионс D3DXF](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="cffc0-118">This value can be one of the [D3DXF\_FILELOADOPTIONS](d3dxf.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="cffc0-119">*ппенумобж* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cffc0-119">*ppEnumObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cffc0-120">Тип: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="cffc0-120">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span></span>

<span data-ttu-id="cffc0-121">Адрес указателя на интерфейс [**ID3DXFileEnumObject**](id3dxfileenumobject.md) , представляющий созданный объект перечислителя.</span><span class="sxs-lookup"><span data-stu-id="cffc0-121">Address of a pointer to an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) interface, representing the created enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cffc0-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cffc0-122">Return value</span></span>

<span data-ttu-id="cffc0-123">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cffc0-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cffc0-124">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="cffc0-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="cffc0-125">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DXFERR \_ бадвалуе, D3DXFERR \_ парсиррор.</span><span class="sxs-lookup"><span data-stu-id="cffc0-125">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="cffc0-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cffc0-126">Remarks</span></span>

<span data-ttu-id="cffc0-127">После использования этого метода используйте один из методов [**ID3DXFileEnumObject**](id3dxfileenumobject.md) для получения объекта данных.</span><span class="sxs-lookup"><span data-stu-id="cffc0-127">After using this method, use one of the [**ID3DXFileEnumObject**](id3dxfileenumobject.md) methods to retrieve a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="cffc0-128">Требования</span><span class="sxs-lookup"><span data-stu-id="cffc0-128">Requirements</span></span>



| <span data-ttu-id="cffc0-129">Требование</span><span class="sxs-lookup"><span data-stu-id="cffc0-129">Requirement</span></span> | <span data-ttu-id="cffc0-130">Значение</span><span class="sxs-lookup"><span data-stu-id="cffc0-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cffc0-131">Header</span><span class="sxs-lookup"><span data-stu-id="cffc0-131">Header</span></span><br/>  | <dl> <span data-ttu-id="cffc0-132"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="cffc0-132"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="cffc0-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cffc0-133">Library</span></span><br/> | <dl> <span data-ttu-id="cffc0-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cffc0-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="cffc0-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cffc0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cffc0-136">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="cffc0-136">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="cffc0-137">**ID3DXFileEnumObject**</span><span class="sxs-lookup"><span data-stu-id="cffc0-137">**ID3DXFileEnumObject**</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
