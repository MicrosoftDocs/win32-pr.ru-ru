---
description: Содержит сведения, используемые диспетчером файлов для добавления пользовательского меню, предоставляемого БИБЛИОТЕКой расширения диспетчера файлов. Структура также предоставляет разностное значение, которое библиотека DLL расширения может использовать для работы с пользовательским меню после того, как диспетчер файлов загрузил меню.
title: Структура FMS_LOAD (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0e76bcc5-76c2-4ec0-8ddb-4042cb5ffa7d
ms.openlocfilehash: efd1777704c775db84c7dabf54b9e06c81535fb4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842195"
---
# <a name="fms_load-structure"></a><span data-ttu-id="66391-104">\_Загрузка структуры FMS</span><span class="sxs-lookup"><span data-stu-id="66391-104">FMS\_LOAD structure</span></span>

<span data-ttu-id="66391-105">Содержит сведения, используемые диспетчером файлов для добавления пользовательского меню, предоставляемого БИБЛИОТЕКой расширения диспетчера файлов.</span><span class="sxs-lookup"><span data-stu-id="66391-105">Contains information that File Manager uses to add a custom menu provided by a File Manager extension DLL.</span></span> <span data-ttu-id="66391-106">Структура также предоставляет разностное значение, которое библиотека DLL расширения может использовать для работы с пользовательским меню после того, как диспетчер файлов загрузил меню.</span><span class="sxs-lookup"><span data-stu-id="66391-106">The structure also provides a delta value that the extension DLL can use to manipulate the custom menu after File Manager has loaded the menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="66391-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66391-107">Syntax</span></span>


```C++
typedef struct _FMS_LOAD {
  DWORD dwSize;
  TCHAR szMenuName[MENU_TEXT_LEN];
  HMENU hMenu;
  UINT  wMenuDelta;
} FMS_LOAD;
```



## <a name="members"></a><span data-ttu-id="66391-108">Члены</span><span class="sxs-lookup"><span data-stu-id="66391-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="66391-109">**двсизе**</span><span class="sxs-lookup"><span data-stu-id="66391-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="66391-110">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="66391-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="66391-111">Длина структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="66391-111">The length, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="66391-112">**сзменунаме**</span><span class="sxs-lookup"><span data-stu-id="66391-112">**szMenuName**</span></span>
</dt> <dd>

<span data-ttu-id="66391-113">Тип: **\[ меню TCHAR \_ текст \_ длина \]**</span><span class="sxs-lookup"><span data-stu-id="66391-113">Type: **TCHAR\[MENU\_TEXT\_LEN\]**</span></span>

</dd> <dd>

<span data-ttu-id="66391-114">Имя, заканчивающееся нулем, для пункта меню, который отображается в строке меню диспетчера файлов.</span><span class="sxs-lookup"><span data-stu-id="66391-114">A null-terminated name for a menu item that appears on the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="66391-115">**hMenu**</span><span class="sxs-lookup"><span data-stu-id="66391-115">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="66391-116">Тип: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="66391-116">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="66391-117">Идентификатор всплывающего меню, добавленного в строку меню в диспетчере файлов.</span><span class="sxs-lookup"><span data-stu-id="66391-117">The identifier of the pop-up menu added to the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="66391-118">**вменуделта**</span><span class="sxs-lookup"><span data-stu-id="66391-118">**wMenuDelta**</span></span>
</dt> <dd>

<span data-ttu-id="66391-119">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="66391-119">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="66391-120">Разностное значение пункта меню.</span><span class="sxs-lookup"><span data-stu-id="66391-120">The menu item delta value.</span></span> <span data-ttu-id="66391-121">Чтобы избежать конфликтов с собственными элементами меню, диспетчер файлов перестраивает идентификаторы пунктов меню во всплывающем меню, определенном элементом **HMENU** , путем добавления этого разностного значения к каждому идентификатору.</span><span class="sxs-lookup"><span data-stu-id="66391-121">To avoid conflicts with its own menu items, File Manager renumbers the menu item identifiers in the pop-up menu identified by the **hMenu** member by adding this delta value to each identifier.</span></span> <span data-ttu-id="66391-122">Библиотека DLL расширения, которая должна изменить пункт меню, должна обозначать элемент путем добавления разностного значения к идентификатору пункта меню.</span><span class="sxs-lookup"><span data-stu-id="66391-122">An extension DLL that must modify a menu item must identify the item by adding the delta value to the menu item's identifier.</span></span> <span data-ttu-id="66391-123">Значение этого элемента может изменяться от сеанса к сеансу.</span><span class="sxs-lookup"><span data-stu-id="66391-123">The value of this member can vary from session to session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66391-124">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="66391-124">Requirements</span></span>



| <span data-ttu-id="66391-125">Требование</span><span class="sxs-lookup"><span data-stu-id="66391-125">Requirement</span></span> | <span data-ttu-id="66391-126">Значение</span><span class="sxs-lookup"><span data-stu-id="66391-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66391-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66391-127">Minimum supported client</span></span><br/> | <span data-ttu-id="66391-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="66391-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="66391-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66391-129">Minimum supported server</span></span><br/> | <span data-ttu-id="66391-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="66391-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="66391-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="66391-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="66391-132"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="66391-132"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66391-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66391-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66391-134">**фмекстенсионпрок**</span><span class="sxs-lookup"><span data-stu-id="66391-134">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




