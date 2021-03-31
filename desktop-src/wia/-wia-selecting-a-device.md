---
description: Когда приложение подключается к аппаратному устройству для получения образа Windows (WIA), WIA создает дерево элементов (иерархическое дерево интерфейсов Ивиаитем или IWiaItem2), которое представляет устройство и его изображения, папки и сканирование кроватях.
ms.assetid: 2a7bcfd4-4075-48a4-9eff-5210b9a635e3
title: Выбор устройства (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a2eab41016397f6505e60efcbf78d1fdf82499
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897438"
---
# <a name="selecting-a-device-wia"></a>Выбор устройства (WIA)

Когда приложение подключается к аппаратному устройству для получения образа Windows (WIA), WIA создает дерево элементов (иерархическое дерево интерфейсов [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) или [**IWiaItem2**](-wia-iwiaitem2.md) ), которое представляет устройство и его изображения, папки и сканирование кроватях. Приложение может выбирать и подключаться к устройству без ввода данных пользователем, а также может отображать диалоговое окно, позволяющее пользователю выбрать устройство.

-   [Выбор устройства без пользовательского интерфейса](#selecting-a-device-without-the-ui)
-   [Выбор устройства с помощью пользовательского интерфейса](#selecting-a-device-with-the-ui)

## <a name="selecting-a-device-without-the-ui"></a>Выбор устройства без пользовательского интерфейса

Чтобы выбрать и подключиться к аппаратному устройству WIA, выполните следующие действия.

-   Вызовите [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения указателя на интерфейс [**ивиадевмгр**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) или [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) .
-   Используйте метод [**ивиадевмгр:: енумдевицеинфо**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) интерфейса [**ивиадевмгр**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) или [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) , чтобы получить указатель на интерфейс [**иенумвиа \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) . Инструкции по перечислению устройств см. в разделе [перечисление системных устройств](-wia-enumerating-system-devices.md).
-   Используйте интерфейс [**иенумвиа \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) для получения указателей интерфейса [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) для каждого перечисленного устройства WIA.
-   Используйте интерфейс [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) для проверки свойств сведений об устройстве каждого устройства и сохранения \_ свойства идентификатора WIA DIP \_ dev \_ с нужного устройства.
-   Используйте свойство DeviceID с методом [**ивиадевмгр:: креатедевице**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) в интерфейсе [**ивиадевмгр**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) или [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) , чтобы создать объект устройства WIA. Метод **ивиадевмгр:: креатедевице** предоставляет приложению указатель на интерфейс [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) или [**IWiaItem2**](-wia-iwiaitem2.md) корневого элемента указанного устройства.

Пример того, как это сделать в приложении, см. в разделе [Создание устройства](-wia-creating-a-device.md) в руководстве этого руководства.

## <a name="selecting-a-device-with-the-ui"></a>Выбор устройства с помощью пользовательского интерфейса

После получения указателя на [**ивиадевмгр**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr)приложение может позволить пользователю выбрать устройство, пропустив оставшиеся действия, описанные выше, и вызвав [**Ивиадевмгр:: селектдевицедлг**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-selectdevicedlg). **Ивиадевмгр:: селектдевицедлг** отображает диалоговое окно, в котором пользователь может выбрать устройство WIA.

Рекомендуется, чтобы приложения были доступны для выбора устройств и изображений с помощью пункта меню **с именем сканер** в меню **файл** .

 

 
