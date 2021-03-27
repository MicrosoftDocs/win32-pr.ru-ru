---
description: В этом кратком руководстве показано, как вызвать всплывающее уведомление из классического приложения.
title: Отправка всплывающего уведомления с рабочего стола
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1D20ED75-E24A-4e60-91AB-CFCBE902A68E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: 36f9da25c20d99da74be30046fc5f9f4789dfd73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910767"
---
# <a name="quickstart-sending-a-toast-notification-from-the-desktop"></a>Краткое руководство. отправка всплывающего уведомления с рабочего стола

В этом кратком руководстве показано, как вызвать всплывающее уведомление из классического приложения.

## <a name="prerequisites"></a>Предварительные условия

-   Библиотеки
    -   C++: Runtime. Object. lib
    -   C \# : Windows. winmd
-   На начальном экране должен быть установлен ярлык приложения с [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md). Однако обратите внимание, что его не нужно закреплять на начальном экране. Дополнительные сведения см. [в статье Включение всплывающих уведомлений на рабочем столе с помощью AppUserModelID](enable-desktop-toast-with-appusermodelid.md).
-   Версия Microsoft Visual Studio, поддерживающая не менее Windows 8

## <a name="instructions"></a>Инструкции

### <a name="1-create-your-toast-content"></a>1. Создание содержимого всплывающего уведомления

> [!Note]  
> При указании шаблона всплывающего уведомления, включающего изображение, следует учитывать, что классические приложения могут использовать только локальные образы. веб-изображения не поддерживаются. Кроме того, путь к локальному файлу изображения должен быть указан как абсолютный (не относительный) путь.

 


```csharp
// Get a toast XML template
XmlDocument toastXml = ToastNotificationManager.GetTemplateContent(ToastTemplateType.ToastImageAndText04);

// Fill in the text elements
XmlNodeList stringElements = toastXml.GetElementsByTagName("text");
for (int i = 0; i < stringElements.Length; i++)
{
    stringElements[i].AppendChild(toastXml.CreateTextNode("Line " + i));
}

// Specify the absolute path to an image
String imagePath = "file:///" + Path.GetFullPath("toastImageAndText.png");
XmlNodeList imageElements = toastXml.GetElementsByTagName("image");

ToastNotification toast = new ToastNotification(toastXml);
```



### <a name="2-create-and-attach-the-event-handlers"></a>2. Создание и присоединение обработчиков событий

Регистрация обработчиков для событий всплывающих уведомлений: активировано, отклонено и сбой. Классическое приложение должно иметь по крайней мере подписываться на событие activated, чтобы оно может справиться с ожидаемой активацией приложения из всплывающего уведомления, когда пользователь его выбирает.


```csharp
toast.Activated += ToastActivated;
toast.Dismissed += ToastDismissed;
toast.Failed += ToastFailed;
```



### <a name="3-send-the-toast"></a>3. отправка всплывающего уведомления

> [!IMPORTANT]
> Вы должны включить [AppUserModelID](../properties/props-system-appusermodel-id.md) для ярлыка приложения на начальном экране при каждом вызове [**креатетоастнотифиер**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041). Если этого не сделать, ваше всплывающее уведомление отображаться не будет.

 


```csharp
ToastNotificationManager.CreateToastNotifier(appID).Show(toast);
```



### <a name="4-handle-the-callbacks"></a>4. Обработайте обратные вызовы

Переведите окно приложения на передний план, если оно получает "активированный" обратный вызов из всплывающего уведомления. Когда пользователь выбирает всплывающее уведомление, ожидание заключается в том, что приложение будет запускаться в представлении, связанном с содержимым этого всплывающего уведомления.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Отправка всплывающих уведомлений из примера классического приложения](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)
</dt> <dt>

[Включение всплывающих уведомлений рабочего стола через AppUserModelID](enable-desktop-toast-with-appusermodelid.md)
</dt> <dt>

[XML-схема всплывающих уведомлений](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

[Обзор всплывающих уведомлений](/previous-versions/windows/apps/hh779727(v=win.10))
</dt> <dt>

[Краткое руководство. отправка всплывающего уведомления](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Краткое руководство. отправка всплывающего push-уведомления](/previous-versions/windows/hh761487(v=win.10))
</dt> <dt>

[Рекомендации и контрольный список для всплывающих уведомлений](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[Выбор и использование шаблона всплывающих уведомлений](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Как выполнять активацию с помощью всплывающего уведомления](/previous-versions/windows/apps/hh761468(v=win.10))
</dt> <dt>

[Как принять участие в всплывающих уведомлениях](/previous-versions/windows/apps/hh781238(v=win.10))
</dt> <dt>

[Выбор шаблона всплывающего уведомления](/previous-versions/windows/apps/hh761494(v=win.10))
</dt> <dt>

[Параметры звука всплывающего уведомления](/previous-versions/windows/apps/hh761492(v=win.10))
</dt> </dl>

 

 
