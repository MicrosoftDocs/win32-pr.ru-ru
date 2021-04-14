---
description: Содержит сведения, используемые диспетчером файлов для добавления строки справки для элемента меню или команды панели инструментов.
title: Структура FMS_HELPSTRING (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b3ae7f86-5d58-47fa-87bd-e4e6a3541a93
ms.openlocfilehash: c934409712ae740797eb3b5af0b55c50ff125342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997738"
---
# <a name="fms_helpstring-structure"></a><span data-ttu-id="a04f9-103">\_Структура FMS HELPSTRING</span><span class="sxs-lookup"><span data-stu-id="a04f9-103">FMS\_HELPSTRING structure</span></span>

<span data-ttu-id="a04f9-104">Содержит сведения, используемые диспетчером файлов для добавления строки справки для элемента меню или команды панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="a04f9-104">Contains information that File Manager uses to add a Help string for a menu or toolbar command item.</span></span>

## <a name="syntax"></a><span data-ttu-id="a04f9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a04f9-105">Syntax</span></span>


```C++
typedef struct _FMS_HELPSTRING {
  INT       idCommand;
  HMENU     hMenu;
  __wchar_t szHelp[128];
} FMS_HELPSTRING;
```



## <a name="members"></a><span data-ttu-id="a04f9-106">Участники</span><span class="sxs-lookup"><span data-stu-id="a04f9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a04f9-107">**идкомманд**</span><span class="sxs-lookup"><span data-stu-id="a04f9-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="a04f9-108">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="a04f9-108">Type: **INT**</span></span>

</dd> <dd>

<span data-ttu-id="a04f9-109">Идентификатор элемента команды.</span><span class="sxs-lookup"><span data-stu-id="a04f9-109">The identifier of the command item.</span></span>

</dd> <dt>

<span data-ttu-id="a04f9-110">**hMenu**</span><span class="sxs-lookup"><span data-stu-id="a04f9-110">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="a04f9-111">Тип: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="a04f9-111">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="a04f9-112">Идентификатор строки меню.</span><span class="sxs-lookup"><span data-stu-id="a04f9-112">The identifier of the menu bar.</span></span>

</dd> <dt>

<span data-ttu-id="a04f9-113">**сзелп**</span><span class="sxs-lookup"><span data-stu-id="a04f9-113">**szHelp**</span></span>
</dt> <dd>

<span data-ttu-id="a04f9-114">Тип: **\_ \_ WCHAR \_ t \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="a04f9-114">Type: **\_\_wchar\_t\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="a04f9-115">Строка, завершающаяся нулем, которая получает текст справки.</span><span class="sxs-lookup"><span data-stu-id="a04f9-115">The null-terminated string that receives the Help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a04f9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a04f9-116">Requirements</span></span>



| <span data-ttu-id="a04f9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a04f9-117">Requirement</span></span> | <span data-ttu-id="a04f9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a04f9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a04f9-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a04f9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a04f9-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a04f9-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="a04f9-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a04f9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a04f9-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a04f9-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a04f9-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a04f9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a04f9-124"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="a04f9-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a04f9-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a04f9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a04f9-126">**фмекстенсионпрок**</span><span class="sxs-lookup"><span data-stu-id="a04f9-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="a04f9-127">**ФМЕВЕНТ \_ хелпменуитем**</span><span class="sxs-lookup"><span data-stu-id="a04f9-127">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




