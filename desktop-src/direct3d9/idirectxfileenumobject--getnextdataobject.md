---
description: Извлекает следующий объект верхнего уровня в файле DirectX. Не рекомендуется.
ms.assetid: 91cd3205-5603-4a62-aab2-7ef4adb9e6d1
title: 'Метод Идиректксфилинумобжект:: Жетнекстдатаобжект (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetNextDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: bc50af216eaae1687351d472b7151aaaeae9116f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354230"
---
# <a name="idirectxfileenumobjectgetnextdataobject-method"></a><span data-ttu-id="86fab-104">Метод Идиректксфилинумобжект:: Жетнекстдатаобжект</span><span class="sxs-lookup"><span data-stu-id="86fab-104">IDirectXFileEnumObject::GetNextDataObject method</span></span>

<span data-ttu-id="86fab-105">Извлекает следующий объект верхнего уровня в файле DirectX.</span><span class="sxs-lookup"><span data-stu-id="86fab-105">Retrieves the next top-level object in the DirectX file.</span></span> <span data-ttu-id="86fab-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="86fab-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="86fab-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86fab-107">Syntax</span></span>


```C++
HRESULT GetNextDataObject(
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="86fab-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="86fab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86fab-109">*ппдатаобж* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="86fab-109">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86fab-110">Тип: **[ **лпдиректксфиледата**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="86fab-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="86fab-111">Адрес указателя на интерфейс [**идиректксфиледата**](idirectxfiledata.md) , представляющий возвращаемый объект данных файла.</span><span class="sxs-lookup"><span data-stu-id="86fab-111">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86fab-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86fab-112">Return value</span></span>

<span data-ttu-id="86fab-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="86fab-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="86fab-114">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="86fab-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="86fab-115">Если метод завершается ошибкой, возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадвалуе, дксфилирр \_ номореобжектс</span><span class="sxs-lookup"><span data-stu-id="86fab-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREOBJECTS</span></span>

## <a name="remarks"></a><span data-ttu-id="86fab-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86fab-116">Remarks</span></span>

<span data-ttu-id="86fab-117">Объекты верхнего уровня всегда являются объектами данных.</span><span class="sxs-lookup"><span data-stu-id="86fab-117">Top-level objects are always data objects.</span></span> <span data-ttu-id="86fab-118">Объекты ссылок на данные и двоичные объекты могут быть только дочерними объектами данных.</span><span class="sxs-lookup"><span data-stu-id="86fab-118">Data reference objects and binary objects can only be children of data objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="86fab-119">Требования</span><span class="sxs-lookup"><span data-stu-id="86fab-119">Requirements</span></span>



| <span data-ttu-id="86fab-120">Требование</span><span class="sxs-lookup"><span data-stu-id="86fab-120">Requirement</span></span> | <span data-ttu-id="86fab-121">Значение</span><span class="sxs-lookup"><span data-stu-id="86fab-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86fab-122">Header</span><span class="sxs-lookup"><span data-stu-id="86fab-122">Header</span></span><br/>  | <dl> <span data-ttu-id="86fab-123"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="86fab-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="86fab-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="86fab-124">Library</span></span><br/> | <dl> <span data-ttu-id="86fab-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86fab-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86fab-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86fab-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86fab-127">идиректксфилинумобжект</span><span class="sxs-lookup"><span data-stu-id="86fab-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 




