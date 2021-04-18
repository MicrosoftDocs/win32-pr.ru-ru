---
description: Извлекает данные для одного из элементов объекта или данные для всех элементов. Не рекомендуется.
ms.assetid: 2a227705-371e-41f1-af5d-20e652cd07f6
title: 'Метод Идиректксфиледата:: GetData (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: ed52aaf0b4c740b675129c81843c0bd49c7f428e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713868"
---
# <a name="idirectxfiledatagetdata-method"></a><span data-ttu-id="114db-104">Метод Идиректксфиледата:: GetData</span><span class="sxs-lookup"><span data-stu-id="114db-104">IDirectXFileData::GetData method</span></span>

<span data-ttu-id="114db-105">Извлекает данные для одного из элементов объекта или данные для всех элементов.</span><span class="sxs-lookup"><span data-stu-id="114db-105">Retrieves the data for one of the object's members or the data for all members.</span></span> <span data-ttu-id="114db-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="114db-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="114db-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="114db-107">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  LPCSTR szMember,
  [out] DWORD  *pcbSize,
  [out] void   **ppvData
);
```



## <a name="parameters"></a><span data-ttu-id="114db-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="114db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="114db-109">*сзмембер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="114db-109">*szMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="114db-110">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="114db-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="114db-111">Указатель на имя элемента, для которого необходимо получить данные.</span><span class="sxs-lookup"><span data-stu-id="114db-111">Pointer to the name of the member for which to retrieve data.</span></span> <span data-ttu-id="114db-112">Укажите **значение NULL** , чтобы получить данные всех необходимых элементов.</span><span class="sxs-lookup"><span data-stu-id="114db-112">Specify **NULL** to retrieve all required members' data.</span></span>

</dd> <dt>

<span data-ttu-id="114db-113">*пкбсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="114db-113">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="114db-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="114db-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="114db-115">Указатель на получение размера буфера Ппвдата в байтах.</span><span class="sxs-lookup"><span data-stu-id="114db-115">Pointer to receive the ppvData buffer size, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="114db-116">*ппвдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="114db-116">*ppvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="114db-117">Тип: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="114db-117">Type: **void\*\***</span></span>

<span data-ttu-id="114db-118">Адрес указателя на буфер для получения данных, связанных с Сзмембер.</span><span class="sxs-lookup"><span data-stu-id="114db-118">Address of a pointer to the buffer to receive the data associated with szMember.</span></span> <span data-ttu-id="114db-119">Если Сзмембер имеет **значение NULL**, ппвдата задается как указатель на буфер, содержащий все необходимые данные элементов в непрерывном блоке памяти.</span><span class="sxs-lookup"><span data-stu-id="114db-119">If szMember is **NULL**, ppvData is set to point to a buffer containing all required members' data in a contiguous block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="114db-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="114db-120">Return value</span></span>

<span data-ttu-id="114db-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="114db-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="114db-122">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="114db-122">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="114db-123">Если метод завершается ошибкой, возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадаррайсизе, дксфилирр \_ БАДДАТАРЕФЕРЕНЦЕ, дксфилирр \_ бадвалуе.</span><span class="sxs-lookup"><span data-stu-id="114db-123">If the method fails, the return value can be one of the following values: DXFILEERR\_BADARRAYSIZE, DXFILEERR\_BADDataReference, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="114db-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="114db-124">Remarks</span></span>

<span data-ttu-id="114db-125">Этот метод получает данные для обязательных элементов объекта данных, но не имеет данных для необязательных (дочерних) элементов.</span><span class="sxs-lookup"><span data-stu-id="114db-125">This method retrieves the data for required members of a data object but no data for optional (child) members.</span></span> <span data-ttu-id="114db-126">Чтобы получить дочерние объекты, используйте [**идиректксфиледата:: жетнекстобжект**](idirectxfiledata--getnextobject.md) .</span><span class="sxs-lookup"><span data-stu-id="114db-126">Use [**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md) to retrieve child objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="114db-127">Требования</span><span class="sxs-lookup"><span data-stu-id="114db-127">Requirements</span></span>



| <span data-ttu-id="114db-128">Требование</span><span class="sxs-lookup"><span data-stu-id="114db-128">Requirement</span></span> | <span data-ttu-id="114db-129">Значение</span><span class="sxs-lookup"><span data-stu-id="114db-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="114db-130">Header</span><span class="sxs-lookup"><span data-stu-id="114db-130">Header</span></span><br/>  | <dl> <span data-ttu-id="114db-131"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="114db-131"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="114db-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="114db-132">Library</span></span><br/> | <dl> <span data-ttu-id="114db-133"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="114db-133"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="114db-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="114db-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="114db-135">идиректксфиледата</span><span class="sxs-lookup"><span data-stu-id="114db-135">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="114db-136">**Идиректксфиледата:: Жетнекстобжект**</span><span class="sxs-lookup"><span data-stu-id="114db-136">**IDirectXFileData::GetNextObject**</span></span>](idirectxfiledata--getnextobject.md)
</dt> </dl>

 

 
