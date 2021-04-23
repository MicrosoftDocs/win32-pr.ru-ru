---
description: Извлекает объект данных с указанным именем. Не рекомендуется.
ms.assetid: d04d5a45-72d9-4256-8700-378e8139ed36
title: 'Метод Идиректксфилинумобжект:: Жетдатаобжектбинаме (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 858097139702770d148765c4c9a57f6522d9633b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713931"
---
# <a name="idirectxfileenumobjectgetdataobjectbyname-method"></a><span data-ttu-id="383ab-104">Метод Идиректксфилинумобжект:: Жетдатаобжектбинаме</span><span class="sxs-lookup"><span data-stu-id="383ab-104">IDirectXFileEnumObject::GetDataObjectByName method</span></span>

<span data-ttu-id="383ab-105">Извлекает объект данных с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="383ab-105">Retrieves the data object that has the specified name.</span></span> <span data-ttu-id="383ab-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="383ab-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="383ab-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="383ab-107">Syntax</span></span>


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR            szName,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="383ab-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="383ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="383ab-109">*szName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="383ab-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="383ab-110">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="383ab-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="383ab-111">Указатель на запрошенное имя.</span><span class="sxs-lookup"><span data-stu-id="383ab-111">Pointer to the requested name.</span></span>

</dd> <dt>

<span data-ttu-id="383ab-112">*ппдатаобж* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="383ab-112">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="383ab-113">Тип: **[ **лпдиректксфиледата**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="383ab-113">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="383ab-114">Адрес указателя на интерфейс [**идиректксфиледата**](idirectxfiledata.md) , представляющий возвращаемый объект данных файла.</span><span class="sxs-lookup"><span data-stu-id="383ab-114">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="383ab-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="383ab-115">Return value</span></span>

<span data-ttu-id="383ab-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="383ab-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="383ab-117">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="383ab-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="383ab-118">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадвалуе, дксфилирр \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="383ab-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="383ab-119">Требования</span><span class="sxs-lookup"><span data-stu-id="383ab-119">Requirements</span></span>



| <span data-ttu-id="383ab-120">Требование</span><span class="sxs-lookup"><span data-stu-id="383ab-120">Requirement</span></span> | <span data-ttu-id="383ab-121">Значение</span><span class="sxs-lookup"><span data-stu-id="383ab-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="383ab-122">Header</span><span class="sxs-lookup"><span data-stu-id="383ab-122">Header</span></span><br/>  | <dl> <span data-ttu-id="383ab-123"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="383ab-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="383ab-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="383ab-124">Library</span></span><br/> | <dl> <span data-ttu-id="383ab-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="383ab-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="383ab-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="383ab-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="383ab-127">идиректксфилинумобжект</span><span class="sxs-lookup"><span data-stu-id="383ab-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 
