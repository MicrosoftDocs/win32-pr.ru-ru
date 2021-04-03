---
title: Сообщение ICM_DECOMPRESS_BEGIN (VFW. h)
description: '\_ \_ Сообщение о начале распаковки ICM уведомляет драйвер о распаковке видео, чтобы подготовиться к распаковке данных. Это сообщение можно отправить явно или с помощью макроса Икдекомпрессбегин.'
ms.assetid: 24cd5220-d473-4968-8678-b00670eecf8f
keywords:
- ICM_DECOMPRESS_BEGIN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b8f55ebb5543c73e0d7a9c9ee800fabfc483d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137070"
---
# <a name="icm_decompress_begin-message"></a><span data-ttu-id="9f297-105">\_Сообщение начала распаковки ICM \_</span><span class="sxs-lookup"><span data-stu-id="9f297-105">ICM\_DECOMPRESS\_BEGIN message</span></span>

<span data-ttu-id="9f297-106">Сообщение **о \_ \_ начале распаковки ICM** уведомляет драйвер о распаковке видео, чтобы подготовиться к распаковке данных.</span><span class="sxs-lookup"><span data-stu-id="9f297-106">The **ICM\_DECOMPRESS\_BEGIN** message notifies a video decompression driver to prepare to decompress data.</span></span> <span data-ttu-id="9f297-107">Это сообщение можно отправить явно или с помощью макроса [**икдекомпрессбегин**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) .</span><span class="sxs-lookup"><span data-stu-id="9f297-107">You can send this message explicitly or by using the [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) macro.</span></span>


```C++
ICM_DECOMPRESS_BEGIN 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="9f297-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f297-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f297-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*лпбиинпут*</span><span class="sxs-lookup"><span data-stu-id="9f297-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="9f297-110">Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , содержащую входной формат.</span><span class="sxs-lookup"><span data-stu-id="9f297-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="9f297-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*лпбиаутпут*</span><span class="sxs-lookup"><span data-stu-id="9f297-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="9f297-112">Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , содержащую выходной формат.</span><span class="sxs-lookup"><span data-stu-id="9f297-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f297-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f297-113">Return Value</span></span>

<span data-ttu-id="9f297-114">Возвращает ИЦЕРР \_ ОК, если указанное распаковка поддерживается или ицерр \_ бадформат в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9f297-114">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f297-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f297-115">Remarks</span></span>

<span data-ttu-id="9f297-116">Когда драйвер получает это сообщение, он должен выделить буферы и выполнить все длительные операции, чтобы они могли эффективно обрабатывать [**\_ файлы ICM**](icm-decompress.md) .</span><span class="sxs-lookup"><span data-stu-id="9f297-116">When the driver receives this message, it should allocate buffers and do any time-consuming operations so that it can process [**ICM\_DECOMPRESS**](icm-decompress.md) messages efficiently.</span></span>

<span data-ttu-id="9f297-117">Если требуется, чтобы драйвер распаковать данные непосредственно на экране, отправьте сообщение [**ICM \_ Draw**](icm-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="9f297-117">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="9f297-118">Не вложены в сообщения End **\_ распаковки \_ Begin** и [**ICM \_ unуплотнение \_**](icm-decompress-end.md) .</span><span class="sxs-lookup"><span data-stu-id="9f297-118">The **ICM\_DECOMPRESS\_BEGIN** and [**ICM\_DECOMPRESS\_END**](icm-decompress-end.md) messages do not nest.</span></span> <span data-ttu-id="9f297-119">Если драйвер Получает подсистему **\_ распаковки ICM \_ Begin** до остановки распаковки **с \_ \_ окончанием распаковки ICM**, необходимо перезапустить распаковку с новыми параметрами.</span><span class="sxs-lookup"><span data-stu-id="9f297-119">If your driver receives **ICM\_DECOMPRESS\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESS\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f297-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9f297-120">Requirements</span></span>



| <span data-ttu-id="9f297-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9f297-121">Requirement</span></span> | <span data-ttu-id="9f297-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9f297-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9f297-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f297-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9f297-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f297-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9f297-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f297-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9f297-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f297-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9f297-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9f297-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f297-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f297-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f297-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f297-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f297-130">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="9f297-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="9f297-131">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="9f297-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

