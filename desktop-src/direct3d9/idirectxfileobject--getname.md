---
description: Получает указатель на имя объекта файла DirectX. Не рекомендуется.
ms.assetid: feb3faa2-22b9-47ed-8a38-33092821d484
title: Метод Идиректксфилеобжект::-Name (Дксфиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 134a1ce61ed1dc0d98a4daf3ba80dd4b0976c372
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105684991"
---
# <a name="idirectxfileobjectgetname-method"></a><span data-ttu-id="735fb-104">Метод Идиректксфилеобжект:: Name</span><span class="sxs-lookup"><span data-stu-id="735fb-104">IDirectXFileObject::GetName method</span></span>

<span data-ttu-id="735fb-105">Получает указатель на имя объекта файла DirectX.</span><span class="sxs-lookup"><span data-stu-id="735fb-105">Retrieves a pointer to a DirectX file object's name.</span></span> <span data-ttu-id="735fb-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="735fb-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="735fb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="735fb-107">Syntax</span></span>


```C++
HRESULT GetName(
  [out]     LPSTR   pstrNameBuf,
  [in, out] LPDWORD pdwBufLen
);
```



## <a name="parameters"></a><span data-ttu-id="735fb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="735fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="735fb-109">*пстрнамебуф* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="735fb-109">*pstrNameBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="735fb-110">Тип: **[ **LPSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="735fb-110">Type: **[**LPSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="735fb-111">Указатель на буфер, в который будет скопировано имя объекта файла DirectX.</span><span class="sxs-lookup"><span data-stu-id="735fb-111">Pointer to the buffer in which the DirectX file object's name will be copied.</span></span> <span data-ttu-id="735fb-112">Задайте **значение NULL** , если требуется только длина буфера.</span><span class="sxs-lookup"><span data-stu-id="735fb-112">Set to **NULL** if only the buffer length is needed.</span></span>

</dd> <dt>

<span data-ttu-id="735fb-113">*пдвбуфлен* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="735fb-113">*pdwBufLen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="735fb-114">Тип: **[ **лпдворд**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="735fb-114">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="735fb-115">Указатель на DWORD, указывающий длину буфера, на который указывает Пстрнамебуф.</span><span class="sxs-lookup"><span data-stu-id="735fb-115">Pointer to a DWORD specifying the length of the buffer pointed to by pstrNameBuf.</span></span> <span data-ttu-id="735fb-116">Значение параметра Пдвбуфлен будет изменено на длину буфера, необходимую для хранения имени объекта, даже если Пстрнамебуф имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="735fb-116">The pdwBufLen parameter value will be modified to the buffer length needed to hold the object's name even if pstrNameBuf is **NULL**.</span></span> <span data-ttu-id="735fb-117">В любом случае функция возвратит ДКСФИЛИРР \_ бадвалуе, если исходное значение пдвбуфлен не превышает длину, необходимую для хранения имени объекта.</span><span class="sxs-lookup"><span data-stu-id="735fb-117">In either case, the function will return DXFILEERR\_BADVALUE if the original value of pdwBufLen is not as large as or larger than the length needed to hold the object's name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="735fb-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="735fb-118">Return value</span></span>

<span data-ttu-id="735fb-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="735fb-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="735fb-120">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="735fb-120">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="735fb-121">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих значений. ДКСФИЛИРР \_ БАДАЛЛОК дксфилирр \_ бадвалуе</span><span class="sxs-lookup"><span data-stu-id="735fb-121">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="735fb-122">Требования</span><span class="sxs-lookup"><span data-stu-id="735fb-122">Requirements</span></span>



| <span data-ttu-id="735fb-123">Требование</span><span class="sxs-lookup"><span data-stu-id="735fb-123">Requirement</span></span> | <span data-ttu-id="735fb-124">Значение</span><span class="sxs-lookup"><span data-stu-id="735fb-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="735fb-125">Header</span><span class="sxs-lookup"><span data-stu-id="735fb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="735fb-126"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="735fb-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="735fb-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="735fb-127">Library</span></span><br/> | <dl> <span data-ttu-id="735fb-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="735fb-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="735fb-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="735fb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="735fb-130">идиректксфилеобжект</span><span class="sxs-lookup"><span data-stu-id="735fb-130">IDirectXFileObject</span></span>](idirectxfileobject.md)
</dt> </dl>

 

 
