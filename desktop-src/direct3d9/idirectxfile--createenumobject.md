---
description: Создает объект перечислителя. Не рекомендуется.
ms.assetid: 9e72bb2f-143e-4690-baef-ccded21572ec
title: 'Метод Идиректксфиле:: Креатинумобжект (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3d15738b78299441fe08333a41f0652f1b4224d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821356"
---
# <a name="idirectxfilecreateenumobject-method"></a><span data-ttu-id="3f11d-104">Метод Идиректксфиле:: Креатинумобжект</span><span class="sxs-lookup"><span data-stu-id="3f11d-104">IDirectXFile::CreateEnumObject method</span></span>

<span data-ttu-id="3f11d-105">Создает объект перечислителя.</span><span class="sxs-lookup"><span data-stu-id="3f11d-105">Creates an enumerator object.</span></span> <span data-ttu-id="3f11d-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="3f11d-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f11d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f11d-107">Syntax</span></span>


```C++
HRESULT CreateEnumObject(
  [in]          LPVOID                  pvSource,
  [in]          DXFILELOADOPTIONS       dwLoadOptions,
  [out, retval] LPDIRECTXFILEENUMOBJECT *ppEnumObj
);
```



## <a name="parameters"></a><span data-ttu-id="3f11d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f11d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f11d-109">*пвсаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3f11d-109">*pvSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f11d-110">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f11d-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3f11d-111">Указатель на данные, содержимое которых зависит от значения Двлоадоптионс</span><span class="sxs-lookup"><span data-stu-id="3f11d-111">Pointer to data whose contents depend on the value of dwLoadOptions</span></span>

</dd> <dt>

<span data-ttu-id="3f11d-112">*двлоадоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3f11d-112">*dwLoadOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f11d-113">Тип: **[ **дксфилелоадоптионс**](dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="3f11d-113">Type: **[**DXFILELOADOPTIONS**](dxfile.md)**</span></span>

<span data-ttu-id="3f11d-114">Значение, указывающее источник данных.</span><span class="sxs-lookup"><span data-stu-id="3f11d-114">Value that specifies the source of the data.</span></span> <span data-ttu-id="3f11d-115">Это значение может быть одним из \_ флагов дксфилелоад XXX в [константах дксфиле](dxfile.md).</span><span class="sxs-lookup"><span data-stu-id="3f11d-115">This value can be one of the DXFILELOAD\_xxx flags in [DXFILE Constants](dxfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3f11d-116">*ппенумобж* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3f11d-116">*ppEnumObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3f11d-117">Тип: **[ **лпдиректксфилинумобжект**](idirectxfileenumobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="3f11d-117">Type: **[**LPDIRECTXFILEENUMOBJECT**](idirectxfileenumobject.md)\***</span></span>

<span data-ttu-id="3f11d-118">Адрес указателя на интерфейс [**идиректксфилинумобжект**](idirectxfileenumobject.md) , представляющий созданный объект перечислителя.</span><span class="sxs-lookup"><span data-stu-id="3f11d-118">Address of a pointer to an [**IDirectXFileEnumObject**](idirectxfileenumobject.md) interface, representing the created enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f11d-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f11d-119">Return value</span></span>

<span data-ttu-id="3f11d-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3f11d-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3f11d-121">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3f11d-121">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="3f11d-122">В случае сбоя метода возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадаллок, дксфилирр \_ БАДФИЛЕФЛОАТСИЗЕ, дксфилирр \_ бадфилетипе, ДКСФИЛИРР \_ бадфилеверсион, DXFILEERR \_ BADRESOURCE, DXFILEERR \_ BADVALUE, DXFILEERR \_ FILENOTFOUND, DXFILEERR \_ RESOURCENOTFOUND, DXFILEERR \_ URLNOTFOUND.</span><span class="sxs-lookup"><span data-stu-id="3f11d-122">If the method fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADFILEFLOATSIZE, DXFILEERR\_BADFILETYPE, DXFILEERR\_BADFILEVERSION, DXFILEERR\_BADRESOURCE, DXFILEERR\_BADVALUE, DXFILEERR\_FILENOTFOUND, DXFILEERR\_RESOURCENOTFOUND, DXFILEERR\_URLNOTFOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f11d-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f11d-123">Remarks</span></span>

<span data-ttu-id="3f11d-124">После использования этого метода используйте один из методов Идиректксфилинумобжект для получения объекта данных.</span><span class="sxs-lookup"><span data-stu-id="3f11d-124">After using this method, use one of the IDirectXFileEnumObject methods to retrieve a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f11d-125">Требования</span><span class="sxs-lookup"><span data-stu-id="3f11d-125">Requirements</span></span>



| <span data-ttu-id="3f11d-126">Требование</span><span class="sxs-lookup"><span data-stu-id="3f11d-126">Requirement</span></span> | <span data-ttu-id="3f11d-127">Значение</span><span class="sxs-lookup"><span data-stu-id="3f11d-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f11d-128">Header</span><span class="sxs-lookup"><span data-stu-id="3f11d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="3f11d-129"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f11d-129"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="3f11d-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3f11d-130">Library</span></span><br/> | <dl> <span data-ttu-id="3f11d-131"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f11d-131"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f11d-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f11d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f11d-133">идиректксфиле</span><span class="sxs-lookup"><span data-stu-id="3f11d-133">IDirectXFile</span></span>](idirectxfile.md)
</dt> </dl>

 

 
