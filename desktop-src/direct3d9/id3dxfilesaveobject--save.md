---
description: Сохраняет объект данных и его дочерние элементы в файл. x на диске.
ms.assetid: a48cd1b2-d1e7-446b-8482-485ccdd59353
title: 'Метод ID3DXFileSaveObject:: Save (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.Save
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c97c2ccf6c509aec1d217e3179c927fe2bb5a797
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424393"
---
# <a name="id3dxfilesaveobjectsave-method"></a><span data-ttu-id="b7eda-103">Метод ID3DXFileSaveObject:: Save</span><span class="sxs-lookup"><span data-stu-id="b7eda-103">ID3DXFileSaveObject::Save method</span></span>

<span data-ttu-id="b7eda-104">Сохраняет объект данных и его дочерние элементы в файл. x на диске.</span><span class="sxs-lookup"><span data-stu-id="b7eda-104">Saves a data object and its children to a .x file on disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7eda-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7eda-105">Syntax</span></span>


```C++
HRESULT Save();
```



## <a name="parameters"></a><span data-ttu-id="b7eda-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7eda-106">Parameters</span></span>

<span data-ttu-id="b7eda-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b7eda-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7eda-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b7eda-108">Return value</span></span>

<span data-ttu-id="b7eda-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b7eda-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b7eda-110">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="b7eda-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b7eda-111">В случае сбоя метода возвращаемое значение может быть следующим: D3DXFERR \_ бадобжект.</span><span class="sxs-lookup"><span data-stu-id="b7eda-111">If the method fails, the return value can be the following: D3DXFERR\_BADOBJECT.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7eda-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7eda-112">Remarks</span></span>

<span data-ttu-id="b7eda-113">После выполнения этого метода [**ID3DXFileSaveObject:: адддатаобжект**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData:: адддатаобжект**](id3dxfilesavedata--adddataobject.md) и [**ID3DXFileSaveData:: адддатареференце**](id3dxfilesavedata--adddatareference.md) нельзя вызвать, пока не будет создан новый объект [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="b7eda-113">After this method succeeds, [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) and [**ID3DXFileSaveData::AddDataReference**](id3dxfilesavedata--adddatareference.md) can no longer be called until a new [**ID3DXFile**](id3dxfile.md) object is created.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7eda-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b7eda-114">Requirements</span></span>



| <span data-ttu-id="b7eda-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b7eda-115">Requirement</span></span> | <span data-ttu-id="b7eda-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b7eda-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7eda-117">Header</span><span class="sxs-lookup"><span data-stu-id="b7eda-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b7eda-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7eda-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="b7eda-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b7eda-119">Library</span></span><br/> | <dl> <span data-ttu-id="b7eda-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7eda-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b7eda-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7eda-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7eda-122">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="b7eda-122">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 




