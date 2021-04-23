---
title: Сообщение EM_GETTOUCHOPTIONS (RichEdit. h)
description: Извлекает параметры касания, связанные с элементом управления Rich Edit.
ms.assetid: 1D367818-5625-4A5A-A7A1-330FED516990
keywords:
- Элементы управления Windows для EM_GETTOUCHOPTIONS сообщений
topic_type:
- apiref
api_name:
- EM_GETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812d37de1972c6da205944d9913dc3fa046c205d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071863"
---
# <a name="em_gettouchoptions-message"></a><span data-ttu-id="cce61-104">\_Сообщение ЖЕТТАУЧОПТИОНС EM</span><span class="sxs-lookup"><span data-stu-id="cce61-104">EM\_GETTOUCHOPTIONS message</span></span>

<span data-ttu-id="cce61-105">Извлекает параметры касания, связанные с элементом управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="cce61-105">Retrieves the touch options that are associated with a rich edit control.</span></span>


```C++
#define EM_GETTOUCHOPTIONS       (WM_USER + 310)
```



## <a name="parameters"></a><span data-ttu-id="cce61-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cce61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cce61-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cce61-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cce61-108">Параметры сенсорного ввода для извлечения.</span><span class="sxs-lookup"><span data-stu-id="cce61-108">The touch options to retrieve.</span></span> <span data-ttu-id="cce61-109">Может быть одним из указанных далее.</span><span class="sxs-lookup"><span data-stu-id="cce61-109">It can be one of the following values.</span></span>



| <span data-ttu-id="cce61-110">Значение</span><span class="sxs-lookup"><span data-stu-id="cce61-110">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="cce61-111">Значение</span><span class="sxs-lookup"><span data-stu-id="cce61-111">Meaning</span></span>                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <span data-ttu-id="cce61-112"><dt>**RTO \_ шовхандлес**</dt></span><span class="sxs-lookup"><span data-stu-id="cce61-112"><dt>**RTO\_SHOWHANDLES**</dt></span></span> </dl>          | <span data-ttu-id="cce61-113">Получает значение, указывающее, видимы ли сенсоры касания.</span><span class="sxs-lookup"><span data-stu-id="cce61-113">Retrieves whether the touch grippers are visible.</span></span><br/> |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <span data-ttu-id="cce61-114"><dt>**RTO \_ дисаблехандлес**</dt></span><span class="sxs-lookup"><span data-stu-id="cce61-114"><dt>**RTO\_DISABLEHANDLES**</dt></span></span> </dl> | <span data-ttu-id="cce61-115">Получение этого флага не реализовано.</span><span class="sxs-lookup"><span data-stu-id="cce61-115">Retrieving this flag is not implemented.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="cce61-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cce61-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cce61-117">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="cce61-117">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cce61-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cce61-118">Return value</span></span>

<span data-ttu-id="cce61-119">Возвращает значение параметра, заданного параметром *wParam* .</span><span class="sxs-lookup"><span data-stu-id="cce61-119">Returns the value of the option specified by the *wParam* parameter.</span></span> <span data-ttu-id="cce61-120">Оно не равно нулю, если *wParam* имеет значение **RTO \_ шовхандлес** , а захваты сенсорного ввода видимы; ноль, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="cce61-120">It is nonzero if *wParam* is **RTO\_SHOWHANDLES** and the touch grippers are visible; zero, otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="cce61-121">Требования</span><span class="sxs-lookup"><span data-stu-id="cce61-121">Requirements</span></span>



| <span data-ttu-id="cce61-122">Требование</span><span class="sxs-lookup"><span data-stu-id="cce61-122">Requirement</span></span> | <span data-ttu-id="cce61-123">Значение</span><span class="sxs-lookup"><span data-stu-id="cce61-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cce61-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cce61-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cce61-125">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cce61-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cce61-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cce61-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cce61-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cce61-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cce61-128">Header</span><span class="sxs-lookup"><span data-stu-id="cce61-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cce61-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cce61-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cce61-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cce61-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cce61-131">**EM \_ сеттаучоптионс**</span><span class="sxs-lookup"><span data-stu-id="cce61-131">**EM\_SETTOUCHOPTIONS**</span></span>](em-settouchoptions.md)
</dt> </dl>

 

 





