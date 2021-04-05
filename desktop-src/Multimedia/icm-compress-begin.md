---
title: Сообщение ICM_COMPRESS_BEGIN (VFW. h)
description: '\_ \_ Сообщение о начале сжатия ICM уведомляет драйвер сжатия видео о подготовке к сжатию данных. Это сообщение можно отправить явно или с помощью макроса Иккомпрессбегин.'
ms.assetid: dd1d3a66-c625-4f55-b65a-8545c1c16301
keywords:
- ICM_COMPRESS_BEGIN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_COMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e358aa3ab589af0be1e4e490c141ed41baeb5874
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104072004"
---
# <a name="icm_compress_begin-message"></a><span data-ttu-id="c1afc-105">\_ \_ Сообщение начала сжатия ICM</span><span class="sxs-lookup"><span data-stu-id="c1afc-105">ICM\_COMPRESS\_BEGIN message</span></span>

<span data-ttu-id="c1afc-106">Сообщение **о \_ \_ начале сжатия ICM** уведомляет драйвер сжатия видео о подготовке к сжатию данных.</span><span class="sxs-lookup"><span data-stu-id="c1afc-106">The **ICM\_COMPRESS\_BEGIN** message notifies a video compression driver to prepare to compress data.</span></span> <span data-ttu-id="c1afc-107">Это сообщение можно отправить явно или с помощью макроса [**иккомпрессбегин**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) .</span><span class="sxs-lookup"><span data-stu-id="c1afc-107">You can send this message explicitly or by using the [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) macro.</span></span>


```C++
ICM_COMPRESS_BEGIN 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="c1afc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1afc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1afc-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*лпбиинпут*</span><span class="sxs-lookup"><span data-stu-id="c1afc-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="c1afc-110">Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , содержащую входной формат.</span><span class="sxs-lookup"><span data-stu-id="c1afc-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="c1afc-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*лпбиаутпут*</span><span class="sxs-lookup"><span data-stu-id="c1afc-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="c1afc-112">Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , содержащую выходной формат.</span><span class="sxs-lookup"><span data-stu-id="c1afc-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1afc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1afc-113">Return Value</span></span>

<span data-ttu-id="c1afc-114">Возвращает ИЦЕРР \_ ОК, если драйвер поддерживает указанное сжатие или ицерр \_ бадформат, если формат входных или выходных данных не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c1afc-114">Returns ICERR\_OK if the driver supports the specified compression or ICERR\_BADFORMAT if the input or output format is not supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1afc-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1afc-115">Remarks</span></span>

<span data-ttu-id="c1afc-116">Драйвер должен выделять и инициализировать любые таблицы или память, необходимые для сжатия форматов данных при получении сообщения [**\_ сжатия ICM**](icm-compress.md) .</span><span class="sxs-lookup"><span data-stu-id="c1afc-116">The driver should allocate and initialize any tables or memory that it needs for compressing the data formats when it receives the [**ICM\_COMPRESS**](icm-compress.md) message.</span></span>

<span data-ttu-id="c1afc-117">ВКМ сохраняет параметры последнего сообщения о **\_ \_ начале сжатия ICM** .</span><span class="sxs-lookup"><span data-stu-id="c1afc-117">VCM saves the settings of the most recent **ICM\_COMPRESS\_BEGIN** message.</span></span> <span data-ttu-id="c1afc-118">Сообщения **о \_ начале сжатия ICM \_ Begin** и [**ICM \_ сжимать \_**](icm-compress-end.md) не вложены.</span><span class="sxs-lookup"><span data-stu-id="c1afc-118">The **ICM\_COMPRESS\_BEGIN** and [**ICM\_COMPRESS\_END**](icm-compress-end.md) messages do not nest.</span></span> <span data-ttu-id="c1afc-119">Если драйвер получает коэффициент **\_ сжатия ICM \_** , прежде чем сжатие будет остановлено с **\_ \_ окончанием сжатия ICM**, необходимо перезапустить сжатие с новыми параметрами.</span><span class="sxs-lookup"><span data-stu-id="c1afc-119">If your driver receives **ICM\_COMPRESS\_BEGIN** before compression is stopped with **ICM\_COMPRESS\_END**, it should restart compression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1afc-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c1afc-120">Requirements</span></span>



| <span data-ttu-id="c1afc-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c1afc-121">Requirement</span></span> | <span data-ttu-id="c1afc-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c1afc-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c1afc-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1afc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c1afc-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c1afc-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c1afc-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1afc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c1afc-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c1afc-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c1afc-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c1afc-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1afc-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1afc-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1afc-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1afc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1afc-130">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="c1afc-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="c1afc-131">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="c1afc-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

