---
description: Получает указатель на этот узел данных файла ID3DXFileSaveObject.
ms.assetid: 092d1c6f-0a53-4b8e-84ec-bc76f3f647ac
title: 'Метод ID3DXFileSaveData:: Save (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetSave
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4e23296ad0a866a0ad289a9a587c433411ef9bb8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273955"
---
# <a name="id3dxfilesavedatagetsave-method"></a><span data-ttu-id="bc94b-103">Метод ID3DXFileSaveData:: Save</span><span class="sxs-lookup"><span data-stu-id="bc94b-103">ID3DXFileSaveData::GetSave method</span></span>

<span data-ttu-id="bc94b-104">Получает указатель на этот узел данных файла [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="bc94b-104">Retrieves a pointer to this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc94b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc94b-105">Syntax</span></span>


```C++
HRESULT GetSave(
  [out] ID3DXFileSaveObject **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="bc94b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc94b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc94b-107">*ппобж* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bc94b-107">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc94b-108">Тип: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="bc94b-108">Type: **[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span></span>

<span data-ttu-id="bc94b-109">Адрес указателя на интерфейс [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) , представляющий этот узел данных файла.</span><span class="sxs-lookup"><span data-stu-id="bc94b-109">Address of a pointer to an [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface representing this file data node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc94b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc94b-110">Return value</span></span>

<span data-ttu-id="bc94b-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bc94b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bc94b-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="bc94b-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bc94b-113">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DXFERR \_ бадвалуе.</span><span class="sxs-lookup"><span data-stu-id="bc94b-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc94b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="bc94b-114">Requirements</span></span>



| <span data-ttu-id="bc94b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="bc94b-115">Requirement</span></span> | <span data-ttu-id="bc94b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="bc94b-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc94b-117">Header</span><span class="sxs-lookup"><span data-stu-id="bc94b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="bc94b-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc94b-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="bc94b-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bc94b-119">Library</span></span><br/> | <dl> <span data-ttu-id="bc94b-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc94b-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="bc94b-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc94b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc94b-122">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="bc94b-122">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 




