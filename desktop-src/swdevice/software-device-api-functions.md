---
title: Функции API для устройств программного обеспечения
description: В этом разделе описываются функции API программного устройства, которые вызываются клиентским приложением, и функция обратного вызова, реализуемая клиентским приложением.
ms.assetid: 68F142A9-08AD-4F74-A0C3-3DCC8F7449B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a3cc9f0cd8b018f40210c434ee22b3512b2e81
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413549"
---
# <a name="software-device-api-functions"></a>Функции API для устройств программного обеспечения

В этом разделе описываются функции API программного устройства, которые вызываются клиентским приложением, и функция обратного вызова, реализуемая клиентским приложением.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                           | Описание                                                                                                                                                      |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**свдевицеклосе**](/windows/win32/api/swdevice/nf-swdevice-swdeviceclose)<br/>                               | Закрывает маркер программного устройства. Когда этот маркер закрыт, PnP инициирует процесс удаления устройства.<br/>                                   |
| [**\_ \_ обратный вызов для создания устройства на SW \_**](/windows/win32/api/swdevice/nc-swdevice-sw_device_create_callback)<br/>    | Предоставляет устройство с резервным копированием в реестре и позволяет вызывающему объекту выполнять вызовы функций API программного устройства с помощью обработчика *хсвдевице* .<br/> |
| [**свдевицекреате**](/windows/win32/api/swdevice/nf-swdevice-swdevicecreate)<br/>                             | Инициирует перечисление программного устройства.<br/>                                                                                                       |
| [**свдевицежетлифетиме**](/windows/win32/api/swdevice/nf-swdevice-swdevicegetlifetime)<br/>                   | Возвращает время существования программного устройства. <br/>                                                                                                              |
| [**свдевицеинтерфацепропертисет**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfacepropertyset)<br/> | Задает свойства интерфейса программного устройства. <br/>                                                                                                      |
| [**свдевицеинтерфацерегистер**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfaceregister)<br/>       | Регистрирует интерфейс устройства для программного устройства и при необходимости задает свойства этого интерфейса. <br/>                                                 |
| [**свдевицеинтерфацесетстате**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfacesetstate)<br/>       | Включает или отключает интерфейс устройства для программного устройства. <br/>                                                                                        |
| [**свдевицепропертисет**](/windows/win32/api/swdevice/nf-swdevice-swdevicepropertyset)<br/>                   | Задает свойства программного устройства. <br/>                                                                                                                |
| [**свдевицесетлифетиме**](/windows/win32/api/swdevice/nf-swdevice-swdevicesetlifetime)<br/>                   | Управляет временем существования программного устройства. <br/>                                                                                                           |
| [**свмемфри**](/windows/win32/api/swdevice/nf-swdevice-swmemfree)<br/>                                       | Освобождает память, выделенную другими функциями API программных устройств.<br/>                                                                                      |



 

 

 

[Отправить комментарии об этом разделе в Майкрософт](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bswdevice\swdevice%5D:%20Software%20Device%20API%20Functions%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Отправить комментарии об этом разделе в Майкрософт")