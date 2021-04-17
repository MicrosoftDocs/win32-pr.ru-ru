---
title: Интерфейс IMsRdpClientAdvancedSettings7
description: Предоставляет методы и свойства, управляющие дополнительными параметрами элемента управления ActiveX.
ms.assetid: 2d6848b4-2ce6-4624-b46e-65e7daf2d0f1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, описание
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eed28c5d26ecf280507ce3cce835a6d0a71fc3bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672547"
---
# <a name="imsrdpclientadvancedsettings7-interface"></a>Интерфейс IMsRdpClientAdvancedSettings7

Предоставляет методы и свойства, управляющие дополнительными параметрами элемента управления ActiveX.

Чтобы получить экземпляр этого интерфейса, используйте свойство [**имстскакс:: адванцедсеттингс**](imstscax-advancedsettings.md) для получения указателя на интерфейс [**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md) . Затем вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в указателе **имстскадванцедсеттингс** и передайте **IID \_ IMsRdpClientAdvancedSettings7** в **QueryInterface**.

## <a name="members"></a>Элементы

Интерфейс **IMsRdpClientAdvancedSettings7** наследует от **IMsRdpClientAdvancedSettings6**. **IMsRdpClientAdvancedSettings7** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Интерфейс **IMsRdpClientAdvancedSettings7** имеет следующие свойства.



| Свойство                                                                                                    | Тип доступа           | Описание                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аудиокаптурередиректионмоде**](imsrdpclientadvancedsettings7-audiocaptureredirectionmode.md)<br/> | Чтение/запись<br/> | Указывает или получает значение, указывающее, перенаправляется ли устройство ввода звука по умолчанию с клиента на удаленный сеанс.<br/> |
| [**аудиокуалитимоде**](imsrdpclientadvancedsettings7-audioqualitymode.md)<br/>                       | Чтение/запись<br/> | Указывает или получает значение, указывающее параметр режима качества звука для перенаправленного звука.<br/>                                        |
| [**енаблесуперпан**](imsrdpclientadvancedsettings7-enablesuperpan.md)<br/>                           | Чтение/запись<br/> | Указывает или получает значение, указывающее, включен или отключен Суперпан.<br/>                                                    |
| [**нетворкконнектионтипе**](imsrdpclientadvancedsettings7-networkconnectiontype.md)<br/>             | Чтение/запись<br/> | Указывает или получает значение, указывающее тип сетевого подключения.<br/>                                                                |
| [**редиректдиректкс**](imsrdpclientadvancedsettings7-redirectdirectx.md)<br/>                         | Чтение/запись<br/> | Это свойство не используется.<br/>                                                                                                                |
| [**суперпанакцелератионфактор**](imsrdpclientadvancedsettings7-superpanaccelerationfactor.md)<br/>   | Чтение/запись<br/> | Указывает или получает значение, указывающее коэффициент ускорения Суперпан.<br/>                                                           |
| [**видеоплайбаккмоде**](imsrdpclientadvancedsettings7-videoplaybackmode.md)<br/>                     | Чтение/запись<br/> | Указывает или получает значение, указывающее режим воспроизведения видео.<br/>                                                                    |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                             |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                                |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 определен как 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

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

 

