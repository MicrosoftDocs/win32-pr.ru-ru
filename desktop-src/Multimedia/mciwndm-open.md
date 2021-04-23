---
title: Сообщение MCIWNDM_OPEN (VFW. h)
description: МЦИВНДМ \_ Open Message открывает устройство MCI и связывает его с окном мЦивнд.
ms.assetid: ad1dfe0f-015b-45a9-ab88-cc0bdf0aa057
keywords:
- MCIWNDM_OPEN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2f232ea9076a1e0ff8c105d8c5cf94104e455c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135670"
---
# <a name="mciwndm_open-message"></a><span data-ttu-id="15132-104">МЦИВНДМ \_ открытое сообщение</span><span class="sxs-lookup"><span data-stu-id="15132-104">MCIWNDM\_OPEN message</span></span>

<span data-ttu-id="15132-105">**МЦивндм \_ Open** Message открывает устройство MCI и связывает его с окном мЦивнд.</span><span class="sxs-lookup"><span data-stu-id="15132-105">The **MCIWNDM\_OPEN** message opens an MCI device and associates it with an MCIWnd window.</span></span> <span data-ttu-id="15132-106">Для устройств MCI, использующих файлы данных, этот макрос также может открыть указанный файл данных, присвоить имя новому создаваемому файлу или открыть диалоговое окно, позволяющее пользователю выбрать открываемый файл.</span><span class="sxs-lookup"><span data-stu-id="15132-106">For MCI devices that use data files, this macro can also open a specified data file, name a new file to be created, or display a dialog box to let the user select a file to open.</span></span> <span data-ttu-id="15132-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндопен**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) .</span><span class="sxs-lookup"><span data-stu-id="15132-107">You can send this message explicitly or by using the [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) macro.</span></span>


```C++
MCIWNDM_OPEN 
wParam = (WPARAM) (UINT) wFlags; 
lParam = (LPARAM) (LPVOID) szFile; 
```



## <a name="parameters"></a><span data-ttu-id="15132-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="15132-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15132-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*вфлагс*</span><span class="sxs-lookup"><span data-stu-id="15132-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span></span>
</dt> <dd>

<span data-ttu-id="15132-110">Флаги, связанные с открываемым устройством или файлом.</span><span class="sxs-lookup"><span data-stu-id="15132-110">Flags associated with the device or file to open.</span></span> <span data-ttu-id="15132-111">\_Флаг New мЦивндопенф указывает, что новый файл создается с именем, указанным в **сзфиле**.</span><span class="sxs-lookup"><span data-stu-id="15132-111">The MCIWNDOPENF\_NEW flag specifies a new file is to be created with the name specified in **szFile**.</span></span>

</dd> <dt>

<span data-ttu-id="15132-112"><span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*сзфиле*</span><span class="sxs-lookup"><span data-stu-id="15132-112"><span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*</span></span>
</dt> <dd>

<span data-ttu-id="15132-113">Указатель на строку, завершающуюся нулем, указывающую имя файла или устройства MCI, которое нужно открыть.</span><span class="sxs-lookup"><span data-stu-id="15132-113">Pointer to a null-terminated string identifying the filename or MCI device name to open.</span></span> <span data-ttu-id="15132-114">Укажите значение 1 для этого параметра, чтобы отобразить диалоговое окно Открыть.</span><span class="sxs-lookup"><span data-stu-id="15132-114">Specify  1 for this parameter to display the Open dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15132-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15132-115">Return Value</span></span>

<span data-ttu-id="15132-116">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="15132-116">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="15132-117">Требования</span><span class="sxs-lookup"><span data-stu-id="15132-117">Requirements</span></span>



| <span data-ttu-id="15132-118">Требование</span><span class="sxs-lookup"><span data-stu-id="15132-118">Requirement</span></span> | <span data-ttu-id="15132-119">Значение</span><span class="sxs-lookup"><span data-stu-id="15132-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15132-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15132-120">Minimum supported client</span></span><br/> | <span data-ttu-id="15132-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="15132-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="15132-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15132-122">Minimum supported server</span></span><br/> | <span data-ttu-id="15132-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="15132-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="15132-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="15132-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="15132-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="15132-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15132-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15132-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15132-127">**мЦивндопен**</span><span class="sxs-lookup"><span data-stu-id="15132-127">**MCIWndOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
</dt> </dl>

 

 





