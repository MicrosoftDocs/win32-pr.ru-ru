---
title: Интерфейс IMsRdpClientAdvancedSettings3
description: Управляет дополнительными параметрами клиента. Является производным от интерфейса IMsRdpClientAdvancedSettings2.
ms.assetid: bfa9cf74-5943-45ca-9259-3ef0cc9ab2ab
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, описание
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df13ccfb0d955714984af82daaf693522ee7d61af9c608107c53dc9f5464b591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001382"
---
# <a name="imsrdpclientadvancedsettings3-interface"></a>Интерфейс IMsRdpClientAdvancedSettings3

Управляет дополнительными параметрами клиента. Является производным от интерфейса [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) . этот интерфейс включает методы для получения и задания дополнительных (необязательных) свойств для элемента управления удаленный рабочий стол ActiveX.

Чтобы получить экземпляр этого интерфейса, используйте свойство [**имстскакс:: адванцедсеттингс**](imstscax-advancedsettings.md) для получения указателя на интерфейс [**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md) . Затем вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в указателе **имстскадванцедсеттингс** и передайте **IID \_ IMsRdpClientAdvancedSettings3** в **QueryInterface**.

## <a name="members"></a>Элементы

Интерфейс **IMsRdpClientAdvancedSettings3** наследует от [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md). **IMsRdpClientAdvancedSettings3** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Интерфейс **IMsRdpClientAdvancedSettings3** имеет следующие свойства.



| Свойство                                                                                                            | Тип доступа           | Описание                                                                            |
|:--------------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------|
| [**коннектионбаршовминимизебуттон**](imsrdpclientadvancedsettings3-connectionbarshowminimizebutton.md)<br/> | Чтение/запись<br/> | Указывает, отображать ли кнопку **сворачивания** на панели подключения.<br/> |
| [**коннектионбаршовресторебуттон**](imsrdpclientadvancedsettings3-connectionbarshowrestorebutton.md)<br/>   | Чтение/запись<br/> | Указывает, следует ли отображать кнопку **восстановить** на панели подключения.<br/>  |



 

## <a name="remarks"></a>Remarks

Этот интерфейс расширен следующими интерфейсами, при этом каждый новый интерфейс наследует все методы и свойства предыдущих интерфейсов:

-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
-   [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                         |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                   |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings3 определен как 19cd856b-C542-4c53-ACee-f127e3be1a59<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**имсрдпклиентадванцедсеттингс**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md)
</dt> <dt>

[Справочник по веб-подключение к удаленному рабочему столу](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

