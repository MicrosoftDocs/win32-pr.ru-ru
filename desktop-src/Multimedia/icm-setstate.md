---
title: Сообщение ICM_SETSTATE (VFW. h)
description: Сообщение ICM \_ SETSTATE уведомляет драйверу о сжатии видео о необходимости установки состояния сжатия. Это сообщение можно отправить явно или с помощью макроса Иксетстате.
ms.assetid: d1a91847-2893-4c8b-9ca1-02db71ec2c81
keywords:
- ICM_SETSTATE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_SETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230e0aaf3752016efd276d7d55624ee2abb4f8e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672927"
---
# <a name="icm_setstate-message"></a><span data-ttu-id="39f12-105">\_Сообщение ICM SETSTATE</span><span class="sxs-lookup"><span data-stu-id="39f12-105">ICM\_SETSTATE message</span></span>

<span data-ttu-id="39f12-106">Сообщение **ICM \_ SETSTATE** уведомляет драйверу о сжатии видео о необходимости установки состояния сжатия.</span><span class="sxs-lookup"><span data-stu-id="39f12-106">The **ICM\_SETSTATE** message notifies a video compression driver to set the state of the compressor.</span></span> <span data-ttu-id="39f12-107">Это сообщение можно отправить явно или с помощью макроса [**иксетстате**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) .</span><span class="sxs-lookup"><span data-stu-id="39f12-107">You can send this message explicitly or by using the [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) macro.</span></span>


```C++
ICM_SETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a><span data-ttu-id="39f12-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="39f12-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39f12-109"><span id="pv"></span><span id="PV"></span>*PV*</span><span class="sxs-lookup"><span data-stu-id="39f12-109"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="39f12-110">Указатель на блок памяти, содержащий данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="39f12-110">Pointer to a block of memory containing configuration data.</span></span> <span data-ttu-id="39f12-111">Можно указать **значение NULL** для этого параметра, чтобы сбросить сжатие до состояния по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="39f12-111">You can specify **NULL** for this parameter to reset the compressor to its default state.</span></span>

</dd> <dt>

<span data-ttu-id="39f12-112"><span id="cb"></span><span id="CB"></span>*CB*</span><span class="sxs-lookup"><span data-stu-id="39f12-112"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="39f12-113">Размер блока памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="39f12-113">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39f12-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39f12-114">Return Value</span></span>

<span data-ttu-id="39f12-115">Возвращает число байтов, используемых модулем сжатия в случае успешного или нулевого значения.</span><span class="sxs-lookup"><span data-stu-id="39f12-115">Returns the number of bytes used by the compressor if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="39f12-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39f12-116">Remarks</span></span>

<span data-ttu-id="39f12-117">Сведения, используемые этим сообщением, являются частными и относятся к конкретному компрессору.</span><span class="sxs-lookup"><span data-stu-id="39f12-117">The information used by this message is private and specific to a given compressor.</span></span> <span data-ttu-id="39f12-118">Клиентские приложения должны использовать это сообщение только для восстановления сведений, ранее полученных с помощью сообщения [**ICM- \_ State**](icm-getstate.md) , и должны использовать параметр [**ICM \_ Configure**](icm-configure.md) для настройки драйвера сжатия видео.</span><span class="sxs-lookup"><span data-stu-id="39f12-118">Client applications should use this message only to restore information previously obtained with the [**ICM\_GETSTATE**](icm-getstate.md) message and should use the [**ICM\_CONFIGURE**](icm-configure.md) message to adjust the configuration of a video compression driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="39f12-119">Требования</span><span class="sxs-lookup"><span data-stu-id="39f12-119">Requirements</span></span>



| <span data-ttu-id="39f12-120">Требование</span><span class="sxs-lookup"><span data-stu-id="39f12-120">Requirement</span></span> | <span data-ttu-id="39f12-121">Значение</span><span class="sxs-lookup"><span data-stu-id="39f12-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="39f12-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39f12-122">Minimum supported client</span></span><br/> | <span data-ttu-id="39f12-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="39f12-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="39f12-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39f12-124">Minimum supported server</span></span><br/> | <span data-ttu-id="39f12-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="39f12-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="39f12-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="39f12-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="39f12-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="39f12-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39f12-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39f12-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39f12-129">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="39f12-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="39f12-130">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="39f12-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





