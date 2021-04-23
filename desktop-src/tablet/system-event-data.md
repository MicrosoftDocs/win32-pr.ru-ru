---
description: Содержит сведения о событии планшетной системы.
ms.assetid: 725f4b43-0bcb-4452-a87f-b24a85de0049
title: Структура SYSTEM_EVENT_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_EVENT_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5d77c78a78a6cecae0368e8d9192a0dc0efc10e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272837"
---
# <a name="system_event_data-structure"></a><span data-ttu-id="aee58-103">\_ \_ Структура данных системных событий</span><span class="sxs-lookup"><span data-stu-id="aee58-103">SYSTEM\_EVENT\_DATA structure</span></span>

<span data-ttu-id="aee58-104">Содержит сведения о событии планшетной системы.</span><span class="sxs-lookup"><span data-stu-id="aee58-104">Contains information about a tablet system event.</span></span>

## <a name="syntax"></a><span data-ttu-id="aee58-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aee58-105">Syntax</span></span>


```C++
typedef struct tagSYSTEM_EVENT_DATA {
  BYTE  bModifier;
  WCHAR wKey;
  LONG  xPos;
  LONG  yPos;
  BYTE  bCursorMode;
  DWORD dwButtonState;
} SYSTEM_EVENT_DATA;
```



## <a name="members"></a><span data-ttu-id="aee58-106">Члены</span><span class="sxs-lookup"><span data-stu-id="aee58-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="aee58-107">**бмодифиер**</span><span class="sxs-lookup"><span data-stu-id="aee58-107">**bModifier**</span></span>
</dt> <dd>

<span data-ttu-id="aee58-108">Битовые значения для модификаторов.</span><span class="sxs-lookup"><span data-stu-id="aee58-108">Bit values for the modifiers.</span></span> <span data-ttu-id="aee58-109">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="aee58-109">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="aee58-110">**вкэй**</span><span class="sxs-lookup"><span data-stu-id="aee58-110">**wKey**</span></span>
</dt> <dd>

<span data-ttu-id="aee58-111">Код сканирования для символа клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="aee58-111">Scan code for the keyboard character.</span></span>

</dd> <dt>

<span data-ttu-id="aee58-112">**кспос**</span><span class="sxs-lookup"><span data-stu-id="aee58-112">**xPos**</span></span>
</dt> <dd>

<span data-ttu-id="aee58-113">Расположение события по оси X.</span><span class="sxs-lookup"><span data-stu-id="aee58-113">X position of the event.</span></span>

</dd> <dt>

<span data-ttu-id="aee58-114">**ипос**</span><span class="sxs-lookup"><span data-stu-id="aee58-114">**yPos**</span></span>
</dt> <dd>

<span data-ttu-id="aee58-115">Расположение по оси Y события.</span><span class="sxs-lookup"><span data-stu-id="aee58-115">Y position of the event.</span></span>

</dd> <dt>

<span data-ttu-id="aee58-116">**бкурсормоде**</span><span class="sxs-lookup"><span data-stu-id="aee58-116">**bCursorMode**</span></span>
</dt> <dd>

<span data-ttu-id="aee58-117">Тип курсора, вызвавшего событие.</span><span class="sxs-lookup"><span data-stu-id="aee58-117">The type of cursor that caused the event.</span></span> <span data-ttu-id="aee58-118">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="aee58-118">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="aee58-119">**двбуттонстате**</span><span class="sxs-lookup"><span data-stu-id="aee58-119">**dwButtonState**</span></span>
</dt> <dd>

<span data-ttu-id="aee58-120">Состояние кнопок во время системного события.</span><span class="sxs-lookup"><span data-stu-id="aee58-120">State of the buttons at the time of the system event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aee58-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aee58-121">Remarks</span></span>

<span data-ttu-id="aee58-122">Следующие системные события определены для использования в элементе **бмодифиер** .</span><span class="sxs-lookup"><span data-stu-id="aee58-122">The following system events are defined for use in the **bModifier** member.</span></span>



| <span data-ttu-id="aee58-123">Значение</span><span class="sxs-lookup"><span data-stu-id="aee58-123">Value</span></span>               | <span data-ttu-id="aee58-124">Описание</span><span class="sxs-lookup"><span data-stu-id="aee58-124">Description</span></span>                  |
|---------------------|------------------------------|
| <span data-ttu-id="aee58-125">\_Модификатор SE \_ CTRL</span><span class="sxs-lookup"><span data-stu-id="aee58-125">SE\_MODIFIER\_CTRL</span></span>  | <span data-ttu-id="aee58-126">Нажата клавиша CTRL.</span><span class="sxs-lookup"><span data-stu-id="aee58-126">The Control key was pressed.</span></span> |
| <span data-ttu-id="aee58-127">\_Модификатор SE \_ ALT</span><span class="sxs-lookup"><span data-stu-id="aee58-127">SE\_MODIFIER\_ALT</span></span>   | <span data-ttu-id="aee58-128">Нажата клавиша ALT.</span><span class="sxs-lookup"><span data-stu-id="aee58-128">The Alt key was pressed.</span></span>     |
| <span data-ttu-id="aee58-129">\_Модификатор SE \_ SHIFT</span><span class="sxs-lookup"><span data-stu-id="aee58-129">SE\_MODIFIER\_SHIFT</span></span> | <span data-ttu-id="aee58-130">Нажата клавиша SHIFT.</span><span class="sxs-lookup"><span data-stu-id="aee58-130">The Shift key was pressed.</span></span>   |



 

<span data-ttu-id="aee58-131">Следующие системные события определены для использования в элементе **бкурсормоде** .</span><span class="sxs-lookup"><span data-stu-id="aee58-131">The following system events are defined for use in the **bCursorMode** member.</span></span>



| <span data-ttu-id="aee58-132">Значение</span><span class="sxs-lookup"><span data-stu-id="aee58-132">Value</span></span>              | <span data-ttu-id="aee58-133">Описание</span><span class="sxs-lookup"><span data-stu-id="aee58-133">Description</span></span>               |
|--------------------|---------------------------|
| <span data-ttu-id="aee58-134">\_стандартный \_ курсор SE</span><span class="sxs-lookup"><span data-stu-id="aee58-134">SE\_NORMAL\_CURSOR</span></span> | <span data-ttu-id="aee58-135">Указывает кончик пера.</span><span class="sxs-lookup"><span data-stu-id="aee58-135">Indicates the pen tip.</span></span>    |
| <span data-ttu-id="aee58-136">\_курсор ластика \_ SE</span><span class="sxs-lookup"><span data-stu-id="aee58-136">SE\_ERASER\_CURSOR</span></span> | <span data-ttu-id="aee58-137">Указывает ластик пера.</span><span class="sxs-lookup"><span data-stu-id="aee58-137">Indicates the pen eraser.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="aee58-138">Требования</span><span class="sxs-lookup"><span data-stu-id="aee58-138">Requirements</span></span>



| <span data-ttu-id="aee58-139">Требование</span><span class="sxs-lookup"><span data-stu-id="aee58-139">Requirement</span></span> | <span data-ttu-id="aee58-140">Значение</span><span class="sxs-lookup"><span data-stu-id="aee58-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="aee58-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aee58-141">Minimum supported client</span></span><br/> | <span data-ttu-id="aee58-142">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="aee58-142">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="aee58-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aee58-143">Minimum supported server</span></span><br/> | <span data-ttu-id="aee58-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="aee58-144">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="aee58-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aee58-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aee58-146">**Метод Истилусплугин:: Системевент**</span><span class="sxs-lookup"><span data-stu-id="aee58-146">**IStylusPlugin::SystemEvent Method**</span></span>](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-systemevent)
</dt> <dt>

[<span data-ttu-id="aee58-147">**Метод Итаблетевентсинк:: Системевент**</span><span class="sxs-lookup"><span data-stu-id="aee58-147">**ITabletEventSink::SystemEvent Method**</span></span>](itableteventsink-systemevent.md)
</dt> </dl>

 

 




