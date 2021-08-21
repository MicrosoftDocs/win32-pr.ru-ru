---
title: Difxapi.h
description: В этом разделе содержатся справочные разделы по заголовку Дифксапи. h.
ms.assetid: 84da7e54-0677-495e-9dc5-aca4ac12c0b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5dcace8f7f8c8ed528849da02016f04e0ca32b2132c7b0587a96872d7cc561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736027"
---
# <a name="difxapih"></a>Difxapi.h

В этом разделе содержатся справочные разделы по заголовку Дифксапи. h.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                 | Описание                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*дифлогкаллбакк*](/previous-versions/windows/hardware/difxapi/diflogcallback)<br/>                     | **Дифлогкаллбакк** функция — это предоставляемая приложением функция обратного вызова, которая регистрируется приложением путем вызова [**сетдифкслогкаллбакк**](/previous-versions/windows/hardware/difxapi/setdifxlogcallback). Дифксапи вызывает функцию обратного вызова для регистрации событий, происходящих во время операции Дифксапи.<br/>                        |
| [*дифксапилогкаллбакк*](/previous-versions/windows/hardware/difxapi/difxapilogcallback)<br/>             | **Дифксапилогкаллбакк** функция — предоставляемая приложением функция обратного вызова, которую приложение регистрирует с помощью дифксапи путем вызова [**дифксаписетлогкаллбакк**](/previous-versions/windows/hardware/difxapi/difxapisetlogcallback). Дифксапи вызывает функцию обратного вызова для регистрации событий, происходящих во время операции Дифксапи.<br/> |
| [**дифксаписетлогкаллбакк**](/previous-versions/windows/hardware/difxapi/difxapisetlogcallback)<br/>     | Функция **дифксаписетлогкаллбакк** регистрирует предоставляемую вызывающей стороной функцию обратного вызова, которая дифксапи вызовы для записи сведений о событиях, происходящих во время операций дифксапи. <br/>                                                                                                            |
| [**дриверпаккажежетпас**](/previous-versions/windows/hardware/difxapi/driverpackagegetpath)<br/>       | Функция **дриверпаккажежетпас** получает полный путь к [INF-файлу](/windows-hardware/drivers/install/overview-of-inf-files) для предварительно установленного [пакета драйверов](/windows-hardware/drivers/install/driver-packages).<br/>                                                                                                               |
| [**дриверпаккажеинсталл**](/previous-versions/windows/hardware/difxapi/driverpackageinstall)<br/>       | Функция **дриверпаккажеинсталл** предустанавливает [пакет драйверов](/windows-hardware/drivers/install/driver-packages) , а затем устанавливает драйвер в системе.<br/>                                                                                                                                                 |
| [**дриверпаккажепреинсталл**](/previous-versions/windows/hardware/difxapi/driverpackagepreinstall)<br/> | Функция **дриверпаккажепреинсталл** предустанавливает [пакет драйверов](/windows-hardware/drivers/install/driver-packages) для [драйвера функции](/windows-hardware/drivers/kernel/function-drivers) Самонастраивающийся (PnP) и устанавливает [INF-файл](/windows-hardware/drivers/install/overview-of-inf-files) для пакета драйвера в системный каталог INF.<br/>             |
| [**дриверпаккажеунинсталл**](/previous-versions/windows/hardware/difxapi/driverpackageuninstall)<br/>   | Функция **дриверпаккажеунинсталл** удаляет указанный [пакет драйверов](/windows-hardware/drivers/install/driver-packages) из системы, удаляя пакет драйверов. <br/>                                                                                                                               |
| [**инсталлеринфо**](/previous-versions/windows/hardware/difxapi/installerinfo)<br/>                     | Структура ИНСТАЛЛЕРИНФО содержит сведения о приложении, которое Дифксапи связывает с [пакетом драйверов](/windows-hardware/drivers/install/driver-packages). <br/>                                                                                                                                          |
| [**сетдифкслогкаллбакк**](/previous-versions/windows/hardware/difxapi/setdifxlogcallback)<br/>           | Функция **сетдифкслогкаллбакк** регистрирует предоставляемую вызывающей стороной функцию обратного вызова, которая дифксапи вызовы для записи сведений о событиях, происходящих во время операций дифксапи. <br/>                                                                                                               |



 

 

 

[Отправить комментарии об этом разделе в Майкрософт](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevinst\devinst%5D:%20Difxapi.h%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Отправить комментарии об этом разделе в Майкрософт")