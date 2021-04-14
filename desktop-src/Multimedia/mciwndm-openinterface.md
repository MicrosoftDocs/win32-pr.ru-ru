---
title: Сообщение MCIWNDM_OPENINTERFACE (VFW. h)
description: Сообщение МЦИВНДМ \_ опенинтерфаце присоединяет поток данных или файл, связанный с указанным интерфейсом, к окну мЦивнд. Это сообщение можно отправить явно или с помощью макроса МЦивндопенинтерфаце.
ms.assetid: 73cbd637-d315-4b39-a978-2b72aed1f303
keywords:
- MCIWNDM_OPENINTERFACE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_OPENINTERFACE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c40453f4d587429508a5aae19bc432fc46088ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414724"
---
# <a name="mciwndm_openinterface-message"></a><span data-ttu-id="dbb6f-105">\_Сообщение мЦивндм опенинтерфаце</span><span class="sxs-lookup"><span data-stu-id="dbb6f-105">MCIWNDM\_OPENINTERFACE message</span></span>

<span data-ttu-id="dbb6f-106">Сообщение **мЦивндм \_ опенинтерфаце** присоединяет поток данных или файл, связанный с указанным интерфейсом, к окну мЦивнд.</span><span class="sxs-lookup"><span data-stu-id="dbb6f-106">The **MCIWNDM\_OPENINTERFACE** message attaches the data stream or file associated with the specified interface to an MCIWnd window.</span></span> <span data-ttu-id="dbb6f-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндопенинтерфаце**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) .</span><span class="sxs-lookup"><span data-stu-id="dbb6f-107">You can send this message explicitly or by using the [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macro.</span></span>


```C++
MCIWNDM_OPENINTERFACE 
wParam = 0; 
lParam = (LPARAM) (LPUNKNOWN) pUnk; 
```



## <a name="parameters"></a><span data-ttu-id="dbb6f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbb6f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbb6f-109"><span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*pUnk*</span><span class="sxs-lookup"><span data-stu-id="dbb6f-109"><span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*pUnk*</span></span>
</dt> <dd>

<span data-ttu-id="dbb6f-110">Указатель на интерфейс ИАВИ, указывающий на файл или поток данных в файле.</span><span class="sxs-lookup"><span data-stu-id="dbb6f-110">Pointer to an IAVI interface that points to a file or a data stream in a file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbb6f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dbb6f-111">Return Value</span></span>

<span data-ttu-id="dbb6f-112">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="dbb6f-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbb6f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="dbb6f-113">Requirements</span></span>



| <span data-ttu-id="dbb6f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="dbb6f-114">Requirement</span></span> | <span data-ttu-id="dbb6f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="dbb6f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dbb6f-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dbb6f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dbb6f-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dbb6f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="dbb6f-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dbb6f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dbb6f-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dbb6f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dbb6f-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="dbb6f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbb6f-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbb6f-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbb6f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbb6f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbb6f-123">**мЦивндопенинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="dbb6f-123">**MCIWndOpenInterface**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface)
</dt> </dl>

 

 





