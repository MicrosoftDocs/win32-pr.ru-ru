---
title: Зарегистрируйте интерфейс устройства как ограниченные для привилегированных приложений
description: В этом разделе показано, как добавить свойство Restricted, указывающее, что только привилегированные приложения могут обращаться к классу интерфейса устройства.
ms.assetid: BCEB1FBF-3D3F-45B8-A92B-7C5FBF6745C0
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: e23f8b7f2cc1884e2f878739f56507e79eb1bb69
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104070818"
---
# <a name="register-the-device-interface-as-restricted-to-privileged-apps"></a><span data-ttu-id="31e5f-103">Зарегистрируйте интерфейс устройства как ограниченные для привилегированных приложений</span><span class="sxs-lookup"><span data-stu-id="31e5f-103">Register the device interface as restricted to privileged apps</span></span>

<span data-ttu-id="31e5f-104">Приложениям запрещается доступ к пользовательским функциям драйвера, если им не предоставлены разрешения через подписанные метаданные устройства.</span><span class="sxs-lookup"><span data-stu-id="31e5f-104">Applications are denied access to custom driver functionality, unless they're granted permissions through signed device metadata.</span></span> <span data-ttu-id="31e5f-105">В этом разделе показано, как добавить свойство **Restricted** , указывающее, что только привилегированные приложения могут обращаться к классу интерфейса устройства.</span><span class="sxs-lookup"><span data-stu-id="31e5f-105">This topic shows how to add the **Restricted** property that indicates that only privileged apps can access a device interface class.</span></span> <span data-ttu-id="31e5f-106">Настраиваемые драйверы устройств должны иметь это свойство.</span><span class="sxs-lookup"><span data-stu-id="31e5f-106">Custom device drivers must have this property.</span></span>

## <a name="instructions"></a><span data-ttu-id="31e5f-107">Инструкции</span><span class="sxs-lookup"><span data-stu-id="31e5f-107">Instructions</span></span>

### <a name="setting-the-restricted-property-in-an-information-inf-file"></a><span data-ttu-id="31e5f-108">Задание ограниченного свойства в файле сведений (INF)</span><span class="sxs-lookup"><span data-stu-id="31e5f-108">Setting the Restricted property in an information (INF) file</span></span>

<span data-ttu-id="31e5f-109">В `InterfaceInstall32` разделе регистрируется идентификатор GUID класса интерфейса устройства.</span><span class="sxs-lookup"><span data-stu-id="31e5f-109">In the `InterfaceInstall32` section, the GUID of the device interface class is registered.</span></span>

<span data-ttu-id="31e5f-110">Строки в директиве **AddProperty** задают свойства класса устройства.</span><span class="sxs-lookup"><span data-stu-id="31e5f-110">The lines under the **AddProperty** directive set the device class properties.</span></span> <span data-ttu-id="31e5f-111">Во второй строке задается пользовательское свойство в категории настраиваемых свойств.</span><span class="sxs-lookup"><span data-stu-id="31e5f-111">The second line sets a custom property in a custom property category.</span></span> <span data-ttu-id="31e5f-112">GUID категории свойств — **14c83a99-0b3f-44b7-be4c-a178d3990564**, а идентификатор свойства — **2**.</span><span class="sxs-lookup"><span data-stu-id="31e5f-112">The property-category GUID is **14c83a99-0b3f-44b7-be4c-a178d3990564**, and the property identifier is **2**.</span></span> <span data-ttu-id="31e5f-113">Необязательное `Flags` значение записи отсутствует, тип — **17** (**DEVPROP_TYPE_BOOLEAN**).</span><span class="sxs-lookup"><span data-stu-id="31e5f-113">The optional `Flags` entry value is not present, and the type is **17** (**DEVPROP_TYPE_BOOLEAN**).</span></span> <span data-ttu-id="31e5f-114">Значение свойства равно **1**.</span><span class="sxs-lookup"><span data-stu-id="31e5f-114">The value of the property is **1**.</span></span>

```Text
; Below, {11111111-0000-1111-0000-111111111111} is the GUID of the
; new device interface class in an AddInterface directive



; -- Interface installation
[InterfaceInstall32]
{11111111-0000-1111-0000-111111111111}=NewInterfaceInstall

[NewInterfaceInstall]
AddProperty=PrivilegedProperties

[PrivilegedProperties]
; DEVPKey_DeviceInterfaceClass_Restricted
{14c83a99-0b3f-44b7-be4c-a178d3990564}, 2, 17,,1 ; -- non-zero indicates privileged
```

## <a name="remarks"></a><span data-ttu-id="31e5f-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31e5f-115">Remarks</span></span>

<span data-ttu-id="31e5f-116">Вместо директивы **аддинтерфаце** драйвер может также вызвать подпрограмму [**иорегистердевицеинтерфаце**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) для регистрации класса интерфейса устройства.</span><span class="sxs-lookup"><span data-stu-id="31e5f-116">Instead of the **AddInterface** directive, the driver can also call the [**IoRegisterDeviceInterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) routine to register the device interface class.</span></span>

<span data-ttu-id="31e5f-117">Можно также задать свойство ограниченного интерфейса, вызвав подпрограммы [**иосетдевицеинтерфацепропертидата**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) .</span><span class="sxs-lookup"><span data-stu-id="31e5f-117">You can also set the restricted interface property by calling the [**IoSetDeviceInterfacePropertyData**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) routine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31e5f-118">См. также</span><span class="sxs-lookup"><span data-stu-id="31e5f-118">Related topics</span></span>

<span data-ttu-id="31e5f-119">[Пример пользовательского доступа к драйверу](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [приложения для устройств UWP для внутренних устройств](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [центр разработки оборудования](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="31e5f-119">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
