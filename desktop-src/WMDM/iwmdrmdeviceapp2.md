---
title: Интерфейс IWMDRMDeviceApp2
description: Интерфейс IWMDRMDeviceApp2 расширяет Ивмдрмдевицеапп, предоставляя новую версию метода Куеридевицестатус.
ms.assetid: a7e28d5a-041f-4102-97db-0c77ca146e26
keywords:
- Интерфейс IWMDRMDeviceApp2 Windows Media диспетчер устройств
- Интерфейс IWMDRMDeviceApp2 Windows Media диспетчер устройств, описание
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17bd0d7aa729103a81fca6732ed178ac5ced583566dd353a28716d4933e602ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584498"
---
# <a name="iwmdrmdeviceapp2-interface"></a>Интерфейс IWMDRMDeviceApp2

Интерфейс **IWMDRMDeviceApp2** расширяет [**ивмдрмдевицеапп**](iwmdrmdeviceapp.md) , предоставляя новую версию метода [**куеридевицестатус**](iwmdrmdeviceapp-querydevicestatus.md) . **QueryDeviceStatus2** позволяет вызывающему объекту запрашивать определенные требования DRM.

Чтобы получить этот интерфейс, вызовите **CoCreateInstance** и передайте CLSID \_ вмдрмдевицеапп.

> [!Note]  
> Этот интерфейс определен в файле заголовка, созданном из Вмдрмдевицеапп. idl. Этот заголовок **\# содержит** "вмдм. h". Может потребоваться изменить это имя файла в соответствии с заголовком, созданным из ВМДМ. idl.

 

## <a name="members"></a>Элементы

Интерфейс **IWMDRMDeviceApp2** наследует от [**ивмдрмдевицеапп**](iwmdrmdeviceapp.md). **IWMDRMDeviceApp2** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **IWMDRMDeviceApp2** содержит следующие методы.



| Метод                                                            | Описание                                                          |
|:------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) | Запрашивает устройство для определенного состояния DRM или возможности.<br/> |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмдрмдевицеапп**](iwmdrmdeviceapp.md)
</dt> <dt>

[**Обработка защищенного содержимого в приложении**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Интерфейсы для приложений**](interfaces-for-applications.md)
</dt> <dt>

[**Использование содержимого измерения**](metering-content-usage.md)
</dt> </dl>

 

 





