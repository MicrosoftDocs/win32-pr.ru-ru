---
description: Отправляется расширением диспетчера файлов для получения числа выбранных файлов в активном окне диспетчера файлов (в окне каталога или в окне результатов поиска).
title: Сообщение FM_GETSELCOUNT (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNT
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0d43bf37-863c-45cc-94ea-5b2aedba5353
ms.openlocfilehash: aac7d08de3785bb02c31dabc1ef7a25fea0d5b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997218"
---
# <a name="fm_getselcount-message"></a><span data-ttu-id="da24b-103">\_Сообщение FM жетселкаунт</span><span class="sxs-lookup"><span data-stu-id="da24b-103">FM\_GETSELCOUNT message</span></span>

<span data-ttu-id="da24b-104">Отправляется расширением диспетчера файлов для получения числа выбранных файлов в активном окне диспетчера файлов (в окне каталога или в окне результатов поиска).</span><span class="sxs-lookup"><span data-stu-id="da24b-104">Sent by a File Manager extension to retrieve a count of the selected files in the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="da24b-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="da24b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da24b-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da24b-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="da24b-107">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="da24b-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="da24b-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da24b-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="da24b-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="da24b-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da24b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da24b-110">Return value</span></span>

<span data-ttu-id="da24b-111">Возвращает число выбранных файлов.</span><span class="sxs-lookup"><span data-stu-id="da24b-111">Returns the number of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="da24b-112">Требования</span><span class="sxs-lookup"><span data-stu-id="da24b-112">Requirements</span></span>



| <span data-ttu-id="da24b-113">Требование</span><span class="sxs-lookup"><span data-stu-id="da24b-113">Requirement</span></span> | <span data-ttu-id="da24b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="da24b-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="da24b-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="da24b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="da24b-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="da24b-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="da24b-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="da24b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="da24b-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="da24b-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="da24b-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="da24b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="da24b-120"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="da24b-120"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da24b-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da24b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da24b-122">**FM \_ жетфилесел**</span><span class="sxs-lookup"><span data-stu-id="da24b-122">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="da24b-123">**FM \_ жетфилеселлфн**</span><span class="sxs-lookup"><span data-stu-id="da24b-123">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="da24b-124">**FM \_ жетселкаунтлфн**</span><span class="sxs-lookup"><span data-stu-id="da24b-124">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




