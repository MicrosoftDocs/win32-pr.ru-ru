---
title: Сообщение ICM_DECOMPRESSEX_BEGIN (VFW. h)
description: Сообщение ICM \_ декомпрессекс \_ Begin уведомляет драйвер сжатия видео о подготовке к распаковке данных.
ms.assetid: 35298274-91b5-4df0-b4b0-4a71d6a49990
keywords:
- ICM_DECOMPRESSEX_BEGIN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ea082c91d48a9964348b762ce13631cd80af30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803365"
---
# <a name="icm_decompressex_begin-message"></a><span data-ttu-id="b93fc-104">\_Сообщение о \_ начале ICM декомпрессекс</span><span class="sxs-lookup"><span data-stu-id="b93fc-104">ICM\_DECOMPRESSEX\_BEGIN message</span></span>

<span data-ttu-id="b93fc-105">Сообщение **ICM \_ декомпрессекс \_ Begin** уведомляет драйвер сжатия видео о подготовке к распаковке данных.</span><span class="sxs-lookup"><span data-stu-id="b93fc-105">The **ICM\_DECOMPRESSEX\_BEGIN** message notifies a video compression driver to prepare to decompress data.</span></span>


```C++
ICM_DECOMPRESSEX_BEGIN 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="b93fc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b93fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b93fc-107"><span id="icdex"></span><span id="ICDEX"></span>*икдекс*</span><span class="sxs-lookup"><span data-stu-id="b93fc-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="b93fc-108">Указатель на структуру [**икдекомпрессекс**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) , содержащую форматы входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b93fc-108">Pointer to a [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure containing the input and output formats.</span></span>

</dd> <dt>

<span data-ttu-id="b93fc-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="b93fc-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="b93fc-110">Размер [**икдекомпрессекс**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)в байтах.</span><span class="sxs-lookup"><span data-stu-id="b93fc-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b93fc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b93fc-111">Return Value</span></span>

<span data-ttu-id="b93fc-112">Возвращает ИЦЕРР \_ ОК, если указанное распаковка поддерживается или ицерр \_ бадформат в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b93fc-112">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b93fc-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b93fc-113">Remarks</span></span>

<span data-ttu-id="b93fc-114">Когда драйвер получает это сообщение, он должен выделить буферы и выполнить все длительные операции, чтобы они могли эффективно обрабатывать сообщения [**ICM \_ декомпрессекс**](icm-decompressex.md) .</span><span class="sxs-lookup"><span data-stu-id="b93fc-114">When the driver receives this message, it should allocate buffers and do any time-consuming operations so that it can process [**ICM\_DECOMPRESSEX**](icm-decompressex.md) messages efficiently.</span></span>

<span data-ttu-id="b93fc-115">Если требуется, чтобы драйвер распаковать данные непосредственно на экране, отправьте сообщение с помощью [**ICM \_ \_**](icm-draw-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="b93fc-115">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span>

<span data-ttu-id="b93fc-116">[**\_ \_ Конечные**](icm-decompressex-end.md) сообщения **ICM \_ декомпрессекс \_ Begin** и ICM декомпрессекс не вложены.</span><span class="sxs-lookup"><span data-stu-id="b93fc-116">The **ICM\_DECOMPRESSEX\_BEGIN** and [**ICM\_DECOMPRESSEX\_END**](icm-decompressex-end.md) messages do not nest.</span></span> <span data-ttu-id="b93fc-117">Если драйвер получает **ICM \_ декомпрессекс \_ Begin** до остановки распаковки с помощью **ICM \_ декомпрессекс \_ End**, он должен перезапустить распаковку с новыми параметрами.</span><span class="sxs-lookup"><span data-stu-id="b93fc-117">If your driver receives **ICM\_DECOMPRESSEX\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESSEX\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="b93fc-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b93fc-118">Requirements</span></span>



| <span data-ttu-id="b93fc-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b93fc-119">Requirement</span></span> | <span data-ttu-id="b93fc-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b93fc-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b93fc-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b93fc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b93fc-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b93fc-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b93fc-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b93fc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b93fc-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b93fc-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b93fc-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b93fc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b93fc-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b93fc-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b93fc-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b93fc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b93fc-128">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="b93fc-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="b93fc-129">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="b93fc-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





