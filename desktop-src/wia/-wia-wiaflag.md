---
description: 'Флаги, используемые методами Ивиадевмгр:: Жетимажедлг, IWiaDevMgr2:: Жетимажедлг, Ивиаитем::D Евицедлг и IWiaItem2::D Евицедлг для управления операцией диалогового окна.'
ms.assetid: 468a3c9e-64f8-456d-aad9-fa7c6876fbe6
title: Виафлаг (Виадеф. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DEVICE_DIALOG_SINGLE_IMAGE
- WIA_DEVICE_DIALOG_USE_COMMON_UI
- WIA_SELECT_DEVICE_NODEFAULT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: c906f22e168ca29aadd2e9450fac6225c8b91c17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656119"
---
# <a name="wiaflag"></a>виафлаг

Флаги, используемые методами [**ивиадевмгр:: жетимажедлг**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg), [**IWiaDevMgr2:: жетимажедлг**](-wia-iwiadevmgr2-getimagedlg.md), [**Ивиаитем::D Евицедлг**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)и [**IWiaItem2::D евицедлг**](-wia-iwiaitem2-devicedlg.md) для управления операцией диалогового окна.



| Константа                                                                                                                                                                                                                | Описание                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DEVICE_DIALOG_SINGLE_IMAGE"></span><span id="wia_device_dialog_single_image"></span><dl> <dt>**\_ \_ \_ одиночное изображение диалогового окна WIA устройства \_**</dt> </dl>     | Ограничить выбор изображения одним изображением в диалоговом окне "получение образа устройства".<br/>                                                                                                           |
| <span id="WIA_DEVICE_DIALOG_USE_COMMON_UI"></span><span id="wia_device_dialog_use_common_ui"></span><dl> <dt>**\_ \_ \_ \_ Общий \_ Пользовательский интерфейс диалогового окна устройства WIA**</dt> </dl> | Используйте пользовательский интерфейс системы, если он доступен, а не пользовательский интерфейс, предоставляемый поставщиком. Если пользовательский интерфейс системы недоступен, используется пользовательский интерфейс поставщика. Если ни один из ИНТЕРФЕЙСов не доступен, функция возвращает E \_ нотимпл.<br/>      |
| <span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span><dl> <dt>**WIA \_ SELECT \_ устройство не \_ по умолчанию**</dt> </dl>               | Выполните принудительный вызов метода [**ивиадевмгр:: жетимажедлг**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) или [**IWiaDevMgr2:: жетимажедлг**](-wia-iwiadevmgr2-getimagedlg.md) , чтобы отобразить диалоговое окно **Выбор устройства** .<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                |
| Header<br/>                   | <dl> <dt>Виадеф. h</dt> </dl> |



 

 




