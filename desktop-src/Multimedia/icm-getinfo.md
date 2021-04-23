---
title: Сообщение ICM_GETINFO (VFW. h)
description: Сообщение ICM \_ info запрашивает драйвер сжатия видео, чтобы получить описание самого себя в структуре иЦинфо.
ms.assetid: 8029f247-9777-4a34-9e84-908482094493
keywords:
- ICM_GETINFO сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_GETINFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634803b7dd9a3b8900c35fabedcadb99908c2b31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672682"
---
# <a name="icm_getinfo-message"></a><span data-ttu-id="44eb6-104">Информационное \_ сообщение ICM</span><span class="sxs-lookup"><span data-stu-id="44eb6-104">ICM\_GETINFO message</span></span>

<span data-ttu-id="44eb6-105">Сообщение **ICM \_ info** запрашивает драйвер сжатия видео, чтобы получить описание самого себя в структуре [**иЦинфо**](/windows/desktop/api/Vfw/ns-vfw-icinfo) .</span><span class="sxs-lookup"><span data-stu-id="44eb6-105">The **ICM\_GETINFO** message queries a video compression driver to return a description of itself in an [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure.</span></span>


```C++
ICM_GETINFO 
wParam = (DWORD) (LPVOID) lpicinfo; 
lParam = sizeof(ICINFO); 
```



## <a name="parameters"></a><span data-ttu-id="44eb6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="44eb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44eb6-107"><span id="lpicinfo"></span><span id="LPICINFO"></span>*лпиЦинфо*</span><span class="sxs-lookup"><span data-stu-id="44eb6-107"><span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*</span></span>
</dt> <dd>

<span data-ttu-id="44eb6-108">Указатель на структуру **иЦинфо** для хранения информации.</span><span class="sxs-lookup"><span data-stu-id="44eb6-108">Pointer to an **ICINFO** structure to contain information.</span></span>

</dd> <dt>

<span data-ttu-id="44eb6-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="44eb6-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="44eb6-110">Размер **иЦинфо** в байтах.</span><span class="sxs-lookup"><span data-stu-id="44eb6-110">Size, in bytes, of **ICINFO**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44eb6-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44eb6-111">Return Value</span></span>

<span data-ttu-id="44eb6-112">Возвращает размер (в байтах) [**иЦинфо**](/windows/desktop/api/Vfw/ns-vfw-icinfo) или нуль в случае возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="44eb6-112">Returns the size, in bytes, of [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) or zero if an error occurs..</span></span>

## <a name="remarks"></a><span data-ttu-id="44eb6-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44eb6-113">Remarks</span></span>

<span data-ttu-id="44eb6-114">Как правило, приложения отправляют это сообщение, чтобы отобразить список установленных компрессоров.</span><span class="sxs-lookup"><span data-stu-id="44eb6-114">Typically, applications send this message to display a list of the installed compressors.</span></span>

<span data-ttu-id="44eb6-115">Драйвер должен заполнить все элементы структуры [**иЦинфо**](/windows/desktop/api/Vfw/ns-vfw-icinfo) , за исключением **сздривер**.</span><span class="sxs-lookup"><span data-stu-id="44eb6-115">The driver should fill all members of the [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure except **szDriver**.</span></span>

## <a name="requirements"></a><span data-ttu-id="44eb6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="44eb6-116">Requirements</span></span>



| <span data-ttu-id="44eb6-117">Требование</span><span class="sxs-lookup"><span data-stu-id="44eb6-117">Requirement</span></span> | <span data-ttu-id="44eb6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="44eb6-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="44eb6-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44eb6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="44eb6-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="44eb6-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="44eb6-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44eb6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="44eb6-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="44eb6-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="44eb6-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="44eb6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="44eb6-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="44eb6-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44eb6-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44eb6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44eb6-126">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="44eb6-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="44eb6-127">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="44eb6-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





