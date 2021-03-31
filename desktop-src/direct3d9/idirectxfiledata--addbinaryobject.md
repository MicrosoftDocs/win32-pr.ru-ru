---
description: Создает двоичный объект и добавляет его в качестве дочернего объекта. Не рекомендуется.
ms.assetid: 6164951d-dd87-4318-ac08-b97c22f58d45
title: 'Метод Идиректксфиледата:: Аддбинарйобжект (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddBinaryObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 8373b9c4328a8683f32c1fe7ab979cb8d7636f87
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273707"
---
# <a name="idirectxfiledataaddbinaryobject-method"></a><span data-ttu-id="83a23-104">Метод Идиректксфиледата:: Аддбинарйобжект</span><span class="sxs-lookup"><span data-stu-id="83a23-104">IDirectXFileData::AddBinaryObject method</span></span>

<span data-ttu-id="83a23-105">Создает двоичный объект и добавляет его в качестве дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="83a23-105">Creates a binary object and adds it as a child object.</span></span> <span data-ttu-id="83a23-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="83a23-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="83a23-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83a23-107">Syntax</span></span>


```C++
HRESULT AddBinaryObject(
  [in]       LPCSTR szName,
  [in] const GUID   *pguid,
  [in]       LPCSTR szMimeType,
  [in]       LPVOID pvData,
  [in]       DWORD  cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="83a23-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="83a23-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83a23-109">*szName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83a23-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83a23-110">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83a23-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83a23-111">Указатель на имя объекта.</span><span class="sxs-lookup"><span data-stu-id="83a23-111">Pointer to the name of the object.</span></span> <span data-ttu-id="83a23-112">Если объекту не требуется имя, укажите **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="83a23-112">Specify **NULL** if the object does not need a name.</span></span>

</dd> <dt>

<span data-ttu-id="83a23-113">*пгуид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83a23-113">*pguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83a23-114">Тип: **константа [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="83a23-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="83a23-115">Указатель на идентификатор GUID, представляющий объект.</span><span class="sxs-lookup"><span data-stu-id="83a23-115">Pointer to the GUID representing the object.</span></span> <span data-ttu-id="83a23-116">Если объекту не требуется GUID, укажите **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="83a23-116">Specify **NULL** if the object does not need a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="83a23-117">*сзмиметипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83a23-117">*szMimeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83a23-118">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83a23-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83a23-119">Указатель на тип MIME объекта.</span><span class="sxs-lookup"><span data-stu-id="83a23-119">Pointer to the object's MIME type.</span></span>

</dd> <dt>

<span data-ttu-id="83a23-120">*пвдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83a23-120">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83a23-121">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83a23-121">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83a23-122">Указатель на данные объекта.</span><span class="sxs-lookup"><span data-stu-id="83a23-122">Pointer to the object's data.</span></span>

</dd> <dt>

<span data-ttu-id="83a23-123">*кбсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83a23-123">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83a23-124">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83a23-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83a23-125">Размер буфера, на который указывает Пвдата, в байтах.</span><span class="sxs-lookup"><span data-stu-id="83a23-125">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83a23-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83a23-126">Return value</span></span>

<span data-ttu-id="83a23-127">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="83a23-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="83a23-128">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="83a23-128">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="83a23-129">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих значений. ДКСФИЛИРР \_ БАДАЛЛОК дксфилирр \_ бадвалуе</span><span class="sxs-lookup"><span data-stu-id="83a23-129">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="83a23-130">Требования</span><span class="sxs-lookup"><span data-stu-id="83a23-130">Requirements</span></span>



| <span data-ttu-id="83a23-131">Требование</span><span class="sxs-lookup"><span data-stu-id="83a23-131">Requirement</span></span> | <span data-ttu-id="83a23-132">Значение</span><span class="sxs-lookup"><span data-stu-id="83a23-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83a23-133">Header</span><span class="sxs-lookup"><span data-stu-id="83a23-133">Header</span></span><br/>  | <dl> <span data-ttu-id="83a23-134"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="83a23-134"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="83a23-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="83a23-135">Library</span></span><br/> | <dl> <span data-ttu-id="83a23-136"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83a23-136"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83a23-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83a23-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83a23-138">идиректксфиледата</span><span class="sxs-lookup"><span data-stu-id="83a23-138">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="83a23-139">**Идиректксфилебинари:: Жетмиметипе**</span><span class="sxs-lookup"><span data-stu-id="83a23-139">**IDirectXFileBinary::GetMimeType**</span></span>](idirectxfilebinary--getmimetype.md)
</dt> </dl>

 

 
