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
ms.openlocfilehash: 847100f494772b3c59ad719d03d7bc2dbe28cc29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496788"
---
# <a name="fm_getfilesellfn-message"></a><span data-ttu-id="62e40-104">\_Сообщение FM жетфилеселлфн</span><span class="sxs-lookup"><span data-stu-id="62e40-104">FM\_GETFILESELLFN message</span></span>

<span data-ttu-id="62e40-105">Отправляется расширением диспетчера файлов для получения сведений о выбранном файле из активного окна диспетчера файлов (в окне каталога или в окне результатов поиска).</span><span class="sxs-lookup"><span data-stu-id="62e40-105">Sent by a File Manager extension to retrieve information about a selected file from the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="62e40-106">Выбранный файл может иметь длинное имя файла.</span><span class="sxs-lookup"><span data-stu-id="62e40-106">The selected file can have a long file name.</span></span>

## <a name="parameters"></a><span data-ttu-id="62e40-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="62e40-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62e40-108">*index*</span><span class="sxs-lookup"><span data-stu-id="62e40-108">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="62e40-109">Отсчитываемый от нуля индекс выбранного файла для извлечения.</span><span class="sxs-lookup"><span data-stu-id="62e40-109">The zero-based index of the selected file to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="62e40-110">*лпфмсгфс*</span><span class="sxs-lookup"><span data-stu-id="62e40-110">*lpfmsgfs*</span></span> 
</dt> <dd>

<span data-ttu-id="62e40-111">Адрес структуры [**FMS \_ жетфилесел**](fms-getfilesel.md) , которая получает сведения о выделенном фрагменте.</span><span class="sxs-lookup"><span data-stu-id="62e40-111">The address of an [**FMS\_GETFILESEL**](fms-getfilesel.md) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62e40-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62e40-112">Return value</span></span>

<span data-ttu-id="62e40-113">Возвращает отсчитываемый от нуля индекс выбранного файла, который был получен.</span><span class="sxs-lookup"><span data-stu-id="62e40-113">Returns the zero-based index of the selected file that was retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="62e40-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="62e40-114">Remarks</span></span>

<span data-ttu-id="62e40-115">Только расширения, поддерживающие длинные имена файлов (например, сетевые расширения), должны использовать это сообщение.</span><span class="sxs-lookup"><span data-stu-id="62e40-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

<span data-ttu-id="62e40-116">Расширение может использовать сообщение [**FM \_ жетселкаунтлфн**](fm-getselcountlfn.md) для получения числа выбранных файлов.</span><span class="sxs-lookup"><span data-stu-id="62e40-116">An extension can use the [**FM\_GETSELCOUNTLFN**](fm-getselcountlfn.md) message to retrieve the count of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="62e40-117">Требования</span><span class="sxs-lookup"><span data-stu-id="62e40-117">Requirements</span></span>



| <span data-ttu-id="62e40-118">Требование</span><span class="sxs-lookup"><span data-stu-id="62e40-118">Requirement</span></span> | <span data-ttu-id="62e40-119">Значение</span><span class="sxs-lookup"><span data-stu-id="62e40-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="62e40-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62e40-120">Minimum supported client</span></span><br/> | <span data-ttu-id="62e40-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="62e40-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="62e40-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62e40-122">Minimum supported server</span></span><br/> | <span data-ttu-id="62e40-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="62e40-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="62e40-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="62e40-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="62e40-125"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="62e40-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62e40-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62e40-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62e40-127">**фмекстенсионпрок**</span><span class="sxs-lookup"><span data-stu-id="62e40-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="62e40-128">**FM \_ жетфилесел**</span><span class="sxs-lookup"><span data-stu-id="62e40-128">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="62e40-129">**FM \_ жетселкаунт**</span><span class="sxs-lookup"><span data-stu-id="62e40-129">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 




