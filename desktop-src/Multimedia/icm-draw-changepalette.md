---
title: Сообщение ICM_DRAW_CHANGEPALETTE (VFW. h)
description: Сообщение ICM \_ Draw \_ чанжепалетте уведомляет драйвер подготовки к просмотру, что изменяется палитра роликов. Это сообщение можно отправить явно или с помощью макроса Икдравчанжепалетте.
ms.assetid: 974fc0d8-d0c7-4a82-af84-68b53f753259
keywords:
- ICM_DRAW_CHANGEPALETTE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_CHANGEPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6364abb2c535158b2e64ff311041b00490c5958c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892109"
---
# <a name="icm_draw_changepalette-message"></a><span data-ttu-id="f404b-105">\_Сообщение ICM Draw \_ чанжепалетте</span><span class="sxs-lookup"><span data-stu-id="f404b-105">ICM\_DRAW\_CHANGEPALETTE message</span></span>

<span data-ttu-id="f404b-106">Сообщение **ICM \_ Draw \_ чанжепалетте** уведомляет драйвер подготовки к просмотру, что изменяется палитра роликов.</span><span class="sxs-lookup"><span data-stu-id="f404b-106">The **ICM\_DRAW\_CHANGEPALETTE** message notifies a rendering driver that the movie palette is changing.</span></span> <span data-ttu-id="f404b-107">Это сообщение можно отправить явно или с помощью макроса [**икдравчанжепалетте**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) .</span><span class="sxs-lookup"><span data-stu-id="f404b-107">You can send this message explicitly or by using the [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) macro.</span></span>


```C++
ICM_DRAW_CHANGEPALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="f404b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f404b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f404b-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*лпбиинпут*</span><span class="sxs-lookup"><span data-stu-id="f404b-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="f404b-110">Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , содержащую новый формат и необязательную таблицу цветов.</span><span class="sxs-lookup"><span data-stu-id="f404b-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the new format and optional color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f404b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f404b-111">Return Value</span></span>

<span data-ttu-id="f404b-112">Возвращает ИЦЕРР \_ ОК в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f404b-112">Returns ICERR\_OK if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f404b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f404b-113">Remarks</span></span>

<span data-ttu-id="f404b-114">Это сообщение должно поддерживаться с помощью устанавливаемых обработчиков отрисовки, которые рисуют DIB с внутренней структурой, содержащей палитру.</span><span class="sxs-lookup"><span data-stu-id="f404b-114">This message should be supported by installable rendering handlers that draw DIBs with an internal structure that includes a palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="f404b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f404b-115">Requirements</span></span>



| <span data-ttu-id="f404b-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f404b-116">Requirement</span></span> | <span data-ttu-id="f404b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f404b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f404b-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f404b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f404b-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f404b-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f404b-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f404b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f404b-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f404b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f404b-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f404b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f404b-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f404b-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f404b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f404b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f404b-125">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="f404b-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="f404b-126">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="f404b-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

