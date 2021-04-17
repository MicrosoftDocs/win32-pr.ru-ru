---
title: Интерфейс IMsRdpClientAdvancedSettings4
description: Управляет дополнительными параметрами клиента. Является производным от интерфейса IMsRdpClientAdvancedSettings3.
ms.assetid: cb1785d6-1f94-4423-bdda-0e3e4e9b8641
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, описание
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d840206a139e3c3272551eab6a187a7b18416e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415464"
---
# <a name="imsrdpclientadvancedsettings4-interface"></a>Интерфейс IMsRdpClientAdvancedSettings4

Управляет дополнительными параметрами клиента. Является производным от интерфейса [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) . Этот интерфейс включает методы для получения и задания дополнительных (необязательных) свойств для удаленный рабочий стол элемента управления ActiveX.

Чтобы получить экземпляр этого интерфейса, используйте свойство [**имстскакс:: адванцедсеттингс**](imstscax-advancedsettings.md) для получения указателя на интерфейс [**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md) . Затем вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в указателе **имстскадванцедсеттингс** и передайте **IID \_ IMsRdpClientAdvancedSettings4** в **QueryInterface**.

## <a name="members"></a>Элементы

Интерфейс **IMsRdpClientAdvancedSettings4** наследует от [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md). **IMsRdpClientAdvancedSettings4** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Интерфейс **IMsRdpClientAdvancedSettings4** имеет следующие свойства.



| Свойство                                                                                    | Тип доступа           | Описание                                                              |
|:--------------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------|
| [**аусентикатионлевел**](imsrdpclientadvancedsettings4-authenticationlevel.md)<br/> | Чтение/запись<br/> | Указывает уровень проверки подлинности, используемый для соединения.<br/> |



 

## <a name="remarks"></a>Комментарии

Этот интерфейс расширен следующими интерфейсами, при этом каждый новый интерфейс наследует все методы и свойства предыдущих интерфейсов:

-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                         |
| Минимальная версия сервера<br/> | Windows Server 2008, Windows Server 2008 с пакетом обновления 1<br/>                                     |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings4 определяется как FBA7F64E-7345-4405-AE50-FA4A763DC0DE<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**имсрдпклиентадванцедсеттингс**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md)
</dt> <dt>

[Справочник по веб-подключение к удаленному рабочему столу](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

