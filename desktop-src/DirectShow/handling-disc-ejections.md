---
description: Обработка извлечения с диска
ms.assetid: c43dd795-749b-4ca7-8510-71d62e0076b3
title: Обработка извлечения с диска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8964c8fd18395e932e1536e885bae1814d5952fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894053"
---
# <a name="handling-disc-ejections"></a>Обработка извлечения с диска

Когда пользователь извлекает DVD-диск из дисковода, Навигатор DVD отправляет в приложение \_ сообщение, извлеченное с DVD- \_ диска EC \_ . Приложение может спокойно проигнорировать это сообщение и позволить DVD-навигатору управлять состоянием графика. Приложение также может \_ \_ использовать извлеченный с DVD-диска EC \_ метод для реализации пользовательского поведения при извлечении диска. При обработке сообщения необходимо установить \_ для флага РЕСЕТОНСТОП DVD **значение true** с помощью метода [**SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) , а затем вызвать [**имедиаконтрол:: остановитесь**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) перед закрытием приложения или воспроизведением другого диска.

## <a name="related-topics"></a>См. также

<dl> <dt>

[DVD-приложения](dvd-applications.md)
</dt> </dl>

 

 



