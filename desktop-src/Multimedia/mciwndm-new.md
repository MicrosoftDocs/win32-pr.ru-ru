---
title: Сообщение MCIWNDM_NEW (VFW. h)
description: '\_Новое сообщение мЦивндм создает новый файл для текущего устройства MCI. Это сообщение можно отправить явно или с помощью макроса МЦивнднев.'
ms.assetid: 18b2340d-8303-415a-867f-bd346034db2a
keywords:
- MCIWNDM_NEW сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_NEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293323cd0404da45e648024b35b7f96ef60fea61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802021"
---
# <a name="mciwndm_new-message"></a><span data-ttu-id="f6ea0-105">МЦИВНДМ \_ новое сообщение</span><span class="sxs-lookup"><span data-stu-id="f6ea0-105">MCIWNDM\_NEW message</span></span>

<span data-ttu-id="f6ea0-106">**\_ Новое сообщение мЦивндм** создает новый файл для текущего устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="f6ea0-106">The **MCIWNDM\_NEW** message creates a new file for the current MCI device.</span></span> <span data-ttu-id="f6ea0-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнднев**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) .</span><span class="sxs-lookup"><span data-stu-id="f6ea0-107">You can send this message explicitly or by using the [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro.</span></span>


```C++
MCIWNDM_NEW 
wParam = 0; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="f6ea0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6ea0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6ea0-109"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="f6ea0-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="f6ea0-110">Указатель на буфер, содержащий имя устройства MCI, которое будет использовать файл.</span><span class="sxs-lookup"><span data-stu-id="f6ea0-110">Pointer to a buffer containing the name of the MCI device that will use the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6ea0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6ea0-111">Return Value</span></span>

<span data-ttu-id="f6ea0-112">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f6ea0-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6ea0-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f6ea0-113">Requirements</span></span>



| <span data-ttu-id="f6ea0-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f6ea0-114">Requirement</span></span> | <span data-ttu-id="f6ea0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f6ea0-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f6ea0-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6ea0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f6ea0-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f6ea0-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f6ea0-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6ea0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f6ea0-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f6ea0-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f6ea0-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f6ea0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6ea0-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6ea0-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6ea0-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6ea0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6ea0-123">**мЦивнднев**</span><span class="sxs-lookup"><span data-stu-id="f6ea0-123">**MCIWndNew**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)
</dt> </dl>

 

 





