---
description: Представляет Управление сопоставлениями от рукописного ввода к окну отображения. Используйте объект Инкрендерер для вывода рукописного ввода в окне. Его также можно использовать для изменения расположения и изменения размера штриха.
ms.assetid: 66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7
title: Класс Инкрендерер (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRenderer
- InkRenderer.IInkRenderer
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: f03b65a1ce009313b996fc7bede03f8c7425ff589fd29506c243f3161a851583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938724"
---
# <a name="inkrenderer-class"></a>Класс Инкрендерер

Представляет Управление сопоставлениями от рукописного ввода к окну отображения. Используйте объект **инкрендерер** для вывода рукописного ввода в окне. Его также можно использовать для изменения расположения и изменения размера штриха.

**Инкрендерер** имеет следующие типы членов:

-   [Интерфейсы](#interfaces)
-   [Методы](#methods)

### <a name="interfaces"></a>Интерфейсы

Класс **инкрендерер** определяет эти интерфейсы.



| Интерфейс        | Описание                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **иинкрендерер** | Этот объект реализует COM-интерфейс **иинкрендерер** .<br/> |



 

### <a name="methods"></a>Методы

Класс **инкрендерер** содержит следующие методы.



| Метод                                                                     | Описание                                                                                                                                              |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw)                                           | Рисует штрихи в контексте устройства.<br/>                                                                                                            |
| [**дравстроке**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)                               | Рисует штрих для указанного контекста устройства Windows.<br/>                                                                                       |
| [**жетобжекттрансформ**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform)               | Возвращает преобразование объекта, которое использовалось для отрисовки рукописного ввода.<br/>                                                                                   |
| [**жетвиевтрансформ**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform)                   | Возвращает преобразование представления, используемое для визуализации рукописного ввода.<br/>                                                                                      |
| [**инкспацетопиксел**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel)                     | Преобразует положение в координатах рукописного пространства в виде пиксельного пространства.<br/>                                                                            |
| [**инкспацетопикселфромпоинтс**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints) | Преобразует массив точек в координатах рукописного пространства в пиксельное пространство.<br/>                                                                          |
| [**Мера**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-measure)                                     | Вычисляет прямоугольник в контексте устройства, который будет содержать коллекцию штрихов, если они были выведены с помощью объекта **инкрендерер** .<br/> |
| [**меасурестроке**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrenderer-measurestroke)                         | Вычисляет прямоугольник в контексте устройства, который будет содержать штрих, если они были выведены с помощью объекта **инкрендерер** .<br/>                |
| [**Переместить**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-move)                                           | Применяет перевод к преобразованию представления в координатах рукописного ввода.<br/>                                                                         |
| [**пикселтоинкспаце**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace)                     | Преобразует положение в координатах пикселей в виде рукописного ввода.<br/>                                                                                  |
| [**пикселтоинкспацефромпоинтс**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints) | Преобразует массив точек в координатах пиксельного пространства в область рукописного ввода.<br/>                                                                          |
| [**Поворот**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-rotate)                                       | Применяет поворот к преобразованию представления.<br/>                                                                                                     |
| [**ScaleTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-scaletransform)                       | Масштабирует преобразование представления в измерении X и Y.<br/>                                                                                           |
| [**сетобжекттрансформ**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)               | Задает преобразование объекта, используемое для отрисовки рукописного ввода.<br/>                                                                                         |
| [**сетвиевтрансформ**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform)                   | Задает преобразование представления, используемое для визуализации рукописного ввода.<br/>                                                                                           |



 

## <a name="remarks"></a>Remarks

Печать также выполняется через объект **инкрендерер** .

Для создания экземпляра этого объекта можно вызвать метод [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) в C++.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Заголовок<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Свойство модуля подготовки отчетов**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)
</dt> <dt>

[**Класс Инкдравингаттрибутес**](inkdrawingattributes-class.md)
</dt> <dt>

[**Интерфейс Иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[Коллекция Инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

