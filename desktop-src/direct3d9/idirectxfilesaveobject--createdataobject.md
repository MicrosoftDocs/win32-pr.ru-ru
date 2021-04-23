---
description: Создает объект данных. Не рекомендуется.
ms.assetid: bb0ef2cf-db76-40f6-968f-3599c58459a7
title: 'Метод Идиректксфилесавеобжект:: Креатедатаобжект (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.CreateDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 7c5a67a72f6ff5a63730167d2fe2d12213a9ab72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354673"
---
# <a name="idirectxfilesaveobjectcreatedataobject-method"></a><span data-ttu-id="72622-104">Метод Идиректксфилесавеобжект:: Креатедатаобжект</span><span class="sxs-lookup"><span data-stu-id="72622-104">IDirectXFileSaveObject::CreateDataObject method</span></span>

<span data-ttu-id="72622-105">Создает объект данных.</span><span class="sxs-lookup"><span data-stu-id="72622-105">Creates a data object.</span></span> <span data-ttu-id="72622-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="72622-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="72622-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72622-107">Syntax</span></span>


```C++
HRESULT CreateDataObject(
  [in]                REFGUID           rguidTemplate,
  [in]                LPCSTR            szName,
  [in]          const GUID              *pguid,
  [in]                DWORD             cbSize,
  [in]                LPVOID            pvData,
  [out, retval]       LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="72622-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="72622-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72622-109">*ргуидтемплате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="72622-109">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72622-110">Тип: **[рефгуид](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="72622-110">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="72622-111">Идентификатор GUID, представляющий шаблон объекта данных.</span><span class="sxs-lookup"><span data-stu-id="72622-111">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="72622-112">*szName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="72622-112">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72622-113">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72622-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="72622-114">Указатель на имя объекта данных.</span><span class="sxs-lookup"><span data-stu-id="72622-114">Pointer to the name of the data object.</span></span> <span data-ttu-id="72622-115">Укажите **значение NULL** , если у объекта нет имени.</span><span class="sxs-lookup"><span data-stu-id="72622-115">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="72622-116">*пгуид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="72622-116">*pguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72622-117">Тип: **константа [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="72622-117">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="72622-118">Указатель на идентификатор GUID, представляющий объект данных.</span><span class="sxs-lookup"><span data-stu-id="72622-118">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="72622-119">Укажите **значение NULL** , если у объекта нет идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="72622-119">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="72622-120">*кбсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="72622-120">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72622-121">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72622-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="72622-122">Размер объекта данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="72622-122">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="72622-123">*пвдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="72622-123">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72622-124">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72622-124">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="72622-125">Указатель на буфер, содержащий все данные необходимых элементов.</span><span class="sxs-lookup"><span data-stu-id="72622-125">Pointer to a buffer containing all required member's data.</span></span>

</dd> <dt>

<span data-ttu-id="72622-126">*ппдатаобж* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="72622-126">*ppDataObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="72622-127">Тип: **[ **лпдиректксфиледата**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="72622-127">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="72622-128">Адрес указателя на интерфейс [**идиректксфиледата**](idirectxfiledata.md) , представляющий созданный объект данных файла.</span><span class="sxs-lookup"><span data-stu-id="72622-128">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the created file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72622-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="72622-129">Return value</span></span>

<span data-ttu-id="72622-130">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="72622-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="72622-131">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="72622-131">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="72622-132">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих значений. ДКСФИЛИРР \_ БАДАЛЛОК дксфилирр \_ бадвалуе</span><span class="sxs-lookup"><span data-stu-id="72622-132">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="72622-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="72622-133">Remarks</span></span>

<span data-ttu-id="72622-134">Если эталонный объект данных будет ссылаться на объект данных, параметр szName или пгуид должен иметь значение, отличное от **null**.</span><span class="sxs-lookup"><span data-stu-id="72622-134">If a data reference object will reference the data object, either the szName or pguid parameter must be non-**NULL**.</span></span>

<span data-ttu-id="72622-135">Сохраните все шаблоны с помощью метода [**идиректксфилесавеобжект:: саветемплатес**](idirectxfilesaveobject--savetemplates.md) перед сохранением данных, созданных этим методом.</span><span class="sxs-lookup"><span data-stu-id="72622-135">Save any templates by using the [**IDirectXFileSaveObject::SaveTemplates**](idirectxfilesaveobject--savetemplates.md) method before saving the data created by this method.</span></span> <span data-ttu-id="72622-136">Сохраните созданные данные с помощью метода [**идиректксфилесавеобжект:: SaveData**](idirectxfilesaveobject--savedata.md) .</span><span class="sxs-lookup"><span data-stu-id="72622-136">Save the created data by using the [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) method.</span></span>

<span data-ttu-id="72622-137">Если необходимо сохранить необязательные данные, используйте метод [**идиректксфиледата:: адддатаобжект**](idirectxfiledata--adddataobject.md) после использования этого метода и перед использованием [**Идиректксфилесавеобжект:: SaveData**](idirectxfilesaveobject--savedata.md).</span><span class="sxs-lookup"><span data-stu-id="72622-137">If you need to save optional data, use the [**IDirectXFileData::AddDataObject**](idirectxfiledata--adddataobject.md) method after using this method and before using [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md).</span></span> <span data-ttu-id="72622-138">Если у объекта есть дочерние объекты, добавьте их перед вызовом **идиректксфилесавеобжект:: SaveData**.</span><span class="sxs-lookup"><span data-stu-id="72622-138">If the object has child objects, add them before calling **IDirectXFileSaveObject::SaveData**.</span></span>

## <a name="requirements"></a><span data-ttu-id="72622-139">Требования</span><span class="sxs-lookup"><span data-stu-id="72622-139">Requirements</span></span>



| <span data-ttu-id="72622-140">Требование</span><span class="sxs-lookup"><span data-stu-id="72622-140">Requirement</span></span> | <span data-ttu-id="72622-141">Значение</span><span class="sxs-lookup"><span data-stu-id="72622-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72622-142">Header</span><span class="sxs-lookup"><span data-stu-id="72622-142">Header</span></span><br/>  | <dl> <span data-ttu-id="72622-143"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="72622-143"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="72622-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="72622-144">Library</span></span><br/> | <dl> <span data-ttu-id="72622-145"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72622-145"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72622-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72622-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72622-147">идиректксфилесавеобжект</span><span class="sxs-lookup"><span data-stu-id="72622-147">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> <dt>

[<span data-ttu-id="72622-148">**Идиректксфиледата:: Адддатаобжект**</span><span class="sxs-lookup"><span data-stu-id="72622-148">**IDirectXFileData::AddDataObject**</span></span>](idirectxfiledata--adddataobject.md)
</dt> <dt>

[<span data-ttu-id="72622-149">**Идиректксфилесавеобжект:: SaveData**</span><span class="sxs-lookup"><span data-stu-id="72622-149">**IDirectXFileSaveObject::SaveData**</span></span>](idirectxfilesaveobject--savedata.md)
</dt> <dt>

[<span data-ttu-id="72622-150">**Идиректксфилесавеобжект:: Саветемплатес**</span><span class="sxs-lookup"><span data-stu-id="72622-150">**IDirectXFileSaveObject::SaveTemplates**</span></span>](idirectxfilesaveobject--savetemplates.md)
</dt> </dl>

 

 
