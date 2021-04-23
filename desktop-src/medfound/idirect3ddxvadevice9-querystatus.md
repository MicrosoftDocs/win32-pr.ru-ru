---
description: Запрашивает состояние чтения/записи для области декодирования видео DirectX Acceleration (ДКСВА).
ms.assetid: 8a4c3173-5911-49ec-8cb8-e30f96a4f1c9
title: 'Метод IDirect3DDXVADevice9:: QueryStatus (Дксва. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.QueryStatus
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: ae2b16ef27b1e172b7927652304104563e120709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711347"
---
# <a name="idirect3ddxvadevice9querystatus-method"></a><span data-ttu-id="42dc9-103">Метод IDirect3DDXVADevice9:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="42dc9-103">IDirect3DDXVADevice9::QueryStatus method</span></span>

<span data-ttu-id="42dc9-104">Запрашивает состояние чтения/записи для области декодирования видео DirectX Acceleration (ДКСВА).</span><span class="sxs-lookup"><span data-stu-id="42dc9-104">Queries the read/write status of a DirectX Video Acceleration (DXVA) decoding surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="42dc9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42dc9-105">Syntax</span></span>


```C++
HRESULT QueryStatus(
   IDirect3DSurface9 *pSurface,
   DWORD             Flags
);
```



## <a name="parameters"></a><span data-ttu-id="42dc9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42dc9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42dc9-107">*псурфаце*</span><span class="sxs-lookup"><span data-stu-id="42dc9-107">*pSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="42dc9-108">Указатель на интерфейс **IDirect3DSurface9** области для запроса.</span><span class="sxs-lookup"><span data-stu-id="42dc9-108">Pointer to the **IDirect3DSurface9** interface of the surface to query.</span></span>

</dd> <dt>

<span data-ttu-id="42dc9-109">*Флаги*</span><span class="sxs-lookup"><span data-stu-id="42dc9-109">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="42dc9-110">Указывает тип выполняемого запроса.</span><span class="sxs-lookup"><span data-stu-id="42dc9-110">Specifies the type of query to perform.</span></span>



| <span data-ttu-id="42dc9-111">Значение</span><span class="sxs-lookup"><span data-stu-id="42dc9-111">Value</span></span>                                                                                                                             | <span data-ttu-id="42dc9-112">Значение</span><span class="sxs-lookup"><span data-stu-id="42dc9-112">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="0x00"></span><span id="0X00"></span><dl> <span data-ttu-id="42dc9-113"><dt>**0x00**</dt></span><span class="sxs-lookup"><span data-stu-id="42dc9-113"><dt>**0x00**</dt></span></span> </dl> | <span data-ttu-id="42dc9-114">Проверьте, является ли поверхность надежной для записи.</span><span class="sxs-lookup"><span data-stu-id="42dc9-114">Test whether the surface is safe to use for writing.</span></span><br/> |
| <span id="0x01"></span><span id="0X01"></span><dl> <span data-ttu-id="42dc9-115"><dt>**0x01**</dt></span><span class="sxs-lookup"><span data-stu-id="42dc9-115"><dt>**0x01**</dt></span></span> </dl> | <span data-ttu-id="42dc9-116">Проверьте, является ли поверхность надежно используемой для чтения.</span><span class="sxs-lookup"><span data-stu-id="42dc9-116">Test whether the surface is safe to use for reading.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42dc9-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42dc9-117">Return value</span></span>

<span data-ttu-id="42dc9-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="42dc9-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="42dc9-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="42dc9-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="42dc9-120">Требования</span><span class="sxs-lookup"><span data-stu-id="42dc9-120">Requirements</span></span>



| <span data-ttu-id="42dc9-121">Требование</span><span class="sxs-lookup"><span data-stu-id="42dc9-121">Requirement</span></span> | <span data-ttu-id="42dc9-122">Значение</span><span class="sxs-lookup"><span data-stu-id="42dc9-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="42dc9-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42dc9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="42dc9-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="42dc9-124">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="42dc9-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42dc9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="42dc9-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="42dc9-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="42dc9-127">Header</span><span class="sxs-lookup"><span data-stu-id="42dc9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="42dc9-128"><dt>Дксва. h</dt></span><span class="sxs-lookup"><span data-stu-id="42dc9-128"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42dc9-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42dc9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42dc9-130">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="42dc9-130">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




