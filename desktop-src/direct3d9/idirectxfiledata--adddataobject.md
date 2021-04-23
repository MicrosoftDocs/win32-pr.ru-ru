---
description: Добавляет объект данных в качестве дочернего объекта. Не рекомендуется.
ms.assetid: 43771dd6-c17f-4376-9b0a-459ba61ff4c5
title: 'Метод Идиректксфиледата:: Адддатаобжект (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 393526bb249b0337964bee0af5be1b55b8dd513e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355400"
---
# <a name="idirectxfiledataadddataobject-method"></a><span data-ttu-id="a21af-104">Метод Идиректксфиледата:: Адддатаобжект</span><span class="sxs-lookup"><span data-stu-id="a21af-104">IDirectXFileData::AddDataObject method</span></span>

<span data-ttu-id="a21af-105">Добавляет объект данных в качестве дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="a21af-105">Adds a data object as a child object.</span></span> <span data-ttu-id="a21af-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a21af-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="a21af-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a21af-107">Syntax</span></span>


```C++
HRESULT AddDataObject(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="a21af-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a21af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a21af-109">*пдатаобж* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a21af-109">*pDataObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a21af-110">Тип: **[ **лпдиректксфиледата**](idirectxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="a21af-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span></span>

<span data-ttu-id="a21af-111">Указатель на интерфейс [**идиректксфиледата**](idirectxfiledata.md) , представляющий файл данных файла, который необходимо добавить в качестве дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="a21af-111">Pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the file data object to add as a child object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a21af-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a21af-112">Return value</span></span>

<span data-ttu-id="a21af-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a21af-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a21af-114">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a21af-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="a21af-115">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих значений. ДКСФИЛИРР \_ БАДАЛЛОК дксфилирр \_ бадвалуе</span><span class="sxs-lookup"><span data-stu-id="a21af-115">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="a21af-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a21af-116">Remarks</span></span>

<span data-ttu-id="a21af-117">Перед вызовом этого метода используйте метод [**идиректксфилесавеобжект:: креатедатаобжект**](idirectxfilesaveobject--createdataobject.md) , чтобы создать объект [**идиректксфиледата**](idirectxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="a21af-117">Use the [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) method to create the [**IDirectXFileData**](idirectxfiledata.md) object before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a21af-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a21af-118">Requirements</span></span>



| <span data-ttu-id="a21af-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a21af-119">Requirement</span></span> | <span data-ttu-id="a21af-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a21af-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a21af-121">Header</span><span class="sxs-lookup"><span data-stu-id="a21af-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a21af-122"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="a21af-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="a21af-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a21af-123">Library</span></span><br/> | <dl> <span data-ttu-id="a21af-124"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a21af-124"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a21af-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a21af-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a21af-126">идиректксфиледата</span><span class="sxs-lookup"><span data-stu-id="a21af-126">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="a21af-127">**Идиректксфилесавеобжект:: Креатедатаобжект**</span><span class="sxs-lookup"><span data-stu-id="a21af-127">**IDirectXFileSaveObject::CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 




