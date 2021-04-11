---
description: Автоматическое преобразование из MTS
ms.assetid: 0848639a-26ce-47ad-8384-8969a7c3bcde
title: Автоматическое преобразование из MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d424a443995c9fff9073878a43543d4c029a2445
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142025"
---
# <a name="automatic-conversion-from-mts"></a><span data-ttu-id="79570-103">Автоматическое преобразование из MTS</span><span class="sxs-lookup"><span data-stu-id="79570-103">Automatic Conversion from MTS</span></span>

<span data-ttu-id="79570-104">Автоматическое преобразование выполняется в два этапа, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="79570-104">Automatic conversion occurs in two steps, as follows:</span></span>

1.  <span data-ttu-id="79570-105">Во время установки Windows.</span><span class="sxs-lookup"><span data-stu-id="79570-105">During Windows setup.</span></span> <span data-ttu-id="79570-106">Преобразование обрабатывается процессом установки Windows с помощью служебной программы МТСТОКОМ.</span><span class="sxs-lookup"><span data-stu-id="79570-106">The conversion is handled by the Windows setup process through the MTSTOCOM utility.</span></span>
    > [!Note]  
    > <span data-ttu-id="79570-107">Если шаг 1 завершается неудачно, некоторые или все пакеты MTS могут быть преобразованы, но при этом могут отсутствовать определенные свойства.</span><span class="sxs-lookup"><span data-stu-id="79570-107">If step 1 fails, some or all of the MTS packages may actually have been converted but may be missing certain properties.</span></span> <span data-ttu-id="79570-108">В этом случае используйте средство администрирования "службы компонентов" для проверки всех атрибутов.</span><span class="sxs-lookup"><span data-stu-id="79570-108">In this case, use the Component Services administrative tool to verify all attributes.</span></span> <span data-ttu-id="79570-109">Атрибуты MTS по-прежнему будут присутствовать на компьютере (в системном реестре на \_ локальном \_ компьютере \\ Microsoft \\ Transaction Server), но будут доступны только через служебную программу regedit.exe.</span><span class="sxs-lookup"><span data-stu-id="79570-109">The MTS attributes will still be present on the computer (in the system registry at HKEY\_LOCAL\_MACHINE\\Microsoft\\Transaction Server) but will be accessible only through the regedit.exe utility.</span></span>

     

2.  <span data-ttu-id="79570-110">После последней перезагрузки перед отображением диалогового окна входа в систему Windows.</span><span class="sxs-lookup"><span data-stu-id="79570-110">After the last reboot before the Windows logon dialog box is displayed.</span></span> <span data-ttu-id="79570-111">Шаг 2 обрабатывает действия преобразования, требующие доступа к сети (в основном создание членов роли).</span><span class="sxs-lookup"><span data-stu-id="79570-111">Step 2 handles those conversion actions that require network access (primarily role member creation).</span></span>
    > [!Note]  
    > <span data-ttu-id="79570-112">Если шаг 2 завершается сбоем (из-за сбоев временных сети или контроллера домена), программа преобразования МТСТОКОМ может быть перезапущена любое количество раз.</span><span class="sxs-lookup"><span data-stu-id="79570-112">If step 2 fails (due to temporary network or domain controller failures), it is possible to rerun the MTSTOCOM conversion utility any number of times.</span></span> <span data-ttu-id="79570-113">Для этого в командной строке или после выбора команды **выполнить** из меню " **Пуск** " введите следующую команду: **% WINDIR% \\ system32 \\mtstocom.exe**.</span><span class="sxs-lookup"><span data-stu-id="79570-113">To do this, at the command prompt or after selecting **Run** from the **Start** menu, type the following: **%windir%\\system32\\mtstocom.exe**.</span></span>

     

## <a name="mtstocom-log-file"></a><span data-ttu-id="79570-114">Файл журнала МТСТОКОМ</span><span class="sxs-lookup"><span data-stu-id="79570-114">MTSTOCOM Log File</span></span>

<span data-ttu-id="79570-115">Служебная программа МТСТОКОМ создает файл журнала (Мтстоком. log) в каталоге Windows.</span><span class="sxs-lookup"><span data-stu-id="79570-115">The MTSTOCOM utility generates a log file (Mtstocom.log) in the Windows directory.</span></span> <span data-ttu-id="79570-116">Этот файл журнала хранит запись о преобразовании из пакетов MTS в приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="79570-116">This log file keeps a record of the conversion from MTS packages to COM+ applications.</span></span> <span data-ttu-id="79570-117">Если во время преобразования возникли ошибки, рекомендуется проверить файл журнала для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="79570-117">If there were any errors during the conversion process, it is always a good idea to check the log file for further information.</span></span> <span data-ttu-id="79570-118">В файле журнала обнаруживаются распространенные проблемы, например недопустимый пользователь или пароль.</span><span class="sxs-lookup"><span data-stu-id="79570-118">The log file catches common problems, such as invalid user or password.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79570-119">См. также</span><span class="sxs-lookup"><span data-stu-id="79570-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79570-120">Результаты и проблемы преобразования COM+</span><span class="sxs-lookup"><span data-stu-id="79570-120">COM+ Conversion Results and Issues</span></span>](com--conversion-results-and-issues.md)
</dt> <dt>

[<span data-ttu-id="79570-121">Ручное преобразование из MTS</span><span class="sxs-lookup"><span data-stu-id="79570-121">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="79570-122">Библиотека администрирования MTS</span><span class="sxs-lookup"><span data-stu-id="79570-122">MTS Administration Library</span></span>](mts-administration-library.md)
</dt> </dl>

 

 



