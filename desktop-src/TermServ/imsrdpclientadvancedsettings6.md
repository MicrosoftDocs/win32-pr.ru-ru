---
title: Интерфейс IMsRdpClientAdvancedSettings6
description: Отображает свойства, управляющие дополнительными параметрами элементов управления ActiveX.
ms.assetid: 45b48cdf-3860-4359-99b2-8d2598146d1d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, описание
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e61d3358f1af228dcd1b5a7431ee759b486df7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681939"
---
# <a name="imsrdpclientadvancedsettings6-interface"></a>Интерфейс IMsRdpClientAdvancedSettings6

Отображает свойства, управляющие дополнительными параметрами элементов управления ActiveX. Интерфейс **IMsRdpClientAdvancedSettings6** является производным от интерфейса [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) .

Чтобы получить экземпляр этого интерфейса, используйте свойство [**имстскакс:: адванцедсеттингс**](imstscax-advancedsettings.md) для получения указателя на интерфейс [**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md) . Затем вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в указателе **имстскадванцедсеттингс** и передайте **IID \_ IMsRdpClientAdvancedSettings6** в **QueryInterface**.

## <a name="members"></a>Элементы

Интерфейс **IMsRdpClientAdvancedSettings6** наследует от [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md). **IMsRdpClientAdvancedSettings6** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Интерфейс **IMsRdpClientAdvancedSettings6** имеет следующие свойства.



| Свойство                                                                                                  | Тип доступа           | Описание                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**аусентикатионсервицекласс**](imsrdpclientadvancedsettings6-authenticationserviceclass.md)<br/> | Чтение/запись<br/> | Указывает имя участника-службы (SPN), используемое для проверки подлинности на сервере.<br/>                                     |
| [**AuthenticationType**](imsrdpclientadvancedsettings6-authenticationtype.md)<br/>                 | Только для чтения<br/>  | Указывает тип проверки подлинности, используемый для этого соединения.<br/>                                                          |
| [**коннекттоадминистерсервер**](imsrdpclientadvancedsettings6-connecttoadministerserver.md)<br/>   | Чтение/запись<br/> | Возвращает или задает значение, указывающее, должен ли элемент управления ActiveX пытаться подключиться к серверу для административных целей.<br/> |
| [**енаблекредсспсуппорт**](imsrdpclientadvancedsettings6-enablecredsspsupport.md)<br/>             | Чтение/запись<br/> | Указывает, включен ли поставщик службы безопасности учетных данных (CredSSP) для этого подключения.<br/>                    |
| [**хоткэйфокусрелеаселефт**](imsrdpclientadvancedsettings6-hotkeyfocusreleaseleft.md)<br/>         | Чтение/запись<br/> | Задает код виртуального ключа, добавляемый в сочетание клавиш CTRL + ALT для определения замены с помощью сочетания клавиш CTRL + ALT + стрелка влево.<br/>          |
| [**хоткэйфокусрелеасеригхт**](imsrdpclientadvancedsettings6-hotkeyfocusreleaseright.md)<br/>       | Чтение/запись<br/> | Указывает код виртуального ключа, добавляемый в сочетание клавиш CTRL + ALT для определения замены с помощью сочетания клавиш CTRL + ALT + стрелка вправо.<br/>         |
| [**пкб**](imsrdpclientadvancedsettings6-pcb.md)<br/>                                               | Чтение/запись<br/> | Задает параметр предварительного подключения BLOB-объекта (ПКБ), используемый перед подключением для передачи на сервер.<br/>               |
| [**релативемаусемоде**](imsrdpclientadvancedsettings6-relativemousemode.md)<br/>                   | Чтение/запись<br/> | Указывает, следует ли использовать относительный режим для мыши.<br/>                                                                   |



 

## <a name="remarks"></a>Комментарии

Этот интерфейс расширен интерфейсом [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) , который наследует все методы и свойства предыдущих интерфейсов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                         |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                   |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 определен как 222c4b5d-45d9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**имсрдпклиентадванцедсеттингс**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

