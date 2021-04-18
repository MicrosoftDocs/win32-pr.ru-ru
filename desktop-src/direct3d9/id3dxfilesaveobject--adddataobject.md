---
description: Добавляет объект данных в качестве дочернего элемента для объекта ID3DXFileSaveData.
ms.assetid: 710a1588-d766-4555-97a3-4b5a517ce805
title: 'Метод ID3DXFileSaveObject:: Адддатаобжект (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d1586035a0d8a81c2210009bad903aac5197bcf7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713656"
---
# <a name="id3dxfilesaveobjectadddataobject-method"></a><span data-ttu-id="c4561-103">Метод ID3DXFileSaveObject:: Адддатаобжект</span><span class="sxs-lookup"><span data-stu-id="c4561-103">ID3DXFileSaveObject::AddDataObject method</span></span>

<span data-ttu-id="c4561-104">Добавляет объект данных в качестве дочернего элемента для объекта [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="c4561-104">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4561-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4561-105">Syntax</span></span>


```C++
HRESULT AddDataObject(
  [in]               REFGUID           rguidTemplate,
  [in]               LPCSTR            szName,
  [in]         const GUID              *pId,
  [in]               SIZE_T            cbSize,
  [in]               LPCVOID           pvData,
  [in, retval]       ID3DXFileSaveData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="c4561-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4561-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4561-107">*ргуидтемплате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4561-107">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4561-108">Тип: **[рефгуид](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="c4561-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="c4561-109">Идентификатор GUID, представляющий шаблон объекта данных.</span><span class="sxs-lookup"><span data-stu-id="c4561-109">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="c4561-110">*szName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4561-110">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4561-111">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4561-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4561-112">Указатель на имя объекта данных.</span><span class="sxs-lookup"><span data-stu-id="c4561-112">Pointer to the name of the data object.</span></span> <span data-ttu-id="c4561-113">Укажите **значение NULL** , если у объекта нет имени.</span><span class="sxs-lookup"><span data-stu-id="c4561-113">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="c4561-114">*идентификатор процесса* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4561-114">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4561-115">Тип: **константа [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="c4561-115">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="c4561-116">Указатель на идентификатор GUID, представляющий объект данных.</span><span class="sxs-lookup"><span data-stu-id="c4561-116">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="c4561-117">Укажите **значение NULL** , если у объекта нет идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="c4561-117">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="c4561-118">*кбсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4561-118">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4561-119">Type: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4561-119">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4561-120">Размер объекта данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="c4561-120">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c4561-121">*пвдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4561-121">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4561-122">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4561-122">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4561-123">Указатель на буфер, содержащий все необходимые данные в объекте данных.</span><span class="sxs-lookup"><span data-stu-id="c4561-123">Pointer to a buffer containing all required data in the data object.</span></span>

</dd> <dt>

<span data-ttu-id="c4561-124">*ппобж* \[ в, retval\]</span><span class="sxs-lookup"><span data-stu-id="c4561-124">*ppObj* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c4561-125">Тип: **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c4561-125">Type: **[**ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span></span>

<span data-ttu-id="c4561-126">Адрес указателя на интерфейс [**ID3DXFileSaveData**](id3dxfilesavedata.md) , представляющий узел данных файла, в который будет добавлен объект данных.</span><span class="sxs-lookup"><span data-stu-id="c4561-126">Address of a pointer to an [**ID3DXFileSaveData**](id3dxfilesavedata.md) interface, representing the file data node to which the data object will be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4561-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4561-127">Return value</span></span>

<span data-ttu-id="c4561-128">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c4561-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c4561-129">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="c4561-129">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c4561-130">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DXFERR \_ бадобжект, дксфилирр \_ Бадвалуе, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c4561-130">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, DXFILEERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4561-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c4561-131">Remarks</span></span>

<span data-ttu-id="c4561-132">Если эталонный объект данных будет ссылаться на объект данных, параметр szName или pId должен иметь значение, отличное от **null**.</span><span class="sxs-lookup"><span data-stu-id="c4561-132">If a data reference object will reference the data object, either the szName or pId parameter must be non-**NULL**.</span></span>

<span data-ttu-id="c4561-133">Сохраните созданные данные на диск с помощью метода [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md) .</span><span class="sxs-lookup"><span data-stu-id="c4561-133">Save the created data to disk by using the [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4561-134">Требования</span><span class="sxs-lookup"><span data-stu-id="c4561-134">Requirements</span></span>



| <span data-ttu-id="c4561-135">Требование</span><span class="sxs-lookup"><span data-stu-id="c4561-135">Requirement</span></span> | <span data-ttu-id="c4561-136">Значение</span><span class="sxs-lookup"><span data-stu-id="c4561-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4561-137">Header</span><span class="sxs-lookup"><span data-stu-id="c4561-137">Header</span></span><br/>  | <dl> <span data-ttu-id="c4561-138"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4561-138"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="c4561-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c4561-139">Library</span></span><br/> | <dl> <span data-ttu-id="c4561-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4561-140"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c4561-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4561-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4561-142">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="c4561-142">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 
