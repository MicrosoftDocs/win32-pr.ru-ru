---
title: Сообщение CCM_DPISCALE (Коммктрл. h)
description: Включает автоматическое масштабирование с высоким числом точек на дюйм в элементах управления Tree-View, List-View элементах управления, элементах управления ComboBoxEx, элементах управления "заголовок", кнопках, элементах управления ToolBar, анимации и списках изображений.
ms.assetid: 3c751f10-992c-41f8-8f0b-3dc58f0591e4
keywords:
- Элементы управления Windows для CCM_DPISCALE сообщений
topic_type:
- apiref
api_name:
- CCM_DPISCALE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef978f486f370adf9872d28e1accbacc37a6de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136458"
---
# <a name="ccm_dpiscale-message"></a>\_Сообщение ДПИСКАЛЕ CCM

Включает автоматическое масштабирование с высоким числом точек на дюйм в [древовидном представлении](tree-view-controls.md), [элементах управления "представление списка](list-view-control-reference.md)", [элементах](comboboxex-controls.md)управления "ComboBoxEx", [элементах управления "заголовок](header-controls.md)", [кнопках](buttons.md), [элементах управления ToolBar](toolbar-controls-overview.md), [элементах управления анимации](animation-control-overview.md)и [списках изображений](image-lists.md).

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Задайте значение **true**.

</dd> <dt>

*lParam* 
</dt> <dd>

Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение не используется.

## <a name="remarks"></a>Комментарии

Для быстрого запуска и [панели задач](/windows/desktop/shell/taskbar) не следует указывать масштабирование DPI, так как изображения уже масштабируются.

Любой элемент управления, использующий список изображений, созданный с помощью метрики маленькие значки, не должен масштабировать свои значки.

> [!Note]  
> Чтобы использовать этот API, необходимо предоставить манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

