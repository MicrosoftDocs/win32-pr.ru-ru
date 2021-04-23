---
title: Сообщение MCIWNDM_GETDEVICE (VFW. h)
description: Сообщение МЦИВНДМing \_ возвращает имя текущего открытого устройства MCI. Это сообщение можно отправить явно или с помощью макроса МЦивнджетдевице.
ms.assetid: e69a73a6-a927-4536-98c7-ee7d5b16668a
keywords:
- MCIWNDM_GETDEVICE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32664508a577db9d5a077e3cb4fd00aab34fbdf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489426"
---
# <a name="mciwndm_getdevice-message"></a><span data-ttu-id="01ab0-105">\_Сообщение мЦивндм</span><span class="sxs-lookup"><span data-stu-id="01ab0-105">MCIWNDM\_GETDEVICE message</span></span>

<span data-ttu-id="01ab0-106">Сообщение **мЦивндмing \_** возвращает имя текущего открытого устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="01ab0-106">The **MCIWNDM\_GETDEVICE** message retrieves the name of the currently open MCI device.</span></span> <span data-ttu-id="01ab0-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетдевице**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) .</span><span class="sxs-lookup"><span data-stu-id="01ab0-107">You can send this message explicitly or by using the [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) macro.</span></span>


```C++
MCIWNDM_GETDEVICE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="01ab0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="01ab0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01ab0-109"><span id="len"></span><span id="LEN"></span>*len*</span><span class="sxs-lookup"><span data-stu-id="01ab0-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="01ab0-110">Размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="01ab0-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="01ab0-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="01ab0-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="01ab0-112">Указатель на определенный приложением буфер для возврата имени устройства.</span><span class="sxs-lookup"><span data-stu-id="01ab0-112">Pointer to an application-defined buffer to return the device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01ab0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01ab0-113">Return Value</span></span>

<span data-ttu-id="01ab0-114">Возвращает нуль в случае успеха или ненулевое значение в противном случае.</span><span class="sxs-lookup"><span data-stu-id="01ab0-114">Returns zero if successful or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="01ab0-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01ab0-115">Remarks</span></span>

<span data-ttu-id="01ab0-116">Если строка, заканчивающаяся символом NULL, содержащая имя устройства, длиннее, чем буфер, МЦивнд усекает его.</span><span class="sxs-lookup"><span data-stu-id="01ab0-116">If the null-terminated string containing the device name is longer than the buffer, MCIWnd truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="01ab0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="01ab0-117">Requirements</span></span>



| <span data-ttu-id="01ab0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="01ab0-118">Requirement</span></span> | <span data-ttu-id="01ab0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="01ab0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="01ab0-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01ab0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="01ab0-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="01ab0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="01ab0-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01ab0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="01ab0-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="01ab0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="01ab0-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="01ab0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="01ab0-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="01ab0-125"><dt>Vfw.h</dt></span></span> </dl> |



 

 





