---
title: Использование обратного вызова OnStatus
description: Использование обратного вызова OnStatus
ms.assetid: 598e2d13-709b-42a3-ae06-b8c7d208ca9e
keywords:
- Пакет SDK для формата Windows Media, метод обратного вызова OnStatus
- Windows Media Format SDK, интерфейс Ивмстатускаллбакк
- Метод обратного вызова OnStatus, сведения
- ивмстатускаллбакк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e96b8d7fd75fd8a1d97a56c8b09304c51d0238
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103987174"
---
# <a name="using-the-onstatus-callback"></a>Использование обратного вызова OnStatus

Метод обратного вызова [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) вызывается несколькими объектами в пакете SDK формата Windows Media. **OnStatus** получает сообщения, представляющие изменения в состоянии операций пакета SDK.

Чтобы использовать метод обратного вызова **OnStatus** , необходимо реализовать в приложении класс, наследующий от интерфейса [**ивмстатускаллбакк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) . Включите код для вашей версии **OnStatus** в класс. Несколько примеров реализации **OnStatus** можно найти в образцах, поставляемых с этим пакетом SDK. Дополнительные сведения о примерах см. в разделе [примеры приложений](sample-applications.md).

Необходимо связать реализацию функции обратного вызова состояния с различными объектами пакета SDK Windows Media Format. Для каждого объекта существует другой способ выполнения этой ассоциации. Список методов, связывающих определенные объекты, см. на странице справочника по **ивмстатускаллбакк** .

Сообщения о состоянии, которые могут быть получены параметром **OnStatus** , определяются в типе перечисления [**\_ состояния ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) .

Вы можете выбрать сообщения для перехвата и игнорировать их. Однако для некоторых функций требуется реагирование на некоторые сообщения о состоянии. Например, при использовании асинхронного модуля чтения метод [**ивмреадер:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) открывает файл асинхронно. Единственный способ определить, когда файл был открыт, — это перехват \_ сообщения МВт Opened. Как правило, сообщения, на которые вы отвечаете, являются уведомлениями о завершении асинхронных задач.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Использование методов обратного вызова**](using-the-callback-methods.md)
</dt> </dl>

 

 




