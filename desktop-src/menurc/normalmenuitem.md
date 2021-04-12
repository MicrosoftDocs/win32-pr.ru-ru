---
title: Структура НОРМАЛМЕНУИТЕМ
description: Содержит сведения о каждом элементе в ресурсе меню, который не открывает меню или подменю. Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.
ms.assetid: c1b84264-2d7f-4bc3-8e74-7b921a0bfe30
keywords:
- Меню структуры НОРМАЛМЕНУИТЕМ и другие ресурсы
topic_type:
- apiref
api_name:
- NORMALMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c90efe624346e30483c42f6f8ff51cd6d3550922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340515"
---
# <a name="normalmenuitem-structure"></a><span data-ttu-id="8b946-105">Структура НОРМАЛМЕНУИТЕМ</span><span class="sxs-lookup"><span data-stu-id="8b946-105">NORMALMENUITEM structure</span></span>

<span data-ttu-id="8b946-106">Содержит сведения о каждом элементе в ресурсе меню, который не открывает меню или подменю.</span><span class="sxs-lookup"><span data-stu-id="8b946-106">Contains information about each item in a menu resource that does not open a menu or a submenu.</span></span> <span data-ttu-id="8b946-107">Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="8b946-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b946-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b946-108">Syntax</span></span>


```C++
typedef struct {
  WORD    resInfo;
  szOrOrd menuText;
} NORMALMENUITEM;
```



## <a name="members"></a><span data-ttu-id="8b946-109">Члены</span><span class="sxs-lookup"><span data-stu-id="8b946-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="8b946-110">**Resinfo:**</span><span class="sxs-lookup"><span data-stu-id="8b946-110">**resInfo**</span></span>
</dt> <dd>

<span data-ttu-id="8b946-111">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="8b946-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="8b946-112">Тип пункта меню.</span><span class="sxs-lookup"><span data-stu-id="8b946-112">The type of menu item.</span></span> <span data-ttu-id="8b946-113">Этот элемент может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="8b946-113">This member can be one of the following values.</span></span>



| <span data-ttu-id="8b946-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8b946-114">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="8b946-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8b946-115">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <span data-ttu-id="8b946-116"><dt>**МФР \_ КОНЕЦ**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="8b946-116"><dt>**MFR\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="8b946-117">Элемент меню является последним в этом подменю или ресурсе меню; Этот флаг используется системой для внутренних целей.</span><span class="sxs-lookup"><span data-stu-id="8b946-117">The menu item is the last in this submenu or menu resource; this flag is used internally by the system.</span></span><br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <span data-ttu-id="8b946-118"><dt>**МФР \_ Всплывающее окно**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="8b946-118"><dt>**MFR\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="8b946-119">Элемент меню открывает меню или подменю; Этот флаг используется системой для внутренних целей.</span><span class="sxs-lookup"><span data-stu-id="8b946-119">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span> <br/>                    |



 

</dd> <dt>

<span data-ttu-id="8b946-120">**менутекст**</span><span class="sxs-lookup"><span data-stu-id="8b946-120">**menuText**</span></span>
</dt> <dd>

<span data-ttu-id="8b946-121">Тип: **сзорорд**</span><span class="sxs-lookup"><span data-stu-id="8b946-121">Type: **szOrOrd**</span></span>

</dd> <dd>

<span data-ttu-id="8b946-122">Строка в Юникоде, заканчивающаяся нулем и содержащая текст для данного элемента меню.</span><span class="sxs-lookup"><span data-stu-id="8b946-122">A null-terminated Unicode string that contains the text for this menu item.</span></span> <span data-ttu-id="8b946-123">Фиксированного ограничения на размер этой строки не существует.</span><span class="sxs-lookup"><span data-stu-id="8b946-123">There is no fixed limit on the size of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b946-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b946-124">Remarks</span></span>

<span data-ttu-id="8b946-125">Существует одна структура **нормалменуитем** для каждого пункта меню, которая не открывает меню или подменю.</span><span class="sxs-lookup"><span data-stu-id="8b946-125">There is one **NORMALMENUITEM** structure for each menu item that does not open a menu or a submenu.</span></span> <span data-ttu-id="8b946-126">Укажите последний пункт меню в меню, установив для элемента **Resinfo:** значение **МФР \_ End**.</span><span class="sxs-lookup"><span data-stu-id="8b946-126">Indicate the last menu item on a menu by setting the **resInfo** member to **MFR\_END**.</span></span>

<span data-ttu-id="8b946-127">Разделитель меню — это специальный тип элемента меню, который неактивен, но отображается в виде разделительной линии между двумя активными элементами меню.</span><span class="sxs-lookup"><span data-stu-id="8b946-127">A menu separator is a special type of menu item that is inactive but appears as a dividing bar between two active menu items.</span></span> <span data-ttu-id="8b946-128">Чтобы указать разделитель меню, оставьте пустой элемент **менутекст** .</span><span class="sxs-lookup"><span data-stu-id="8b946-128">Indicate a menu separator by leaving the **menuText** member empty.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b946-129">Требования</span><span class="sxs-lookup"><span data-stu-id="8b946-129">Requirements</span></span>



| <span data-ttu-id="8b946-130">Требование</span><span class="sxs-lookup"><span data-stu-id="8b946-130">Requirement</span></span> | <span data-ttu-id="8b946-131">Значение</span><span class="sxs-lookup"><span data-stu-id="8b946-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8b946-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b946-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8b946-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8b946-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8b946-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b946-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8b946-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8b946-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8b946-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b946-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="8b946-137">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="8b946-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8b946-138">**менухеадер**</span><span class="sxs-lookup"><span data-stu-id="8b946-138">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="8b946-139">**ОБЪЕКТАМИ MENUITEMINFO**</span><span class="sxs-lookup"><span data-stu-id="8b946-139">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[<span data-ttu-id="8b946-140">**попупменуитем**</span><span class="sxs-lookup"><span data-stu-id="8b946-140">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="8b946-141">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="8b946-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8b946-142">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="8b946-142">Resources</span></span>](resources.md)
</dt> </dl>

 

 





