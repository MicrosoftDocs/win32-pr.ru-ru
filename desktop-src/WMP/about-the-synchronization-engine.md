---
title: Сведения о модуле синхронизации
description: Сведения о модуле синхронизации
ms.assetid: bb57ffb0-3833-463b-b66c-c23224fa2ba7
keywords:
- Проигрыватель Windows Media, модуль синхронизации
- Объектная модель проигрывателя Windows Media, модуль синхронизации
- Объектная модель, модуль синхронизации
- Элемент управления ActiveX проигрывателя Windows Media, модуль синхронизации
- Элемент управления ActiveX, модуль синхронизации
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, модуль синхронизации
- Проигрыватель Windows Media Mobile, модуль синхронизации
- синхронизация устройств, модуль синхронизации
- синхронизация устройств, модуль синхронизации
- модуль синхронизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe0768c4805b074fdaf628a25daf47b9ced97ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412539"
---
# <a name="about-the-synchronization-engine"></a><span data-ttu-id="8850f-113">Сведения о модуле синхронизации</span><span class="sxs-lookup"><span data-stu-id="8850f-113">About the Synchronization Engine</span></span>

<span data-ttu-id="8850f-114">Модуль синхронизации — это компонент проигрывателя Windows Media, который управляет копированием цифрового мультимедийного содержимого на портативные устройства.</span><span class="sxs-lookup"><span data-stu-id="8850f-114">The synchronization engine is the component of Windows Media Player that manages copying digital media content to portable devices.</span></span> <span data-ttu-id="8850f-115">Проигрыватель Windows Media поддерживает один экземпляр модуля синхронизации для каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="8850f-115">Windows Media Player supports a single instance of the synchronization engine for each device.</span></span> <span data-ttu-id="8850f-116">Для выполнения задач синхронизации программным способом необходимо использовать удаленный экземпляр элемента управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8850f-116">You must use a remoted instance of the Windows Media Player control to perform synchronization tasks programmatically.</span></span> <span data-ttu-id="8850f-117">По сути, программа совместно использует экземпляры модуля синхронизации с проигрывателем Windows Media и другими программами, которые используют интерфейсы проигрывателя для синхронизации устройств.</span><span class="sxs-lookup"><span data-stu-id="8850f-117">In effect, your program shares the synchronization engine instances with Windows Media Player and all other programs that use the Player interfaces for device synchronization.</span></span>

<span data-ttu-id="8850f-118">Можно использовать [ивмпсинкдевице:: Start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) и [ивмпсинкдевице:: останавливаться](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) для управления тем, когда модуль синхронизации выполняет свою работу.</span><span class="sxs-lookup"><span data-stu-id="8850f-118">You can use [IWMPSyncDevice::start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) and [IWMPSyncDevice::stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) to control when the synchronization engine does its work.</span></span> <span data-ttu-id="8850f-119">В большинстве случаев не следует использовать эти методы.</span><span class="sxs-lookup"><span data-stu-id="8850f-119">In most cases, you should not use these methods.</span></span> <span data-ttu-id="8850f-120">Вместо этого следует разрешить модулю синхронизации запланировать свою работу автоматически.</span><span class="sxs-lookup"><span data-stu-id="8850f-120">Instead, you should let the synchronization engine schedule its work automatically.</span></span> <span data-ttu-id="8850f-121">Методы **Start** и **останавливают** существуют, поэтому их можно использовать, если программа предназначена для замены пользовательского интерфейса проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8850f-121">The **start** and **stop** methods exist so that you can use them if your program is designed to replace the Windows Media Player user interface.</span></span> <span data-ttu-id="8850f-122">В этом случае может потребоваться кнопка запуска и окончания, аналогичная одному проигрывателю Windows Media на вкладке **устройства** .</span><span class="sxs-lookup"><span data-stu-id="8850f-122">In this case, you might want to provide a start/stop button similar to the one Windows Media Player provides in the **Devices** tab.</span></span>

<span data-ttu-id="8850f-123">Ход выполнения синхронизации для устройства можно отслеживать с помощью опроса [ивмпсинкдевице:: Get \_ Progress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress).</span><span class="sxs-lookup"><span data-stu-id="8850f-123">You can monitor the synchronization progress for a device by polling [IWMPSyncDevice::get\_progress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress).</span></span> <span data-ttu-id="8850f-124">Этот метод получает значение хода выполнения для всего процесса синхронизации с определенным устройством.</span><span class="sxs-lookup"><span data-stu-id="8850f-124">This method retrieves a progress value for the entire synchronization process with a particular device.</span></span> <span data-ttu-id="8850f-125">Полученное значение представляет собой число, представляющее процент выполнения синхронизации.</span><span class="sxs-lookup"><span data-stu-id="8850f-125">The value retrieved is a number that represents the percentage of synchronization complete.</span></span> <span data-ttu-id="8850f-126">Есть два события, которые можно получить, связанные с синхронизацией.</span><span class="sxs-lookup"><span data-stu-id="8850f-126">There are two events you can receive that are related to synchronization.</span></span> <span data-ttu-id="8850f-127">Событие **девицесинцеррор** уведомляет о возникновении проблемы.</span><span class="sxs-lookup"><span data-stu-id="8850f-127">The **DeviceSyncError** event notifies you when a problem occurs.</span></span> <span data-ttu-id="8850f-128">Событие **девицесинкстатечанже** предупреждает о смене состояния обработчика синхронизации для текущего устройства.</span><span class="sxs-lookup"><span data-stu-id="8850f-128">The **DeviceSyncStateChange** event alerts you when the synchronization engine has changed state for the current device.</span></span>

<span data-ttu-id="8850f-129">Можно ограничить объем хранилища устройств, используемого проигрывателем Windows Media для синхронизации, вызвав [IWMPSyncDevice2:: сетитеминфо](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) с атрибутом **перцентспацересервед** .</span><span class="sxs-lookup"><span data-stu-id="8850f-129">You can limit the amount of device storage that Windows Media Player uses for synchronization by calling [IWMPSyncDevice2::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) with the **PercentSpaceReserved** attribute.</span></span> <span data-ttu-id="8850f-130">Для использования этого интерфейса требуется проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="8850f-130">Using this interface requires Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8850f-131">См. также</span><span class="sxs-lookup"><span data-stu-id="8850f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8850f-132">**Сведения о синхронизации устройств**</span><span class="sxs-lookup"><span data-stu-id="8850f-132">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="8850f-133">**Интерфейс IWMPEvents2**</span><span class="sxs-lookup"><span data-stu-id="8850f-133">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="8850f-134">**Отображение хода выполнения синхронизации**</span><span class="sxs-lookup"><span data-stu-id="8850f-134">**Showing Synchronization Progress**</span></span>](showing-synchronization-progress.md)
</dt> </dl>

 

 




