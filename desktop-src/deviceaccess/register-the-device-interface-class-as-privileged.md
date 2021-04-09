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
# <a name="register-the-device-interface-as-restricted-to-privileged-apps"></a>Зарегистрируйте интерфейс устройства как ограниченные для привилегированных приложений

Приложениям запрещается доступ к пользовательским функциям драйвера, если им не предоставлены разрешения через подписанные метаданные устройства. В этом разделе показано, как добавить свойство **Restricted** , указывающее, что только привилегированные приложения могут обращаться к классу интерфейса устройства. Настраиваемые драйверы устройств должны иметь это свойство.

## <a name="instructions"></a>Инструкции

### <a name="setting-the-restricted-property-in-an-information-inf-file"></a>Задание ограниченного свойства в файле сведений (INF)

В `InterfaceInstall32` разделе регистрируется идентификатор GUID класса интерфейса устройства.

Строки в директиве **AddProperty** задают свойства класса устройства. Во второй строке задается пользовательское свойство в категории настраиваемых свойств. GUID категории свойств — **14c83a99-0b3f-44b7-be4c-a178d3990564**, а идентификатор свойства — **2**. Необязательное `Flags` значение записи отсутствует, тип — **17** (**DEVPROP_TYPE_BOOLEAN**). Значение свойства равно **1**.

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

## <a name="remarks"></a>Комментарии

Вместо директивы **аддинтерфаце** драйвер может также вызвать подпрограмму [**иорегистердевицеинтерфаце**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) для регистрации класса интерфейса устройства.

Можно также задать свойство ограниченного интерфейса, вызвав подпрограммы [**иосетдевицеинтерфацепропертидата**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) .

## <a name="related-topics"></a>См. также

[Пример пользовательского доступа к драйверу](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [приложения для устройств UWP для внутренних устройств](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [центр разработки оборудования](/windows-hardware/drivers/)
