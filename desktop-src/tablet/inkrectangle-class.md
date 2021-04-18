---
description: Представляет доступ к прямоугольнику.
ms.assetid: 78e6c29c-0f43-46a5-9d30-948de5f369c8
title: Класс Инкректангле (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRectangle
- InkRectangle.IInkRectangle
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: d643696fe19523bac93ebca71cf885cd93b8570a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713066"
---
# <a name="inkrectangle-class"></a>Класс Инкректангле

Представляет доступ к прямоугольнику.

**Инкректангле** имеет следующие типы членов:

-   [Интерфейсы](#interfaces)
-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="interfaces"></a>Интерфейсы

Класс **инкректангле** определяет эти интерфейсы.



| Интерфейс         | Описание                                                            |
|:------------------|:-----------------------------------------------------------------------|
| **иинкректангле** | Этот объект реализует COM-интерфейс **иинкректангле** .<br/> |



 

### <a name="methods"></a>Методы

Класс **инкректангле** содержит следующие методы.



| Метод                                            | Описание                                                                        |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**@ Rectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-getrectangle) | Извлекает элементы объекта **инкректангле** в одном вызове.<br/> |
| [**сетректангле**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-setrectangle) | Изменяет элементы объекта **инкректангле** в одном вызове.<br/>  |



 

### <a name="properties"></a>Свойства

Класс **инкректангле** имеет следующие свойства.



| Свойство                                         | Тип доступа           | Описание                                                        |
|:-------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [**Нижнее**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom)<br/> | Чтение/запись<br/> | Возвращает или задает нижнюю точку прямоугольника.<br/>      |
| [**Data**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_data)<br/>     | Чтение/запись<br/> | Возвращает или задает доступ к структуре прямоугольника (только C++).<br/> |
| [**Слева**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left)<br/>     | Чтение/запись<br/> | Возвращает или задает левую точку прямоугольника.<br/>        |
| [**Правильно**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right)<br/>   | Чтение/запись<br/> | Возвращает или задает правую точку прямоугольника.<br/>       |
| [**Вверх**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top)<br/>       | Чтение/запись<br/> | Возвращает или задает верхнюю точку прямоугольника.<br/>         |



 

## <a name="remarks"></a>Комментарии

> [!Note]  
> Точка находится внутри **инкректангле** , если она находится на [**левой**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left) или [**верхней**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top) стороне или находится внутри всех четырех сторон. Точка с [**правой**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right) или [**нижней**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom) стороны считается за пределами прямоугольника.

 

Для создания экземпляра этого объекта можно вызвать метод [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .

> [!Note]  
> Невозможно использовать **инкректангле** , если он больше, чем Long \_ Max (2 ^ 31-1) в любом измерении.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



 

