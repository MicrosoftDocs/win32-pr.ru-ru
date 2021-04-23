---
description: Существует множество ситуаций, в которых может потребоваться временно или постоянно отключить автозапуск.
ms.assetid: 5e65a3d8-04b9-46ba-b4e5-a976e1923bfd
title: Включение и отключение автозапуска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567f50db75cd129346e193e66ba0ae5f74fa955
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423722"
---
# <a name="enabling-and-disabling-autorun"></a><span data-ttu-id="674f0-103">Включение и отключение автозапуска</span><span class="sxs-lookup"><span data-stu-id="674f0-103">Enabling and Disabling AutoRun</span></span>

<span data-ttu-id="674f0-104">Существует множество ситуаций, в которых может потребоваться временно или постоянно отключить автозапуск.</span><span class="sxs-lookup"><span data-stu-id="674f0-104">There are many situations where AutoRun may need to be temporarily or persistently disabled.</span></span> <span data-ttu-id="674f0-105">Например, функция автозапуска может мешать работе работающего приложения и должна быть отключена в течение длительного времени.</span><span class="sxs-lookup"><span data-stu-id="674f0-105">For example, AutoRun might interfere with the operation of a running application and need to be disabled for the duration.</span></span> <span data-ttu-id="674f0-106">Система предоставляет несколько способов отключения функции AutoRun.</span><span class="sxs-lookup"><span data-stu-id="674f0-106">The system provides several ways to disable AutoRun.</span></span>

-   [<span data-ttu-id="674f0-107">Подавление автозапуска программным способом</span><span class="sxs-lookup"><span data-stu-id="674f0-107">Suppressing AutoRun Programmatically</span></span>](#suppressing-autorun-programmatically)
-   [<span data-ttu-id="674f0-108">Отключение автозапуска с помощью реестра</span><span class="sxs-lookup"><span data-stu-id="674f0-108">Using the Registry to Disable AutoRun</span></span>](#using-the-registry-to-disable-autorun)
-   [<span data-ttu-id="674f0-109">Автозапуск для других типов носителей хранилища</span><span class="sxs-lookup"><span data-stu-id="674f0-109">AutoRun for Other Types of Storage Media</span></span>](#autorun-for-other-types-of-storage-media)

## <a name="suppressing-autorun-programmatically"></a><span data-ttu-id="674f0-110">Подавление автозапуска программным способом</span><span class="sxs-lookup"><span data-stu-id="674f0-110">Suppressing AutoRun Programmatically</span></span>

<span data-ttu-id="674f0-111">Существует множество ситуаций, в которых может потребоваться подавлять Автозапуск программным способом.</span><span class="sxs-lookup"><span data-stu-id="674f0-111">There are a variety of situations where AutoRun may need to be suppressed programmatically.</span></span> <span data-ttu-id="674f0-112">Ниже приведены два примера:</span><span class="sxs-lookup"><span data-stu-id="674f0-112">Two examples are:</span></span>

-   <span data-ttu-id="674f0-113">Приложение содержит программу установки, которая требует, чтобы пользователь вставил другой диск, который может содержать файл autorun. INF.</span><span class="sxs-lookup"><span data-stu-id="674f0-113">Your application has a setup program that requires the user to insert another disc that may contain an Autorun.inf file.</span></span>
-   <span data-ttu-id="674f0-114">Во время работы приложения пользователю может потребоваться вставить другой диск, который может содержать файл autorun. INF.</span><span class="sxs-lookup"><span data-stu-id="674f0-114">During the operation of your application, the user may need to insert another disc that may contain an Autorun.inf file.</span></span>

<span data-ttu-id="674f0-115">В любом случае, как правило, не требуется запускать другое приложение во время выполнения исходной операции.</span><span class="sxs-lookup"><span data-stu-id="674f0-115">In either case, you will normally not want to launch another application while the original is in progress.</span></span>

<span data-ttu-id="674f0-116">Пользователи могут вручную отключить автозапуск, удерживая клавишу SHIFT при вставке компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="674f0-116">Users can manually suppress AutoRun by holding down the SHIFT key when they insert the CD-ROM.</span></span> <span data-ttu-id="674f0-117">Однако обычно предпочтительнее выполнять эту операцию программно, а не в зависимости от пользователя.</span><span class="sxs-lookup"><span data-stu-id="674f0-117">However, it is usually preferable to handle this operation programmatically rather than depending on the user.</span></span>

<span data-ttu-id="674f0-118">В системах с оболочкой [версии 4,70](versions.md) и более поздней Windows отправляет сообщение "куериканцелаутоплай" в передний план.</span><span class="sxs-lookup"><span data-stu-id="674f0-118">With systems that have Shell [version 4.70](versions.md) and later, Windows sends a "QueryCancelAutoPlay" message to the foreground window.</span></span> <span data-ttu-id="674f0-119">Приложение может ответить на это сообщение, чтобы отключить автозапуск.</span><span class="sxs-lookup"><span data-stu-id="674f0-119">Your application can respond to this message to suppress AutoRun.</span></span> <span data-ttu-id="674f0-120">Этот подход используется системными служебными программами, такими как [Открытие](../dlgbox/open-and-save-as-dialog-boxes.md) общего диалогового окна для отключения автозапуска.</span><span class="sxs-lookup"><span data-stu-id="674f0-120">This approach is used by system utilities such as the [Open](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog box to disable AutoRun.</span></span>

<span data-ttu-id="674f0-121">В следующих фрагментах кода показано, как настроить и обработано это сообщение.</span><span class="sxs-lookup"><span data-stu-id="674f0-121">The following code fragments illustrate how to set up and handle this message.</span></span> <span data-ttu-id="674f0-122">Приложение должно работать в окне переднего плана.</span><span class="sxs-lookup"><span data-stu-id="674f0-122">Your application must be running in the foreground window.</span></span> <span data-ttu-id="674f0-123">Сначала зарегистрируйте "Куериканцелаутоплай" как сообщение Windows:</span><span class="sxs-lookup"><span data-stu-id="674f0-123">First, register "QueryCancelAutoPlay" as a Windows message:</span></span>


```C++
uMessage = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
```



<span data-ttu-id="674f0-124">Для получения этого сообщения окно приложения должно быть на переднем плане.</span><span class="sxs-lookup"><span data-stu-id="674f0-124">Your application's window must be in the foreground to receive this message.</span></span> <span data-ttu-id="674f0-125">Обработчик сообщений должен возвращать **значение true** , чтобы отменить автозапуск, и **false** , чтобы включить его.</span><span class="sxs-lookup"><span data-stu-id="674f0-125">The message handler should return **TRUE** to cancel AutoRun and **FALSE** to enable it.</span></span> <span data-ttu-id="674f0-126">В следующем фрагменте кода показано, как использовать это сообщение для отключения функции AutoRun.</span><span class="sxs-lookup"><span data-stu-id="674f0-126">The following code fragment illustrates how to use this message to disable AutoRun.</span></span>


```C++
UINT g_uQueryCancelAutoPlay = 0;

LRESULT WndProc(HWND hwnd, UINT uMsg,  WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ... 
    default: 
        if (!g_uQueryCancelAutoPlay)
        { 
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg && uMsg == g_uQueryCancelAutoPlay)
        { 
            return TRUE;       // Cancel AutoRun
        }
    }
}
```



<span data-ttu-id="674f0-127">Если приложение использует диалоговое окно и должно реагировать на сообщение "Куериканцелаутоплай", оно не может просто возвращать **значение true** или **false**.</span><span class="sxs-lookup"><span data-stu-id="674f0-127">If your application is using a dialog box and needs to respond to a "QueryCancelAutoPlay" message, it cannot simply return **TRUE** or **FALSE**.</span></span> <span data-ttu-id="674f0-128">Вместо этого вызовите [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) с параметром *ниндекс* , установленным в значение **DWL \_ мсгресулт**.</span><span class="sxs-lookup"><span data-stu-id="674f0-128">Instead, call [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) with *nIndex* set to **DWL\_MSGRESULT**.</span></span> <span data-ttu-id="674f0-129">Задайте для параметра *Двневлонг* **значение true** , чтобы отменить автозапуск, и **false** , чтобы включить ее.</span><span class="sxs-lookup"><span data-stu-id="674f0-129">Set the *dwNewLong* parameter to **TRUE** to cancel AutoRun, and **FALSE** to enable it.</span></span> <span data-ttu-id="674f0-130">Например, следующий пример процедуры диалогового окна отменяет Автозапуск при получении сообщения "Куериканцелаутоплай".</span><span class="sxs-lookup"><span data-stu-id="674f0-130">For example, the following sample dialog box procedure cancels AutoRun when it receives a "QueryCancelAutoPlay" message.</span></span>


```C++
UINT g_uQueryCancelAutoPlay = 0;

BOOL DialogProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ...
    default: 
        if (!g_uQueryCancelAutoPlay)
        {
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg == g_uQueryCancelAutoPlay) 
        {
            SetWindowLong(hDlg, DWL_MSGRESULT, TRUE);          
            return 1;               
        }
    } 
```



## <a name="using-the-registry-to-disable-autorun"></a><span data-ttu-id="674f0-131">Отключение автозапуска с помощью реестра</span><span class="sxs-lookup"><span data-stu-id="674f0-131">Using the Registry to Disable AutoRun</span></span>

<span data-ttu-id="674f0-132">Существует два значения реестра, которые можно использовать для постоянного отключения AutoRun: Нодривеауторун и Нодриветипеауторун.</span><span class="sxs-lookup"><span data-stu-id="674f0-132">There are two registry values that can be used to persistently disable AutoRun: NoDriveAutoRun and NoDriveTypeAutoRun.</span></span> <span data-ttu-id="674f0-133">Первое значение отключает автозапуск для указанных букв диска, а второй отключает автозапуск для класса дисков.</span><span class="sxs-lookup"><span data-stu-id="674f0-133">The first value disables AutoRun for specified drive letters and the second disables AutoRun for a class of drives.</span></span> <span data-ttu-id="674f0-134">Если одно из этих значений имеет значение отключить автозапуск для конкретного устройства, оно будет отключено.</span><span class="sxs-lookup"><span data-stu-id="674f0-134">If either of these values is set to disable AutoRun for a particular device, it will be disabled.</span></span> <span data-ttu-id="674f0-135">Дополнительные сведения об отключении функций автозапуска см. в статье базы знаний [как отключить функцию автозапуска в Windows](https://support.microsoft.com/kb/967715) .</span><span class="sxs-lookup"><span data-stu-id="674f0-135">See the Knowledge Base article [How to disable the Autorun functionality in Windows](https://support.microsoft.com/kb/967715) for more information on disabling AutoRun functionality.</span></span> <span data-ttu-id="674f0-136">В этой статье перечислены различные обновления, которые необходимо установить, чтобы правильно отключить функцию автозапуска.</span><span class="sxs-lookup"><span data-stu-id="674f0-136">This article lists the different updates that you must have installed to correctly disable the Autorun functionality.</span></span>

> [!Note]  
> <span data-ttu-id="674f0-137">Значения Нодривеауторун и Нодриветипеауторун должны быть изменены только системными администраторами для изменения значения всей системы в целях тестирования или администрирования.</span><span class="sxs-lookup"><span data-stu-id="674f0-137">The NoDriveAutoRun and NoDriveTypeAutoRun values should only be modified by system administrators to change the value for the entire system for testing or administrative purposes.</span></span> <span data-ttu-id="674f0-138">Приложения не должны изменять эти значения, так как не существует способа надежного восстановления их исходных значений.</span><span class="sxs-lookup"><span data-stu-id="674f0-138">Applications should not modify these values, as there is no way to reliably restore them to their original values.</span></span>

 

<span data-ttu-id="674f0-139">Значение Нодривеауторун отключает автозапуск для указанных букв диска.</span><span class="sxs-lookup"><span data-stu-id="674f0-139">The NoDriveAutoRun value disables AutoRun for specified drive letters.</span></span> <span data-ttu-id="674f0-140">Это \_ значение реестра типа DWORD, которое находится в следующем разделе:</span><span class="sxs-lookup"><span data-stu-id="674f0-140">It is a REG\_DWORD data value, found under the following key:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

<span data-ttu-id="674f0-141">Первый бит значения соответствует диску A:, второму — B: и т. д.</span><span class="sxs-lookup"><span data-stu-id="674f0-141">The first bit of the value corresponds to drive A:, the second to B:, and so on.</span></span> <span data-ttu-id="674f0-142">Чтобы отключить функцию AutoRun для одного или нескольких букв диска, установите соответствующие биты.</span><span class="sxs-lookup"><span data-stu-id="674f0-142">To disable AutoRun for one or more drive letters, set the corresponding bits.</span></span> <span data-ttu-id="674f0-143">Например, чтобы отключить диски A: и C:, задайте для Нодривеауторун значение `0x00000005` .</span><span class="sxs-lookup"><span data-stu-id="674f0-143">For example, to disable the A: and C: drives, set NoDriveAutoRun to `0x00000005`.</span></span>

<span data-ttu-id="674f0-144">Значение Нодриветипеауторун отключает автозапуск для класса дисков.</span><span class="sxs-lookup"><span data-stu-id="674f0-144">The NoDriveTypeAutoRun value disables AutoRun for a class of drives.</span></span> <span data-ttu-id="674f0-145">Это \_ двоичное значение в формате DWORD или 4-байтового типа \_ данных reg, которое находится в том же ключе.</span><span class="sxs-lookup"><span data-stu-id="674f0-145">It is a REG\_DWORD or 4-byte REG\_BINARY data value, found under the same key.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

<span data-ttu-id="674f0-146">Установив биты первого байта этого значения, можно исключить другие диски из работы с функцией автозапуска.</span><span class="sxs-lookup"><span data-stu-id="674f0-146">By setting the bits of this value's first byte, different drives can be excluded from working with AutoRun.</span></span>

<span data-ttu-id="674f0-147">В следующей таблице приводятся константы битов и битовой маски, которые можно задать в первом байте Нодриветипеауторун, чтобы отключить автозапуск для определенного типа диска.</span><span class="sxs-lookup"><span data-stu-id="674f0-147">The following table gives the bits and bitmask constants, that can be set in the first byte of NoDriveTypeAutoRun to disable AutoRun for a particular drive type.</span></span> <span data-ttu-id="674f0-148">Чтобы изменения вступили в силу, необходимо перезапустить проводник Windows.</span><span class="sxs-lookup"><span data-stu-id="674f0-148">You must restart Windows Explorer before the changes take effect.</span></span>



| <span data-ttu-id="674f0-149">Разрядное число</span><span class="sxs-lookup"><span data-stu-id="674f0-149">Bit Number</span></span> | <span data-ttu-id="674f0-150">Константа битовой маски</span><span class="sxs-lookup"><span data-stu-id="674f0-150">Bitmask Constant</span></span>      | <span data-ttu-id="674f0-151">Описание</span><span class="sxs-lookup"><span data-stu-id="674f0-151">Description</span></span>                                             |
|------------|-----------------------|---------------------------------------------------------|
| <span data-ttu-id="674f0-152">0x04</span><span class="sxs-lookup"><span data-stu-id="674f0-152">0x04</span></span>       | <span data-ttu-id="674f0-153">**ДИСК \_ ПЕРЕмещается**</span><span class="sxs-lookup"><span data-stu-id="674f0-153">**DRIVE\_REMOVEABLE**</span></span> | <span data-ttu-id="674f0-154">Диск можно удалить с диска (например, с дискеты).</span><span class="sxs-lookup"><span data-stu-id="674f0-154">Disk can be removed from drive (such as a floppy disk).</span></span> |
| <span data-ttu-id="674f0-155">0x08</span><span class="sxs-lookup"><span data-stu-id="674f0-155">0x08</span></span>       | <span data-ttu-id="674f0-156">**ДИСК \_ фиксирован**</span><span class="sxs-lookup"><span data-stu-id="674f0-156">**DRIVE\_FIXED**</span></span>      | <span data-ttu-id="674f0-157">Невозможно удалить диск из накопителя (жесткий диск).</span><span class="sxs-lookup"><span data-stu-id="674f0-157">Disk cannot be removed from drive (a hard disk).</span></span>        |
| <span data-ttu-id="674f0-158">0x10</span><span class="sxs-lookup"><span data-stu-id="674f0-158">0x10</span></span>       | <span data-ttu-id="674f0-159">**ДИСК \_ удаленно**</span><span class="sxs-lookup"><span data-stu-id="674f0-159">**DRIVE\_REMOTE**</span></span>     | <span data-ttu-id="674f0-160">Сетевой диск.</span><span class="sxs-lookup"><span data-stu-id="674f0-160">Network drive.</span></span>                                          |
| <span data-ttu-id="674f0-161">0x20</span><span class="sxs-lookup"><span data-stu-id="674f0-161">0x20</span></span>       | <span data-ttu-id="674f0-162">**ДИСКОВОД \_ CDROM**</span><span class="sxs-lookup"><span data-stu-id="674f0-162">**DRIVE\_CDROM**</span></span>      | <span data-ttu-id="674f0-163">Дисковод компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="674f0-163">CD-ROM drive.</span></span>                                           |
| <span data-ttu-id="674f0-164">0x40</span><span class="sxs-lookup"><span data-stu-id="674f0-164">0x40</span></span>       | <span data-ttu-id="674f0-165">**ДИСК \_ Ramdisk**</span><span class="sxs-lookup"><span data-stu-id="674f0-165">**DRIVE\_RAMDISK**</span></span>    | <span data-ttu-id="674f0-166">ЭЛЕКТРОННЫЙ диск.</span><span class="sxs-lookup"><span data-stu-id="674f0-166">RAM disk.</span></span>                                               |



 

## <a name="autorun-for-other-types-of-storage-media"></a><span data-ttu-id="674f0-167">Автозапуск для других типов носителей хранилища</span><span class="sxs-lookup"><span data-stu-id="674f0-167">AutoRun for Other Types of Storage Media</span></span>

<span data-ttu-id="674f0-168">Автозапуск в основном предназначен для общедоступного распространения приложений на компакт-дисках и DVD-ДИСКах, и его использование не рекомендуется для других носителей.</span><span class="sxs-lookup"><span data-stu-id="674f0-168">AutoRun is primarily intended for public distribution of applications on CD-ROM and DVD-ROM, and its use is discouraged for other storage media.</span></span> <span data-ttu-id="674f0-169">Однако часто бывает полезно включить автоматический запуск на съемных носителях других типов.</span><span class="sxs-lookup"><span data-stu-id="674f0-169">However, it is often useful to enable AutoRun on other types of removable storage media.</span></span> <span data-ttu-id="674f0-170">Эта функция обычно используется для упрощения отладки файлов AutoRun. INF.</span><span class="sxs-lookup"><span data-stu-id="674f0-170">This feature is typically used simplify the debugging of AutoRun.inf files.</span></span> <span data-ttu-id="674f0-171">Автозапуск работает только на съемных устройствах хранения при соблюдении следующих условий.</span><span class="sxs-lookup"><span data-stu-id="674f0-171">AutoRun only works on removable storage devices when the following criteria are met:</span></span>

-   <span data-ttu-id="674f0-172">Устройство должно иметь драйверы, совместимые с автозапуском.</span><span class="sxs-lookup"><span data-stu-id="674f0-172">The device must have AutoRun-compatible drivers.</span></span> <span data-ttu-id="674f0-173">Чтобы обеспечить совместимость с автозагрузкаю, драйвер должен уведомить систему о том, что диск вставлен, отправив сообщение [**WM \_ девицечанже**](../devio/wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="674f0-173">To be AutoRun-compatible, a driver must notify the system that a disk has been inserted by sending a [**WM\_DEVICECHANGE**](../devio/wm-devicechange.md) message.</span></span>
-   <span data-ttu-id="674f0-174">Корневой каталог вставленного носителя должен содержать файл autorun. INF.</span><span class="sxs-lookup"><span data-stu-id="674f0-174">The root directory of the inserted media must contain an Autorun.inf file.</span></span>
-   <span data-ttu-id="674f0-175">На устройстве не должно быть отключено Автозагрузка с помощью [реестра](#using-the-registry-to-disable-autorun).</span><span class="sxs-lookup"><span data-stu-id="674f0-175">The device must not have AutoRun disabled through the [registry](#using-the-registry-to-disable-autorun).</span></span>
-   <span data-ttu-id="674f0-176">Приложение переднего плана не [подавляет](#suppressing-autorun-programmatically) автозапуск.</span><span class="sxs-lookup"><span data-stu-id="674f0-176">The foreground application has not [suppressed](#suppressing-autorun-programmatically) AutoRun.</span></span>

> [!Note]  
> <span data-ttu-id="674f0-177">Эта функция не должна использоваться для распространения приложений на съемные носители.</span><span class="sxs-lookup"><span data-stu-id="674f0-177">This feature should not be used to distribute applications on removable media.</span></span> <span data-ttu-id="674f0-178">Поскольку реализация автозапуска на съемных носителях обеспечивает простой способ распространения компьютерных вирусов, пользователи должны быть подозрительными на общедоступной распределенной гибкой дискете, содержащей файл autorun. INF.</span><span class="sxs-lookup"><span data-stu-id="674f0-178">Because implementing AutoRun on removable media provides an easy way to spread computer viruses, users should be suspicious of any publicly distributed floppy disk that contains an Autorun.inf file.</span></span>

 

<span data-ttu-id="674f0-179">Обычно Автозапуск запускается автоматически, но его также можно запустить вручную.</span><span class="sxs-lookup"><span data-stu-id="674f0-179">Normally, AutoRun starts automatically, but it can also be started manually.</span></span> <span data-ttu-id="674f0-180">Если устройство соответствует указанным выше критериям, в контекстном меню буквы диска будет указана команда **автозапуска** .</span><span class="sxs-lookup"><span data-stu-id="674f0-180">If the device meets the criteria listed above, the drive letter's shortcut menu will include an **AutoPlay** command.</span></span> <span data-ttu-id="674f0-181">Чтобы запустить автоматический запуск вручную, щелкните правой кнопкой мыши значок диска и выберите **Автозапуск** в контекстном меню или дважды щелкните значок диска.</span><span class="sxs-lookup"><span data-stu-id="674f0-181">To run AutoRun manually, either right-click the drive icon and select **AutoPlay** from the shortcut menu or double-click the drive icon.</span></span> <span data-ttu-id="674f0-182">Если драйверы не совместимы с автозапуском, в контекстном меню не будет элемента **автозапуска** , и запуск автозапуска невозможен.</span><span class="sxs-lookup"><span data-stu-id="674f0-182">If the drivers are not AutoRun-compatible, the shortcut menu will not have an **AutoPlay** item and AutoRun cannot be started.</span></span>

<span data-ttu-id="674f0-183">Драйверы, совместимые с автозапуском, предоставляются с помощью некоторых съемных дисков, а также некоторых других типов съемных носителей, например адаптеров CompactFlash.</span><span class="sxs-lookup"><span data-stu-id="674f0-183">AutoRun-compatible drivers are provided with some removable disk drives, as well as some other types of removable media such as CompactFlash cards.</span></span> <span data-ttu-id="674f0-184">Автозапуск также работает с сетевыми дисками, которые сопоставлены с буквой диска с помощью проводника Windows или подключены к [консоли управления (MMC)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page).</span><span class="sxs-lookup"><span data-stu-id="674f0-184">AutoRun also works with network drives that are mapped to a drive letter with Windows Explorer or mounted with the [Microsoft Management Console (MMC)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page).</span></span> <span data-ttu-id="674f0-185">Как и в случае с подключенным оборудованием, подключенный сетевой диск должен иметь файл autorun. INF в корневом каталоге и не должен быть отключен в [реестре](#using-the-registry-to-disable-autorun).</span><span class="sxs-lookup"><span data-stu-id="674f0-185">As with mounted hardware, a mounted network drive must have an Autorun.inf file in its root directory, and must not be disabled through the [registry](#using-the-registry-to-disable-autorun).</span></span>

 

 
