---
description: как получить доступ к сведениям об системном Management BIOS (SMBIOS) из универсального Windows приложения.
ms.assetid: 4D185319-C093-4B1B-A182-E845E72FEA5D
title: доступ к сведениям SMBIOS из универсального Windows приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936d30a653059b3573e962b2e52770aa2bd000180ee0612c1855de3d6a1a9778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764958"
---
# <a name="access-smbios-information-from-a-universal-windows-app"></a>доступ к сведениям SMBIOS из универсального Windows приложения

> МЕТИМ Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.

как получить доступ к сведениям об системном Management BIOS (SMBIOS) из универсального Windows приложения.

## <a name="access-smbios-information-from-a-universal-windows-platform-app"></a>доступ к сведениям SMBIOS из универсальная платформа Windows приложения

начиная с Windows 10 версии 1803, универсальные приложения Windows могут использовать [жетсистемфирмваретабле](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) и [енумсистемфирмваретаблес](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) для доступа к информации SMBIOS, объявляя возможность ограничения **smbios** в манифесте приложения.

> [!IMPORTANT]
> только доступ к необработанным таблицам встроенного по SMBIOS (рсмб) поддерживается из универсального приложения Windows. **Доступ к \_** если вы попытаетесь получить доступ к другим типам таблиц встроенного по в универсальном Windows приложении, будет возвращен отказ.

 

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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Особые и ограниченные возможности](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[жетсистемфирмваретабле](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable)
</dt> <dt>

[енумсистемфирмваретаблес](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables)
</dt> <dt>

[доступ к переменным встроенного по UEFI из универсального Windows приложения](access-uefi-firmware-variables-from-a-universal-windows-app.md)
</dt> </dl>

 

 
