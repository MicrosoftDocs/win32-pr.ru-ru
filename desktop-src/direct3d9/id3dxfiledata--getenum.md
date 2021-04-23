---
description: Извлекает объект перечисления в этом объекте данных файла.
ms.assetid: 383560e2-1888-4e37-9883-2ddbcb101cf6
title: Метод ID3DXFileData::-Enum (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetEnum
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7dd565f6f76d42159d77d8b83c638c75648f293b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713803"
---
# <a name="id3dxfiledatagetenum-method"></a><span data-ttu-id="2a65a-103">Метод ID3DXFileData:: Enum</span><span class="sxs-lookup"><span data-stu-id="2a65a-103">ID3DXFileData::GetEnum method</span></span>

<span data-ttu-id="2a65a-104">Извлекает объект перечисления в этом объекте данных файла.</span><span class="sxs-lookup"><span data-stu-id="2a65a-104">Retrieves the enumeration object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a65a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a65a-105">Syntax</span></span>


```C++
HRESULT GetEnum(
  [in] ID3DXFileEnumObject **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="2a65a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a65a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a65a-107">*ппобж* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2a65a-107">*ppObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a65a-108">Тип: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="2a65a-108">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span></span>

<span data-ttu-id="2a65a-109">Адрес указателя для получения объекта перечисления в этом объекте данных файла.</span><span class="sxs-lookup"><span data-stu-id="2a65a-109">Address of a pointer to receive the enumeration object in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a65a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a65a-110">Return value</span></span>

<span data-ttu-id="2a65a-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2a65a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2a65a-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="2a65a-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2a65a-113">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DXFERR \_ бадвалуе.</span><span class="sxs-lookup"><span data-stu-id="2a65a-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a65a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="2a65a-114">Requirements</span></span>



| <span data-ttu-id="2a65a-115">Требование</span><span class="sxs-lookup"><span data-stu-id="2a65a-115">Requirement</span></span> | <span data-ttu-id="2a65a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2a65a-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a65a-117">Header</span><span class="sxs-lookup"><span data-stu-id="2a65a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2a65a-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a65a-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="2a65a-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2a65a-119">Library</span></span><br/> | <dl> <span data-ttu-id="2a65a-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a65a-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2a65a-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a65a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a65a-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="2a65a-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 




