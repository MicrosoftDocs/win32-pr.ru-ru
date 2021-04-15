---
title: Структура МЕНУХЕЛПИД
description: 'Содержит окончательные данные, записанные в \_ ресурс меню RT для меню или подменю, если элемент Resinfo: структуры попупменуитем имеет значение МФР \_ Popup.'
ms.assetid: f17fdaaa-b37c-4902-bad4-a1181ffee9f9
keywords:
- Меню структуры МЕНУХЕЛПИД и другие ресурсы
topic_type:
- apiref
api_name:
- MENUHELPID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b90b5a4745433c92a859a168611aa1c14f1fa45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661979"
---
# <a name="menuhelpid-structure"></a><span data-ttu-id="80bc7-104">Структура МЕНУХЕЛПИД</span><span class="sxs-lookup"><span data-stu-id="80bc7-104">MENUHELPID structure</span></span>

<span data-ttu-id="80bc7-105">Содержит окончательные данные, записанные в ресурс [**\_ меню RT**](/windows/desktop/menurc/resource-types) для меню или подменю, если элемент **Resinfo:** структуры [**попупменуитем**](popupmenuitem.md) имеет значение **МФР \_ Popup**.</span><span class="sxs-lookup"><span data-stu-id="80bc7-105">Contains the final data written to the [**RT\_MENU**](/windows/desktop/menurc/resource-types) resource for a menu or submenu if the **resInfo** member of the [**POPUPMENUITEM**](popupmenuitem.md) structure is set to **MFR\_POPUP**.</span></span> <span data-ttu-id="80bc7-106">Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="80bc7-106">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="80bc7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80bc7-107">Syntax</span></span>


```C++
typedef struct {
  DWORD helpID;
} MENUHELPID;
```



## <a name="members"></a><span data-ttu-id="80bc7-108">Члены</span><span class="sxs-lookup"><span data-stu-id="80bc7-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="80bc7-109">**Идентификатор справки**</span><span class="sxs-lookup"><span data-stu-id="80bc7-109">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="80bc7-110">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="80bc7-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="80bc7-111">Идентификатор, используемый для идентификации меню во время [**обработки \_ справки WM**](/windows/desktop/shell/wm-help) .</span><span class="sxs-lookup"><span data-stu-id="80bc7-111">The identifier used to identify the menu during [**WM\_HELP**](/windows/desktop/shell/wm-help) processing.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80bc7-112">Требования</span><span class="sxs-lookup"><span data-stu-id="80bc7-112">Requirements</span></span>



| <span data-ttu-id="80bc7-113">Требование</span><span class="sxs-lookup"><span data-stu-id="80bc7-113">Requirement</span></span> | <span data-ttu-id="80bc7-114">Значение</span><span class="sxs-lookup"><span data-stu-id="80bc7-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="80bc7-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80bc7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="80bc7-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="80bc7-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="80bc7-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80bc7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="80bc7-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="80bc7-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="80bc7-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80bc7-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="80bc7-120">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="80bc7-120">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="80bc7-121">**менухеадер**</span><span class="sxs-lookup"><span data-stu-id="80bc7-121">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="80bc7-122">**попупменуитем**</span><span class="sxs-lookup"><span data-stu-id="80bc7-122">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="80bc7-123">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="80bc7-123">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="80bc7-124">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="80bc7-124">Resources</span></span>](resources.md)
</dt> </dl>

 

