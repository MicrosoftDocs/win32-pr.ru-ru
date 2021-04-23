---
description: Возвращает интерфейс ID3DXFile объекта, который создал этот объект ID3DXFileSaveObject.
ms.assetid: 79249d17-cae3-43d9-9ccb-fa804b02a353
title: Метод ID3DXFileSaveObject::-File (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 137f8245b94bb0ebd14e81d5f73a7ba9622a4933
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424442"
---
# <a name="id3dxfilesaveobjectgetfile-method"></a><span data-ttu-id="b89f7-103">Метод ID3DXFileSaveObject:: onfile</span><span class="sxs-lookup"><span data-stu-id="b89f7-103">ID3DXFileSaveObject::GetFile method</span></span>

<span data-ttu-id="b89f7-104">Возвращает интерфейс [**ID3DXFile**](id3dxfile.md) объекта, который создал этот объект [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="b89f7-104">Gets the [**ID3DXFile**](id3dxfile.md) interface of the object that created this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b89f7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b89f7-105">Syntax</span></span>


```C++
HRESULT GetFile(
  [in] ID3DXFile ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="b89f7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b89f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b89f7-107">*ппфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b89f7-107">*ppFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b89f7-108">Тип: **[ **ID3DXFile**](id3dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="b89f7-108">Type: **[**ID3DXFile**](id3dxfile.md)**</span></span>

<span data-ttu-id="b89f7-109">Адрес указателя на объект [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="b89f7-109">Address of a pointer to an [**ID3DXFile**](id3dxfile.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b89f7-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b89f7-110">Return value</span></span>

<span data-ttu-id="b89f7-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b89f7-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b89f7-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="b89f7-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b89f7-113">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DXFERR \_ бадвалуе, e \_ Interface, e \_ указатель.</span><span class="sxs-lookup"><span data-stu-id="b89f7-113">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, E\_NOINTERFACE, E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="b89f7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b89f7-114">Requirements</span></span>



| <span data-ttu-id="b89f7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b89f7-115">Requirement</span></span> | <span data-ttu-id="b89f7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b89f7-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b89f7-117">Header</span><span class="sxs-lookup"><span data-stu-id="b89f7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b89f7-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="b89f7-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="b89f7-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b89f7-119">Library</span></span><br/> | <dl> <span data-ttu-id="b89f7-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b89f7-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b89f7-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b89f7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b89f7-122">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="b89f7-122">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 




