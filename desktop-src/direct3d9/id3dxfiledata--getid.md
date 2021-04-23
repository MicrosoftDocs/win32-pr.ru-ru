---
description: Извлекает идентификатор GUID для этого файлового объекта данных.
ms.assetid: 79bf56b5-5900-4427-8092-3a1df86f8a57
title: 'Метод ID3DXFileData:: GetId (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e1dafb296541b1702e9163dcc6d460cf149b4007
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821220"
---
# <a name="id3dxfiledatagetid-method"></a><span data-ttu-id="59a76-103">Метод ID3DXFileData:: GetId</span><span class="sxs-lookup"><span data-stu-id="59a76-103">ID3DXFileData::GetId method</span></span>

<span data-ttu-id="59a76-104">Извлекает идентификатор GUID для этого файлового объекта данных.</span><span class="sxs-lookup"><span data-stu-id="59a76-104">Retrieves the GUID of this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="59a76-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59a76-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a><span data-ttu-id="59a76-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="59a76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59a76-107">*идентификатор процесса* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="59a76-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59a76-108">Тип: **лпгуид**</span><span class="sxs-lookup"><span data-stu-id="59a76-108">Type: **LPGUID**</span></span>

<span data-ttu-id="59a76-109">Указатель на идентификатор GUID для получения идентификатора этого объекта файловых данных.</span><span class="sxs-lookup"><span data-stu-id="59a76-109">Pointer to a GUID to receive the ID of this file data object.</span></span> <span data-ttu-id="59a76-110">Если объект данных файла не имеет идентификатора, возвращаемое значение параметра будет \_ равно GUID null.</span><span class="sxs-lookup"><span data-stu-id="59a76-110">If the file data object has no ID, the returned parameter value will be GUID\_NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59a76-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59a76-111">Return value</span></span>

<span data-ttu-id="59a76-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="59a76-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="59a76-113">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="59a76-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="59a76-114">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DXFERR \_ бадвалуе.</span><span class="sxs-lookup"><span data-stu-id="59a76-114">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="59a76-115">Требования</span><span class="sxs-lookup"><span data-stu-id="59a76-115">Requirements</span></span>



| <span data-ttu-id="59a76-116">Требование</span><span class="sxs-lookup"><span data-stu-id="59a76-116">Requirement</span></span> | <span data-ttu-id="59a76-117">Значение</span><span class="sxs-lookup"><span data-stu-id="59a76-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59a76-118">Header</span><span class="sxs-lookup"><span data-stu-id="59a76-118">Header</span></span><br/>  | <dl> <span data-ttu-id="59a76-119"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="59a76-119"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="59a76-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="59a76-120">Library</span></span><br/> | <dl> <span data-ttu-id="59a76-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59a76-121"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="59a76-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59a76-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59a76-123">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="59a76-123">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 




