---
title: Функции (проверка нажатия касания)
description: В подразделах этого раздела приводятся справочные сведения по функциям проверки попадания в касание.
ms.assetid: C7275A12-4F76-485D-896F-3CCB8CE92F8E
keywords:
- взаимодействие с пользователем
- input
- указатель
- Сенсорный ввод
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 83ab93fbff031423b6478926e499077ac78b1aec686d596ca069fda6d1b2298b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248361"
---
# <a name="touch-hit-testing-functions"></a>Функции проверки нажатия касания

В подразделах этого раздела приводятся справочные сведения по [функциям проверки попадания в касание](functions.md).

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
| --- | --- |
| [**евалуатепроксимититополигон**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytopolygon)<br/> | Возвращает оценку многоугольника как вероятного сенсорного объекта (по сравнению со всеми другими многоугольниками, пересекающимися с контактной областью касания) и настроенной сенсорной точке многоугольника. <br/> |
| [**евалуатепроксимититорект**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytorect)<br/> | Возвращает оценку прямоугольника как вероятного сенсорного объекта, по сравнению с другими прямоугольниками, пересекающимися с контактной областью касания, и скорректированной сенсорной точкой внутри прямоугольника. <br/> |
| [**пакктаучхиттестингпроксимитевалуатион**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)<br/> | Возвращает оценку оценки близости, а также скорректированные координаты сенсорной точки в виде упакованного значения для обратного вызова [WM_TOUCHHITTESTINGного сообщения](../inputmsg/wm-touchhittesting.md) . <br/> |
| [**регистертаучхиттестингвиндов**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)<br/> | Регистрирует окно для обработки уведомления [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md)<br/> |

## <a name="related-topics"></a>Связанные темы

[Ссылка на проверку нажатия касания](touchhittest-reference.md)
