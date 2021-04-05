---
description: Извлекает тип MIME для двоичных данных. Не рекомендуется.
ms.assetid: 57c42ace-4313-40d8-9992-eaf12edf3a30
title: 'Метод Идиректксфилебинари:: Жетмиметипе (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetMimeType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 965006dc6fbad1176307341a19fd1f186e670104
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000348"
---
# <a name="idirectxfilebinarygetmimetype-method"></a><span data-ttu-id="b5cd3-104">Метод Идиректксфилебинари:: Жетмиметипе</span><span class="sxs-lookup"><span data-stu-id="b5cd3-104">IDirectXFileBinary::GetMimeType method</span></span>

<span data-ttu-id="b5cd3-105">Извлекает тип MIME для двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="b5cd3-105">Retrieves the Multipurpose Internet Mail Extensions (MIME) type for the binary data.</span></span> <span data-ttu-id="b5cd3-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="b5cd3-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5cd3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5cd3-107">Syntax</span></span>


```C++
HRESULT GetMimeType(
  [out] LPCSTR *pszMimeType
);
```



## <a name="parameters"></a><span data-ttu-id="b5cd3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5cd3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5cd3-109">*псзмиметипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b5cd3-109">*pszMimeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5cd3-110">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5cd3-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b5cd3-111">Адрес указателя для получения строки типа MIME.</span><span class="sxs-lookup"><span data-stu-id="b5cd3-111">Address of a pointer to receive the MIME type string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5cd3-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5cd3-112">Return value</span></span>

<span data-ttu-id="b5cd3-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b5cd3-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b5cd3-114">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b5cd3-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="b5cd3-115">В случае сбоя метода возвращаемое значение может быть ДКСФИЛИРР \_ бадвалуе.</span><span class="sxs-lookup"><span data-stu-id="b5cd3-115">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5cd3-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5cd3-116">Remarks</span></span>

<span data-ttu-id="b5cd3-117">Если в файле DirectX для двоичного объекта не указан тип MIME, функция устанавливает Псзмиметипе в **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b5cd3-117">When there is no MIME type specified in a DirectX file for a binary object, the function will set pszMimeType to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5cd3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b5cd3-118">Requirements</span></span>



| <span data-ttu-id="b5cd3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b5cd3-119">Requirement</span></span> | <span data-ttu-id="b5cd3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b5cd3-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5cd3-121">Header</span><span class="sxs-lookup"><span data-stu-id="b5cd3-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b5cd3-122"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5cd3-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5cd3-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b5cd3-123">Library</span></span><br/> | <dl> <span data-ttu-id="b5cd3-124"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5cd3-124"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5cd3-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5cd3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5cd3-126">идиректксфилебинари</span><span class="sxs-lookup"><span data-stu-id="b5cd3-126">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
