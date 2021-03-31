---
title: Подключение к проигрывателю Windows Media
description: Подключение к проигрывателю Windows Media
ms.assetid: c6afbd95-bcf8-438a-b854-776c543a5d51
keywords:
- Подключаемые модули проигрывателя Windows Media, записи реестра
- подключаемые модули, записи реестра
- Подключаемые модули проигрывателя Windows Media, подключение
- подключаемые модули, подключение
- подключаемые модули обработки цифровых сигналов, подключение
- Подключаемые модули DSP, подключение
- подключаемые модули обработки цифровых сигналов, записи реестра
- Подключаемые модули DSP, записи реестра
- реестр, подключаемые модули DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fa0851e271631e2c37bf716c427b5af34ade14
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412480"
---
# <a name="connecting-to-windows-media-player"></a><span data-ttu-id="252ca-112">Подключение к проигрывателю Windows Media</span><span class="sxs-lookup"><span data-stu-id="252ca-112">Connecting to Windows Media Player</span></span>

<span data-ttu-id="252ca-113">Проигрыватель Windows Media автоматически подключается к установленным и правильно зарегистрированным подключаемым модулям DSP.</span><span class="sxs-lookup"><span data-stu-id="252ca-113">Windows Media Player automatically connects to DSP plug-ins that have been installed and properly registered.</span></span> <span data-ttu-id="252ca-114">Подключаемые модули DSP должны вызывать [ивмпмедиаплугинрегистрар:: вмпрегистерплайерплугин](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) для создания записей реестра, необходимых для того, чтобы проигрыватель Windows Media мог распознать подключаемый модуль и вывести его на вкладку **подключаемые** модули диалогового окна Параметры.</span><span class="sxs-lookup"><span data-stu-id="252ca-114">DSP plug-ins must call [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) to create the registry entries necessary to allow Windows Media Player to recognize the plug-in and to list it on the **Plug-ins** tab of the Options dialog box.</span></span> <span data-ttu-id="252ca-115">Чтобы удалить записи реестра, созданные с помощью **ивмпмедиаплугинрегистрар:: вмпрегистерплайерплугин**, подключаемый модуль вызывает [Ивмпмедиаплугинрегистрар:: вмпунрегистерплайерплугин](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin).</span><span class="sxs-lookup"><span data-stu-id="252ca-115">To remove the registry entries created by **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin**, the plug-in calls [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin).</span></span>

## <a name="related-topics"></a><span data-ttu-id="252ca-116">См. также</span><span class="sxs-lookup"><span data-stu-id="252ca-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="252ca-117">**Обзор подключаемого модуля DSP**</span><span class="sxs-lookup"><span data-stu-id="252ca-117">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




