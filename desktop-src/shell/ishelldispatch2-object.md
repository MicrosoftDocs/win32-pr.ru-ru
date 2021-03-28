---
description: Расширяет объект Ишеллдиспатч с помощью ряда новых функциональных возможностей.
ms.assetid: 74687929-0777-479b-9853-2b0cf4b6adc9
title: Объект IShellDispatch2 (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 79d3abbed038e09f2e73c62e5e3d9b16545e8f60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984676"
---
# <a name="ishelldispatch2-object"></a><span data-ttu-id="607c6-103">Объект IShellDispatch2</span><span class="sxs-lookup"><span data-stu-id="607c6-103">IShellDispatch2 object</span></span>

<span data-ttu-id="607c6-104">Расширяет объект [**ишеллдиспатч**](ishelldispatch.md) с помощью ряда новых функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="607c6-104">Extends the [**IShellDispatch**](ishelldispatch.md) object with a variety of new functionality.</span></span>

> [!Note]  
> <span data-ttu-id="607c6-105">**IShellDispatch2** реализован и доступен через объект [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="607c6-105">**IShellDispatch2** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="607c6-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="607c6-106">Members</span></span>

<span data-ttu-id="607c6-107">Объект **IShellDispatch2** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="607c6-107">The **IShellDispatch2** object has these types of members:</span></span>

-   [<span data-ttu-id="607c6-108">Методы</span><span class="sxs-lookup"><span data-stu-id="607c6-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="607c6-109">Методы</span><span class="sxs-lookup"><span data-stu-id="607c6-109">Methods</span></span>

<span data-ttu-id="607c6-110">Объект **IShellDispatch2** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="607c6-110">The **IShellDispatch2** object has these methods.</span></span>



| <span data-ttu-id="607c6-111">Метод</span><span class="sxs-lookup"><span data-stu-id="607c6-111">Method</span></span>                                                               | <span data-ttu-id="607c6-112">Описание</span><span class="sxs-lookup"><span data-stu-id="607c6-112">Description</span></span>                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="607c6-113">**канстартстопсервице**</span><span class="sxs-lookup"><span data-stu-id="607c6-113">**CanStartStopService**</span></span>](ishelldispatch2-canstartstopservice.md)   | <span data-ttu-id="607c6-114">Определяет, может ли текущий пользователь запускать и прекращать работу именованной службы.</span><span class="sxs-lookup"><span data-stu-id="607c6-114">Determines if the current user can start and stop the named service.</span></span><br/>    |
| [<span data-ttu-id="607c6-115">**финдпринтер**</span><span class="sxs-lookup"><span data-stu-id="607c6-115">**FindPrinter**</span></span>](ishelldispatch2-findprinter.md)                   | <span data-ttu-id="607c6-116">Отображает диалоговое окно **Поиск принтера** .</span><span class="sxs-lookup"><span data-stu-id="607c6-116">Displays the **Find Printer** dialog box.</span></span><br/>                               |
| [<span data-ttu-id="607c6-117">**жетсистеминформатион**</span><span class="sxs-lookup"><span data-stu-id="607c6-117">**GetSystemInformation**</span></span>](ishelldispatch2-getsysteminformation.md) | <span data-ttu-id="607c6-118">Возвращает сведения о системе.</span><span class="sxs-lookup"><span data-stu-id="607c6-118">Retrieves system information.</span></span><br/>                                           |
| [<span data-ttu-id="607c6-119">**Ограниченный доступ**</span><span class="sxs-lookup"><span data-stu-id="607c6-119">**IsRestricted**</span></span>](ishelldispatch2-isrestricted.md)                 | <span data-ttu-id="607c6-120">Извлекает из реестра параметр ограничений группы.</span><span class="sxs-lookup"><span data-stu-id="607c6-120">Retrieves a group's restriction setting from the registry.</span></span><br/>              |
| [<span data-ttu-id="607c6-121">**иссервицеруннинг**</span><span class="sxs-lookup"><span data-stu-id="607c6-121">**IsServiceRunning**</span></span>](ishelldispatch2-isservicerunning.md)         | <span data-ttu-id="607c6-122">Возвращает значение, указывающее, запущена ли определенная служба.</span><span class="sxs-lookup"><span data-stu-id="607c6-122">Returns a value that indicates whether a particular service is running.</span></span><br/> |
| [<span data-ttu-id="607c6-123">**сервицестарт**</span><span class="sxs-lookup"><span data-stu-id="607c6-123">**ServiceStart**</span></span>](ishelldispatch2-servicestart.md)                 | <span data-ttu-id="607c6-124">Запускает именованную службу.</span><span class="sxs-lookup"><span data-stu-id="607c6-124">Starts a named service.</span></span><br/>                                                 |
| [<span data-ttu-id="607c6-125">**сервицестоп**</span><span class="sxs-lookup"><span data-stu-id="607c6-125">**ServiceStop**</span></span>](ishelldispatch2-servicestop.md)                   | <span data-ttu-id="607c6-126">Останавливает именованную службу.</span><span class="sxs-lookup"><span data-stu-id="607c6-126">Stops a named service.</span></span><br/>                                                  |
| [<span data-ttu-id="607c6-127">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="607c6-127">**ShellExecute**</span></span>](ishelldispatch2-shellexecute.md)                 | <span data-ttu-id="607c6-128">Выполняет указанную операцию с указанным файлом.</span><span class="sxs-lookup"><span data-stu-id="607c6-128">Performs a specified operation on a specified file.</span></span><br/>                     |
| [<span data-ttu-id="607c6-129">**шовбровсербар**</span><span class="sxs-lookup"><span data-stu-id="607c6-129">**ShowBrowserBar**</span></span>](ishelldispatch2-showbrowserbar.md)             | <span data-ttu-id="607c6-130">Отображает панель браузера.</span><span class="sxs-lookup"><span data-stu-id="607c6-130">Displays a browser bar.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="607c6-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="607c6-131">Remarks</span></span>

<span data-ttu-id="607c6-132">Обсуждение служб Windows см. в документации по [службам](../services/services.md) .</span><span class="sxs-lookup"><span data-stu-id="607c6-132">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="607c6-133">Требования</span><span class="sxs-lookup"><span data-stu-id="607c6-133">Requirements</span></span>



| <span data-ttu-id="607c6-134">Требование</span><span class="sxs-lookup"><span data-stu-id="607c6-134">Requirement</span></span> | <span data-ttu-id="607c6-135">Значение</span><span class="sxs-lookup"><span data-stu-id="607c6-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="607c6-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="607c6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="607c6-137">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="607c6-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="607c6-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="607c6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="607c6-139">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="607c6-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="607c6-140">Header</span><span class="sxs-lookup"><span data-stu-id="607c6-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="607c6-141"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="607c6-141"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="607c6-142">IDL</span><span class="sxs-lookup"><span data-stu-id="607c6-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="607c6-143"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="607c6-143"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="607c6-144">DLL</span><span class="sxs-lookup"><span data-stu-id="607c6-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="607c6-145"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="607c6-145"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="607c6-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="607c6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="607c6-147">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="607c6-147">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="607c6-148">**Объект оболочки**</span><span class="sxs-lookup"><span data-stu-id="607c6-148">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="607c6-149">**ишеллдиспатч**</span><span class="sxs-lookup"><span data-stu-id="607c6-149">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> </dl>

 

 
