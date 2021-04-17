---
title: Структура MENUEX_TEMPLATE_HEADER
description: Определяет заголовок для расширенного шаблона меню. Это определение структуры предназначено только для объяснения; он отсутствует в любом стандартном файле заголовка.
ms.assetid: df763349-7127-482e-8613-74e68addde5d
keywords:
- Меню структуры MENUEX_TEMPLATE_HEADER и другие ресурсы
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa255ccdbe76c3959d9c730bcaa52ec07428742
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710463"
---
# <a name="menuex_template_header-structure"></a><span data-ttu-id="d013a-105">\_ \_ Структура заголовка шаблона менуекс</span><span class="sxs-lookup"><span data-stu-id="d013a-105">MENUEX\_TEMPLATE\_HEADER structure</span></span>

<span data-ttu-id="d013a-106">Определяет заголовок для расширенного шаблона меню.</span><span class="sxs-lookup"><span data-stu-id="d013a-106">Defines the header for an extended menu template.</span></span> <span data-ttu-id="d013a-107">Это определение структуры предназначено только для объяснения; он отсутствует в любом стандартном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="d013a-107">This structure definition is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d013a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d013a-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wVersion;
  WORD  wOffset;
  DWORD dwHelpId;
} MENUEX_TEMPLATE_HEADER;
```



## <a name="members"></a><span data-ttu-id="d013a-109">Члены</span><span class="sxs-lookup"><span data-stu-id="d013a-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="d013a-110">**вверсион**</span><span class="sxs-lookup"><span data-stu-id="d013a-110">**wVersion**</span></span>
</dt> <dd>

<span data-ttu-id="d013a-111">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="d013a-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="d013a-112">Номер версии шаблона.</span><span class="sxs-lookup"><span data-stu-id="d013a-112">The template version number.</span></span> <span data-ttu-id="d013a-113">Для расширенных шаблонов меню этот элемент должен быть равен 1.</span><span class="sxs-lookup"><span data-stu-id="d013a-113">This member must be 1 for extended menu templates.</span></span>

</dd> <dt>

<span data-ttu-id="d013a-114">**воффсет**</span><span class="sxs-lookup"><span data-stu-id="d013a-114">**wOffset**</span></span>
</dt> <dd>

<span data-ttu-id="d013a-115">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="d013a-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="d013a-116">Смещение первой структуры [**\_ \_ элемента шаблона менуекс**](menuex-template-item.md) относительно конца этого элемента структуры.</span><span class="sxs-lookup"><span data-stu-id="d013a-116">The offset to the first [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) structure, relative to the end of this structure member.</span></span> <span data-ttu-id="d013a-117">Если первое определение элемента следует сразу за элементом **двхелпид** , этот элемент должен иметь значение 4.</span><span class="sxs-lookup"><span data-stu-id="d013a-117">If the first item definition immediately follows the **dwHelpId** member, this member should be 4.</span></span>

</dd> <dt>

<span data-ttu-id="d013a-118">**двхелпид**</span><span class="sxs-lookup"><span data-stu-id="d013a-118">**dwHelpId**</span></span>
</dt> <dd>

<span data-ttu-id="d013a-119">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d013a-119">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d013a-120">Идентификатор справки строки меню.</span><span class="sxs-lookup"><span data-stu-id="d013a-120">The help identifier of menu bar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d013a-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d013a-121">Remarks</span></span>

<span data-ttu-id="d013a-122">Расширенный шаблон меню состоит из структуры **\_ \_ заголовка шаблона менуекс** , за которой следуют одна или несколько структурных [**\_ \_ элементов шаблона менуекс**](menuex-template-item.md) .</span><span class="sxs-lookup"><span data-stu-id="d013a-122">An extended menu template consists of a **MENUEX\_TEMPLATE\_HEADER** structure followed by one or more contiguous [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) structures.</span></span> <span data-ttu-id="d013a-123">Структуры **\_ \_ элементов шаблона менуекс** , которые имеют переменную длину, вычисляются по границам **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="d013a-123">The **MENUEX\_TEMPLATE\_ITEM** structures, which are variable in length, are aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="d013a-124">Чтобы создать меню из расширенного шаблона меню в памяти, используйте функцию [**лоадменуиндирект**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .</span><span class="sxs-lookup"><span data-stu-id="d013a-124">To create a menu from an extended menu template in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d013a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d013a-125">Requirements</span></span>



| <span data-ttu-id="d013a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d013a-126">Requirement</span></span> | <span data-ttu-id="d013a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d013a-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d013a-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d013a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d013a-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d013a-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d013a-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d013a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d013a-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d013a-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d013a-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d013a-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="d013a-133">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="d013a-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d013a-134">**лоадменуиндирект**</span><span class="sxs-lookup"><span data-stu-id="d013a-134">**LoadMenuIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[<span data-ttu-id="d013a-135">**\_элемент шаблона \_ менуекс**</span><span class="sxs-lookup"><span data-stu-id="d013a-135">**MENUEX\_TEMPLATE\_ITEM**</span></span>](menuex-template-item.md)
</dt> <dt>

<span data-ttu-id="d013a-136">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="d013a-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d013a-137">Меню</span><span class="sxs-lookup"><span data-stu-id="d013a-137">Menus</span></span>](menus.md)
</dt> </dl>

 

 





