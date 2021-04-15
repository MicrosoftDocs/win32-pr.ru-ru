---
title: Сообщение ICM_DRAW_QUERY (VFW. h)
description: Сообщение с \_ \_ запросом ICM Draw запрашивает драйвер подготовки к просмотру, чтобы определить, может ли он визуализировать данные в определенном формате. Это сообщение можно отправить явно или с помощью макроса Икдравкуери.
ms.assetid: b829a04b-c1be-47c6-96e9-a6dc6f802811
keywords:
- ICM_DRAW_QUERY сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27266484cffa503583df32b60c6e8a0c04f344f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491148"
---
# <a name="icm_draw_query-message"></a><span data-ttu-id="c8e01-105">\_ \_ Сообщение запроса ICM Draw</span><span class="sxs-lookup"><span data-stu-id="c8e01-105">ICM\_DRAW\_QUERY message</span></span>

<span data-ttu-id="c8e01-106">Сообщение **с \_ \_ запросом ICM Draw** запрашивает драйвер подготовки к просмотру, чтобы определить, может ли он визуализировать данные в определенном формате.</span><span class="sxs-lookup"><span data-stu-id="c8e01-106">The **ICM\_DRAW\_QUERY** message queries a rendering driver to determine if it can render data in a specific format.</span></span> <span data-ttu-id="c8e01-107">Это сообщение можно отправить явно или с помощью макроса [**икдравкуери**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) .</span><span class="sxs-lookup"><span data-stu-id="c8e01-107">You can send this message explicitly or by using the [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) macro.</span></span>


```C++
ICM_DRAW_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="c8e01-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8e01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8e01-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*лпбиинпут*</span><span class="sxs-lookup"><span data-stu-id="c8e01-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="c8e01-110">Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , содержащую входной формат.</span><span class="sxs-lookup"><span data-stu-id="c8e01-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8e01-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8e01-111">Return Value</span></span>

<span data-ttu-id="c8e01-112">Возвращает ИЦЕРР \_ ОК, если драйвер может отображать данные в указанном формате или ицерр \_ бадформат в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c8e01-112">Returns ICERR\_OK if the driver can render data in the specified format or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8e01-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c8e01-113">Remarks</span></span>

<span data-ttu-id="c8e01-114">Это сообщение отличается от [**ICM- \_ сообщений \_ Begin**](icm-draw-begin.md) , так как оно запрашивает драйвер в общем смысле.</span><span class="sxs-lookup"><span data-stu-id="c8e01-114">This message differs from the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message in that it queries the driver in a general sense.</span></span> <span data-ttu-id="c8e01-115">**ICM \_ \_Начало рисования** определяет, может ли драйвер выводить данные с использованием указанного формата в определенных условиях, таких как растяжение изображения.</span><span class="sxs-lookup"><span data-stu-id="c8e01-115">**ICM\_DRAW\_BEGIN** determines if the driver can draw the data using the specified format under specific conditions, such as stretching the image.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8e01-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c8e01-116">Requirements</span></span>



| <span data-ttu-id="c8e01-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c8e01-117">Requirement</span></span> | <span data-ttu-id="c8e01-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c8e01-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c8e01-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8e01-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c8e01-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c8e01-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c8e01-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8e01-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c8e01-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c8e01-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c8e01-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c8e01-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8e01-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8e01-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8e01-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8e01-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8e01-126">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="c8e01-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="c8e01-127">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="c8e01-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

