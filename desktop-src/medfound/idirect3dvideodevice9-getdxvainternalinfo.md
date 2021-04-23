---
description: Запрашивает объем вспомогательной памяти, выделяемой слоем абстрагирования оборудования (HAL) для частного использования.
ms.assetid: 20e3dbef-daf5-487a-8d50-e2ebdb712cc0
title: 'Метод IDirect3DVideoDevice9:: Жетдксваинтерналинфо (Дксва. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAInternalInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: aa512130b622d192acc37d8c309f462f8ecc87e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711345"
---
# <a name="idirect3dvideodevice9getdxvainternalinfo-method"></a><span data-ttu-id="d88a9-103">Метод IDirect3DVideoDevice9:: Жетдксваинтерналинфо</span><span class="sxs-lookup"><span data-stu-id="d88a9-103">IDirect3DVideoDevice9::GetDXVAInternalInfo method</span></span>

<span data-ttu-id="d88a9-104">Запрашивает объем вспомогательной памяти, выделяемой слоем абстрагирования оборудования (HAL) для частного использования.</span><span class="sxs-lookup"><span data-stu-id="d88a9-104">Queries for the amount of scratch memory that the hardware abstraction layer (HAL) will allocate for its private use.</span></span>

## <a name="syntax"></a><span data-ttu-id="d88a9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d88a9-105">Syntax</span></span>


```C++
HRESULT GetDXVAInternalInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pMemoryUsed
);
```



## <a name="parameters"></a><span data-ttu-id="d88a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d88a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d88a9-107">*пгуид*</span><span class="sxs-lookup"><span data-stu-id="d88a9-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="d88a9-108">Указатель на идентификатор GUID, указывающий профиль ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="d88a9-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="d88a9-109">Чтобы получить список поддерживаемых профилей, вызовите [**IDirect3DVideoDevice9:: жетдксвагуидс**](idirect3dvideodevice9-getdxvaguids.md).</span><span class="sxs-lookup"><span data-stu-id="d88a9-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="d88a9-110">*пункомпдата*</span><span class="sxs-lookup"><span data-stu-id="d88a9-110">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="d88a9-111">Указатель на структуру [**дксваункомпдатаинфо**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) , указывающую размер и формат пикселей для несжатых данных.</span><span class="sxs-lookup"><span data-stu-id="d88a9-111">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the size and pixel format of the uncompressed data.</span></span>

</dd> <dt>

<span data-ttu-id="d88a9-112">*пмеморюсед*</span><span class="sxs-lookup"><span data-stu-id="d88a9-112">*pMemoryUsed*</span></span> 
</dt> <dd>

<span data-ttu-id="d88a9-113">Получает объем вспомогательной памяти, выделяемой HAL, в байтах.</span><span class="sxs-lookup"><span data-stu-id="d88a9-113">Receives the amount of scratch memory that the HAL will allocate, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d88a9-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d88a9-114">Return value</span></span>

<span data-ttu-id="d88a9-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d88a9-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d88a9-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d88a9-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d88a9-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d88a9-117">Requirements</span></span>



| <span data-ttu-id="d88a9-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d88a9-118">Requirement</span></span> | <span data-ttu-id="d88a9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d88a9-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d88a9-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d88a9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d88a9-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d88a9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d88a9-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d88a9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d88a9-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d88a9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d88a9-124">Header</span><span class="sxs-lookup"><span data-stu-id="d88a9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d88a9-125"><dt>Дксва. h</dt></span><span class="sxs-lookup"><span data-stu-id="d88a9-125"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d88a9-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d88a9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d88a9-127">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="d88a9-127">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




