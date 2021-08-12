---
title: Включение уведомлений
description: Включение уведомлений
ms.assetid: b4fc7714-a7d0-409f-a47c-4903bab883cc
keywords:
- Windows Диспетчер устройств мультимедиа, уведомления
- Диспетчер устройств, уведомления
- инструкции по программированию, уведомления
- Классические приложения, уведомления
- создание Windows мультимедиа диспетчер устройств приложений, уведомления
- Уведомления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ab1b71482db78571f141b7042d8abc926b0d79ca2f487ee7dc961396993b9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585067"
---
# <a name="enabling-notifications"></a>Включение уведомлений

Windows Диспетчер устройств носителя объявляет четыре интерфейса, которые приложение может реализовать в COM-классе для получения уведомлений о событиях. Эти интерфейсы делятся на две группы, как показано в следующей таблице.



| Интерфейсы                                                                                                                                                | Описание                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ивмдмнотификатион**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                            | Уведомляет приложение о том, что устройства или носитель хранилища подключены или отключены.                                                                                         |
| [**ивмдмпрогресс**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)<br/> [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)<br/> [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)<br/> | Очень простая система уведомлений для оповещения приложения о ходе выполнения любого события. Приложению не требуется предпринимать никаких действий в ответ на эти сообщения. |



 

**ивмдмнотификатион**

**Ивмдмнотификатион** предупреждает приложение, когда Самонастраивающийся устройства подключены или отключены от компьютера, а также Самонастраивающийся когда на устройстве вставляются или удаляются съемные носители (например, Флэш-карты). Эти уведомления могут помочь приложению обновить пользовательский интерфейс для отражения изменений.

Чтобы получать эти уведомления, приложение должно зарегистрироваться для получения их с помощью интерфейсов Platform SDK **IConnectionPointContainer** и **IConnectionPoint** . Приложение должно зарегистрироваться для получения событий при запуске и отмены регистрации при закрытии. Выполните следующие действия, чтобы зарегистрироваться для получения этих уведомлений.

1.  Запросите основной интерфейс **ивмдевицеманажер** , полученный при проверке подлинности приложения для **IConnectionPointContainer**.
2.  Вызовите **IConnectionPointContainer:: финдконнектионпоинт** , чтобы получить точку подключения контейнера для интерфейсов **ивмдмнотификатион** .
3.  Зарегистрируйтесь для получения событий, вызвав метод **IConnectionPoint:: Advise**. Передайте класс, который реализует **ивмдмнотификатион**, и извлеките файл cookie, уникальный идентификатор, определяющий точку подключения. Этот параметр должен быть сохранен и использоваться позже для отмены регистрации уведомлений о событиях.

В следующем коде C++ показано, как можно зарегистрироваться для получения уведомлений от **ивмдмнотификатион**.


```C++
HRESULT CWMDMController::RegisterForNotifications()
{
    HRESULT hr = S_OK;
    CComPtr<IConnectionPointContainer> pConxnPointCont;
    CComPtr<IConnectionPoint> pIConnPoint;

    // Get the IConnectionPointContainer interface from IWMDeviceManager.
    if (SUCCEEDED (hr = m_IWMDMDeviceMgr->QueryInterface(IID_IConnectionPointContainer, (void**) & pConxnPointCont)))
    {
        // Get a connection point from the container.
        if (SUCCEEDED (hr = pConxnPointCont->FindConnectionPoint(IID_IWMDMNotification, &pIConnPoint)))
        {
            // Add ourselves as a callback handler for the connection point.
            // If we succeeded, indicate that by storing the connection point ID.
            DWORD dwCookie;
            if (SUCCEEDED (hr = pIConnPoint->Advise((IUnknown*)((IWMDMNotification*)this), &dwCookie)))
            {
                m_dwNotificationCookie = dwCookie;
            }
        }
    }

    return hr;
}
```



При закрытии приложения необходимо отменить регистрацию в **IConnectionPoint** , чтобы указать, что он больше не должен отправлять уведомления. Чтобы отменить регистрацию для получения уведомлений, выполните следующие действия.

1.  Запросите основной интерфейс **ивмдевицеманажер** для **IConnectionPointContainer**.
2.  Получение точки подключения для интерфейсов **ивмдмнотификатион** .
3.  Отмените регистрацию приложения для получения уведомлений о событиях, вызвав метод **IConnectionPoint:: Unregister**, ПЕРЕДАВ уникальный идентификатор, полученный при регистрации на получение событий.

В следующем коде C++ показано, как отменить регистрацию для событий **ивмдмнотификатион** при закрытии приложения.


```C++
HRESULT CWMDMController::UnregisterForNotifications()
{
    HRESULT hr = S_FALSE;

    // On class initialization, we initialized the handle to -1 as a flag 
    // to indicate we had not yet registered for notifications. If registration 
    // never happened, don't bother to unregister.
    if (-1 != m_dwNotificationCookie)
    {
        CComPtr<IConnectionPointContainer> pConxnPointCont;
        CComPtr<IConnectionPoint> pIConnPoint;

        // Get the connection point container from IWMDeviceManager. 
        if (SUCCEEDED (hr = 
           m_IWMDMDeviceMgr->QueryInterface(IID_IConnectionPointContainer,
           (void**) & pConxnPointCont)))
        {
            // Get a connection point from the container.
            if (SUCCEEDED (hr = pConxnPointCont->FindConnectionPoint(IID_IWMDMNotification, &pIConnPoint)))
            {
                // Remove ourselves as a callback from the connection point.
                // If successful, reset the ID to a flag value.
                if (SUCCEEDED (hr = 
                    pIConnPoint->Unadvise(m_dwNotificationCookie)))
                {
                    m_dwNotificationCookie = -1;
                    hr = S_OK;
                }
            }
        }
    }

    return hr;
}
```



**Использование Ивмдмпрогресс**

Windows Носители диспетчер устройств могут отсылать сообщения о состоянии приложения, когда выполняются определенные действия, такие как передача содержимого, безопасное получение данных о часах и возникновение сведений о файлах DRM. Приложение может использовать эти сообщения для отслеживания состояния события или отмены события. Чтобы использовать этот интерфейс, реализуйте [**ивмдмпрогресс**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress), [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)или [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)и передайте его в качестве параметра в метод, который будет принимать сообщение о ходе выполнения. Обратите внимание, что **IWMDMProgress3** является старшим интерфейсом, так как он предоставляет идентификатор GUID, указывающий, какое действие отслеживается. Следующие методы приложения принимают интерфейс выполнения (соответствующие методы поставщика услуг должны иметь возможность отправлять уведомления в отправленный интерфейс):

[**Ивмдмсторажеконтрол::D удалить**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-delete)

[**Ивмдмсторажеконтрол:: INSERT**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)

[**Ивмдмсторажеконтрол:: Move**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-move)

[**Ивмдмсторажеконтрол:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read)

[**Ивмдмсторажеконтрол:: Rename**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-rename)

[**IWMDMStorageControl2::Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)

[**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)

[**Ивмдмсторажеглобалс:: Initialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-initialize)

[**Ивмдрмдевицеапп:: Аккуиредевицедата**](iwmdrmdeviceapp-acquiredevicedata.md)

Примеры передачи интерфейса в метод приведены в документации по этим методам. Примеры реализации интерфейсов обратного вызова см. в документации по методам **ивмдмпрогресс**, **IWMDMProgress2** или **IWMDMProgress3**.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**создание Windows мультимедиа диспетчер устройств приложение**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 





