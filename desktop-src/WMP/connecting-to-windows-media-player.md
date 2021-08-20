---
title: подключение к проигрыватель Windows Media
description: подключение к проигрыватель Windows Media
ms.assetid: c6afbd95-bcf8-438a-b854-776c543a5d51
keywords:
- подключаемые модули проигрыватель Windows Media, записи реестра
- подключаемые модули, записи реестра
- подключаемые модули проигрыватель Windows Media, подключение
- подключаемые модули, подключение
- подключаемые модули обработки цифровых сигналов, подключение
- Подключаемые модули DSP, подключение
- подключаемые модули обработки цифровых сигналов, записи реестра
- Подключаемые модули DSP, записи реестра
- реестр, подключаемые модули DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d266f1715147d3c7631909e8e23e3e7b1f786337c998d188968a96f6c26b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997634"
---
# <a name="connecting-to-windows-media-player"></a>подключение к проигрыватель Windows Media

проигрыватель Windows Media автоматически подключается к подключаемым модулям DSP, которые были установлены и должным образом зарегистрированы. подключаемые модули DSP должны вызывать [ивмпмедиаплугинрегистрар:: вмпрегистерплайерплугин](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) , чтобы создать записи реестра, необходимые для того, чтобы проигрыватель Windows Media распознать подключаемый модуль и вывести его на вкладку **подключаемые** модули диалогового окна параметры. Чтобы удалить записи реестра, созданные с помощью **ивмпмедиаплугинрегистрар:: вмпрегистерплайерплугин**, подключаемый модуль вызывает [Ивмпмедиаплугинрегистрар:: вмпунрегистерплайерплугин](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Обзор подключаемого модуля DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




