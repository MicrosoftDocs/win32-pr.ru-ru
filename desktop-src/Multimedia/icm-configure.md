---
title: Сообщение ICM_CONFIGURE (VFW. h)
description: Сообщение ICM \_ Configure уведомляет драйвер сжатия видео о необходимости отобразить диалоговое окно настройки или запрашивает драйвер сжатия видео, чтобы определить, имеется ли в нем диалоговое окно конфигурации.
ms.assetid: 9760788e-fa66-44d7-bda6-aa9536143774
keywords:
- ICM_CONFIGURE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_CONFIGURE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9faae26fcf132abfa424b0db7a88670735d30727
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672804"
---
# <a name="icm_configure-message"></a><span data-ttu-id="3ea9a-104">\_Сообщение настройки ICM</span><span class="sxs-lookup"><span data-stu-id="3ea9a-104">ICM\_CONFIGURE message</span></span>

<span data-ttu-id="3ea9a-105">Сообщение **ICM \_ Configure** уведомляет драйвер сжатия видео о необходимости отобразить диалоговое окно настройки или запрашивает драйвер сжатия видео, чтобы определить, имеется ли в нем диалоговое окно конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3ea9a-105">The **ICM\_CONFIGURE** message notifies a video compression driver to display its configuration dialog box or queries a video compression driver to determine if it has a configuration dialog box.</span></span> <span data-ttu-id="3ea9a-106">Это сообщение можно отправить явно или с помощью макроса [**икконфигуре**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) .</span><span class="sxs-lookup"><span data-stu-id="3ea9a-106">You can send this message explicitly or by using the [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) macro.</span></span>


```C++
ICM_CONFIGURE 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="3ea9a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ea9a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ea9a-108"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="3ea9a-108"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="3ea9a-109">Обработано с родительским окном отображаемого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="3ea9a-109">Handle to the parent window of the displayed dialog box.</span></span> <span data-ttu-id="3ea9a-110">Можно определить, имеется ли в драйвере диалоговое окно конфигурации, указав в этом параметре значение 1, как в макросе [**иккуериконфигуре**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) .</span><span class="sxs-lookup"><span data-stu-id="3ea9a-110">You can determine if a driver has a configuration dialog box by specifying  1 in this parameter, as in the [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ea9a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ea9a-111">Return Value</span></span>

<span data-ttu-id="3ea9a-112">Возвращает ИЦЕРР \_ ОК, если драйвер поддерживает это сообщение или ИЦЕРР \_ не поддерживается в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3ea9a-112">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ea9a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ea9a-113">Remarks</span></span>

<span data-ttu-id="3ea9a-114">Это сообщение отличается от сообщения конфигурации [**DRV \_**](drv-configure.md) , используемого для настройки оборудования.</span><span class="sxs-lookup"><span data-stu-id="3ea9a-114">This message is different from the [**DRV\_CONFIGURE**](drv-configure.md) message used for hardware configuration.</span></span> <span data-ttu-id="3ea9a-115">Диалоговое окно этого сообщения должно предоставить пользователю возможность задать и изменить внутреннее состояние, на которое ссылаются сообщения [**ICM \_**](icm-getstate.md) [**\_ SETSTATE и ICM**](icm-setstate.md) .</span><span class="sxs-lookup"><span data-stu-id="3ea9a-115">The dialog box for this message should let the user set and edit the internal state referenced by the [**ICM\_GETSTATE**](icm-getstate.md) and [**ICM\_SETSTATE**](icm-setstate.md) messages.</span></span> <span data-ttu-id="3ea9a-116">Например, это диалоговое окно может изменять параметры пользователя, влияющие на уровень качества и другие аналогичные параметры сжатия.</span><span class="sxs-lookup"><span data-stu-id="3ea9a-116">For example, this dialog box can let the user change parameters affecting the quality level and other similar compression options.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ea9a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3ea9a-117">Requirements</span></span>



| <span data-ttu-id="3ea9a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3ea9a-118">Requirement</span></span> | <span data-ttu-id="3ea9a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3ea9a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3ea9a-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ea9a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3ea9a-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3ea9a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3ea9a-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ea9a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3ea9a-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3ea9a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3ea9a-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3ea9a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ea9a-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ea9a-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ea9a-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ea9a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ea9a-127">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="3ea9a-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="3ea9a-128">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="3ea9a-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





