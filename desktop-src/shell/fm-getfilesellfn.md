---
description: Отправляется расширением диспетчера файлов для получения сведений о выбранном файле из активного окна диспетчера файлов (в окне каталога или в окне результатов поиска). Выбранный файл может иметь длинное имя файла.
title: Сообщение FM_GETFILESELLFN (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESELLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 461fd171-d47f-41d6-953e-8e497e023ab1
ms.openlocfilehash: e991d2705f74aa8822dcef89878e9762f22b08dc
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842395"
---
# <a name="fm_getfilesellfn-message"></a><span data-ttu-id="632ad-104">\_Сообщение FM жетфилеселлфн</span><span class="sxs-lookup"><span data-stu-id="632ad-104">FM\_GETFILESELLFN message</span></span>

<span data-ttu-id="632ad-105">Отправляется расширением диспетчера файлов для получения сведений о выбранном файле из активного окна диспетчера файлов (в окне каталога или в окне результатов поиска).</span><span class="sxs-lookup"><span data-stu-id="632ad-105">Sent by a File Manager extension to retrieve information about a selected file from the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="632ad-106">Выбранный файл может иметь длинное имя файла.</span><span class="sxs-lookup"><span data-stu-id="632ad-106">The selected file can have a long file name.</span></span>

## <a name="parameters"></a><span data-ttu-id="632ad-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="632ad-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="632ad-108">*index*</span><span class="sxs-lookup"><span data-stu-id="632ad-108">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="632ad-109">Отсчитываемый от нуля индекс выбранного файла для извлечения.</span><span class="sxs-lookup"><span data-stu-id="632ad-109">The zero-based index of the selected file to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="632ad-110">*лпфмсгфс*</span><span class="sxs-lookup"><span data-stu-id="632ad-110">*lpfmsgfs*</span></span> 
</dt> <dd>

<span data-ttu-id="632ad-111">Адрес структуры [**FMS \_ жетфилесел**](fms-getfilesel.md) , которая получает сведения о выделенном фрагменте.</span><span class="sxs-lookup"><span data-stu-id="632ad-111">The address of an [**FMS\_GETFILESEL**](fms-getfilesel.md) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="632ad-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="632ad-112">Return value</span></span>

<span data-ttu-id="632ad-113">Возвращает отсчитываемый от нуля индекс выбранного файла, который был получен.</span><span class="sxs-lookup"><span data-stu-id="632ad-113">Returns the zero-based index of the selected file that was retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="632ad-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="632ad-114">Remarks</span></span>

<span data-ttu-id="632ad-115">Только расширения, поддерживающие длинные имена файлов (например, сетевые расширения), должны использовать это сообщение.</span><span class="sxs-lookup"><span data-stu-id="632ad-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

<span data-ttu-id="632ad-116">Расширение может использовать сообщение [**FM \_ жетселкаунтлфн**](fm-getselcountlfn.md) для получения числа выбранных файлов.</span><span class="sxs-lookup"><span data-stu-id="632ad-116">An extension can use the [**FM\_GETSELCOUNTLFN**](fm-getselcountlfn.md) message to retrieve the count of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="632ad-117">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="632ad-117">Requirements</span></span>



| <span data-ttu-id="632ad-118">Требование</span><span class="sxs-lookup"><span data-stu-id="632ad-118">Requirement</span></span> | <span data-ttu-id="632ad-119">Значение</span><span class="sxs-lookup"><span data-stu-id="632ad-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="632ad-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="632ad-120">Minimum supported client</span></span><br/> | <span data-ttu-id="632ad-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="632ad-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="632ad-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="632ad-122">Minimum supported server</span></span><br/> | <span data-ttu-id="632ad-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="632ad-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="632ad-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="632ad-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="632ad-125"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="632ad-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="632ad-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="632ad-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="632ad-127">**фмекстенсионпрок**</span><span class="sxs-lookup"><span data-stu-id="632ad-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="632ad-128">**FM \_ жетфилесел**</span><span class="sxs-lookup"><span data-stu-id="632ad-128">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="632ad-129">**FM \_ жетселкаунт**</span><span class="sxs-lookup"><span data-stu-id="632ad-129">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 




