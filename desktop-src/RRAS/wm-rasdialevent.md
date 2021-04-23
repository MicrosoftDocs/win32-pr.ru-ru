---
title: Сообщение WM_RASDIALEVENT (RAS. h)
description: Операционная система отправляет \_ сообщение WM расдиалевент в процедуру окна, когда происходит изменение события состояния во время процесса подключения RAS.
ms.assetid: 4526da20-04e7-47b2-b576-8dc36c08b053
keywords:
- RAS сообщения WM_RASDIALEVENT
topic_type:
- apiref
api_name:
- WM_RASDIALEVENT
api_location:
- Ras.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 470fe3915c9f672c4663971159386e529ea60db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672471"
---
# <a name="wm_rasdialevent-message"></a><span data-ttu-id="1af8d-104">\_Сообщение РАСДИАЛЕВЕНТ WM</span><span class="sxs-lookup"><span data-stu-id="1af8d-104">WM\_RASDIALEVENT message</span></span>

<span data-ttu-id="1af8d-105">Операционная система отправляет сообщение **WM \_ расдиалевент** в процедуру окна, когда происходит изменение события состояния во время процесса подключения RAS.</span><span class="sxs-lookup"><span data-stu-id="1af8d-105">The operating system sends a **WM\_RASDIALEVENT** message to a window procedure when a change of state event occurs during a RAS connection process.</span></span> <span data-ttu-id="1af8d-106">Это происходит, когда указано окно для управления уведомлениями о таких событиях с помощью параметра " *уведомление* " в [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala).</span><span class="sxs-lookup"><span data-stu-id="1af8d-106">This happens when a window has been specified to handle notifications of such events by using the *notifier* parameter of [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).</span></span>

<span data-ttu-id="1af8d-107">Два параметра сообщения эквивалентны параметрам тех же имен, которые используются с функциями обратного вызова [**расдиалфунк**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) и [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) .</span><span class="sxs-lookup"><span data-stu-id="1af8d-107">The two message parameters are equivalent to the parameters of the same names that are used with [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span>


```C++
WM_RASDIALEVENT 
rasconnstate = (RASCONNSTATE) wParam; 
dwError = (DWORD) lParam;
            
```



## <a name="parameters"></a><span data-ttu-id="1af8d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1af8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1af8d-109">*расконнстате*</span><span class="sxs-lookup"><span data-stu-id="1af8d-109">*rasconnstate*</span></span> 
</dt> <dd>

<span data-ttu-id="1af8d-110">Значение параметра *wParam*.</span><span class="sxs-lookup"><span data-stu-id="1af8d-110">Value of *wParam*.</span></span> <span data-ttu-id="1af8d-111">Эквивалентно параметру *расконнстате* функций обратного вызова [**расдиалфунк**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) и [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) .</span><span class="sxs-lookup"><span data-stu-id="1af8d-111">Equivalent to the *rasconnstate* parameter of the [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span> <span data-ttu-id="1af8d-112">Указывает значение перечислителя [**расконнстате**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) , указывающее состояние, которое будет введено процессом подключения к удаленному доступу RasDial.</span><span class="sxs-lookup"><span data-stu-id="1af8d-112">Specifies a [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) enumerator value that indicates the state the RasDial remote access connection process is about to enter.</span></span>

</dd> <dt>

<span data-ttu-id="1af8d-113">*дверрор*</span><span class="sxs-lookup"><span data-stu-id="1af8d-113">*dwError*</span></span> 
</dt> <dd>

<span data-ttu-id="1af8d-114">Значение *lParam*.</span><span class="sxs-lookup"><span data-stu-id="1af8d-114">Value of *lParam*.</span></span> <span data-ttu-id="1af8d-115">Эквивалентно параметру *дверрор* функций обратного вызова [**расдиалфунк**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) и [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) .</span><span class="sxs-lookup"><span data-stu-id="1af8d-115">Equivalent to the *dwError* parameter of the [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span> <span data-ttu-id="1af8d-116">Ненулевое значение указывает на произошедшее ошибку или нуль, если ошибка не возникла.</span><span class="sxs-lookup"><span data-stu-id="1af8d-116">A nonzero value indicates the error that has occurred, or zero if no error has occurred.</span></span>

<span data-ttu-id="1af8d-117">[**Rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) отправляет это сообщение с параметром *дверрор* , имеющим значение 0, после ввода каждого состояния подключения.</span><span class="sxs-lookup"><span data-stu-id="1af8d-117">[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) sends this message with *dwError* set to zero upon entry to each connection state.</span></span> <span data-ttu-id="1af8d-118">Если ошибка возникает в состоянии, сообщение снова отправляется в состояние, на этот раз с ненулевым *дверрор* значением.</span><span class="sxs-lookup"><span data-stu-id="1af8d-118">If an error occurs within a state, the message is sent again for the state, this time with a nonzero *dwError* value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1af8d-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1af8d-119">Return value</span></span>

<span data-ttu-id="1af8d-120">Если приложение обрабатывает это сообщение, оно должно возвращать **значение true**.</span><span class="sxs-lookup"><span data-stu-id="1af8d-120">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1af8d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="1af8d-121">Requirements</span></span>



| <span data-ttu-id="1af8d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="1af8d-122">Requirement</span></span> | <span data-ttu-id="1af8d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="1af8d-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1af8d-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1af8d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1af8d-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1af8d-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1af8d-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1af8d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1af8d-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1af8d-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1af8d-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1af8d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1af8d-129"><dt>RAS. h</dt></span><span class="sxs-lookup"><span data-stu-id="1af8d-129"><dt>Ras.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1af8d-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1af8d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1af8d-131">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="1af8d-131">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="1af8d-132">Сообщения службы удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="1af8d-132">Remote Access Service Messages</span></span>](remote-access-service-messages.md)
</dt> <dt>

[<span data-ttu-id="1af8d-133">**RasDial**</span><span class="sxs-lookup"><span data-stu-id="1af8d-133">**RasDial**</span></span>](/windows/desktop/api/Ras/nf-ras-rasdiala)
</dt> <dt>

[<span data-ttu-id="1af8d-134">**расдиалфунк**</span><span class="sxs-lookup"><span data-stu-id="1af8d-134">**RasDialFunc**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc)
</dt> <dt>

[<span data-ttu-id="1af8d-135">**RasDialFunc1**</span><span class="sxs-lookup"><span data-stu-id="1af8d-135">**RasDialFunc1**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)
</dt> <dt>

<span data-ttu-id="1af8d-136">[**расконнстате**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1af8d-136">[**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))</span></span>
</dt> </dl>

 

