---
title: Структура ПРОПШИТКФГ
description: Используется для хранения данных конфигурации страницы свойств.
ms.assetid: d3bde744-9d85-4506-894f-f8be3463721f
ms.tgt_platform: multiple
keywords:
- Active Directory структуры ПРОПШИТКФГ
- Active Directory указателя структуры ППРОПШИТКФГ
topic_type:
- apiref
api_name:
- PROPSHEETCFG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33f4a1186cc756435cc49ed7c81592385faaee60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071660"
---
# <a name="propsheetcfg-structure"></a><span data-ttu-id="65240-105">Структура ПРОПШИТКФГ</span><span class="sxs-lookup"><span data-stu-id="65240-105">PROPSHEETCFG structure</span></span>

<span data-ttu-id="65240-106">Структура **пропшиткфг** используется для хранения данных конфигурации страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="65240-106">The **PROPSHEETCFG** structure is used to contain property sheet configuration data.</span></span> <span data-ttu-id="65240-107">Эта структура содержится в формате буфера [**обмена \_ \_ пропшитконфиг DS кфстр**](cfstr-ds-propsheetconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="65240-107">This structure is contained in the [**CFSTR\_DS\_PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) clipboard format.</span></span>

> [!Note]  
> <span data-ttu-id="65240-108">Эта структура не определена в файле опубликованного заголовка.</span><span class="sxs-lookup"><span data-stu-id="65240-108">This structure is not defined in a published header file.</span></span> <span data-ttu-id="65240-109">Чтобы использовать эту структуру, необходимо определить ее самостоятельно в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="65240-109">To use this structure, you must define it yourself in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="65240-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65240-110">Syntax</span></span>


```C++
typedef struct {
  LONG_PTR lNotifyHandle;
  HWND     hwndParentSheet;
  HWND     hwndHidden;
  WPARAM   wParamSheetClose;
} PROPSHEETCFG, *PPROPSHEETCFG;
```



## <a name="members"></a><span data-ttu-id="65240-111">Члены</span><span class="sxs-lookup"><span data-stu-id="65240-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="65240-112">**лнотифихандле**</span><span class="sxs-lookup"><span data-stu-id="65240-112">**lNotifyHandle**</span></span>
</dt> <dd>

<span data-ttu-id="65240-113">Содержит маркер уведомления.</span><span class="sxs-lookup"><span data-stu-id="65240-113">Contains the notification handle.</span></span> <span data-ttu-id="65240-114">Это идентично маркеру, переданному для параметра *Handle* в методе [**IExtendPropertySheet2:: креатепропертипажес**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="65240-114">This is identical to the handle passed for the *handle* parameter in the [**IExtendPropertySheet2::CreatePropertyPages**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)) method.</span></span>

</dd> <dt>

<span data-ttu-id="65240-115">**хвндпарентшит**</span><span class="sxs-lookup"><span data-stu-id="65240-115">**hwndParentSheet**</span></span>
</dt> <dd>

<span data-ttu-id="65240-116">Содержит маркер окна родительской страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="65240-116">Contains the window handle of the parent property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="65240-117">**хвндхидден**</span><span class="sxs-lookup"><span data-stu-id="65240-117">**hwndHidden**</span></span>
</dt> <dd>

<span data-ttu-id="65240-118">Содержит маркер скрытого окна.</span><span class="sxs-lookup"><span data-stu-id="65240-118">Contains the handle of the hidden window.</span></span>

</dd> <dt>

<span data-ttu-id="65240-119">**впарамшитклосе**</span><span class="sxs-lookup"><span data-stu-id="65240-119">**wParamSheetClose**</span></span>
</dt> <dd>

<span data-ttu-id="65240-120">Содержит определяемое приложением 32-разрядное значение.</span><span class="sxs-lookup"><span data-stu-id="65240-120">Contains an application-defined 32-bit value.</span></span> <span data-ttu-id="65240-121">Это значение передается обратно в приложение в параметре *wParam* сообщения [**\_ \_ \_ \_ о закрытии страницы WM DSA**](wm-dsa-sheet-close-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="65240-121">This value is passed back to the application in the *wParam* of the [**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**](wm-dsa-sheet-close-notify.md) message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65240-122">Требования</span><span class="sxs-lookup"><span data-stu-id="65240-122">Requirements</span></span>



| <span data-ttu-id="65240-123">Требование</span><span class="sxs-lookup"><span data-stu-id="65240-123">Requirement</span></span> | <span data-ttu-id="65240-124">Значение</span><span class="sxs-lookup"><span data-stu-id="65240-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="65240-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65240-125">Minimum supported client</span></span><br/> | <span data-ttu-id="65240-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65240-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="65240-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65240-127">Minimum supported server</span></span><br/> | <span data-ttu-id="65240-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65240-128">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65240-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65240-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65240-130">**\_ПРОПШИТКОНФИГ кфстр DS \_**</span><span class="sxs-lookup"><span data-stu-id="65240-130">**CFSTR\_DS\_PROPSHEETCONFIG**</span></span>](cfstr-ds-propsheetconfig.md)
</dt> <dt>

[<span data-ttu-id="65240-131">**\_ \_ \_ уведомление о закрытии листа WM DSA \_**</span><span class="sxs-lookup"><span data-stu-id="65240-131">**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**</span></span>](wm-dsa-sheet-close-notify.md)
</dt> </dl>

 

