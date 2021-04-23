---
description: Добавляет объект данных в качестве дочернего элемента для узла данных файла ID3DXFileSaveData.
ms.assetid: 47faad99-3ee8-4ca8-b8d7-413d4cd5b090
title: 'Метод ID3DXFileSaveData:: Адддатаобжект (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b097e63792b32bc1688ce93c8ce32ffaedeae6ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355220"
---
# <a name="id3dxfilesavedataadddataobject-method"></a><span data-ttu-id="7deda-103">Метод ID3DXFileSaveData:: Адддатаобжект</span><span class="sxs-lookup"><span data-stu-id="7deda-103">ID3DXFileSaveData::AddDataObject method</span></span>

<span data-ttu-id="7deda-104">Добавляет объект данных в качестве дочернего элемента для узла данных файла [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="7deda-104">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="7deda-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7deda-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="7deda-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7deda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7deda-107">*ргуидтемплате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7deda-107">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7deda-108">Тип: **[рефгуид](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="7deda-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="7deda-109">Идентификатор GUID, представляющий шаблон объекта данных.</span><span class="sxs-lookup"><span data-stu-id="7deda-109">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="7deda-110">*szName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7deda-110">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7deda-111">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7deda-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7deda-112">Указатель на имя добавляемого объекта данных.</span><span class="sxs-lookup"><span data-stu-id="7deda-112">Pointer to the name of the data object to add.</span></span> <span data-ttu-id="7deda-113">Укажите **значение NULL** , если у объекта нет имени.</span><span class="sxs-lookup"><span data-stu-id="7deda-113">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="7deda-114">*идентификатор процесса* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7deda-114">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7deda-115">Тип: **константа [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="7deda-115">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="7deda-116">Указатель на идентификатор GUID, представляющий объект данных.</span><span class="sxs-lookup"><span data-stu-id="7deda-116">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="7deda-117">Объект данных должен быть зарегистрирован с помощью [**ID3DXFile:: регистертемплатес**](id3dxfile--registertemplates.md) или [**ID3DXFile:: регистеренумтемплатес**](id3dxfile--registerenumtemplates.md).</span><span class="sxs-lookup"><span data-stu-id="7deda-117">The data object must have been registered with [**ID3DXFile::RegisterTemplates**](id3dxfile--registertemplates.md) or [**ID3DXFile::RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md).</span></span> <span data-ttu-id="7deda-118">Укажите **значение NULL** , если у объекта нет идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="7deda-118">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="7deda-119">*кбсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7deda-119">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7deda-120">Type: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7deda-120">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7deda-121">Размер объекта данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="7deda-121">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7deda-122">*пвдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7deda-122">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7deda-123">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7deda-123">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7deda-124">Указатель на буфер, содержащий все необходимые данные в объекте данных.</span><span class="sxs-lookup"><span data-stu-id="7deda-124">Pointer to a buffer containing all required data in the data object.</span></span>

</dd> <dt>

<span data-ttu-id="7deda-125">*ппобж* \[ в, retval\]</span><span class="sxs-lookup"><span data-stu-id="7deda-125">*ppObj* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7deda-126">Тип: **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="7deda-126">Type: **[**ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span></span>

<span data-ttu-id="7deda-127">Адрес указателя на интерфейс [**ID3DXFileSaveData**](id3dxfilesavedata.md) , представляющий узел данных файла, в который будет добавлен объект данных.</span><span class="sxs-lookup"><span data-stu-id="7deda-127">Address of a pointer to an [**ID3DXFileSaveData**](id3dxfilesavedata.md) interface, representing the file data node to which the data object will be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7deda-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7deda-128">Return value</span></span>

<span data-ttu-id="7deda-129">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7deda-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7deda-130">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="7deda-130">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7deda-131">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DXFERR \_ бадобжект, D3DXFERR \_ Бадвалуе, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7deda-131">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, D3DXFERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="7deda-132">Требования</span><span class="sxs-lookup"><span data-stu-id="7deda-132">Requirements</span></span>



| <span data-ttu-id="7deda-133">Требование</span><span class="sxs-lookup"><span data-stu-id="7deda-133">Requirement</span></span> | <span data-ttu-id="7deda-134">Значение</span><span class="sxs-lookup"><span data-stu-id="7deda-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7deda-135">Header</span><span class="sxs-lookup"><span data-stu-id="7deda-135">Header</span></span><br/>  | <dl> <span data-ttu-id="7deda-136"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="7deda-136"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="7deda-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7deda-137">Library</span></span><br/> | <dl> <span data-ttu-id="7deda-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7deda-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7deda-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7deda-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7deda-140">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="7deda-140">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 
