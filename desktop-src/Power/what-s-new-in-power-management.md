---
description: Windows 10 помогает вашему приложению оптимизировать энергопотребление при работе на мобильном устройстве.
ms.assetid: a956b88c-8a75-4c1c-af27-53c69feb1596
title: Новые возможности управления питанием
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ac6ba320a98fce339f5bfacfe2d9b4a259be5a8150b2bcaabcac41179869e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143197"
---
# <a name="whats-new-in-power-management"></a>Новые возможности управления питанием

Windows 10 помогает вашему приложению оптимизировать энергопотребление при работе на мобильном устройстве.

## <a name="battery-saver"></a>Экономия заряда

В этом выпуске приложение может получать уведомления при включении или отключении заставки аккумулятора. Отвечая на изменение условий электропитания, приложение может работать совместно с заставкой аккумулятора для экономии энергии и увеличения времени работы аккумулятора. Общие сведения о экономии заряда батареи см. [в разделе Заставка аккумулятора (в руководстве по компонентам оборудования)](/windows-hardware/design/component-guidelines/battery-saver).

-   [**Идентификатор GUID \_ \_ \_ Состояние энергосбережения**](power-setting-guids.md) . Используйте этот новый идентификатор GUID с функцией [**поверсеттингрегистернотификатион**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) , чтобы получать уведомления при включении или отключении заставки аккумулятора.

-   [**Система \_ \_Состояние питания**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) . Эта структура была обновлена для поддержки экономии заряда. Четвертый элемент, **системстатусфлаг** (ранее именуемый **Reserved1**), теперь указывает, включена ли экономия заряда. Используйте функцию [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) для получения указателя на эту структуру.

 

 
