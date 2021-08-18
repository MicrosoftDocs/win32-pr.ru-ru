---
title: Интерфейс IMsRdpClientAdvancedSettings2
description: Управляет дополнительными параметрами клиента. Является производным от интерфейса Имсрдпклиентадванцедсеттингс.
ms.assetid: 78cffdf5-bd99-4140-80b6-aa8632894487
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, описание
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b97584aa3b37adc148672777e95fe0b2c8b101e09989bfa1ab5debbffe489640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001412"
---
# <a name="imsrdpclientadvancedsettings2-interface"></a>Интерфейс IMsRdpClientAdvancedSettings2

Управляет дополнительными параметрами клиента. Является производным от интерфейса [**имсрдпклиентадванцедсеттингс**](imsrdpclientadvancedsettings-interface.md) . этот интерфейс включает методы для получения и задания дополнительных (необязательных) свойств для элемента управления удаленный рабочий стол ActiveX.

Чтобы получить экземпляр этого интерфейса, используйте свойство [**имстскакс:: адванцедсеттингс**](imstscax-advancedsettings.md) для получения указателя на интерфейс [**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md) . Затем вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в указателе **имстскадванцедсеттингс** и передайте **IID \_ IMsRdpClientAdvancedSettings2** в **QueryInterface**.

## <a name="members"></a>Элементы

Интерфейс **IMsRdpClientAdvancedSettings2** наследует от [**имсрдпклиентадванцедсеттингс**](imsrdpclientadvancedsettings-interface.md). **IMsRdpClientAdvancedSettings2** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Интерфейс **IMsRdpClientAdvancedSettings2** имеет следующие свойства.



| Свойство                                                                                      | Тип доступа           | Описание                                                                                                                                           |
|:----------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**канаутореконнект**](imsrdpclientadvancedsettings2-canautoreconnect.md)<br/>         | Только для чтения<br/>  | Указывает, может ли клиентский элемент управления автоматически подключаться к текущему сеансу в случае отключения от сети.<br/>    |
| [**енаблеаутореконнект**](imsrdpclientadvancedsettings2-enableautoreconnect.md)<br/>   | Чтение/запись<br/> | Указывает, следует ли включить клиентский элемент управления для автоматического подключения к сеансу в случае отключения от сети.<br/>            |
| [**максреконнектаттемптс**](imsrdpclientadvancedsettings2-maxreconnectattempts.md)<br/> | Чтение/запись<br/> | Указывает количество повторных попыток подключения во время автоматического повторного подключения. Допустимые значения этого свойства: от 0 до 200 включительно.<br/> |



 

## <a name="remarks"></a>Remarks

Этот интерфейс расширен следующими интерфейсами, при этом каждый новый интерфейс наследует все методы и свойства предыдущих интерфейсов:

-   [**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                         |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                   |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings2 определен как 9ac42117-2b76-4320-aa44-0e616ab8437b<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**имсрдпклиентадванцедсеттингс**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md)
</dt> <dt>

[Справочник по веб-подключение к удаленному рабочему столу](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

