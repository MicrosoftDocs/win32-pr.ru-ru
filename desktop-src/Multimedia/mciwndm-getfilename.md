---
title: Сообщение MCIWNDM_GETFILENAME (VFW. h)
description: Сообщение МЦИВНДМ \_ . filename извлекает имя файла, которое в настоящее время используется устройством MCI. Это сообщение можно отправить явно или с помощью макроса МЦивнджетфиленаме.
ms.assetid: d61b1b6d-0fae-4732-993c-41e08a4e05be
keywords:
- MCIWNDM_GETFILENAME сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETFILENAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 232a1d829b5cdd6da23e7dd3fb0294b95ca79f4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533812"
---
# <a name="mciwndm_getfilename-message"></a><span data-ttu-id="3ecf5-105">Сообщение МЦИВНДМ. \_ имя_файла</span><span class="sxs-lookup"><span data-stu-id="3ecf5-105">MCIWNDM\_GETFILENAME message</span></span>

<span data-ttu-id="3ecf5-106">Сообщение **мЦивндм. \_ filename** извлекает имя файла, которое в настоящее время используется устройством MCI.</span><span class="sxs-lookup"><span data-stu-id="3ecf5-106">The **MCIWNDM\_GETFILENAME** message retrieves the filename currently used by an MCI device.</span></span> <span data-ttu-id="3ecf5-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетфиленаме**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) .</span><span class="sxs-lookup"><span data-stu-id="3ecf5-107">You can send this message explicitly or by using the [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) macro.</span></span>


```C++
MCIWNDM_GETFILENAME 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="3ecf5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ecf5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ecf5-109"><span id="len"></span><span id="LEN"></span>*len*</span><span class="sxs-lookup"><span data-stu-id="3ecf5-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="3ecf5-110">Размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="3ecf5-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3ecf5-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="3ecf5-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="3ecf5-112">Указатель на определенный приложением буфер для возврата имени файла.</span><span class="sxs-lookup"><span data-stu-id="3ecf5-112">Pointer to an application-defined buffer to return the filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ecf5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ecf5-113">Return Value</span></span>

<span data-ttu-id="3ecf5-114">Возвращает нуль в случае успеха или 1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3ecf5-114">Returns zero if successful or 1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ecf5-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ecf5-115">Remarks</span></span>

<span data-ttu-id="3ecf5-116">Если строка с завершающим нулем, содержащая имя файла, длиннее, чем буфер, МЦивнд усекает имя файла.</span><span class="sxs-lookup"><span data-stu-id="3ecf5-116">If the null-terminated string containing the filename is longer than the buffer, MCIWnd truncates the filename.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ecf5-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3ecf5-117">Requirements</span></span>



| <span data-ttu-id="3ecf5-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3ecf5-118">Requirement</span></span> | <span data-ttu-id="3ecf5-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3ecf5-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3ecf5-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ecf5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3ecf5-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3ecf5-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3ecf5-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ecf5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3ecf5-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3ecf5-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3ecf5-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3ecf5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ecf5-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ecf5-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ecf5-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ecf5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ecf5-127">**мЦивнджетфиленаме**</span><span class="sxs-lookup"><span data-stu-id="3ecf5-127">**MCIWndGetFileName**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename)
</dt> </dl>

 

 





