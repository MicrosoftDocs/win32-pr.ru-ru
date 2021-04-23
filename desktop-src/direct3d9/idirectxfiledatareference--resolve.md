---
description: Разрешает ссылки на данные. Не рекомендуется.
ms.assetid: e8cf6e5d-c9b2-4a47-b058-24282dc65e74
title: 'Метод Идиректксфиледатареференце:: Resolve (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference.Resolve
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 1b047245e3f89a618cde83e5c18a323f9364f3ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713865"
---
# <a name="idirectxfiledatareferenceresolve-method"></a><span data-ttu-id="6bc84-104">Метод Идиректксфиледатареференце:: Resolve</span><span class="sxs-lookup"><span data-stu-id="6bc84-104">IDirectXFileDataReference::Resolve method</span></span>

<span data-ttu-id="6bc84-105">Разрешает ссылки на данные.</span><span class="sxs-lookup"><span data-stu-id="6bc84-105">Resolves data references.</span></span> <span data-ttu-id="6bc84-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="6bc84-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bc84-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6bc84-107">Syntax</span></span>


```C++
HRESULT Resolve(
  [out, retval] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="6bc84-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6bc84-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bc84-109">*ппдатаобж* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6bc84-109">*ppDataObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6bc84-110">Тип: **[ **лпдиректксфиледата**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="6bc84-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="6bc84-111">Адрес указателя на интерфейс [**идиректксфиледата**](idirectxfiledata.md) , представляющий возвращаемый объект данных файла.</span><span class="sxs-lookup"><span data-stu-id="6bc84-111">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bc84-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6bc84-112">Return value</span></span>

<span data-ttu-id="6bc84-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6bc84-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6bc84-114">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6bc84-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="6bc84-115">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадвалуе, дксфилирр \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="6bc84-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bc84-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6bc84-116">Requirements</span></span>



| <span data-ttu-id="6bc84-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6bc84-117">Requirement</span></span> | <span data-ttu-id="6bc84-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6bc84-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6bc84-119">Header</span><span class="sxs-lookup"><span data-stu-id="6bc84-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6bc84-120"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bc84-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="6bc84-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6bc84-121">Library</span></span><br/> | <dl> <span data-ttu-id="6bc84-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bc84-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bc84-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6bc84-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bc84-124">идиректксфиледатареференце</span><span class="sxs-lookup"><span data-stu-id="6bc84-124">IDirectXFileDataReference</span></span>](idirectxfiledatareference.md)
</dt> </dl>

 

 




