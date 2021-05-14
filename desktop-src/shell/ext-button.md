---
description: Содержит сведения о кнопке, которая добавляется БИБЛИОТЕКой расширения диспетчера файлов на панель инструментов диспетчера файлов.
title: Структура EXT_BUTTON (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXT_BUTTON
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8cd29a06-0f38-4285-9092-647a391b72d7
ms.openlocfilehash: 6d1505ef7b330f0e935136eacaf808da3add8cd8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843155"
---
# <a name="ext_button-structure"></a><span data-ttu-id="c96ca-103">\_Структура кнопки ext</span><span class="sxs-lookup"><span data-stu-id="c96ca-103">EXT\_BUTTON structure</span></span>

<span data-ttu-id="c96ca-104">Содержит сведения о кнопке, которая добавляется БИБЛИОТЕКой расширения диспетчера файлов на панель инструментов диспетчера файлов.</span><span class="sxs-lookup"><span data-stu-id="c96ca-104">Contains information about a button that a File Manager extension DLL is adding to the toolbar of File Manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="c96ca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c96ca-105">Syntax</span></span>


```C++
typedef struct tagEXT_BUTTON {
  WORD idCommand;
  WORD idsHelp;
  WORD fsStyle;
} EXT_BUTTON, *LPEXT_BUTTON;
```



## <a name="members"></a><span data-ttu-id="c96ca-106">Члены</span><span class="sxs-lookup"><span data-stu-id="c96ca-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c96ca-107">**идкомманд**</span><span class="sxs-lookup"><span data-stu-id="c96ca-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="c96ca-108">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="c96ca-108">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c96ca-109">Идентификатор команды для кнопки.</span><span class="sxs-lookup"><span data-stu-id="c96ca-109">A command identifier for the button.</span></span>

</dd> <dt>

<span data-ttu-id="c96ca-110">**идшелп**</span><span class="sxs-lookup"><span data-stu-id="c96ca-110">**idsHelp**</span></span>
</dt> <dd>

<span data-ttu-id="c96ca-111">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="c96ca-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c96ca-112">Идентификатор строки справки для кнопки.</span><span class="sxs-lookup"><span data-stu-id="c96ca-112">The identifier of the Help string for the button.</span></span>

</dd> <dt>

<span data-ttu-id="c96ca-113">**фсстиле**</span><span class="sxs-lookup"><span data-stu-id="c96ca-113">**fsStyle**</span></span>
</dt> <dd>

<span data-ttu-id="c96ca-114">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="c96ca-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c96ca-115">Стиль кнопки.</span><span class="sxs-lookup"><span data-stu-id="c96ca-115">The style of the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c96ca-116">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="c96ca-116">Requirements</span></span>



| <span data-ttu-id="c96ca-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c96ca-117">Requirement</span></span> | <span data-ttu-id="c96ca-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c96ca-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c96ca-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c96ca-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c96ca-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c96ca-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="c96ca-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c96ca-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c96ca-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c96ca-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c96ca-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c96ca-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c96ca-124"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="c96ca-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c96ca-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c96ca-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c96ca-126">**ФМЕВЕНТ \_ тулбарлоад**</span><span class="sxs-lookup"><span data-stu-id="c96ca-126">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> <dt>

[<span data-ttu-id="c96ca-127">**FMS \_ тулбарлоад**</span><span class="sxs-lookup"><span data-stu-id="c96ca-127">**FMS\_TOOLBARLOAD**</span></span>](fms-toolbarload.md)
</dt> </dl>

 

 




