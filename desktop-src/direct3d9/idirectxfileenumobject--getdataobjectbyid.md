---
description: Извлекает объект данных с указанным GUID. Не рекомендуется.
ms.assetid: dd079b5c-18e1-4252-aabd-498c24910a08
title: 'Метод Идиректксфилинумобжект:: Жетдатаобжектбид (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: a27ac17963d4876a3cb0a26d05b63f4c34bf99fc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713443"
---
# <a name="idirectxfileenumobjectgetdataobjectbyid-method"></a><span data-ttu-id="b3be8-104">Метод Идиректксфилинумобжект:: Жетдатаобжектбид</span><span class="sxs-lookup"><span data-stu-id="b3be8-104">IDirectXFileEnumObject::GetDataObjectById method</span></span>

<span data-ttu-id="b3be8-105">Извлекает объект данных с указанным GUID.</span><span class="sxs-lookup"><span data-stu-id="b3be8-105">Retrieves the data object that has the specified GUID.</span></span> <span data-ttu-id="b3be8-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="b3be8-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3be8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3be8-107">Syntax</span></span>


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID           rguid,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="b3be8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3be8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3be8-109">*ргуид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3be8-109">*rguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3be8-110">Тип: **[рефгуид](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="b3be8-110">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="b3be8-111">Ссылка на запрошенный GUID.</span><span class="sxs-lookup"><span data-stu-id="b3be8-111">Reference to the requested GUID.</span></span>

</dd> <dt>

<span data-ttu-id="b3be8-112">*ппдатаобж* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b3be8-112">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3be8-113">Тип: **[ **лпдиректксфиледата**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3be8-113">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="b3be8-114">Адрес указателя на интерфейс [**идиректксфиледата**](idirectxfiledata.md) , представляющий возвращаемый объект данных файла.</span><span class="sxs-lookup"><span data-stu-id="b3be8-114">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3be8-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3be8-115">Return value</span></span>

<span data-ttu-id="b3be8-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b3be8-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b3be8-117">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b3be8-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="b3be8-118">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадвалуе, дксфилирр \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="b3be8-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3be8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b3be8-119">Requirements</span></span>



| <span data-ttu-id="b3be8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b3be8-120">Requirement</span></span> | <span data-ttu-id="b3be8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b3be8-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3be8-122">Header</span><span class="sxs-lookup"><span data-stu-id="b3be8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b3be8-123"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3be8-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="b3be8-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b3be8-124">Library</span></span><br/> | <dl> <span data-ttu-id="b3be8-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3be8-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3be8-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3be8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3be8-127">идиректксфилинумобжект</span><span class="sxs-lookup"><span data-stu-id="b3be8-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 
