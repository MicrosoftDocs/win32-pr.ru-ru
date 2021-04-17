---
description: Как получить доступ к информации о BIOS для управления системой из универсального приложения Windows.
ms.assetid: 4D185319-C093-4B1B-A182-E845E72FEA5D
title: Доступ к сведениям SMBIOS из универсального приложения Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76791622ad4bcba15ddd889f36a6f0feeb5e3dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545783"
---
# <a name="access-smbios-information-from-a-universal-windows-app"></a>Доступ к сведениям SMBIOS из универсального приложения Windows

> МЕТИМ Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.

Как получить доступ к информации о BIOS для управления системой из универсального приложения Windows.

## <a name="access-smbios-information-from-a-universal-windows-platform-app"></a>Доступ к сведениям SMBIOS из универсальная платформа Windows приложения

Начиная с Windows 10 версии 1803, универсальные приложения для Windows могут использовать [жетсистемфирмваретабле](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) и [енумсистемфирмваретаблес](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) для доступа к информации SMBIOS, объявляя возможность ограничения **SMBIOS** в манифесте приложения.

> [!IMPORTANT]
> Только доступ к необработанным таблицам встроенного по SMBIOS (РСМБ) поддерживается из универсального приложения Windows. **Доступ к \_** Если вы попытаетесь получить доступ к другим типам таблиц встроенного по в универсальном приложении Windows, будет возвращен отказ.

 

Чтобы объявить ограниченную функциональность **SMBIOS** в манифесте приложения, добавьте пространство имен **рескап** и возможности **SMBIOS** следующим образом:

``` syntax
<Package
  ...
  xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities"
  IgnorableNamespaces="uap mp rescap">  
  ...
  <Capabilities>
    <rescap:Capability Name="smbios"/>
  </Capabilities>
</Package>
```

## <a name="related-topics"></a>См. также

<dl> <dt>

[Особые и ограниченные возможности](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[жетсистемфирмваретабле](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable)
</dt> <dt>

[енумсистемфирмваретаблес](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables)
</dt> <dt>

[Доступ к переменным встроенного по UEFI из универсального приложения Windows](access-uefi-firmware-variables-from-a-universal-windows-app.md)
</dt> </dl>

 

 
