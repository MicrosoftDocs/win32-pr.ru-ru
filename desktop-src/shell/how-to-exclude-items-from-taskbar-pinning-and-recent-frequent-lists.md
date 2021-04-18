---
description: Приложения, процессы и Windows могут сделать недоступными для закрепления на панели задач или для включения в список наиболее часто используемых программных решений в меню "Пуск".
title: Как исключить элементы из закрепления панели задач и последних или часто встречающихся списков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7f32ad641832703804f94b8cc28f47ea9cabb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985441"
---
# <a name="how-to-exclude-items-from-taskbar-pinning-and-recentfrequent-lists"></a><span data-ttu-id="66890-103">Как исключить элементы из закрепления панели задач и последних или часто встречающихся списков</span><span class="sxs-lookup"><span data-stu-id="66890-103">How to Exclude Items from Taskbar Pinning and Recent/Frequent Lists</span></span>

<span data-ttu-id="66890-104">Приложения, процессы и Windows могут сделать недоступными для закрепления на панели задач или для включения в список наиболее часто используемых программных решений в меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="66890-104">Applications, processes, and windows can opt to make themselves unavailable for pinning to the taskbar or for inclusion in the **Start** menu's Most Frequently Used (MFU) list.</span></span>

## <a name="instructions"></a><span data-ttu-id="66890-105">Инструкции</span><span class="sxs-lookup"><span data-stu-id="66890-105">Instructions</span></span>


<span data-ttu-id="66890-106">Существует три механизма для выполнения исключения элементов из списка закрепления панели задач и последних или часто встречающихся списков.</span><span class="sxs-lookup"><span data-stu-id="66890-106">There are three mechanisms to accomplish the exclusion of items from taskbar pinning and recent/frequent lists:</span></span>

-   <span data-ttu-id="66890-107">Добавьте запись OnStartPage в регистрацию приложения, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="66890-107">Add the NoStartPage entry to the application's registration as shown in this example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    <span data-ttu-id="66890-108">Данные, связанные с записью "OnStartPage", игнорируются.</span><span class="sxs-lookup"><span data-stu-id="66890-108">The data associated with the NoStartPage entry is ignored.</span></span> <span data-ttu-id="66890-109">Требуется только присутствие записи.</span><span class="sxs-lookup"><span data-stu-id="66890-109">Only the presence of the entry is required.</span></span> <span data-ttu-id="66890-110">Таким образом, идеальный тип для OnStartPage — **reg \_ None**.</span><span class="sxs-lookup"><span data-stu-id="66890-110">Therefore, the ideal type for NoStartPage is **REG\_NONE**.</span></span>

    <span data-ttu-id="66890-111">Обратите внимание, что любое использование явного идентификатора модели пользователя приложения (AppUserModelID) переопределяет запись OnStartPage.</span><span class="sxs-lookup"><span data-stu-id="66890-111">Note that any use of an explicit Application User Model ID (AppUserModelID) overrides the NoStartPage entry.</span></span> <span data-ttu-id="66890-112">Если явный AppUserModelID применяется к ярлыку, процессу или окну, он становится также прикрепляемые и доступен для списка наиболее часто используемых в меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="66890-112">If an explicit AppUserModelID is applied to a shortcut, process, or window, it becomes pinnable and eligible for the **Start** menu MFU list.</span></span>

-   <span data-ttu-id="66890-113">Задайте свойство [System. аппусермодел. превентпиннинг](../properties/props-system-appusermodel-preventpinning.md) в окнах и сочетаниях клавиш.</span><span class="sxs-lookup"><span data-stu-id="66890-113">Set the [System.AppUserModel.PreventPinning](../properties/props-system-appusermodel-preventpinning.md) property on windows and shortcuts.</span></span> <span data-ttu-id="66890-114">Это свойство должно быть установлено в окне до установки свойства [ \_ аппусермодел \_ ID для PKEY](../properties/props-system-appusermodel-id.md) .</span><span class="sxs-lookup"><span data-stu-id="66890-114">This property must be set on a window before the [PKEY\_AppUserModel\_ID](../properties/props-system-appusermodel-id.md) property is set.</span></span>
-   <span data-ttu-id="66890-115">Добавьте явный AppUserModelID в качестве значения в следующий подраздел реестра, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="66890-115">Add an explicit AppUserModelID as a value under the following registry subkey as shown in this example:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    <span data-ttu-id="66890-116">Каждая запись является значением **reg \_ null** с именем AppUserModelID.</span><span class="sxs-lookup"><span data-stu-id="66890-116">Each entry is a **REG\_NULL** value with the name of the AppUserModelID.</span></span> <span data-ttu-id="66890-117">Любой AppUserModelID, найденный в этом списке, не также прикрепляемые и не может быть включен в список часто используемых меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="66890-117">Any AppUserModelID that is found in this list is not pinnable and not eligible for inclusion in the **Start** menu MFU list.</span></span>

## <a name="remarks"></a><span data-ttu-id="66890-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="66890-118">Remarks</span></span>

<span data-ttu-id="66890-119">Имейте в виду, что определенные исполняемые файлы, а также ярлыки, содержащие определенные строки в своих именах, автоматически исключаются из закрепления и включения в список часто используемых программ.</span><span class="sxs-lookup"><span data-stu-id="66890-119">Be aware that certain executable files, as well as shortcuts that contain certain strings in their names, are automatically excluded from pinning and inclusion in the MFU list.</span></span>

> [!Note]  
> <span data-ttu-id="66890-120">Это автоматическое исключение можно переопределить, применив явный AppUserModelID.</span><span class="sxs-lookup"><span data-stu-id="66890-120">This automatic exclusion can be overridden by applying an explicit AppUserModelID.</span></span>

 

<span data-ttu-id="66890-121">Если любая из следующих строк, независимо от регистра, включается в имя ярлыка, программа не также прикрепляемые и не отображается в списке наиболее часто используемых (неприменимо к Windows 10):</span><span class="sxs-lookup"><span data-stu-id="66890-121">If any of the following strings, regardless of case, are included in the shortcut name, the program is not pinnable and is not displayed in the most frequently used list (not applicable to Windows 10):</span></span>

-   <span data-ttu-id="66890-122">Документация</span><span class="sxs-lookup"><span data-stu-id="66890-122">Documentation</span></span>
-   <span data-ttu-id="66890-123">Справка</span><span class="sxs-lookup"><span data-stu-id="66890-123">Help</span></span>
-   <span data-ttu-id="66890-124">Установка</span><span class="sxs-lookup"><span data-stu-id="66890-124">Install</span></span>
-   <span data-ttu-id="66890-125">Подробнее</span><span class="sxs-lookup"><span data-stu-id="66890-125">More Info</span></span>
-   <span data-ttu-id="66890-126">Чтение</span><span class="sxs-lookup"><span data-stu-id="66890-126">Read me</span></span>
-   <span data-ttu-id="66890-127">Сначала прочитать</span><span class="sxs-lookup"><span data-stu-id="66890-127">Read First</span></span>
-   <span data-ttu-id="66890-128">Readme</span><span class="sxs-lookup"><span data-stu-id="66890-128">Readme</span></span>
-   <span data-ttu-id="66890-129">Удалить</span><span class="sxs-lookup"><span data-stu-id="66890-129">Remove</span></span>
-   <span data-ttu-id="66890-130">Настройка</span><span class="sxs-lookup"><span data-stu-id="66890-130">Setup</span></span>
-   <span data-ttu-id="66890-131">Поддержка</span><span class="sxs-lookup"><span data-stu-id="66890-131">Support</span></span>
-   <span data-ttu-id="66890-132">What's New</span><span class="sxs-lookup"><span data-stu-id="66890-132">What's New</span></span>

<span data-ttu-id="66890-133">Следующий список программ не также прикрепляемые и исключен из списка наиболее часто используемых:</span><span class="sxs-lookup"><span data-stu-id="66890-133">The following list of programs are not pinnable and are excluded from the most frequently used list:</span></span>

-   <span data-ttu-id="66890-134">Applaunch.exe</span><span class="sxs-lookup"><span data-stu-id="66890-134">Applaunch.exe</span></span>
-   <span data-ttu-id="66890-135">Control.exe</span><span class="sxs-lookup"><span data-stu-id="66890-135">Control.exe</span></span>
-   <span data-ttu-id="66890-136">Dfsvc.exe</span><span class="sxs-lookup"><span data-stu-id="66890-136">Dfsvc.exe</span></span>
-   <span data-ttu-id="66890-137">Dllhost.exe</span><span class="sxs-lookup"><span data-stu-id="66890-137">Dllhost.exe</span></span>
-   <span data-ttu-id="66890-138">Guestmodemsg.exe</span><span class="sxs-lookup"><span data-stu-id="66890-138">Guestmodemsg.exe</span></span>
-   <span data-ttu-id="66890-139">Hh.exe</span><span class="sxs-lookup"><span data-stu-id="66890-139">Hh.exe</span></span>
-   <span data-ttu-id="66890-140">Install.exe</span><span class="sxs-lookup"><span data-stu-id="66890-140">Install.exe</span></span>
-   <span data-ttu-id="66890-141">Isuninst.exe</span><span class="sxs-lookup"><span data-stu-id="66890-141">Isuninst.exe</span></span>
-   <span data-ttu-id="66890-142">Lnkstub.exe</span><span class="sxs-lookup"><span data-stu-id="66890-142">Lnkstub.exe</span></span>
-   <span data-ttu-id="66890-143">Mmc.exe</span><span class="sxs-lookup"><span data-stu-id="66890-143">Mmc.exe</span></span>
-   <span data-ttu-id="66890-144">Mshta.exe</span><span class="sxs-lookup"><span data-stu-id="66890-144">Mshta.exe</span></span>
-   <span data-ttu-id="66890-145">Msiexec.exe</span><span class="sxs-lookup"><span data-stu-id="66890-145">Msiexec.exe</span></span>
-   <span data-ttu-id="66890-146">Msoobe.exe</span><span class="sxs-lookup"><span data-stu-id="66890-146">Msoobe.exe</span></span>
-   <span data-ttu-id="66890-147">Rundll32.exe</span><span class="sxs-lookup"><span data-stu-id="66890-147">Rundll32.exe</span></span>
-   <span data-ttu-id="66890-148">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="66890-148">Setup.exe</span></span>
-   <span data-ttu-id="66890-149">St5unst.exe</span><span class="sxs-lookup"><span data-stu-id="66890-149">St5unst.exe</span></span>
-   <span data-ttu-id="66890-150">Unwise.exe</span><span class="sxs-lookup"><span data-stu-id="66890-150">Unwise.exe</span></span>
-   <span data-ttu-id="66890-151">Unwise32.exe</span><span class="sxs-lookup"><span data-stu-id="66890-151">Unwise32.exe</span></span>
-   <span data-ttu-id="66890-152">Werfault.exe</span><span class="sxs-lookup"><span data-stu-id="66890-152">Werfault.exe</span></span>
-   <span data-ttu-id="66890-153">Winhlp32.exe</span><span class="sxs-lookup"><span data-stu-id="66890-153">Winhlp32.exe</span></span>
-   <span data-ttu-id="66890-154">Wlrmdr.exe</span><span class="sxs-lookup"><span data-stu-id="66890-154">Wlrmdr.exe</span></span>
-   <span data-ttu-id="66890-155">Wuapp.exe</span><span class="sxs-lookup"><span data-stu-id="66890-155">Wuapp.exe</span></span>

<span data-ttu-id="66890-156">Приведенные выше списки хранятся в следующих значениях реестра.</span><span class="sxs-lookup"><span data-stu-id="66890-156">The preceding lists are stored in the following registry values.</span></span>

> [!Note]  
> <span data-ttu-id="66890-157">Эти списки не должны изменяться приложениями.</span><span class="sxs-lookup"><span data-stu-id="66890-157">These lists should not be modified by applications.</span></span> <span data-ttu-id="66890-158">Используйте один из методов списка исключений, описанных ранее в этом разделе, для того же интерфейса.</span><span class="sxs-lookup"><span data-stu-id="66890-158">Use one of the exclusion list methods described earlier in this topic for the same experience.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a><span data-ttu-id="66890-159">См. также</span><span class="sxs-lookup"><span data-stu-id="66890-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66890-160">Панель задач</span><span class="sxs-lookup"><span data-stu-id="66890-160">The Taskbar</span></span>](taskbar.md)
</dt> <dt>

[<span data-ttu-id="66890-161">Расширения панели задач</span><span class="sxs-lookup"><span data-stu-id="66890-161">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 
