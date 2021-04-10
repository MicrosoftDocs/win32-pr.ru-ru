---
title: Коды ошибок (Уиаутоматионкореапи. h)
description: В этом разделе описываются коды ошибок, предоставляемые Microsoft UI Automation.
ms.assetid: f7820aa3-908e-426e-851c-84397019d735
topic_type:
- apiref
api_name:
- UIA_E_ELEMENTNOTAVAILABLE
- UIA_E_ELEMENTNOTENABLED
- UIA_E_INVALIDOPERATION
- UIA_E_NOCLICKABLEPOINT
- UIA_E_NOTSUPPORTED
- UIA_E_PROXYASSEMBLYNOTLOADED
- UIA_E_TIMEOUT
api_location:
- UIAutomationCoreApi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaa03746bfb1a5e56fcac8b39d326581159f459
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071048"
---
# <a name="error-codes-uiautomationcoreapih"></a>Коды ошибок (Уиаутоматионкореапи. h)

В этом разделе описываются коды ошибок, предоставляемые Microsoft UI Automation. Список сортируется в алфавитном порядке по имени.



| Константа/значение                                                                                                                                                                                                                                                              | Описание                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIA_E_ELEMENTNOTAVAILABLE"></span><span id="uia_e_elementnotavailable"></span><dl> <dt>**UIA \_ E \_ елементнотаваилабле**</dt> <dt>0x80040201</dt> </dl>          | Указывает, что метод был вызван для виртуализированного элемента или для элемента, который больше не существует, обычно потому, что он был уничтожен. <br/>                                                                                                  |
| <span id="UIA_E_ELEMENTNOTENABLED"></span><span id="uia_e_elementnotenabled"></span><dl> <dt>**UIA \_ E \_ елементнотенаблед**</dt> <dt>0x80040200</dt> </dl>                | Указывает, что метод, которому требуется включенный элемент, такой как [**SELECT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) или [**expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand), был вызван для элемента, который был отключен. <br/>             |
| <span id="UIA_E_INVALIDOPERATION"></span><span id="uia_e_invalidoperation"></span><dl> <dt>**UIA \_ E \_ INVALIDOPERATION**</dt> <dt>0x80131509</dt> </dl>                   | Указывает, что метод попытался выполнить операцию, которая является недопустимой.<br/>                                                                                                                                                                          |
| <span id="UIA_E_NOCLICKABLEPOINT"></span><span id="uia_e_noclickablepoint"></span><dl> <dt>**UIA \_ E \_ нокликкаблепоинт**</dt> <dt>0x80040202</dt> </dl>                   | Указывает, что метод [**жеткликкаблепоинт**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) был вызван для элемента, который не имеет точки, которую нельзя щелкнуть.<br/>                                                                                    |
| <span id="UIA_E_NOTSUPPORTED"></span><span id="uia_e_notsupported"></span><dl> <dt>**UIA \_ E \_ NOTSUPPORTED**</dt> <dt>0x80040204</dt> </dl>                               | Указывает, что поставщик явно не поддерживает указанное свойство или шаблон элемента управления. Модель автоматизации пользовательского интерфейса возвратит этот код ошибки вызывающему объекту без попытки предоставить значение по умолчанию или вернуться к другому поставщику.<br/> |
| <span id="UIA_E_PROXYASSEMBLYNOTLOADED"></span><span id="uia_e_proxyassemblynotloaded"></span><dl> <dt>**UIA \_ E \_ проксяссемблинотлоадед**</dt> <dt>0x80040203</dt> </dl> | Указывает, что возникла проблема при загрузке сборки, содержащей клиентский поставщик (прокси-сервер).<br/>                                                                                                                                      |
| <span id="UIA_E_TIMEOUT"></span><span id="uia_e_timeout"></span><dl> <dt>**UIA \_ E \_ timeout**</dt> <dt>0x80131505</dt> </dl>                                                      | Указывает, что время, выделенное для процесса или операции, истекло.<br/>                                                                                                                                                                      |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                                      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                             |
| Header<br/>                   | <dl> <dt>Уиаутоматионкореапи. h</dt> </dl> |



 

 





