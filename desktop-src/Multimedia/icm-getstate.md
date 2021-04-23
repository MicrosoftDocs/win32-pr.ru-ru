---
title: Сообщение ICM_GETSTATE (VFW. h)
description: Сообщение ICM \_ -State запрашивает драйвер сжатия видео, чтобы вернуть его текущую конфигурацию в блок памяти или определить объем памяти, необходимый для получения сведений о конфигурации.
ms.assetid: 4b77e294-f3aa-45f9-a4f4-f103b83eae8d
keywords:
- ICM_GETSTATE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_GETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b6a45dcde627a02c1a4a402ea9a2a725f0429a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137811"
---
# <a name="icm_getstate-message"></a><span data-ttu-id="303b6-104">\_Сообщение о состоянии ICM</span><span class="sxs-lookup"><span data-stu-id="303b6-104">ICM\_GETSTATE message</span></span>

<span data-ttu-id="303b6-105">Сообщение **ICM- \_ State** запрашивает драйвер сжатия видео, чтобы вернуть его текущую конфигурацию в блок памяти или определить объем памяти, необходимый для получения сведений о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="303b6-105">The **ICM\_GETSTATE** message queries a video compression driver to return its current configuration in a block of memory or to determine the amount of memory required to retrieve the configuration information.</span></span> <span data-ttu-id="303b6-106">Это сообщение можно отправить явно или с помощью макроса [**икжетстате**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) .</span><span class="sxs-lookup"><span data-stu-id="303b6-106">You can send this message explicitly or by using the [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) macro.</span></span>


```C++
ICM_GETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a><span data-ttu-id="303b6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="303b6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="303b6-108"><span id="pv"></span><span id="PV"></span>*PV*</span><span class="sxs-lookup"><span data-stu-id="303b6-108"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="303b6-109">Указатель на блок памяти, в котором должны содержаться текущие сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="303b6-109">Pointer to a block of memory to contain the current configuration information.</span></span> <span data-ttu-id="303b6-110">Можно указать **значение NULL** для этого параметра, чтобы определить объем памяти, необходимый для данных конфигурации, как в [**икжетстатесизе**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize).</span><span class="sxs-lookup"><span data-stu-id="303b6-110">You can specify **NULL** for this parameter to determine the amount of memory required for the configuration information, as in [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize).</span></span>

</dd> <dt>

<span data-ttu-id="303b6-111"><span id="cb"></span><span id="CB"></span>*CB*</span><span class="sxs-lookup"><span data-stu-id="303b6-111"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="303b6-112">Размер блока памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="303b6-112">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="303b6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="303b6-113">Return Value</span></span>

<span data-ttu-id="303b6-114">Если *ПС* имеет **значение NULL**, возвращает объем памяти в байтах, необходимый для сведений о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="303b6-114">If *pv* is **NULL**, returns the amount of memory, in bytes, required for configuration information.</span></span>

<span data-ttu-id="303b6-115">Если *ПС* не **равен null**, функция возвращает ицерр \_ ОК в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="303b6-115">If *pv* is not **NULL**, returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="303b6-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="303b6-116">Remarks</span></span>

<span data-ttu-id="303b6-117">Структура, используемая для представления сведений о конфигурации, зависит от драйвера и определяется драйвером.</span><span class="sxs-lookup"><span data-stu-id="303b6-117">The structure used to represent configuration information is driver specific and is defined by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="303b6-118">Требования</span><span class="sxs-lookup"><span data-stu-id="303b6-118">Requirements</span></span>



| <span data-ttu-id="303b6-119">Требование</span><span class="sxs-lookup"><span data-stu-id="303b6-119">Requirement</span></span> | <span data-ttu-id="303b6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="303b6-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="303b6-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="303b6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="303b6-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="303b6-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="303b6-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="303b6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="303b6-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="303b6-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="303b6-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="303b6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="303b6-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="303b6-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="303b6-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="303b6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="303b6-128">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="303b6-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="303b6-129">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="303b6-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





