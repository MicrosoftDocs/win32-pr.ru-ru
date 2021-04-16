---
description: Представляет матрицу 3x3, которая, в свою очередь, представляет аффинное преобразование.
ms.assetid: 79abff2e-d1d3-4a32-9ac2-f46c1b21f742
title: Класс Инктрансформ (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkTransform
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 61641f0fed8ec98321e155f82ff9a35150e7fdcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713065"
---
# <a name="inktransform-class"></a>Класс Инктрансформ

Представляет матрицу 3x3, которая, в свою очередь, представляет аффинное преобразование.

**Инктрансформ** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **инктрансформ** содержит следующие методы.



| Метод                                                  | Описание                                                                                                                 |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**Преобразование**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-gettransform)       | Извлекает **инктрансформ** как 6 с плавающей запятой.<br/>                                                                      |
| [**Характеризу**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reflect)                 | Отражает преобразование в горизонтальном или вертикальном направлении.<br/>                                          |
| [**Перезапуск**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reset)                     | Сбрасывает преобразование в исходное состояние.<br/>                                                                      |
| [**Поворот**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-rotate)                   | Поворачивает преобразование на угол, измеренный в градусах, и при необходимости задает центральную точку для поворота.<br/> |
| [**ScaleTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-scaletransform) | Масштабирует преобразование по коэффициентам X и Y.<br/>                                                                         |
| [**сеттрансформ**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-settransform)       | Изменяет **инктрансформ** , используя 6 с плавающей запятой.<br/>                                                                    |
| [**Сдвиг**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-shear)                     | Применяет наклон с заданными коэффициентами горизонтального и вертикального.<br/>                                              |
| [**Перевести**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-translate)             | Перемещает преобразование на указанные горизонтальные и вертикальные компоненты.<br/>                                         |



 

### <a name="properties"></a>Свойства

Класс **инктрансформ** имеет следующие свойства.



| Свойство                                     | Тип доступа           | Описание                                                                                          |
|:---------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [**Данные**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_data)<br/> | Чтение/запись<br/> | Возвращает или задает версию автоматизации структуры XFORM WIN32.<br/>                            |
| [**eDx**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edx)<br/>   | Чтение/запись<br/> | Возвращает или задает вещественное число, указывающее элемент в третьей строке, первый столбец.<br/>   |
| [**еди**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edy)<br/>   | Чтение/запись<br/> | Возвращает или задает вещественное число, указывающее элемент в третьей строке второго столбца.<br/>  |
| [**eM11**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em11)<br/> | Чтение/запись<br/> | Возвращает или задает вещественное число, указывающее элемент в первой строке, первый столбец.<br/>   |
| [**eM12**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em12)<br/> | Чтение/запись<br/> | Возвращает или задает вещественное число, указывающее элемент в первой строке второго столбца.<br/>  |
| [**eM21**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em21)<br/> | Чтение/запись<br/> | Возвращает или задает вещественное число, указывающее элемент во второй строке, первый столбец.<br/>  |
| [**eM22**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em22)<br/> | Чтение/запись<br/> | Возвращает или задает вещественное число, указывающее элемент во второй строке второго столбца.<br/> |



 

## <a name="remarks"></a>Комментарии

Для создания экземпляра этого объекта можно вызвать метод [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) в C++.

Объект хранит только шесть из девяти чисел в матрице 3x3, так как все матрицы 3x3, представляющие аффинных преобразований, имеют тот же третий столбец (0, 0, 1). Этот объект в свою очередь используется для описания операций преобразования, таких как перемещение, наклон, масштабирование или вращение в объекте [**инкрендерер**](inkrenderer-class.md) , [**Иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) Object или [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) Collection.

> [!Note]  
> Объект **инктрансформ** соотносится с структурой [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) .

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



 

