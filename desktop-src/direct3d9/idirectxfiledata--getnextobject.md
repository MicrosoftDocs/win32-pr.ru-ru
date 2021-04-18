---
description: Извлекает следующий дочерний объект данных, объект ссылки на данные или двоичный объект в файле DirectX. Не рекомендуется.
ms.assetid: 8232e911-6552-4b2b-a9c2-59e6a13a0d9b
title: 'Метод Идиректксфиледата:: Жетнекстобжект (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetNextObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: e03351068cdc4f8fca28c612b7bb4c546125a4cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713867"
---
# <a name="idirectxfiledatagetnextobject-method"></a><span data-ttu-id="2cb19-104">Метод Идиректксфиледата:: Жетнекстобжект</span><span class="sxs-lookup"><span data-stu-id="2cb19-104">IDirectXFileData::GetNextObject method</span></span>

<span data-ttu-id="2cb19-105">Извлекает следующий дочерний объект данных, объект ссылки на данные или двоичный объект в файле DirectX.</span><span class="sxs-lookup"><span data-stu-id="2cb19-105">Retrieves the next child data object, data reference object, or binary object in the DirectX file.</span></span> <span data-ttu-id="2cb19-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="2cb19-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cb19-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2cb19-107">Syntax</span></span>


```C++
HRESULT GetNextObject(
  [out, retval] LPDIRECTXFILEOBJECT *ppChildObj
);
```



## <a name="parameters"></a><span data-ttu-id="2cb19-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cb19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cb19-109">*ппчилдобж* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2cb19-109">*ppChildObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2cb19-110">Тип: **[ **лпдиректксфилеобжект**](idirectxfileobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="2cb19-110">Type: **[**LPDIRECTXFILEOBJECT**](idirectxfileobject.md)\***</span></span>

<span data-ttu-id="2cb19-111">Адрес указателя на интерфейс [**идиректксфилеобжект**](idirectxfileobject.md) , представляющий интерфейс объектного объекта, возвращенного дочерним объектом.</span><span class="sxs-lookup"><span data-stu-id="2cb19-111">Address of a pointer to an [**IDirectXFileObject**](idirectxfileobject.md) interface, representing the returned child object's file object interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cb19-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2cb19-112">Return value</span></span>

<span data-ttu-id="2cb19-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2cb19-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2cb19-114">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="2cb19-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="2cb19-115">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадвалуе, дксфилирр \_ номореобжектс.</span><span class="sxs-lookup"><span data-stu-id="2cb19-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREOBJECTS.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cb19-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2cb19-116">Remarks</span></span>

<span data-ttu-id="2cb19-117">Чтобы определить тип извлекаемого объекта, используйте QueryInterface для запроса полученного объекта для поддержки интерфейсов [**идиректксфиледата**](idirectxfiledata.md), [**идиректксфиледатареференце**](idirectxfiledatareference.md)или [**идиректксфилебинари**](idirectxfilebinary.md) .</span><span class="sxs-lookup"><span data-stu-id="2cb19-117">To determine the type of object retrieved, use QueryInterface to query the retrieved object for support of [**IDirectXFileData**](idirectxfiledata.md), [**IDirectXFileDataReference**](idirectxfiledatareference.md), or [**IDirectXFileBinary**](idirectxfilebinary.md) interfaces.</span></span> <span data-ttu-id="2cb19-118">Поддерживаемый интерфейс указывает тип объекта (данные, ссылку на данные или двоичный).</span><span class="sxs-lookup"><span data-stu-id="2cb19-118">The interface supported indicates the type of object (data, data reference, or binary).</span></span>

## <a name="requirements"></a><span data-ttu-id="2cb19-119">Требования</span><span class="sxs-lookup"><span data-stu-id="2cb19-119">Requirements</span></span>



| <span data-ttu-id="2cb19-120">Требование</span><span class="sxs-lookup"><span data-stu-id="2cb19-120">Requirement</span></span> | <span data-ttu-id="2cb19-121">Значение</span><span class="sxs-lookup"><span data-stu-id="2cb19-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2cb19-122">Header</span><span class="sxs-lookup"><span data-stu-id="2cb19-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2cb19-123"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cb19-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="2cb19-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2cb19-124">Library</span></span><br/> | <dl> <span data-ttu-id="2cb19-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cb19-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cb19-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2cb19-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cb19-127">**идиректксфилебинари**</span><span class="sxs-lookup"><span data-stu-id="2cb19-127">**IDirectXFileBinary**</span></span>](idirectxfilebinary.md)
</dt> <dt>

[<span data-ttu-id="2cb19-128">**идиректксфиледата**</span><span class="sxs-lookup"><span data-stu-id="2cb19-128">**IDirectXFileData**</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="2cb19-129">**идиректксфиледатареференце**</span><span class="sxs-lookup"><span data-stu-id="2cb19-129">**IDirectXFileDataReference**</span></span>](idirectxfiledatareference.md)
</dt> </dl>

 

 




