---
title: Включение уведомлений
description: Включение уведомлений
ms.assetid: b4fc7714-a7d0-409f-a47c-4903bab883cc
keywords:
- Диспетчер устройств Windows Media, уведомления
- Диспетчер устройств, уведомления
- инструкции по программированию, уведомления
- Классические приложения, уведомления
- Создание приложений диспетчер устройств Windows Media, уведомления
- Уведомления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618356c9d63d20a8b6b14e6c99072074cfc75073
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775233"
---
# <a name="enabling-notifications"></a><span data-ttu-id="a886d-109">Включение уведомлений</span><span class="sxs-lookup"><span data-stu-id="a886d-109">Enabling Notifications</span></span>

<span data-ttu-id="a886d-110">Диспетчер устройств Windows Media объявляет четыре интерфейса, которые приложение может реализовать в COM-классе для получения уведомлений о событиях.</span><span class="sxs-lookup"><span data-stu-id="a886d-110">Windows Media Device Manager declares four interfaces that an application can implement in a COM class to receive event notifications.</span></span> <span data-ttu-id="a886d-111">Эти интерфейсы делятся на две группы, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a886d-111">These interfaces fall into two groups, as shown in the following table.</span></span>



| <span data-ttu-id="a886d-112">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="a886d-112">Interfaces</span></span>                                                                                                                                                | <span data-ttu-id="a886d-113">Описание</span><span class="sxs-lookup"><span data-stu-id="a886d-113">Description</span></span>                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a886d-114">**ивмдмнотификатион**</span><span class="sxs-lookup"><span data-stu-id="a886d-114">**IWMDMNotification**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                            | <span data-ttu-id="a886d-115">Уведомляет приложение о том, что устройства или носитель хранилища подключены или отключены.</span><span class="sxs-lookup"><span data-stu-id="a886d-115">Notifies the application when devices or storage media are connected or disconnected.</span></span>                                                                                         |
| [<span data-ttu-id="a886d-116">**ивмдмпрогресс**</span><span class="sxs-lookup"><span data-stu-id="a886d-116">**IWMDMProgress**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)<br/> [<span data-ttu-id="a886d-117">**IWMDMProgress2**</span><span class="sxs-lookup"><span data-stu-id="a886d-117">**IWMDMProgress2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)<br/> [<span data-ttu-id="a886d-118">**IWMDMProgress3**</span><span class="sxs-lookup"><span data-stu-id="a886d-118">**IWMDMProgress3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)<br/> | <span data-ttu-id="a886d-119">Очень простая система уведомлений для оповещения приложения о ходе выполнения любого события.</span><span class="sxs-lookup"><span data-stu-id="a886d-119">A very simple notification system to alert an application about the progress of any event.</span></span> <span data-ttu-id="a886d-120">Приложению не требуется предпринимать никаких действий в ответ на эти сообщения.</span><span class="sxs-lookup"><span data-stu-id="a886d-120">The application is not required to take any actions in response to these messages.</span></span> |



 

<span data-ttu-id="a886d-121">**ивмдмнотификатион**</span><span class="sxs-lookup"><span data-stu-id="a886d-121">**IWMDMNotification**</span></span>

<span data-ttu-id="a886d-122">**Ивмдмнотификатион** предупреждает приложение, когда Самонастраивающийся устройства подключены или отключены от компьютера, а также Самонастраивающийся когда на устройстве вставляются или удаляются съемные носители (например, Флэш-карты).</span><span class="sxs-lookup"><span data-stu-id="a886d-122">**IWMDMNotification** alerts the application when Plug and Play devices are connected or disconnected from the computer, as well as when Plug and Play storage media (such as flash cards) are inserted or removed from the device.</span></span> <span data-ttu-id="a886d-123">Эти уведомления могут помочь приложению обновить пользовательский интерфейс для отражения изменений.</span><span class="sxs-lookup"><span data-stu-id="a886d-123">These notifications can help the application update its user interface to reflect changes.</span></span>

<span data-ttu-id="a886d-124">Чтобы получать эти уведомления, приложение должно зарегистрироваться для получения их с помощью интерфейсов Platform SDK **IConnectionPointContainer** и **IConnectionPoint** .</span><span class="sxs-lookup"><span data-stu-id="a886d-124">In order to receive these notifications, your application must register to receive them using the Platform SDK **IConnectionPointContainer** and **IConnectionPoint** interfaces.</span></span> <span data-ttu-id="a886d-125">Приложение должно зарегистрироваться для получения событий при запуске и отмены регистрации при закрытии.</span><span class="sxs-lookup"><span data-stu-id="a886d-125">Your application should register to receive events when it starts up, and unregister when it closes.</span></span> <span data-ttu-id="a886d-126">Выполните следующие действия, чтобы зарегистрироваться для получения этих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a886d-126">Follow these steps to register to receive these notifications.</span></span>

1.  <span data-ttu-id="a886d-127">Запросите основной интерфейс **ивмдевицеманажер** , полученный при проверке подлинности приложения для **IConnectionPointContainer**.</span><span class="sxs-lookup"><span data-stu-id="a886d-127">Query the main **IWMDeviceManager** interface you received when you authenticated your application for **IConnectionPointContainer**.</span></span>
2.  <span data-ttu-id="a886d-128">Вызовите **IConnectionPointContainer:: финдконнектионпоинт** , чтобы получить точку подключения контейнера для интерфейсов **ивмдмнотификатион** .</span><span class="sxs-lookup"><span data-stu-id="a886d-128">Call **IConnectionPointContainer::FindConnectionPoint** to retrieve a container connection point for **IWMDMNotification** interfaces.</span></span>
3.  <span data-ttu-id="a886d-129">Зарегистрируйтесь для получения событий, вызвав метод **IConnectionPoint:: Advise**.</span><span class="sxs-lookup"><span data-stu-id="a886d-129">Register to receive events by calling **IConnectionPoint::Advise**.</span></span> <span data-ttu-id="a886d-130">Передайте класс, который реализует **ивмдмнотификатион**, и извлеките файл cookie, уникальный идентификатор, определяющий точку подключения.</span><span class="sxs-lookup"><span data-stu-id="a886d-130">Pass in the class that implements **IWMDMNotification**, and retrieve a cookie, a unique ID that identifies your connection point.</span></span> <span data-ttu-id="a886d-131">Этот параметр должен быть сохранен и использоваться позже для отмены регистрации уведомлений о событиях.</span><span class="sxs-lookup"><span data-stu-id="a886d-131">This must be stored, and used later to unregister for event notifications.</span></span>

<span data-ttu-id="a886d-132">В следующем коде C++ показано, как можно зарегистрироваться для получения уведомлений от **ивмдмнотификатион**.</span><span class="sxs-lookup"><span data-stu-id="a886d-132">The following C++ code demonstrates how you can register to receive notifications from **IWMDMNotification**.</span></span>


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



<span data-ttu-id="a886d-133">При закрытии приложения необходимо отменить регистрацию в **IConnectionPoint** , чтобы указать, что он больше не должен отправлять уведомления.</span><span class="sxs-lookup"><span data-stu-id="a886d-133">When your application closes, you must unregister with **IConnectionPoint** to indicate that it should no longer send you notifications.</span></span> <span data-ttu-id="a886d-134">Чтобы отменить регистрацию для получения уведомлений, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a886d-134">Follow these steps to unregister for notifications:</span></span>

1.  <span data-ttu-id="a886d-135">Запросите основной интерфейс **ивмдевицеманажер** для **IConnectionPointContainer**.</span><span class="sxs-lookup"><span data-stu-id="a886d-135">Query the main **IWMDeviceManager** interface for **IConnectionPointContainer**.</span></span>
2.  <span data-ttu-id="a886d-136">Получение точки подключения для интерфейсов **ивмдмнотификатион** .</span><span class="sxs-lookup"><span data-stu-id="a886d-136">Get a connection point for **IWMDMNotification** interfaces.</span></span>
3.  <span data-ttu-id="a886d-137">Отмените регистрацию приложения для получения уведомлений о событиях, вызвав метод **IConnectionPoint:: Unregister**, ПЕРЕДАВ уникальный идентификатор, полученный при регистрации на получение событий.</span><span class="sxs-lookup"><span data-stu-id="a886d-137">Unregister your application for event notifications by calling **IConnectionPoint::Unadvise**, passing in the unique ID received when you registered to receive events.</span></span>

<span data-ttu-id="a886d-138">В следующем коде C++ показано, как отменить регистрацию для событий **ивмдмнотификатион** при закрытии приложения.</span><span class="sxs-lookup"><span data-stu-id="a886d-138">The following C++ code shows how to unregister for **IWMDMNotification** events when your application closes.</span></span>


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



<span data-ttu-id="a886d-139">**Использование Ивмдмпрогресс**</span><span class="sxs-lookup"><span data-stu-id="a886d-139">**Using IWMDMProgress**</span></span>

<span data-ttu-id="a886d-140">Windows Media диспетчер устройств может отсылать сообщения о состоянии приложения, когда выполняются определенные действия, такие как передача содержимого, безопасное получение данных о часах и возникновение сведений о файлах DRM.</span><span class="sxs-lookup"><span data-stu-id="a886d-140">Windows Media Device Manager can send your application status messages when specific actions, such as content transfer, secure clock acquisition, and encountering DRM file information, occur.</span></span> <span data-ttu-id="a886d-141">Приложение может использовать эти сообщения для отслеживания состояния события или отмены события.</span><span class="sxs-lookup"><span data-stu-id="a886d-141">Your application can use these messages to monitor the status of the event or cancel an event.</span></span> <span data-ttu-id="a886d-142">Чтобы использовать этот интерфейс, реализуйте [**ивмдмпрогресс**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress), [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)или [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)и передайте его в качестве параметра в метод, который будет принимать сообщение о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="a886d-142">To use this interface, implement [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress), [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2), or [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3), and pass it in as a parameter to a method that will accept a progress message.</span></span> <span data-ttu-id="a886d-143">Обратите внимание, что **IWMDMProgress3** является старшим интерфейсом, так как он предоставляет идентификатор GUID, указывающий, какое действие отслеживается.</span><span class="sxs-lookup"><span data-stu-id="a886d-143">Note that **IWMDMProgress3** is the superior interface because it provides an identification GUID that specifies what action is being tracked.</span></span> <span data-ttu-id="a886d-144">Следующие методы приложения принимают интерфейс выполнения (соответствующие методы поставщика услуг должны иметь возможность отправлять уведомления в отправленный интерфейс):</span><span class="sxs-lookup"><span data-stu-id="a886d-144">The following application methods accept a progress interface (the corresponding service provider methods should be able to send notifications to a submitted interface):</span></span>

[<span data-ttu-id="a886d-145">**Ивмдмсторажеконтрол::D удалить**</span><span class="sxs-lookup"><span data-stu-id="a886d-145">**IWMDMStorageControl::Delete**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-delete)

[<span data-ttu-id="a886d-146">**Ивмдмсторажеконтрол:: INSERT**</span><span class="sxs-lookup"><span data-stu-id="a886d-146">**IWMDMStorageControl::Insert**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)

[<span data-ttu-id="a886d-147">**Ивмдмсторажеконтрол:: Move**</span><span class="sxs-lookup"><span data-stu-id="a886d-147">**IWMDMStorageControl::Move**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-move)

[<span data-ttu-id="a886d-148">**Ивмдмсторажеконтрол:: Read**</span><span class="sxs-lookup"><span data-stu-id="a886d-148">**IWMDMStorageControl::Read**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read)

[<span data-ttu-id="a886d-149">**Ивмдмсторажеконтрол:: Rename**</span><span class="sxs-lookup"><span data-stu-id="a886d-149">**IWMDMStorageControl::Rename**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-rename)

[<span data-ttu-id="a886d-150">**IWMDMStorageControl2::Insert2**</span><span class="sxs-lookup"><span data-stu-id="a886d-150">**IWMDMStorageControl2::Insert2**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)

[<span data-ttu-id="a886d-151">**IWMDMStorageControl3::Insert3**</span><span class="sxs-lookup"><span data-stu-id="a886d-151">**IWMDMStorageControl3::Insert3**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)

[<span data-ttu-id="a886d-152">**Ивмдмсторажеглобалс:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="a886d-152">**IWMDMStorageGlobals::Initialize**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-initialize)

[<span data-ttu-id="a886d-153">**Ивмдрмдевицеапп:: Аккуиредевицедата**</span><span class="sxs-lookup"><span data-stu-id="a886d-153">**IWMDRMDeviceApp::AcquireDeviceData**</span></span>](iwmdrmdeviceapp-acquiredevicedata.md)

<span data-ttu-id="a886d-154">Примеры передачи интерфейса в метод приведены в документации по этим методам.</span><span class="sxs-lookup"><span data-stu-id="a886d-154">Examples of passing an interface into a method are given in the documentation for these methods.</span></span> <span data-ttu-id="a886d-155">Примеры реализации интерфейсов обратного вызова см. в документации по методам **ивмдмпрогресс**, **IWMDMProgress2** или **IWMDMProgress3**.</span><span class="sxs-lookup"><span data-stu-id="a886d-155">For examples of implementing the callback interfaces, see the documentation for the methods of **IWMDMProgress**, **IWMDMProgress2**, or **IWMDMProgress3**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a886d-156">См. также</span><span class="sxs-lookup"><span data-stu-id="a886d-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a886d-157">**Создание приложения диспетчер устройств Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a886d-157">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 





