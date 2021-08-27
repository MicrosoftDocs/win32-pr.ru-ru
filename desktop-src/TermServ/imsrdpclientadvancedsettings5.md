---
title: Интерфейс IMsRdpClientAdvancedSettings5
description: Управляет дополнительными параметрами клиента. Является производным от интерфейса IMsRdpClientAdvancedSettings4.
ms.assetid: a927cd4c-7f70-493e-a4f6-056d0352d56e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, описание
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ad2b26697cd3985cc0e39a8ed7345bc4bbe941
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622350"
---
# <a name="imsrdpclientadvancedsettings5-interface"></a>Интерфейс IMsRdpClientAdvancedSettings5

Управляет дополнительными параметрами клиента. Является производным от интерфейса [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .

Чтобы получить экземпляр этого интерфейса, используйте свойство [**имстскакс:: адванцедсеттингс**](imstscax-advancedsettings.md) для получения указателя на интерфейс [**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md) . Затем вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в указателе **имстскадванцедсеттингс** и передайте **IID \_ IMsRdpClientAdvancedSettings5** в **QueryInterface**.

## <a name="members"></a>Участники

Интерфейс **IMsRdpClientAdvancedSettings5** наследует от [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md). **IMsRdpClientAdvancedSettings5** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Интерфейс **IMsRdpClientAdvancedSettings5** имеет следующие свойства.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Свойство</th>
<th >Тип доступа</th>
<th >Описание:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>аудиоредиректионмоде</strong></a><br/></td>
<td >Чтение/запись<br/></td>
<td >Режим перенаправления звука. Свойство <a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>аудиоредиректионмоде</strong></a> имеет следующие возможные значения.<br/>
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (перенаправление звука включено, а параметр перенаправления — &quot; на этот компьютер) &quot; . Это режим по умолчанию.)<br/> </dt> <dd></dd> <dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (перенаправление звука включено, а параметр — &quot; оставить на удаленном компьютере) &quot; . &quot;параметр оставить на удаленном компьютере &quot; поддерживается только при удаленном подключении к главному компьютеру, на котором работает Windows Vista. если подключение выполняется к главному компьютеру, на котором работает Windows Server 2008, параметр &quot; оставить на удаленном компьютере &quot; изменен на не &quot; воспроизводить &quot; .)<br/> </dt> <dd></dd> <dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (перенаправление звука включено и режим не &quot; воспроизводится &quot; ).<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td ><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a><br/></td>
<td >Чтение/запись<br/></td>
<td >Задает размер файла виртуального кэша для точечных рисунков 32 бит на пиксель (бит в пикселах). Максимальное значение — 48 МБ.<br/></td>
</tr>
<tr class="odd">
<td ><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>коннектионбаршовпинбуттон</strong></a><br/></td>
<td >Чтение/запись<br/></td>
<td >Указывает, должна ли отображаться кнопка закрепить на панели подключения. По умолчанию значение равно <strong>true</strong>.<br/></td>
</tr>
<tr class="even">
<td ><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>публикмоде</strong></a><br/></td>
<td >Чтение/запись<br/></td>
<td >Указывает, следует ли включить или отключить общедоступный режим. По умолчанию общедоступный режим имеет значение <strong>false</strong>.<br/></td>
</tr>
<tr class="odd">
<td ><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>редиректклипбоард</strong></a><br/></td>
<td >Чтение/запись<br/></td>
<td >Указывает, следует ли включить или отключить перенаправление буфера обмена. По умолчанию режим перенаправления буфера обмена имеет значение <strong>true</strong> (включено).<br/></td>
</tr>
<tr class="even">
<td ><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>редиректдевицес</strong></a><br/></td>
<td >Чтение/запись<br/></td>
<td >Указывает, должны ли перенаправленные устройства быть включены или отключены. По умолчанию для параметра режим перенаправленных устройств задано значение <strong>false</strong>.<br/></td>
</tr>
<tr class="odd">
<td ><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>редиректпосдевицес</strong></a><br/></td>
<td >Чтение/запись<br/></td>
<td >Указывает, следует ли включить или отключить перенаправленные устройства точки обслуживания. По умолчанию режим перенаправленных устройств точки обслуживания имеет значение <strong>false</strong>.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Remarks

Этот интерфейс расширен следующими интерфейсами, при этом каждый новый интерфейс наследует все методы и свойства предыдущих интерфейсов:

-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
-   [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                         |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                   |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 определяется как FBA7F64E-6783-4405-DA45-FA4A763DABD0<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

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

 

