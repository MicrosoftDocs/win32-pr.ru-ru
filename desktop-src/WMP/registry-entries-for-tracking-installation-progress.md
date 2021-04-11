---
title: Записи реестра для отслеживания хода установки
description: Записи реестра для отслеживания хода установки
ms.assetid: 898f9117-94fd-4230-9378-b8c6a4401a96
keywords:
- Проигрыватель Windows Media, отслеживание хода выполнения установки
- Проигрыватель Windows Media, отслеживание хода выполнения установки
- Проигрыватель Windows Media, отслеживание хода установки
- Проигрыватель Windows Media, реестр
- реестр, отслеживание хода выполнения установки
- реестр, отслеживание хода установки
- реестр, отслеживание хода установки
- реестр, параметры для проигрывателя Windows Media
- Отслеживание хода установки
- Установка отслеживания хода выполнения
- Отслеживание хода установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3add1d2feb668ee90418704b9a11b0072530f120
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068606"
---
# <a name="registry-entries-for-tracking-installation-progress"></a><span data-ttu-id="0dadf-114">Записи реестра для отслеживания хода установки</span><span class="sxs-lookup"><span data-stu-id="0dadf-114">Registry Entries for Tracking Installation Progress</span></span>

<span data-ttu-id="0dadf-115">Программа установки проигрывателя Windows Media 11, программа установки \_wm.exe, записывает в реестр следующие записи, чтобы программы установки могли отслеживать ход выполнения программы установки проигрывателя Windows Media во время ее выполнения.</span><span class="sxs-lookup"><span data-stu-id="0dadf-115">The Windows Media Player 11 setup program, setup\_wm.exe, writes the following entries in the registry so that installation programs can track the progress of the Windows Media Player setup program as it runs.</span></span>


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Setup]
"Progress_CurrentDialog" = dword:value
"Progress_MaxDialog" = dword:value
"Progress_CurrentInstall" = dword:value
"Progress_MaxInstall" = dword:value
```



<span data-ttu-id="0dadf-116">В приведенном выше синтаксисе реестра *value* является заполнителем для целочисленного значения.</span><span class="sxs-lookup"><span data-stu-id="0dadf-116">In the preceding registry syntax, *value* is a placeholder for an integer value.</span></span>

<span data-ttu-id="0dadf-117">Куррентдиалог хода выполнения \_ указывает, какое диалоговое окно программа установки проигрывателя Windows Media Player в данный момент отображает.</span><span class="sxs-lookup"><span data-stu-id="0dadf-117">Progress\_CurrentDialog indicates which dialog box Windows Media Player setup is currently displaying.</span></span> <span data-ttu-id="0dadf-118">Максдиалог хода выполнения \_ указывает общее количество диалоговых окон, отображаемых Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0dadf-118">Progress\_MaxDialog indicates the total number of dialog boxes that Windows Media will display.</span></span> <span data-ttu-id="0dadf-119">Например, если \_ куррентдиалог = 2 и Progress \_ максдиалог = 5, проигрыватель Windows Media в настоящее время отображает второе диалоговое окно в последовательности, равной пяти.</span><span class="sxs-lookup"><span data-stu-id="0dadf-119">For example, if Progress\_CurrentDialog = 2 and Progress\_MaxDialog = 5, Windows Media Player is currently displaying the second dialog box in a sequence of five.</span></span>

<span data-ttu-id="0dadf-120">\_Куррентинсталл и ход выполнения \_ максинсталл, взятые вместе, указывают процент завершения текущего диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0dadf-120">Progress\_CurrentInstall and Progress\_MaxInstall, taken together, indicate the percent of completion of the current dialog.</span></span> <span data-ttu-id="0dadf-121">Например, если \_ куррентинсталл = 6 и Progress \_ максинсталл = 25, то текущим диалоговым окном является 6/25 (то есть 24%) завершения.</span><span class="sxs-lookup"><span data-stu-id="0dadf-121">For example, if Progress\_CurrentInstall = 6 and Progress\_MaxInstall = 25, the current dialog is 6/25 (that is, 24%) complete.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0dadf-122">См. также</span><span class="sxs-lookup"><span data-stu-id="0dadf-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0dadf-123">**Параметры реестра**</span><span class="sxs-lookup"><span data-stu-id="0dadf-123">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




