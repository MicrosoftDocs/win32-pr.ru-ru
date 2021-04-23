---
title: Структура МЕНУХЕАДЕР
description: Содержит сведения о версии для ресурса меню. Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.
ms.assetid: 1e34b0b6-18ff-4cb6-901e-a2aabad0df74
keywords:
- Меню структуры МЕНУХЕАДЕР и другие ресурсы
topic_type:
- apiref
api_name:
- MENUHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eacc67d34d04502aa17eeaca78240a0a3e0e219d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654429"
---
# <a name="menuheader-structure"></a><span data-ttu-id="582cb-105">Структура МЕНУХЕАДЕР</span><span class="sxs-lookup"><span data-stu-id="582cb-105">MENUHEADER structure</span></span>

<span data-ttu-id="582cb-106">Содержит сведения о версии для ресурса меню.</span><span class="sxs-lookup"><span data-stu-id="582cb-106">Contains version information for the menu resource.</span></span> <span data-ttu-id="582cb-107">Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="582cb-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="582cb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="582cb-108">Syntax</span></span>


```C++
typedef struct {
  WORD wVersion;
  WORD cbHeaderSize;
} MENUHEADER;
```



## <a name="members"></a><span data-ttu-id="582cb-109">Члены</span><span class="sxs-lookup"><span data-stu-id="582cb-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="582cb-110">**вверсион**</span><span class="sxs-lookup"><span data-stu-id="582cb-110">**wVersion**</span></span>
</dt> <dd>

<span data-ttu-id="582cb-111">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="582cb-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="582cb-112">Номер версии шаблона меню.</span><span class="sxs-lookup"><span data-stu-id="582cb-112">The version number of the menu template.</span></span> <span data-ttu-id="582cb-113">Этот элемент должен быть равен нулю, чтобы указать, что это [**\_ меню RT**](/windows/desktop/menurc/resource-types) , созданное с помощью стандартного шаблона меню.</span><span class="sxs-lookup"><span data-stu-id="582cb-113">This member must be equal to zero to indicate that this is an [**RT\_MENU**](/windows/desktop/menurc/resource-types) created with a standard menu template.</span></span>

</dd> <dt>

<span data-ttu-id="582cb-114">**кбхеадерсизе**</span><span class="sxs-lookup"><span data-stu-id="582cb-114">**cbHeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="582cb-115">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="582cb-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="582cb-116">Размер заголовка шаблона меню.</span><span class="sxs-lookup"><span data-stu-id="582cb-116">The size of the menu template header.</span></span> <span data-ttu-id="582cb-117">Это значение равно нулю для меню, создаваемых с помощью стандартного шаблона меню.</span><span class="sxs-lookup"><span data-stu-id="582cb-117">This value is zero for menus you create with a standard menu template.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="582cb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="582cb-118">Requirements</span></span>



| <span data-ttu-id="582cb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="582cb-119">Requirement</span></span> | <span data-ttu-id="582cb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="582cb-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="582cb-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="582cb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="582cb-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="582cb-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="582cb-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="582cb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="582cb-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="582cb-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="582cb-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="582cb-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="582cb-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="582cb-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="582cb-127">**\_заголовок шаблона \_ менуекс**</span><span class="sxs-lookup"><span data-stu-id="582cb-127">**MENUEX\_TEMPLATE\_HEADER**</span></span>](menuex-template-header.md)
</dt> <dt>

[<span data-ttu-id="582cb-128">**\_элемент шаблона \_ менуекс**</span><span class="sxs-lookup"><span data-stu-id="582cb-128">**MENUEX\_TEMPLATE\_ITEM**</span></span>](menuex-template-item.md)
</dt> <dt>

[<span data-ttu-id="582cb-129">**менуитемтемплате**</span><span class="sxs-lookup"><span data-stu-id="582cb-129">**MENUITEMTEMPLATE**</span></span>](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)
</dt> <dt>

[<span data-ttu-id="582cb-130">**менуитемтемплатехеадер**</span><span class="sxs-lookup"><span data-stu-id="582cb-130">**MENUITEMTEMPLATEHEADER**</span></span>](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader)
</dt> <dt>

[<span data-ttu-id="582cb-131">**нормалменуитем**</span><span class="sxs-lookup"><span data-stu-id="582cb-131">**NORMALMENUITEM**</span></span>](normalmenuitem.md)
</dt> <dt>

[<span data-ttu-id="582cb-132">**попупменуитем**</span><span class="sxs-lookup"><span data-stu-id="582cb-132">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="582cb-133">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="582cb-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="582cb-134">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="582cb-134">Resources</span></span>](resources.md)
</dt> </dl>

 

