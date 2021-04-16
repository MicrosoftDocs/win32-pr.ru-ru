---
description: Создает экземпляр объекта Директксфиле. Не рекомендуется.
ms.assetid: c920d480-2557-491d-87ea-7eea1f470498
title: Функция Директксфилекреате (Дксфиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DirectXFileCreate
api_type:
- DllExport
api_location:
- d3dxof.dll
ms.openlocfilehash: 8ee1787941bbb902e6f0f50b082867aaf2f0a8bc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720875"
---
# <a name="directxfilecreate-function"></a><span data-ttu-id="2d2fd-104">Функция Директксфилекреате</span><span class="sxs-lookup"><span data-stu-id="2d2fd-104">DirectXFileCreate function</span></span>

<span data-ttu-id="2d2fd-105">Создает экземпляр объекта Директксфиле.</span><span class="sxs-lookup"><span data-stu-id="2d2fd-105">Creates an instance of a DirectXFile object.</span></span> <span data-ttu-id="2d2fd-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="2d2fd-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d2fd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d2fd-107">Syntax</span></span>


```C++
HRESULT STDAPICALLTYPE DirectXFileCreate(
   LPDIRECTXFILE *lplpDirectXFile
);
```



## <a name="parameters"></a><span data-ttu-id="2d2fd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d2fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d2fd-109">*лплпдиректксфиле*</span><span class="sxs-lookup"><span data-stu-id="2d2fd-109">*lplpDirectXFile*</span></span> 
</dt> <dd>

<span data-ttu-id="2d2fd-110">Тип: **[ **лпдиректксфиле**](idirectxfile.md)\***</span><span class="sxs-lookup"><span data-stu-id="2d2fd-110">Type: **[**LPDIRECTXFILE**](idirectxfile.md)\***</span></span>

<span data-ttu-id="2d2fd-111">Адрес указателя на интерфейс [**идиректксфиле**](idirectxfile.md) , представляющий созданный объект директксфиле.</span><span class="sxs-lookup"><span data-stu-id="2d2fd-111">Address of a pointer to an [**IDirectXFile**](idirectxfile.md) interface, representing the created DirectXFile object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d2fd-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d2fd-112">Return value</span></span>

<span data-ttu-id="2d2fd-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2d2fd-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2d2fd-114">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="2d2fd-114">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2d2fd-115">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадаллок, дксфилирр \_ бадвалуе.</span><span class="sxs-lookup"><span data-stu-id="2d2fd-115">If the function fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d2fd-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2d2fd-116">Remarks</span></span>

<span data-ttu-id="2d2fd-117">После использования этой функции используйте [**регистертемплатес**](idirectxfile--registertemplates.md) для регистрации шаблонов, [**креатинумобжект**](idirectxfile--createenumobject.md) для создания объекта перечислителя или [**креатесавеобжект**](idirectxfile--createsaveobject.md) для создания объекта Save.</span><span class="sxs-lookup"><span data-stu-id="2d2fd-117">After using this function, use [**RegisterTemplates**](idirectxfile--registertemplates.md) to register templates, [**CreateEnumObject**](idirectxfile--createenumobject.md) to create an enumerator object, or [**CreateSaveObject**](idirectxfile--createsaveobject.md) to create a save object.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d2fd-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2d2fd-118">Requirements</span></span>



| <span data-ttu-id="2d2fd-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2d2fd-119">Requirement</span></span> | <span data-ttu-id="2d2fd-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2d2fd-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d2fd-121">Header</span><span class="sxs-lookup"><span data-stu-id="2d2fd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2d2fd-122"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d2fd-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d2fd-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2d2fd-123">Library</span></span><br/> | <dl> <span data-ttu-id="2d2fd-124"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d2fd-124"><dt>D3dxof.lib</dt></span></span> </dl> |
| <span data-ttu-id="2d2fd-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2d2fd-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="2d2fd-126"><dt>D3dxof.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d2fd-126"><dt>D3dxof.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d2fd-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d2fd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d2fd-128">Функции файла X</span><span class="sxs-lookup"><span data-stu-id="2d2fd-128">X File Functions</span></span>](dx9-graphics-reference-x-file-functions.md)
</dt> <dt>

[<span data-ttu-id="2d2fd-129">**креатинумобжект**</span><span class="sxs-lookup"><span data-stu-id="2d2fd-129">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="2d2fd-130">**креатесавеобжект**</span><span class="sxs-lookup"><span data-stu-id="2d2fd-130">**CreateSaveObject**</span></span>](idirectxfile--createsaveobject.md)
</dt> <dt>

[<span data-ttu-id="2d2fd-131">**регистертемплатес**</span><span class="sxs-lookup"><span data-stu-id="2d2fd-131">**RegisterTemplates**</span></span>](idirectxfile--registertemplates.md)
</dt> </dl>

 

 




