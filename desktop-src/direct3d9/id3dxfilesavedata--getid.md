---
description: Извлекает идентификатор GUID для этого узла данных файла ID3DXFileSaveData.
ms.assetid: 79413eb4-4889-4148-b1a1-58a0b780403c
title: 'Метод ID3DXFileSaveData:: GetId (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b03322e03d1bedc10f9deec82c60418b5ad846b8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694226"
---
# <a name="id3dxfilesavedatagetid-method"></a><span data-ttu-id="a2ef5-103">Метод ID3DXFileSaveData:: GetId</span><span class="sxs-lookup"><span data-stu-id="a2ef5-103">ID3DXFileSaveData::GetId method</span></span>

<span data-ttu-id="a2ef5-104">Извлекает идентификатор GUID для этого узла данных файла [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="a2ef5-104">Retrieves the GUID of this [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2ef5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2ef5-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a><span data-ttu-id="a2ef5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2ef5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2ef5-107">*идентификатор процесса* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a2ef5-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ef5-108">Тип: **лпгуид**</span><span class="sxs-lookup"><span data-stu-id="a2ef5-108">Type: **LPGUID**</span></span>

<span data-ttu-id="a2ef5-109">Указатель на GUID, получающий идентификатор этого узла файловых данных.</span><span class="sxs-lookup"><span data-stu-id="a2ef5-109">Pointer to a GUID to receive the ID of this file data node.</span></span> <span data-ttu-id="a2ef5-110">Если у объекта нет идентификатора, возвращаемое значение параметра будет \_ равно GUID null.</span><span class="sxs-lookup"><span data-stu-id="a2ef5-110">If the object has no ID, the returned parameter value will be GUID\_NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2ef5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2ef5-111">Return value</span></span>

<span data-ttu-id="a2ef5-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a2ef5-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a2ef5-113">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="a2ef5-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a2ef5-114">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DXFERR \_ бадвалуе.</span><span class="sxs-lookup"><span data-stu-id="a2ef5-114">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2ef5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a2ef5-115">Requirements</span></span>



| <span data-ttu-id="a2ef5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a2ef5-116">Requirement</span></span> | <span data-ttu-id="a2ef5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a2ef5-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2ef5-118">Header</span><span class="sxs-lookup"><span data-stu-id="a2ef5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a2ef5-119"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2ef5-119"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="a2ef5-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a2ef5-120">Library</span></span><br/> | <dl> <span data-ttu-id="a2ef5-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2ef5-121"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a2ef5-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2ef5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2ef5-123">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="a2ef5-123">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 




