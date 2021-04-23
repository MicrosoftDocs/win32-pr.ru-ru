---
description: Извлекает идентификатор GUID шаблона объекта. Не рекомендуется.
ms.assetid: bb4a4a32-a9e7-4caa-869d-24cfb310d8d1
title: 'Метод Идиректксфиледата:: GetType (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 463391c661b2d166a6fba773e3b01590daf0ebd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157223"
---
# <a name="idirectxfiledatagettype-method"></a><span data-ttu-id="bb30b-104">Метод Идиректксфиледата:: GetType</span><span class="sxs-lookup"><span data-stu-id="bb30b-104">IDirectXFileData::GetType method</span></span>

<span data-ttu-id="bb30b-105">Извлекает идентификатор GUID шаблона объекта.</span><span class="sxs-lookup"><span data-stu-id="bb30b-105">Retrieves the GUID of the object's template.</span></span> <span data-ttu-id="bb30b-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="bb30b-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb30b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb30b-107">Syntax</span></span>


```C++
HRESULT GetType(
  [out, retval] const GUID **ppguid
);
```



## <a name="parameters"></a><span data-ttu-id="bb30b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb30b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb30b-109">*ппгуид* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="bb30b-109">*ppguid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bb30b-110">Тип: **константа [**GUID**](guid.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="bb30b-110">Type: **const [**GUID**](guid.md)\*\***</span></span>

<span data-ttu-id="bb30b-111">Адрес указателя для получения идентификатора GUID шаблона объекта.</span><span class="sxs-lookup"><span data-stu-id="bb30b-111">Address of a pointer to receive the GUID of the object's template.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb30b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bb30b-112">Return value</span></span>

<span data-ttu-id="bb30b-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bb30b-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bb30b-114">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="bb30b-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="bb30b-115">В случае сбоя метода возвращаемое значение может быть ДКСФИЛИРР \_ бадвалуе.</span><span class="sxs-lookup"><span data-stu-id="bb30b-115">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb30b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="bb30b-116">Requirements</span></span>



| <span data-ttu-id="bb30b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="bb30b-117">Requirement</span></span> | <span data-ttu-id="bb30b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="bb30b-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb30b-119">Header</span><span class="sxs-lookup"><span data-stu-id="bb30b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="bb30b-120"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb30b-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb30b-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bb30b-121">Library</span></span><br/> | <dl> <span data-ttu-id="bb30b-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb30b-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb30b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb30b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb30b-124">идиректксфиледата</span><span class="sxs-lookup"><span data-stu-id="bb30b-124">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> </dl>

 

 




