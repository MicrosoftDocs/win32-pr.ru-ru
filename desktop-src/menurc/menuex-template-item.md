---
title: Структура MENUEX_TEMPLATE_ITEM
description: Определяет пункт меню в расширенном шаблоне меню. Это определение структуры предназначено только для объяснения; он отсутствует в любом стандартном файле заголовка.
ms.assetid: f6e2fd0a-16b8-48e3-8597-341085a7adbd
keywords:
- Меню структуры MENUEX_TEMPLATE_ITEM и другие ресурсы
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_ITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca1f73d1174590db5948f54f5c51c91a8c65a8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535084"
---
# <a name="menuex_template_item-structure"></a><span data-ttu-id="e644d-105">\_ \_ Структура элемента шаблона менуекс</span><span class="sxs-lookup"><span data-stu-id="e644d-105">MENUEX\_TEMPLATE\_ITEM structure</span></span>

<span data-ttu-id="e644d-106">Определяет пункт меню в расширенном шаблоне меню.</span><span class="sxs-lookup"><span data-stu-id="e644d-106">Defines a menu item in an extended menu template.</span></span> <span data-ttu-id="e644d-107">Это определение структуры предназначено только для объяснения; он отсутствует в любом стандартном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="e644d-107">This structure definition is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e644d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e644d-108">Syntax</span></span>

```C++
typedef struct {
  DWORD dwType;
  DWORD dwState;
  UINT  uId;
  WORD  wFlags;
  WCHAR szText[1];
} MENUEX_TEMPLATE_ITEM;
```

## <a name="members"></a><span data-ttu-id="e644d-109">Члены</span><span class="sxs-lookup"><span data-stu-id="e644d-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="e644d-110">**двтипе**</span><span class="sxs-lookup"><span data-stu-id="e644d-110">**dwType**</span></span>
</dt> <dd>

<span data-ttu-id="e644d-111">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e644d-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e644d-112">Тип элемента меню.</span><span class="sxs-lookup"><span data-stu-id="e644d-112">The menu item type.</span></span> <span data-ttu-id="e644d-113">Этот элемент может быть сочетанием типа (начиная с MFT) со значениями, перечисленными в структуре [**объектами menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="e644d-113">This member can be a combination of the type (beginning with MFT) values listed with the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e644d-114">**двстате**</span><span class="sxs-lookup"><span data-stu-id="e644d-114">**dwState**</span></span>
</dt> <dd>

<span data-ttu-id="e644d-115">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e644d-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e644d-116">Состояние пункта меню.</span><span class="sxs-lookup"><span data-stu-id="e644d-116">The menu item state.</span></span> <span data-ttu-id="e644d-117">Этот элемент может быть сочетанием значений State (начиная с MFA), указанных в структуре [**объектами menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="e644d-117">This member can be a combination of the state (beginning with MFS) values listed with the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e644d-118">**Такой**</span><span class="sxs-lookup"><span data-stu-id="e644d-118">**uId**</span></span>
</dt> <dd>

<span data-ttu-id="e644d-119">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="e644d-119">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="e644d-120">Идентификатор пункта меню.</span><span class="sxs-lookup"><span data-stu-id="e644d-120">The menu item identifier.</span></span> <span data-ttu-id="e644d-121">Это определяемое приложением значение, идентифицирующее пункт меню.</span><span class="sxs-lookup"><span data-stu-id="e644d-121">This is an application-defined value that identifies the menu item.</span></span> <span data-ttu-id="e644d-122">В ресурсе расширенного меню элементы, открывающие раскрывающиеся меню или подменю, а также элементы команд могут иметь идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="e644d-122">In an extended menu resource, items that open drop-down menus or submenus as well as command items can have identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="e644d-123">**вфлагс**</span><span class="sxs-lookup"><span data-stu-id="e644d-123">**wFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e644d-124">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="e644d-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e644d-125">Указывает, является ли пункт меню последним элементом в строке меню, раскрывающемся меню, подменю или контекстном меню, а также является ли он элементом, открывающим раскрывающееся меню или подменю.</span><span class="sxs-lookup"><span data-stu-id="e644d-125">Specifies whether the menu item is the last item in the menu bar, drop-down menu, submenu, or shortcut menu and whether it is an item that opens a drop-down menu or submenu.</span></span> <span data-ttu-id="e644d-126">Этот элемент может быть равен нулю или нескольким из этих значений.</span><span class="sxs-lookup"><span data-stu-id="e644d-126">This member can be zero or more of these values.</span></span> <span data-ttu-id="e644d-127">Для 32-разрядных приложений этот член является словом; для 16-разрядных приложений это байт.</span><span class="sxs-lookup"><span data-stu-id="e644d-127">For 32-bit applications, this member is a word; for 16-bit applications, it is a byte.</span></span>

<dt>

<span data-ttu-id="e644d-128">0x80</span><span class="sxs-lookup"><span data-stu-id="e644d-128">0x80</span></span>
</dt> <dd>

<span data-ttu-id="e644d-129">Структура определяет последний пункт меню в строке меню, раскрывающемся меню, подменю или контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="e644d-129">The structure defines the last menu item in the menu bar, drop-down menu, submenu, or shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="e644d-130">0x01</span><span class="sxs-lookup"><span data-stu-id="e644d-130">0x01</span></span>
</dt> <dd>

<span data-ttu-id="e644d-131">Структура определяет элемент, открывающий раскрывающееся меню или подменю.</span><span class="sxs-lookup"><span data-stu-id="e644d-131">The structure defines a item that opens a drop-down menu or submenu.</span></span> <span data-ttu-id="e644d-132">Последующие структуры определяют пункты меню в соответствующем раскрывающемся меню или подменю.</span><span class="sxs-lookup"><span data-stu-id="e644d-132">Subsequent structures define menu items in the corresponding drop-down menu or submenu.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e644d-133">**сзтекст**</span><span class="sxs-lookup"><span data-stu-id="e644d-133">**szText**</span></span>
</dt> <dd>

<span data-ttu-id="e644d-134">Тип: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="e644d-134">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="e644d-135">Текст пункта меню.</span><span class="sxs-lookup"><span data-stu-id="e644d-135">The menu item text.</span></span> <span data-ttu-id="e644d-136">Этот элемент является строкой в Юникоде, завершающейся нулем и выравниваемая по границе слова.</span><span class="sxs-lookup"><span data-stu-id="e644d-136">This member is a null-terminated Unicode string, aligned on a word boundary.</span></span> <span data-ttu-id="e644d-137">Размер определения элемента меню зависит от длины этой строки.</span><span class="sxs-lookup"><span data-stu-id="e644d-137">The size of the menu item definition varies depending on the length of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e644d-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e644d-138">Remarks</span></span>

<span data-ttu-id="e644d-139">Расширенный шаблон меню состоит из структуры [**\_ \_ заголовка шаблона менуекс**](menuex-template-header.md) , за которой следуют одна или несколько структурных **\_ \_ элементов шаблона менуекс** .</span><span class="sxs-lookup"><span data-stu-id="e644d-139">An extended menu template consists of a [**MENUEX\_TEMPLATE\_HEADER**](menuex-template-header.md) structure followed by one or more contiguous **MENUEX\_TEMPLATE\_ITEM** structures.</span></span> <span data-ttu-id="e644d-140">Структуры **\_ \_ элементов шаблона менуекс** , которые имеют переменную длину, вычисляются по границам **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e644d-140">The **MENUEX\_TEMPLATE\_ITEM** structures, which are variable in length, are aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="e644d-141">Чтобы создать меню из расширенного шаблона меню в памяти, используйте функцию [**лоадменуиндирект**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .</span><span class="sxs-lookup"><span data-stu-id="e644d-141">To create a menu from an extended menu template in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e644d-142">Требования</span><span class="sxs-lookup"><span data-stu-id="e644d-142">Requirements</span></span>



| <span data-ttu-id="e644d-143">Требование</span><span class="sxs-lookup"><span data-stu-id="e644d-143">Requirement</span></span> | <span data-ttu-id="e644d-144">Значение</span><span class="sxs-lookup"><span data-stu-id="e644d-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e644d-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e644d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e644d-146">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e644d-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e644d-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e644d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e644d-148">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e644d-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e644d-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e644d-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="e644d-150">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="e644d-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e644d-151">**лоадменуиндирект**</span><span class="sxs-lookup"><span data-stu-id="e644d-151">**LoadMenuIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[<span data-ttu-id="e644d-152">**\_заголовок шаблона \_ менуекс**</span><span class="sxs-lookup"><span data-stu-id="e644d-152">**MENUEX\_TEMPLATE\_HEADER**</span></span>](menuex-template-header.md)
</dt> <dt>

[<span data-ttu-id="e644d-153">**ОБЪЕКТАМИ MENUITEMINFO**</span><span class="sxs-lookup"><span data-stu-id="e644d-153">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

<span data-ttu-id="e644d-154">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="e644d-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e644d-155">Меню</span><span class="sxs-lookup"><span data-stu-id="e644d-155">Menus</span></span>](menus.md)
</dt> </dl>

 

 





