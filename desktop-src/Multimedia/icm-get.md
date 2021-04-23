---
title: Сообщение ICM_GET (VFW. h)
description: ICM \_ -сообщение get получает значение DWORD, определенное приложением, из драйвера сжатия видео.
ms.assetid: 288c0053-16a1-4547-b748-da218a0b588c
keywords:
- ICM_GET сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_GET
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e23cd994546be41b5f938331b2dc632897635c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801522"
---
# <a name="icm_get-message"></a><span data-ttu-id="3b8fb-104">ICM \_ Get, сообщение</span><span class="sxs-lookup"><span data-stu-id="3b8fb-104">ICM\_GET message</span></span>

<span data-ttu-id="3b8fb-105">ICM-сообщение **\_ Get** получает значение **DWORD** , определенное приложением, из драйвера сжатия видео.</span><span class="sxs-lookup"><span data-stu-id="3b8fb-105">The **ICM\_GET** message retrieves an application-defined **DWORD** value from a video compression driver.</span></span>


```C++
ICM_GET 
wParam = (DWORD) (LPVOID) pv; 
lParam = (DWORD) cb; 
```



## <a name="parameters"></a><span data-ttu-id="3b8fb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b8fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b8fb-107"><span id="pv"></span><span id="PV"></span>*PV*</span><span class="sxs-lookup"><span data-stu-id="3b8fb-107"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="3b8fb-108">Указатель на блок памяти, который должен быть заполнен текущим состоянием.</span><span class="sxs-lookup"><span data-stu-id="3b8fb-108">Pointer to a block of memory to be filled with the current state.</span></span> <span data-ttu-id="3b8fb-109">Можно также указать **значение NULL** , чтобы определить объем памяти, необходимый для сведений о состоянии.</span><span class="sxs-lookup"><span data-stu-id="3b8fb-109">You can also specify **NULL** to determine the amount of memory required by the state information.</span></span>

</dd> <dt>

<span data-ttu-id="3b8fb-110"><span id="cb"></span><span id="CB"></span>*CB*</span><span class="sxs-lookup"><span data-stu-id="3b8fb-110"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="3b8fb-111">Размер блока памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="3b8fb-111">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b8fb-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b8fb-112">Return Value</span></span>

<span data-ttu-id="3b8fb-113">Возвращает объем памяти в байтах, необходимый для хранения сведений о состоянии.</span><span class="sxs-lookup"><span data-stu-id="3b8fb-113">Returns the amount of memory, in bytes, required to store the status information.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b8fb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b8fb-114">Remarks</span></span>

<span data-ttu-id="3b8fb-115">Структура, используемая для представления сведений о состоянии, зависит от драйвера и определяется драйвером.</span><span class="sxs-lookup"><span data-stu-id="3b8fb-115">The structure used to represent state information is driver specific and is defined by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b8fb-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3b8fb-116">Requirements</span></span>



| <span data-ttu-id="3b8fb-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3b8fb-117">Requirement</span></span> | <span data-ttu-id="3b8fb-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3b8fb-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3b8fb-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3b8fb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3b8fb-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3b8fb-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3b8fb-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3b8fb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3b8fb-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3b8fb-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3b8fb-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3b8fb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b8fb-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b8fb-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b8fb-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b8fb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b8fb-126">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="3b8fb-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="3b8fb-127">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="3b8fb-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





