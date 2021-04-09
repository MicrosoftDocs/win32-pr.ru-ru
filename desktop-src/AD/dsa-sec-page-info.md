---
title: Структура DSA_SEC_PAGE_INFO
description: Используется с \_ листом WM адспроп на листе \_ \_ CREATE и WM \_ DSA \_ \_ Создание \_ уведомления об уведомлении для определения дополнительной страницы свойств в оснастке консоли MMC Active Directory.
ms.assetid: 422d84dc-6b5e-43bf-ac4f-3b99cb59f9df
ms.tgt_platform: multiple
keywords:
- DSA_SEC_PAGE_INFO структуры Active Directory
- PDSA_SEC_PAGE_INFO Active Directory указателя на структуру
topic_type:
- apiref
api_name:
- DSA_SEC_PAGE_INFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e4c8602a958c50c72942d89657a812d24f64571d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988919"
---
# <a name="dsa_sec_page_info-structure"></a><span data-ttu-id="c6098-105">\_ \_ \_ Структура сведений о странице DSA sec</span><span class="sxs-lookup"><span data-stu-id="c6098-105">DSA\_SEC\_PAGE\_INFO structure</span></span>

<span data-ttu-id="c6098-106">Структура **\_ \_ \_ сведений о странице DSA sec** используется с листом [**WM \_ адспроп \_ листов \_ CREATE**](wm-adsprop-sheet-create.md) и [**WM \_ DSA \_ \_ Создание сообщения \_ уведомления**](wm-dsa-sheet-create-notify.md) для определения дополнительной страницы свойств в оснастке консоли управления Active Directory MMC.</span><span class="sxs-lookup"><span data-stu-id="c6098-106">The **DSA\_SEC\_PAGE\_INFO** structure is used with the [**WM\_ADSPROP\_SHEET\_CREATE**](wm-adsprop-sheet-create.md) and [**WM\_DSA\_SHEET\_CREATE\_NOTIFY**](wm-dsa-sheet-create-notify.md) messages to define a secondary property sheet in an Active Directory MMC snap-in.</span></span>

> [!Note]  
> <span data-ttu-id="c6098-107">Эта структура не определена в файле опубликованного заголовка.</span><span class="sxs-lookup"><span data-stu-id="c6098-107">This structure is not defined in a published header file.</span></span> <span data-ttu-id="c6098-108">Чтобы использовать эту структуру, определите ее в точно указанном формате.</span><span class="sxs-lookup"><span data-stu-id="c6098-108">To use this structure, define it in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c6098-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6098-109">Syntax</span></span>


```C++
typedef struct _DSA_SEC_PAGE_INFO {
  HWND          hwndParentSheet;
  DWORD         offsetTitle;
  DSOBJECTNAMES dsObjectNames;
} DSA_SEC_PAGE_INFO, *PDSA_SEC_PAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="c6098-110">Члены</span><span class="sxs-lookup"><span data-stu-id="c6098-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="c6098-111">**хвндпарентшит**</span><span class="sxs-lookup"><span data-stu-id="c6098-111">**hwndParentSheet**</span></span>
</dt> <dd>

<span data-ttu-id="c6098-112">Содержит маркер окна родителя страницы вторичного свойства.</span><span class="sxs-lookup"><span data-stu-id="c6098-112">Contains the window handle of the parent of the secondary property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="c6098-113">**оффсеттитле**</span><span class="sxs-lookup"><span data-stu-id="c6098-113">**offsetTitle**</span></span>
</dt> <dd>

<span data-ttu-id="c6098-114">Содержит смещение в байтах от начала структуры **\_ \_ \_ сведений о странице DSA sec** до завершающейся нулем строки Юникода, которая содержит заголовок дополнительной страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="c6098-114">Contains the offset, in bytes, from the start of the **DSA\_SEC\_PAGE\_INFO** structure to a NULL-terminated, Unicode string that contains the title of the secondary property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="c6098-115">**дсобжектнамес**</span><span class="sxs-lookup"><span data-stu-id="c6098-115">**dsObjectNames**</span></span>
</dt> <dd>

<span data-ttu-id="c6098-116">Содержит структуру [**дсобжектнамес**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) , определяющую вторичную страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="c6098-116">Contains a [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) structure that defines the secondary property sheet.</span></span> <span data-ttu-id="c6098-117">За раз можно создать только одну вторичную страницу свойств, поэтому структура **дсобжектнамес** может содержать только одну структуру [**дсобжект**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .</span><span class="sxs-lookup"><span data-stu-id="c6098-117">Only one secondary property sheet can be created at a time, so the **DSOBJECTNAMES** structure can only contain one [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c6098-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c6098-118">Requirements</span></span>



| <span data-ttu-id="c6098-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c6098-119">Requirement</span></span> | <span data-ttu-id="c6098-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c6098-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c6098-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c6098-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c6098-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6098-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c6098-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c6098-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c6098-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6098-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6098-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6098-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6098-126">**\_ \_ Создание листа WM \_ адспроп**</span><span class="sxs-lookup"><span data-stu-id="c6098-126">**WM\_ADSPROP\_SHEET\_CREATE**</span></span>](wm-adsprop-sheet-create.md)
</dt> <dt>

[<span data-ttu-id="c6098-127">**\_ \_ \_ уведомление о создании листа WM DSA \_**</span><span class="sxs-lookup"><span data-stu-id="c6098-127">**WM\_DSA\_SHEET\_CREATE\_NOTIFY**</span></span>](wm-dsa-sheet-create-notify.md)
</dt> <dt>

[<span data-ttu-id="c6098-128">**дсобжектнамес**</span><span class="sxs-lookup"><span data-stu-id="c6098-128">**DSOBJECTNAMES**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[<span data-ttu-id="c6098-129">**дсобжект**</span><span class="sxs-lookup"><span data-stu-id="c6098-129">**DSOBJECT**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> </dl>

 

 





