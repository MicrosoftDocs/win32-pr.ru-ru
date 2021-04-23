---
description: СФВМная \_ панель может быть изменена или недоступна.
ms.assetid: 9621b921-e97f-4219-953a-7c961a81c379
title: Сообщение SFVM_GETPANE (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2800be1b7b427e13014686e587b51fc4bf7d7617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998846"
---
# <a name="sfvm_getpane-message"></a><span data-ttu-id="56f01-103">\_Сообщение сфвм</span><span class="sxs-lookup"><span data-stu-id="56f01-103">SFVM\_GETPANE message</span></span>

<span data-ttu-id="56f01-104">\[**Сфвм \_ Группа доступности доступна для** использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="56f01-104">\[**SFVM\_GETPANE** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="56f01-105">В последующих версиях он может быть изменен или недоступен.\]</span><span class="sxs-lookup"><span data-stu-id="56f01-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="56f01-106">Позволяет объекту обратного вызова предоставлять панель строки состояния, в которой отображаются сведения о зоне Интернета.</span><span class="sxs-lookup"><span data-stu-id="56f01-106">Allows the callback object to provide the status bar pane in which to display the Internet zone information.</span></span> <span data-ttu-id="56f01-107">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="56f01-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETPANE
    wParam = (WPARAM)(int) paneID;
    lParam = (LPARAM)(DWORD*) pane;
            
```



## <a name="parameters"></a><span data-ttu-id="56f01-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="56f01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56f01-109">*панеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="56f01-109">*paneID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56f01-110">Идентификатор запрошенной панели.</span><span class="sxs-lookup"><span data-stu-id="56f01-110">ID of the requested pane.</span></span> <span data-ttu-id="56f01-111">Обычно это зона области \_ , но может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="56f01-111">This is normally PANE\_ZONE, but can be any one of the following values.</span></span>

<dt>

<span id="PANE_NONE"></span><span id="pane_none"></span>

<span data-ttu-id="56f01-112"><span id="PANE_NONE"></span><span id="pane_none"></span>**ПАНЕЛЬ \_ нет**</span><span class="sxs-lookup"><span data-stu-id="56f01-112"><span id="PANE_NONE"></span><span id="pane_none"></span>**PANE\_NONE**</span></span>


</dt> <dd>

<span data-ttu-id="56f01-113">Нет области.</span><span class="sxs-lookup"><span data-stu-id="56f01-113">No pane.</span></span>

</dd> <dt>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>

<span data-ttu-id="56f01-114"><span id="PANE_ZONE"></span><span id="pane_zone"></span>**\_зона области**</span><span class="sxs-lookup"><span data-stu-id="56f01-114"><span id="PANE_ZONE"></span><span id="pane_zone"></span>**PANE\_ZONE**</span></span>


</dt> <dd>

<span data-ttu-id="56f01-115">Область зоны Интернета.</span><span class="sxs-lookup"><span data-stu-id="56f01-115">The Internet zone pane.</span></span>

</dd> <dt>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>

<span data-ttu-id="56f01-116"><span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**\_Автономная работа с панелью**</span><span class="sxs-lookup"><span data-stu-id="56f01-116"><span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**PANE\_OFFLINE**</span></span>


</dt> <dd>

<span data-ttu-id="56f01-117">Автономная область.</span><span class="sxs-lookup"><span data-stu-id="56f01-117">The offline pane.</span></span>

</dd> <dt>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>

<span data-ttu-id="56f01-118"><span id="PANE_PRINTER"></span><span id="pane_printer"></span>**ПАНЕЛЬ \_ принтера**</span><span class="sxs-lookup"><span data-stu-id="56f01-118"><span id="PANE_PRINTER"></span><span id="pane_printer"></span>**PANE\_PRINTER**</span></span>


</dt> <dd>

<span data-ttu-id="56f01-119">Панель «индикации печати».</span><span class="sxs-lookup"><span data-stu-id="56f01-119">The print indication pane.</span></span>

</dd> <dt>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>

<span data-ttu-id="56f01-120"><span id="PANE_SSL"></span><span id="pane_ssl"></span>**\_SSL панели**</span><span class="sxs-lookup"><span data-stu-id="56f01-120"><span id="PANE_SSL"></span><span id="pane_ssl"></span>**PANE\_SSL**</span></span>


</dt> <dd>

<span data-ttu-id="56f01-121">Панель SSL.</span><span class="sxs-lookup"><span data-stu-id="56f01-121">The SSL pane.</span></span>

</dd> <dt>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>

<span data-ttu-id="56f01-122"><span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**Навигация по ПАНЕЛЯМ \_**</span><span class="sxs-lookup"><span data-stu-id="56f01-122"><span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**PANE\_NAVIGATION**</span></span>


</dt> <dd>

<span data-ttu-id="56f01-123">Область навигации.</span><span class="sxs-lookup"><span data-stu-id="56f01-123">The navigation pane.</span></span>

</dd> <dt>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>

<span data-ttu-id="56f01-124"><span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**\_ход выполнения панели**</span><span class="sxs-lookup"><span data-stu-id="56f01-124"><span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**PANE\_PROGRESS**</span></span>


</dt> <dd>

<span data-ttu-id="56f01-125">Панель индикатора выполнения.</span><span class="sxs-lookup"><span data-stu-id="56f01-125">The progress bar pane.</span></span>

</dd> <dt>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>

<span data-ttu-id="56f01-126"><span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**\_Конфиденциальность области**</span><span class="sxs-lookup"><span data-stu-id="56f01-126"><span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**PANE\_PRIVACY**</span></span>


</dt> <dd>

<span data-ttu-id="56f01-127">Панель «индикатор конфиденциальности».</span><span class="sxs-lookup"><span data-stu-id="56f01-127">The privacy indicator pane.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="56f01-128">*панель* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="56f01-128">*pane* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56f01-129">Указатель на **DWORD** , содержащий номер панели.</span><span class="sxs-lookup"><span data-stu-id="56f01-129">Pointer to a **DWORD** containing the pane number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56f01-130">Требования</span><span class="sxs-lookup"><span data-stu-id="56f01-130">Requirements</span></span>



| <span data-ttu-id="56f01-131">Требование</span><span class="sxs-lookup"><span data-stu-id="56f01-131">Requirement</span></span> | <span data-ttu-id="56f01-132">Значение</span><span class="sxs-lookup"><span data-stu-id="56f01-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="56f01-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56f01-133">Minimum supported client</span></span><br/> | <span data-ttu-id="56f01-134">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="56f01-134">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="56f01-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56f01-135">Minimum supported server</span></span><br/> | <span data-ttu-id="56f01-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="56f01-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="56f01-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="56f01-137">End of client support</span></span><br/>    | <span data-ttu-id="56f01-138">Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="56f01-138">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="56f01-139">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="56f01-139">End of server support</span></span><br/>    | <span data-ttu-id="56f01-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="56f01-140">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="56f01-141">Header</span><span class="sxs-lookup"><span data-stu-id="56f01-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="56f01-142"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="56f01-142"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
