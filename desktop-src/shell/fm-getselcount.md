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
ms.openlocfilehash: 727e098a98ecfe4a4349ebcf9c6f931a8579b70d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842375"
---
# <a name="fm_getselcount-message"></a><span data-ttu-id="733c4-103">\_Сообщение FM жетселкаунт</span><span class="sxs-lookup"><span data-stu-id="733c4-103">FM\_GETSELCOUNT message</span></span>

<span data-ttu-id="733c4-104">Отправляется расширением диспетчера файлов для получения числа выбранных файлов в активном окне диспетчера файлов (в окне каталога или в окне результатов поиска).</span><span class="sxs-lookup"><span data-stu-id="733c4-104">Sent by a File Manager extension to retrieve a count of the selected files in the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="733c4-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="733c4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="733c4-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="733c4-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="733c4-107">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="733c4-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="733c4-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="733c4-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="733c4-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="733c4-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="733c4-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="733c4-110">Return value</span></span>

<span data-ttu-id="733c4-111">Возвращает число выбранных файлов.</span><span class="sxs-lookup"><span data-stu-id="733c4-111">Returns the number of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="733c4-112">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="733c4-112">Requirements</span></span>



| <span data-ttu-id="733c4-113">Требование</span><span class="sxs-lookup"><span data-stu-id="733c4-113">Requirement</span></span> | <span data-ttu-id="733c4-114">Значение</span><span class="sxs-lookup"><span data-stu-id="733c4-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="733c4-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="733c4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="733c4-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="733c4-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="733c4-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="733c4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="733c4-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="733c4-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="733c4-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="733c4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="733c4-120"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="733c4-120"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="733c4-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="733c4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="733c4-122">**FM \_ жетфилесел**</span><span class="sxs-lookup"><span data-stu-id="733c4-122">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="733c4-123">**FM \_ жетфилеселлфн**</span><span class="sxs-lookup"><span data-stu-id="733c4-123">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="733c4-124">**FM \_ жетселкаунтлфн**</span><span class="sxs-lookup"><span data-stu-id="733c4-124">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




