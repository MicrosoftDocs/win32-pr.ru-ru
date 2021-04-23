---
description: Извлекает объект ID3DXFile.
ms.assetid: 832878c6-73a4-400a-af30-57112b172977
title: Метод ID3DXFileEnumObject::-File (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d3b5d672ca9b462e08c75a6f3352b01b07ead43c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000418"
---
# <a name="id3dxfileenumobjectgetfile-method"></a><span data-ttu-id="ce604-103">Метод ID3DXFileEnumObject:: onfile</span><span class="sxs-lookup"><span data-stu-id="ce604-103">ID3DXFileEnumObject::GetFile method</span></span>

<span data-ttu-id="ce604-104">Извлекает объект [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="ce604-104">Retrieves the [**ID3DXFile**](id3dxfile.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce604-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce604-105">Syntax</span></span>


```C++
HRESULT GetFile(
  [out] ID3DXFile **ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="ce604-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce604-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce604-107">*ппфиле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ce604-107">*ppFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce604-108">Тип: **[ **ID3DXFile**](id3dxfile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="ce604-108">Type: **[**ID3DXFile**](id3dxfile.md)\*\***</span></span>

<span data-ttu-id="ce604-109">Адрес указателя на интерфейс [**ID3DXFile**](id3dxfile.md) , представляющий возвращаемый объект.</span><span class="sxs-lookup"><span data-stu-id="ce604-109">Address of a pointer to an [**ID3DXFile**](id3dxfile.md) interface, representing the returned object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce604-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce604-110">Return value</span></span>

<span data-ttu-id="ce604-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ce604-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ce604-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="ce604-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ce604-113">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DXFERR \_ бадвалуе.</span><span class="sxs-lookup"><span data-stu-id="ce604-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce604-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ce604-114">Requirements</span></span>



| <span data-ttu-id="ce604-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ce604-115">Requirement</span></span> | <span data-ttu-id="ce604-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ce604-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce604-117">Header</span><span class="sxs-lookup"><span data-stu-id="ce604-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ce604-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce604-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="ce604-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ce604-119">Library</span></span><br/> | <dl> <span data-ttu-id="ce604-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce604-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ce604-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce604-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce604-122">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="ce604-122">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 




