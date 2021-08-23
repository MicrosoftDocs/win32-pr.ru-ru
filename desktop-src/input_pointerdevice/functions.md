---
description: В подразделах этого раздела приведены справочные сведения о функциях входного стека устройства с указателем.
ms.assetid: 44942954-3EA6-4C33-8CF1-E8BF72A914CB
title: Функции (входной стек устройства указателя)
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: 5101847d78f396edcb317986ab3d95d578dabdfe12197531787115f49c9a69a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611744"
---
# <a name="pointer-device-input-stack-functions"></a>Функции стека входных данных устройства указателя

В подразделах этого раздела приведены справочные сведения о функциях [входного стека устройства с указателем](pointer-device-stack-portal.md) .

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|---|---|
| [**креатесинсетикпоинтердевице**](/windows/win32/api/winuser/nf-winuser-createsyntheticpointerdevice)<br/> | Настраивает устройство вставки указателя для вызывающего приложения и инициализирует максимальное число одновременных указателей, которые может ввести приложение.<br/> |
| [**дестройсинсетикпоинтердевице**](/windows/win32/api/winuser/nf-winuser-destroysyntheticpointerdevice)<br/> | Уничтожает указанное устройство внедрения указателя.<br/> |
| [**жетпоинтердевице**](/windows/win32/api/winuser/nf-winuser-getpointerdevice)<br/> | Возвращает сведения об устройстве указателя.<br/> |
| [**жетпоинтердевицекурсорс**](/windows/win32/api/winuser/nf-winuser-getpointerdevicecursors)<br/> | Возвращает идентификаторы курсоров, сопоставленные с курсорами, связанными с устройством указателя.<br/> |
| [**жетпоинтердевицепропертиес**](/windows/win32/api/winuser/nf-winuser-getpointerdeviceproperties)<br/> | Возвращает свойства устройства, которые не входят в [**структуру \_ \_ сведений об устройстве указателей**](/previous-versions/windows/desktop/api) . <br/> |
| [**жетпоинтердевицеректс**](/windows/win32/api/winuser/nf-winuser-getpointerdevicerects)<br/> | Возвращает диапазон x и y для устройства указателя (в HIMETRIC) и диапазона x и y (текущее разрешение) для отображения, с которым сопоставлен указатель устройства. <br/> |
| [**жетпоинтердевицес**](/windows/win32/api/winuser/nf-winuser-getpointerdevices)<br/> | Возвращает сведения об устройствах указателей, подключенных к системе.<br/> |
| [**жетравпоинтердевицедата**](/windows/win32/api/winuser/nf-winuser-getrawpointerdevicedata)<br/> | Получает необработанные входные данные с устройства указателя. <br/> |
| [**инжектсинсетикпоинтеринпут**](/windows/win32/api/winuser/nf-winuser-injectsyntheticpointerinput)<br/> | Имитирует ввод указателя (перо или касание).<br/> |
| [**регистерпоинтердевиценотификатионс**](/windows/win32/api/winuser/nf-winuser-registerpointerdevicenotifications)<br/> | Регистрирует окно для обработки уведомлений [**WM_POINTERDEVICECHANGE**](../inputmsg/wm-pointerdevicechange.md), [**WM_POINTERDEVICEINRANGE**](../inputmsg/wm-pointerdeviceinrange.md)и [**WM_POINTERDEVICEOUTOFRANGE**](../inputmsg/wm-pointerdeviceoutofrange.md) указателя устройств.<br/> |

## <a name="related-topics"></a>Связанные темы

[Указатель на входной стек устройства указателя](unified-input-stack-reference.md)
