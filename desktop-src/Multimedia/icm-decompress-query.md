---
title: Сообщение ICM_DECOMPRESS_QUERY (VFW. h)
description: Сообщение с \_ запросом ICM распаковка \_ запрашивает драйвер распаковки видео, чтобы определить, поддерживает ли он определенный входной формат, или же он может распаковать определенный входной формат в определенный выходной формат.
ms.assetid: 622dd1de-3f7a-4841-913c-282c2ad766f4
keywords:
- ICM_DECOMPRESS_QUERY сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838c946a38f9c2fda0c9178a36107af73f539a03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672800"
---
# <a name="icm_decompress_query-message"></a><span data-ttu-id="4a7f8-104">\_Сообщение о распаковке \_ запроса ICM</span><span class="sxs-lookup"><span data-stu-id="4a7f8-104">ICM\_DECOMPRESS\_QUERY message</span></span>

<span data-ttu-id="4a7f8-105">Сообщение **с \_ \_ ЗАПРОСом ICM распаковка** запрашивает драйвер распаковки видео, чтобы определить, поддерживает ли он определенный входной формат, или же он может распаковать определенный входной формат в определенный выходной формат.</span><span class="sxs-lookup"><span data-stu-id="4a7f8-105">The **ICM\_DECOMPRESS\_QUERY** message queries a video decompression driver to determine if it supports a specific input format or if it can decompress a specific input format to a specific output format.</span></span> <span data-ttu-id="4a7f8-106">Это сообщение можно отправить явно или с помощью макроса [**икдекомпресскуери**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) .</span><span class="sxs-lookup"><span data-stu-id="4a7f8-106">You can send this message explicitly or by using the [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) macro.</span></span>


```C++
ICM_DECOMPRESS_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="4a7f8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a7f8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a7f8-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*лпбиинпут*</span><span class="sxs-lookup"><span data-stu-id="4a7f8-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="4a7f8-109">Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , содержащую входной формат.</span><span class="sxs-lookup"><span data-stu-id="4a7f8-109">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="4a7f8-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*лпбиаутпут*</span><span class="sxs-lookup"><span data-stu-id="4a7f8-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="4a7f8-111">Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , содержащую выходной формат.</span><span class="sxs-lookup"><span data-stu-id="4a7f8-111">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span> <span data-ttu-id="4a7f8-112">Для этого параметра можно указать ноль, чтобы указать допустимый выходной формат.</span><span class="sxs-lookup"><span data-stu-id="4a7f8-112">You can specify zero for this parameter to indicate any output format is acceptable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a7f8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a7f8-113">Return Value</span></span>

<span data-ttu-id="4a7f8-114">Возвращает ИЦЕРР \_ ОК, если указанное распаковка поддерживается или ицерр \_ бадформат в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4a7f8-114">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a7f8-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4a7f8-115">Requirements</span></span>



| <span data-ttu-id="4a7f8-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4a7f8-116">Requirement</span></span> | <span data-ttu-id="4a7f8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4a7f8-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4a7f8-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a7f8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4a7f8-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4a7f8-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4a7f8-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a7f8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4a7f8-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4a7f8-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4a7f8-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4a7f8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a7f8-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a7f8-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a7f8-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a7f8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a7f8-125">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="4a7f8-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="4a7f8-126">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="4a7f8-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

