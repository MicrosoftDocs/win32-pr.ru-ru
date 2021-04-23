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
# <a name="access-smbios-information-from-a-universal-windows-app"></a><span data-ttu-id="da06d-103">Доступ к сведениям SMBIOS из универсального приложения Windows</span><span class="sxs-lookup"><span data-stu-id="da06d-103">Access SMBIOS information from a Universal Windows App</span></span>

> <span data-ttu-id="da06d-104">МЕТИМ Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="da06d-104">[NOTE] Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="da06d-105">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.</span><span class="sxs-lookup"><span data-stu-id="da06d-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="da06d-106">Как получить доступ к информации о BIOS для управления системой из универсального приложения Windows.</span><span class="sxs-lookup"><span data-stu-id="da06d-106">How to access System Management BIOS (SMBIOS) information from a Universal Windows app.</span></span>

## <a name="access-smbios-information-from-a-universal-windows-platform-app"></a><span data-ttu-id="da06d-107">Доступ к сведениям SMBIOS из универсальная платформа Windows приложения</span><span class="sxs-lookup"><span data-stu-id="da06d-107">Access SMBIOS information from a Universal Windows Platform App</span></span>

<span data-ttu-id="da06d-108">Начиная с Windows 10 версии 1803, универсальные приложения для Windows могут использовать [жетсистемфирмваретабле](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) и [енумсистемфирмваретаблес](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) для доступа к информации SMBIOS, объявляя возможность ограничения **SMBIOS** в манифесте приложения.</span><span class="sxs-lookup"><span data-stu-id="da06d-108">Starting with Windows 10, version 1803, Universal Windows apps can use [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) and [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) to access SMBIOS information by declaring the **smbios** restricted capability in the app manifest.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da06d-109">Только доступ к необработанным таблицам встроенного по SMBIOS (РСМБ) поддерживается из универсального приложения Windows.</span><span class="sxs-lookup"><span data-stu-id="da06d-109">Only access to raw SMBIOS (RSMB) firmware tables is supported from a Universal Windows app.</span></span> <span data-ttu-id="da06d-110">**Доступ к \_** Если вы попытаетесь получить доступ к другим типам таблиц встроенного по в универсальном приложении Windows, будет возвращен отказ.</span><span class="sxs-lookup"><span data-stu-id="da06d-110">**ACCESS\_DENIED** will be returned if you try to access other firmware table types from a Universal Windows app.</span></span>

 

<span data-ttu-id="da06d-111">Чтобы объявить ограниченную функциональность **SMBIOS** в манифесте приложения, добавьте пространство имен **рескап** и возможности **SMBIOS** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="da06d-111">To declare the **smbios** restricted capability in the app manifest, add the **rescap** namespace and **smbios** capability as follows:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="da06d-112">См. также</span><span class="sxs-lookup"><span data-stu-id="da06d-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da06d-113">Особые и ограниченные возможности</span><span class="sxs-lookup"><span data-stu-id="da06d-113">Special and restricted capabilities</span></span>](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[<span data-ttu-id="da06d-114">жетсистемфирмваретабле</span><span class="sxs-lookup"><span data-stu-id="da06d-114">GetSystemFirmwareTable</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable)
</dt> <dt>

[<span data-ttu-id="da06d-115">енумсистемфирмваретаблес</span><span class="sxs-lookup"><span data-stu-id="da06d-115">EnumSystemFirmwareTables</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables)
</dt> <dt>

[<span data-ttu-id="da06d-116">Доступ к переменным встроенного по UEFI из универсального приложения Windows</span><span class="sxs-lookup"><span data-stu-id="da06d-116">Access UEFI firmware variables from a Universal Windows App</span></span>](access-uefi-firmware-variables-from-a-universal-windows-app.md)
</dt> </dl>

 

 
