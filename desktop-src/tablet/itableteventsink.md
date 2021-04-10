---
description: Определяет методы, обрабатывающие события интерфейса Итаблет.
ms.assetid: 9acf32fa-b33f-4b9a-be73-804b7d5434e8
title: Интерфейс Итаблетевентсинк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fc42bfe8a6e69504c35d7926c4c5a8b688404897
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272631"
---
# <a name="itableteventsink-interface"></a><span data-ttu-id="46e95-103">Интерфейс Итаблетевентсинк</span><span class="sxs-lookup"><span data-stu-id="46e95-103">ITabletEventSink interface</span></span>

<span data-ttu-id="46e95-104">Определяет методы, обрабатывающие события [**интерфейса итаблет**](itablet.md) .</span><span class="sxs-lookup"><span data-stu-id="46e95-104">Defines methods that handle the [**ITablet Interface**](itablet.md) events.</span></span>

## <a name="members"></a><span data-ttu-id="46e95-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="46e95-105">Members</span></span>

<span data-ttu-id="46e95-106">Интерфейс **итаблетевентсинк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="46e95-106">The **ITabletEventSink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="46e95-107">**Итаблетевентсинк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="46e95-107">**ITabletEventSink** also has these types of members:</span></span>

-   [<span data-ttu-id="46e95-108">Методы</span><span class="sxs-lookup"><span data-stu-id="46e95-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="46e95-109">Методы</span><span class="sxs-lookup"><span data-stu-id="46e95-109">Methods</span></span>

<span data-ttu-id="46e95-110">Интерфейс **итаблетевентсинк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="46e95-110">The **ITabletEventSink** interface has these methods.</span></span>



| <span data-ttu-id="46e95-111">Метод</span><span class="sxs-lookup"><span data-stu-id="46e95-111">Method</span></span>                                                        | <span data-ttu-id="46e95-112">Описание</span><span class="sxs-lookup"><span data-stu-id="46e95-112">Description</span></span>                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46e95-113">**контексткреате**</span><span class="sxs-lookup"><span data-stu-id="46e95-113">**ContextCreate**</span></span>](itableteventsink-contextcreate.md)       | <span data-ttu-id="46e95-114">Происходит при создании нового контекста планшета.</span><span class="sxs-lookup"><span data-stu-id="46e95-114">Occurs when a new tablet context is created.</span></span><br/>                                          |
| [<span data-ttu-id="46e95-115">**контекстдестрой**</span><span class="sxs-lookup"><span data-stu-id="46e95-115">**ContextDestroy**</span></span>](itableteventsink-contextdestroy.md)     | <span data-ttu-id="46e95-116">Происходит при уничтожении контекста планшета.</span><span class="sxs-lookup"><span data-stu-id="46e95-116">Occurs when a tablet context is being destroyed.</span></span><br/>                                      |
| [<span data-ttu-id="46e95-117">**курсордовн**</span><span class="sxs-lookup"><span data-stu-id="46e95-117">**CursorDown**</span></span>](itableteventsink-cursordown.md)             | <span data-ttu-id="46e95-118">Происходит, когда подсказка пера обращается к поверхности планшета в дигитайзере.</span><span class="sxs-lookup"><span data-stu-id="46e95-118">Occurs when the stylus tip contacts the digitizing tablet surface.</span></span><br/>                    |
| [<span data-ttu-id="46e95-119">**курсоринранже**</span><span class="sxs-lookup"><span data-stu-id="46e95-119">**CursorInRange**</span></span>](itableteventsink-cursorinrange.md)       | <span data-ttu-id="46e95-120">Происходит, когда перо попадает в диапазон обнаружения дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="46e95-120">Occurs when a stylus comes within the digitizer's range of detection.</span></span><br/>                 |
| [<span data-ttu-id="46e95-121">**курсормове**</span><span class="sxs-lookup"><span data-stu-id="46e95-121">**CursorMove**</span></span>](itableteventsink-cursormove.md)             | <span data-ttu-id="46e95-122">Происходит при наведении курсора мыши на планшетном дигитайзере.</span><span class="sxs-lookup"><span data-stu-id="46e95-122">Occurs when the cursor moves over the tablet digitizer.</span></span><br/>                               |
| [<span data-ttu-id="46e95-123">**курсорнев**</span><span class="sxs-lookup"><span data-stu-id="46e95-123">**CursorNew**</span></span>](itableteventsink-cursornew.md)               | <span data-ttu-id="46e95-124">Происходит при добавлении нового пера в систему.</span><span class="sxs-lookup"><span data-stu-id="46e95-124">Occurs when a new stylus is added to the system.</span></span><br/>                                      |
| [<span data-ttu-id="46e95-125">**курсораутофранже**</span><span class="sxs-lookup"><span data-stu-id="46e95-125">**CursorOutOfRange**</span></span>](itableteventsink-cursoroutofrange.md) | <span data-ttu-id="46e95-126">Происходит, когда перо покидает диапазон физического обнаружения (близость) планшета.</span><span class="sxs-lookup"><span data-stu-id="46e95-126">Occurs when the stylus leaves the physical detection range (proximity) of the tablet.</span></span><br/> |
| [<span data-ttu-id="46e95-127">**курсоруп**</span><span class="sxs-lookup"><span data-stu-id="46e95-127">**CursorUp**</span></span>](itableteventsink-cursorup.md)                 | <span data-ttu-id="46e95-128">Происходит, когда пользователь порождает перо из поверхности планшета дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="46e95-128">Occurs when the user has raised the stylus from the tablet digitizer surface.</span></span><br/>         |
| [<span data-ttu-id="46e95-129">**Пакеты**</span><span class="sxs-lookup"><span data-stu-id="46e95-129">**Packets**</span></span>](itableteventsink-packets.md)                   | <span data-ttu-id="46e95-130">Происходит при перемещении пера на дигитайзер.</span><span class="sxs-lookup"><span data-stu-id="46e95-130">Occurs when the stylus is moving on the digitizer.</span></span><br/>                                    |
| [<span data-ttu-id="46e95-131">**системевент**</span><span class="sxs-lookup"><span data-stu-id="46e95-131">**SystemEvent**</span></span>](itableteventsink-systemevent.md)           | <span data-ttu-id="46e95-132">Происходит при наличии системного события.</span><span class="sxs-lookup"><span data-stu-id="46e95-132">Occurs when a system event is available.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="46e95-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46e95-133">Remarks</span></span>

<span data-ttu-id="46e95-134">Разработчики не должны использовать этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="46e95-134">Developers should not use this interface.</span></span>

<span data-ttu-id="46e95-135">В следующем коде показано, как определяется интерфейс **итаблетевентсинк** .</span><span class="sxs-lookup"><span data-stu-id="46e95-135">The following code shows how the **ITabletEventSink** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(788459C8-26C8-4666-BF57-04AD3A0A5EB5),
    pointer_default(unique)
]
interface ITabletEventSink: IUnknown
{

    HRESULT ContextCreate(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT ContextDestroy(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT CursorNew(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorInRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorOutOfRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorDown(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT CursorUp(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT Packets(
        [in] TABLET_CONTEXT_ID tcid,
        [in] ULONG cPkts,
        [in] ULONG cbPkts,
        [in, size_is(cbPkts)] BYTE * pbPkts,
        [in, unique, size_is(cPkts)
#ifndef NT_TARGET_XP
         ,disable_consistency_check
#endif
        ] ULONG *pnSerialNumbers,
        [in] CURSOR_ID cid
    );

    HRESULT SystemEvent(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] SYSTEM_EVENT event,
        [in] SYSTEM_EVENT_DATA eventdata
    );
};

     
```

## <a name="requirements"></a><span data-ttu-id="46e95-136">Требования</span><span class="sxs-lookup"><span data-stu-id="46e95-136">Requirements</span></span>



| <span data-ttu-id="46e95-137">Требование</span><span class="sxs-lookup"><span data-stu-id="46e95-137">Requirement</span></span> | <span data-ttu-id="46e95-138">Значение</span><span class="sxs-lookup"><span data-stu-id="46e95-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46e95-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46e95-139">Minimum supported client</span></span><br/> | <span data-ttu-id="46e95-140">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="46e95-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="46e95-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46e95-141">Minimum supported server</span></span><br/> | <span data-ttu-id="46e95-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="46e95-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="46e95-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="46e95-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="46e95-144"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="46e95-144"><dt>Wisptis.exe</dt></span></span> </dl> |



 

