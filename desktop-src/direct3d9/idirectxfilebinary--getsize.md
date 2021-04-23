---
description: Возвращает размер двоичных данных. Не рекомендуется.
ms.assetid: 99a74043-ce87-4545-961f-dade54e77735
title: 'Метод Идиректксфилебинари:: resize (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetSize
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 664e2bf026df6d9e4b5bc07067ce1ce7fe7669db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548031"
---
# <a name="idirectxfilebinarygetsize-method"></a><span data-ttu-id="c0110-104">Метод Идиректксфилебинари:: resize</span><span class="sxs-lookup"><span data-stu-id="c0110-104">IDirectXFileBinary::GetSize method</span></span>

<span data-ttu-id="c0110-105">Возвращает размер двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="c0110-105">Retrieves the size of the binary data.</span></span> <span data-ttu-id="c0110-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="c0110-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0110-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0110-107">Syntax</span></span>


```C++
HRESULT GetSize(
  [out] DWORD *pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="c0110-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0110-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0110-109">*пкбсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c0110-109">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0110-110">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c0110-110">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c0110-111">Указатель на возвращаемый размер двоичных данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="c0110-111">Pointer to the returned size of the binary data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0110-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0110-112">Return value</span></span>

<span data-ttu-id="c0110-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c0110-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c0110-114">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c0110-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="c0110-115">В случае сбоя метода возвращаемое значение может быть ДКСФИЛИРР \_ бадвалуе.</span><span class="sxs-lookup"><span data-stu-id="c0110-115">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0110-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c0110-116">Requirements</span></span>



| <span data-ttu-id="c0110-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c0110-117">Requirement</span></span> | <span data-ttu-id="c0110-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c0110-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0110-119">Header</span><span class="sxs-lookup"><span data-stu-id="c0110-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c0110-120"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0110-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0110-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c0110-121">Library</span></span><br/> | <dl> <span data-ttu-id="c0110-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0110-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0110-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0110-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0110-124">идиректксфилебинари</span><span class="sxs-lookup"><span data-stu-id="c0110-124">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
