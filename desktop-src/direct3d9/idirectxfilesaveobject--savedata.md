---
description: Сохраняет объект данных и его дочерние элементы в файле DirectX. Не рекомендуется.
ms.assetid: 18bd5ef6-9e17-4c21-bc14-373de8df9ffb
title: 'Метод Идиректксфилесавеобжект:: SaveData (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: cb901bd984e1fcd923d0ea172fb5f387b3a9302a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713626"
---
# <a name="idirectxfilesaveobjectsavedata-method"></a><span data-ttu-id="23239-104">Метод Идиректксфилесавеобжект:: SaveData</span><span class="sxs-lookup"><span data-stu-id="23239-104">IDirectXFileSaveObject::SaveData method</span></span>

<span data-ttu-id="23239-105">Сохраняет объект данных и его дочерние элементы в файле DirectX.</span><span class="sxs-lookup"><span data-stu-id="23239-105">Saves a data object and its children to a DirectX file.</span></span> <span data-ttu-id="23239-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="23239-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="23239-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23239-107">Syntax</span></span>


```C++
HRESULT SaveData(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="23239-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="23239-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23239-109">*пдатаобж* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23239-109">*pDataObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23239-110">Тип: **[ **лпдиректксфиледата**](idirectxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="23239-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span></span>

<span data-ttu-id="23239-111">Указатель на интерфейс [**идиректксфиледата**](idirectxfiledata.md) , представляющий объект данных файла для сохранения.</span><span class="sxs-lookup"><span data-stu-id="23239-111">Pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the file data object to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23239-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23239-112">Return value</span></span>

<span data-ttu-id="23239-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="23239-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="23239-114">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="23239-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="23239-115">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадаррайсизе, дксфилирр \_ бадвалуе.</span><span class="sxs-lookup"><span data-stu-id="23239-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADARRAYSIZE, DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="23239-116">Требования</span><span class="sxs-lookup"><span data-stu-id="23239-116">Requirements</span></span>



| <span data-ttu-id="23239-117">Требование</span><span class="sxs-lookup"><span data-stu-id="23239-117">Requirement</span></span> | <span data-ttu-id="23239-118">Значение</span><span class="sxs-lookup"><span data-stu-id="23239-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23239-119">Header</span><span class="sxs-lookup"><span data-stu-id="23239-119">Header</span></span><br/>  | <dl> <span data-ttu-id="23239-120"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="23239-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="23239-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="23239-121">Library</span></span><br/> | <dl> <span data-ttu-id="23239-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23239-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23239-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23239-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23239-124">идиректксфилесавеобжект</span><span class="sxs-lookup"><span data-stu-id="23239-124">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> </dl>

 

 




