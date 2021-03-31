---
description: Создает экземпляр объекта ID3DXFile.
ms.assetid: c086cb66-b1dc-4180-b966-e9a3b1f36f22
title: Функция D3DXFileCreate (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFileCreate
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 36fd57d15257323e86c0068709c3c73662eb0658
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157187"
---
# <a name="d3dxfilecreate-function"></a><span data-ttu-id="c6d2a-103">Функция D3DXFileCreate</span><span class="sxs-lookup"><span data-stu-id="c6d2a-103">D3DXFileCreate function</span></span>

<span data-ttu-id="c6d2a-104">Создает экземпляр объекта [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="c6d2a-104">Creates an instance of an [**ID3DXFile**](id3dxfile.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6d2a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6d2a-105">Syntax</span></span>


```C++
HRESULT STDAPICALLTYPE D3DXFileCreate(
   ID3DXFile **lplpDirectXFile
);
```



## <a name="parameters"></a><span data-ttu-id="c6d2a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6d2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6d2a-107">*лплпдиректксфиле*</span><span class="sxs-lookup"><span data-stu-id="c6d2a-107">*lplpDirectXFile*</span></span> 
</dt> <dd>

<span data-ttu-id="c6d2a-108">Тип: **[ **ID3DXFile**](id3dxfile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c6d2a-108">Type: **[**ID3DXFile**](id3dxfile.md)\*\***</span></span>

<span data-ttu-id="c6d2a-109">Адрес указателя на интерфейс [**ID3DXFile**](id3dxfile.md) , представляющий созданный объект файла. x.</span><span class="sxs-lookup"><span data-stu-id="c6d2a-109">Address of a pointer to an [**ID3DXFile**](id3dxfile.md) interface, representing the created .x file object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6d2a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c6d2a-110">Return value</span></span>

<span data-ttu-id="c6d2a-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c6d2a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c6d2a-112">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c6d2a-112">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c6d2a-113">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: \_ указатель e, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c6d2a-113">If the function fails, the return value can be one of the following: E\_POINTER, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6d2a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6d2a-114">Remarks</span></span>

<span data-ttu-id="c6d2a-115">После использования этой функции используйте [**регистертемплатес**](id3dxfile--registertemplates.md) или [**регистеренумтемплатес**](id3dxfile--registerenumtemplates.md) для регистрации шаблонов, [**креатинумобжект**](id3dxfile--createenumobject.md) для создания объекта перечислителя или [**креатесавеобжект**](id3dxfile--createsaveobject.md) для создания объекта Save.</span><span class="sxs-lookup"><span data-stu-id="c6d2a-115">After using this function, use [**RegisterTemplates**](id3dxfile--registertemplates.md) or [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) to register templates, [**CreateEnumObject**](id3dxfile--createenumobject.md) to create an enumerator object, or [**CreateSaveObject**](id3dxfile--createsaveobject.md) to create a save object.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6d2a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c6d2a-116">Requirements</span></span>



| <span data-ttu-id="c6d2a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c6d2a-117">Requirement</span></span> | <span data-ttu-id="c6d2a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c6d2a-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d2a-119">Header</span><span class="sxs-lookup"><span data-stu-id="c6d2a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c6d2a-120"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6d2a-120"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="c6d2a-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c6d2a-121">Library</span></span><br/> | <dl> <span data-ttu-id="c6d2a-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6d2a-122"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c6d2a-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6d2a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6d2a-124">Функции файла D3DX X</span><span class="sxs-lookup"><span data-stu-id="c6d2a-124">D3DX X File Functions</span></span>](dx9-graphics-reference-d3dx-x-file-functions.md)
</dt> <dt>

[<span data-ttu-id="c6d2a-125">**креатинумобжект**</span><span class="sxs-lookup"><span data-stu-id="c6d2a-125">**CreateEnumObject**</span></span>](id3dxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="c6d2a-126">**креатесавеобжект**</span><span class="sxs-lookup"><span data-stu-id="c6d2a-126">**CreateSaveObject**</span></span>](id3dxfile--createsaveobject.md)
</dt> <dt>

[<span data-ttu-id="c6d2a-127">**регистеренумтемплатес**</span><span class="sxs-lookup"><span data-stu-id="c6d2a-127">**RegisterEnumTemplates**</span></span>](id3dxfile--registerenumtemplates.md)
</dt> <dt>

[<span data-ttu-id="c6d2a-128">**регистертемплатес**</span><span class="sxs-lookup"><span data-stu-id="c6d2a-128">**RegisterTemplates**</span></span>](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




