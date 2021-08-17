---
description: следующие константы указывают тип элемента Windowsного получения изображений (WIA).
ms.assetid: 7961f692-088a-4f3b-84e9-5fabb0373c3c
title: Флаги типа элемента WIA (Виадеф. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaItemTypeAnalyze
- WiaItemTypeAudio
- WiaItemTypeBurst
- WiaItemTypeDeleted
- WiaItemTypeDevice
- WiaItemTypeDisconnected
- WiaItemTypeDocument
- WiaItemTypeFile
- WiaItemTypeFolder
- WiaItemTypeFree
- WiaItemTypeGenerated
- WiaItemTypeHasAttachments
- WiaItemTypeHPanorama
- WiaItemTypeImage
- WiaItemTypeProgrammableDataSource
- WiaItemTypeRemoved
- WiaItemTypeRoot
- WiaItemTypeStorage
- WiaItemTypeTransfer
- WiaItemTypeTwainCapabilityPassThrough
- WiaItemTypeVideo
- WiaItemTypeVPanorama
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 5a1a76792a79321ba909607ec7f514a40dac4da92fbbfc4623f87eb99881aaa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965533"
---
# <a name="wia-item-type-flags"></a>Флаги типа элемента WIA

следующие константы указывают тип элемента Windowsного получения изображений (WIA).



| Константа                                                                                                                                                                                                                                                                                     | Описание                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WiaItemTypeAnalyze"></span><span id="wiaitemtypeanalyze"></span><span id="WIAITEMTYPEANALYZE"></span><dl> <dt>**виаитемтипеанализе**</dt> </dl>                                                                             | Этот элемент поддерживает метод [**ивиаитем:: анализеитем**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem) . *эта константа не поддерживается* Windows Vista *и более поздних версий.*<br/>                                                                                                                               |
| <span id="WiaItemTypeAudio"></span><span id="wiaitemtypeaudio"></span><span id="WIAITEMTYPEAUDIO"></span><dl> <dt>**виаитемтипеаудио**</dt> </dl>                                                                                     | Элемент является звуковым файлом. Допускается только для элементов, у которых также есть атрибут **виаитемтипефиле** . <br/>                                                                                                                                                                                     |
| <span id="WiaItemTypeBurst"></span><span id="wiaitemtypeburst"></span><span id="WIAITEMTYPEBURST"></span><dl> <dt>**виаитемтипебурст**</dt> </dl>                                                                                     | Только для папок. Изображения в этой папке были собраны в непрерывной последовательности времени. *эта константа не поддерживается* Windows Vista *и более поздних версий.*<br/>                                                                                                                                       |
| <span id="WiaItemTypeDeleted"></span><span id="wiaitemtypedeleted"></span><span id="WIAITEMTYPEDELETED"></span><dl> <dt>**виаитемтипеделетед**</dt> </dl>                                                                             | Элемент помечается как удаленный из дерева. <br/>                                                                                                                                                                                                                                          |
| <span id="WiaItemTypeDevice"></span><span id="wiaitemtypedevice"></span><span id="WIAITEMTYPEDEVICE"></span><dl> <dt>**виаитемтипедевице**</dt> </dl>                                                                                 | Элемент представляет подключенное устройство. <br/>                                                                                                                                                                                                                                               |
| <span id="WiaItemTypeDisconnected"></span><span id="wiaitemtypedisconnected"></span><span id="WIAITEMTYPEDISCONNECTED"></span><dl> <dt>**виаитемтипедисконнектед**</dt> </dl>                                                         | Элемент представляет отключенное устройство. <br/>                                                                                                                                                                                                                                            |
| <span id="WiaItemTypeDocument"></span><span id="wiaitemtypedocument"></span><span id="WIAITEMTYPEDOCUMENT"></span><dl> <dt>**виаитемтипедокумент**</dt> </dl>                                                                         | Элемент представляет документ. *эта константа поддерживается только* Windows Vista *и более поздних версий.*<br/>                                                                                                                                                                                        |
| <span id="WiaItemTypeFile"></span><span id="wiaitemtypefile"></span><span id="WIAITEMTYPEFILE"></span><dl> <dt>**виаитемтипефиле**</dt> </dl>                                                                                         | Элемент является файлом. <br/>                                                                                                                                                                                                                                                                   |
| <span id="WiaItemTypeFolder"></span><span id="wiaitemtypefolder"></span><span id="WIAITEMTYPEFOLDER"></span><dl> <dt>**виаитемтипефолдер**</dt> </dl>                                                                                 | Элемент является папкой. <br/>                                                                                                                                                                                                                                                                 |
| <span id="WiaItemTypeFree"></span><span id="wiaitemtypefree"></span><span id="WIAITEMTYPEFREE"></span><dl> <dt>**виаитемтипефри**</dt> </dl>                                                                                         | Элемент не инициализирован или был удален. <br/>                                                                                                                                                                                                                                        |
| <span id="WiaItemTypeGenerated"></span><span id="wiaitemtypegenerated"></span><span id="WIAITEMTYPEGENERATED"></span><dl> <dt>**виаитемтипеженератед**</dt> </dl>                                                                     | Этот элемент был создан приложением или драйвером и не имеет соответствующего элемента в дереве элементов драйвера. <br/>                                                                                                                                                               |
| <span id="WiaItemTypeHasAttachments"></span><span id="wiaitemtypehasattachments"></span><span id="WIAITEMTYPEHASATTACHMENTS"></span><dl> <dt>**виаитемтипехасаттачментс**</dt> </dl>                                                 | Элемент содержит вложенные файлы. *эта константа не поддерживается* Windows Vista *и более поздних версий.*<br/>                                                                                                                                                                                          |
| <span id="WiaItemTypeHPanorama"></span><span id="wiaitemtypehpanorama"></span><span id="WIAITEMTYPEHPANORAMA"></span><dl> <dt>**виаитемтипехпанорама**</dt> </dl>                                                                     | Элемент представляет горизонтальное изображение панорамы. *эта константа не поддерживается* Windows Vista *и более поздних версий.*<br/>                                                                                                                                                                       |
| <span id="WiaItemTypeImage"></span><span id="wiaitemtypeimage"></span><span id="WIAITEMTYPEIMAGE"></span><dl> <dt>**виаитемтипеимаже**</dt> </dl>                                                                                     | Элемент является файлом изображения. Допускается только для элементов, у которых также есть атрибут **виаитемтипефиле** . <br/>                                                                                                                                                                                     |
| <span id="WiaItemTypeProgrammableDataSource"></span><span id="wiaitemtypeprogrammabledatasource"></span><span id="WIAITEMTYPEPROGRAMMABLEDATASOURCE"></span><dl> <dt>**виаитемтипепрограммабледатасаурце**</dt> </dl>                 | Элемент представляет программируемый источник данных. *эта константа поддерживается только* Windows Vista *и более поздних версий.*<br/>                                                                                                                                                                        |
| <span id="WiaItemTypeRemoved"></span><span id="wiaitemtyperemoved"></span><span id="WIAITEMTYPEREMOVED"></span><dl> <dt>**виаитемтиперемовед**</dt> </dl>                                                                             | Элемент был удален с устройства. <br/>                                                                                                                                                                                                                                            |
| <span id="WiaItemTypeRoot"></span><span id="wiaitemtyperoot"></span><span id="WIAITEMTYPEROOT"></span><dl> <dt>**виаитемтиперут**</dt> </dl>                                                                                         | Определяет корневой элемент в дереве устройства объектов элементов. *эта константа поддерживается только* Windows Vista *и более поздних версий.*<br/>                                                                                                                                                         |
| <span id="WiaItemTypeStorage"></span><span id="wiaitemtypestorage"></span><span id="WIAITEMTYPESTORAGE"></span><dl> <dt>**виаитемтипестораже**</dt> </dl>                                                                             | Элемент представляет среду хранения. <br/>                                                                                                                                                                                                                                                 |
| <span id="WiaItemTypeTransfer"></span><span id="wiaitemtypetransfer"></span><span id="WIAITEMTYPETRANSFER"></span><dl> <dt>**виаитемтипетрансфер**</dt> </dl>                                                                         | Элемент можно передать. <br/>                                                                                                                                                                                                                                                          |
| <span id="WiaItemTypeTwainCapabilityPassThrough"></span><span id="wiaitemtypetwaincapabilitypassthrough"></span><span id="WIAITEMTYPETWAINCAPABILITYPASSTHROUGH"></span><dl> <dt>**виаитемтипетваинкапабилитипасссраугх**</dt> </dl> | Этот тип указывает, что устройство WIA может получать данные о TWAIN с уровня совместимости TWAIN. Если этот тип задан, то все возможности TWAIN, не распознаваемые уровнем совместимости TWAIN во время сеанса TWAIN, будут переданы драйверу WIA. <br/> |
| <span id="WiaItemTypeVideo"></span><span id="wiaitemtypevideo"></span><span id="WIAITEMTYPEVIDEO"></span><dl> <dt>**виаитемтипевидео**</dt> </dl>                                                                                     | Элемент представляет потоковую передачу видео. *эта константа не поддерживается* Windows Server 2003 *,* Windows Vista *или более поздней версии.*<br/>                                                                                                                                                      |
| <span id="WiaItemTypeVPanorama"></span><span id="wiaitemtypevpanorama"></span><span id="WIAITEMTYPEVPANORAMA"></span><dl> <dt>**виаитемтипевпанорама**</dt> </dl>                                                                     | Элемент представляет вертикальную панорамное изображение. *эта константа не поддерживается* Windows Vista *и более поздних версий.*<br/>                                                                                                                                                                         |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>              |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Виадеф. h</dt> </dl> |



 

 




