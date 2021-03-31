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
# <a name="connecting-to-windows-media-player"></a>Подключение к проигрывателю Windows Media

Проигрыватель Windows Media автоматически подключается к установленным и правильно зарегистрированным подключаемым модулям DSP. Подключаемые модули DSP должны вызывать [ивмпмедиаплугинрегистрар:: вмпрегистерплайерплугин](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) для создания записей реестра, необходимых для того, чтобы проигрыватель Windows Media мог распознать подключаемый модуль и вывести его на вкладку **подключаемые** модули диалогового окна Параметры. Чтобы удалить записи реестра, созданные с помощью **ивмпмедиаплугинрегистрар:: вмпрегистерплайерплугин**, подключаемый модуль вызывает [Ивмпмедиаплугинрегистрар:: вмпунрегистерплайерплугин](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Обзор подключаемого модуля DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




