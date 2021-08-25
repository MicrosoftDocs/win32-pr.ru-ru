---
description: Нельзя задать временные подписки с помощью средства администрирования "службы компонентов". Для создания или обновления временной подписки необходимо использовать административные интерфейсы COM+.
ms.assetid: 28d48d59-abb2-4682-ab54-60b6aa7b31b1
title: Регистрация временной подписки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f93b543a4602b0b4ed7ed4177133f3eb8f543a0db02750af8657ab36f310993
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990444"
---
# <a name="registering-a-transient-subscription"></a>Регистрация временной подписки

Временные подписки запрашивают событие для определенного объекта подписчика, который уже существует. Временные подписки хранятся в каталоге COM+, но подписка удаляется при остановке системы событий или операционной системы. В отличие от постоянных подписок, временные подписки привязаны к определенному объекту и хранятся только в системе событий. Если возникла проблема с системой событий или операционной системой, подписка исчезнет. Временные подписки могут быть более эффективными, чем постоянные подписки, но необходимо управлять жизненным циклом объектов.

Нельзя задать временные подписки с помощью средства администрирования "службы компонентов". Для создания или обновления временной подписки необходимо использовать административные интерфейсы COM+.

## <a name="visual-basic"></a>Visual Basic

В следующей процедуре описано, как создать временную подписку с помощью Microsoft Visual Basic.

1.  Укажите временную подписку, добавив новую запись в коллекцию [**трансиентсубскриптионс**](transientsubscriptions.md) и задав для свойства Субскриберинтерфаце интерфейс [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) объекта подписчика. События COM+ не создают новый экземпляр объекта подписчика при срабатывании события, а используют указанный вами экземпляр. События COM+ содержат счетчик ссылок для объекта подписчика до тех пор, пока подписка не будет удалена из системы.
2.  Создайте серверное приложение COM+ (.exe, .dll или OCX-файл) с объектом, реализующим интерфейсы или методы, на которые необходимо подписываться.
3.  Создайте временную подписку с помощью следующего кода, передав идентификатор CLSID объекта [класса событий](the-com--event-class-object.md) и экземпляра объекта подписчика. С помощью средства администрирования "службы компонентов" можно получить свойство Евентклсид, щелкнув правой кнопкой мыши компонент COM+, выбрав пункт " **Свойства**" и выбрав вкладку " **Общие** ".

    ``` syntax
    Public Function CreateTransientSubscription( _
      ByVal clsid As String, ByVal objref As Object) As String 
        Dim oCOMAdminCatalog As COMAdmin.COMAdminCatalog
        Dim oTSCol As COMAdminCatalogCollection
        Dim oSubscription As ICatalogObject
        Dim objvar As Variant
        On Error GoTo CreateTransientSubscriptionError
        Set oCOMAdminCatalog = CreateObject("COMAdmin.COMAdminCatalog")
        'Gets the TransientSubscriptions collection
        Set oTSCol = oCOMAdminCatalog.GetCollection( _
          "TransientSubscriptions")
        Set oSubscription = oTSCol.Add
        Set objvar = objref
        oSubscription.Value("SubscriberInterface") = objref
        oSubscription.Value("EventCLSID") = clsid
        oSubscription.Value("Name") = "TransientSubscription"
        oTSCol.SaveChanges
        CreateTransientSubscription = oSubscription.Value("ID")
        Set oSubscription = Nothing
        Set oTSCol = Nothing
        Set oCOMAdminCatalog = Nothing
        Set objvar = Nothing
        Exit Function
    CreateTransientSubscriptionError:
        CreateTransientSubscription = ""
        Err.Raise Err.Number, "[CreateTransientSubscription]" & _
          Err.Source, Err.Description
    End Function
    ```

В следующем примере показано, как вызвать функцию Креатетрансиентсубскриптион для подписки на интерфейс с именем Истокктиккер, который имеет метод с именем Упдатестокк.

1.  Создайте класс событий, который поддерживает интерфейс Истокктиккер с одним методом Упдатестокк.
2.  В проекте подписчика добавьте класс, реализующий интерфейс Истокктиккер.
3.  Если вы хотите подписываться, выполните следующий код:

    ``` syntax
    Dim oMyTicker As Object
    Dim sSubscriptionID As String
    Set oMyTicker = CreateObject("TheProject.CMyTicker")
    sSubscriptionID = CreateTransientSubscription( _
      "{..CLSID for the Event Class..}", oMyTicker)
    ```

Функция Креатетрансиентсубскриптион возвращает строку, которая представляет собой идентификатор GUID, который можно использовать в качестве обработчика или файла cookie для последующего отзыва подписки. Чтобы удалить подписку, вызовите метод [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**Комадминкаталогколлектион**](comadmincatalogcollection.md) в коллекции [**трансиентсубскриптионс**](transientsubscriptions.md) , передав индекс, соответствующий подписке, с ранее полученным идентификатором GUID.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Регистрация подписки](registering-a-subscription.md)
</dt> </dl>

 

 
