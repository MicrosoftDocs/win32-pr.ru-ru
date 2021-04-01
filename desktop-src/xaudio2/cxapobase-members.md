---
description: Показывает члены класса Кксапобасе.
ms.assetid: 0791888B-7215-475B-95C8-B558A1E57783
title: Элементы Кксапобасе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ab63cf7e8ac6e4d0fa14ec412b53682aff2ba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081093"
---
# <a name="cxapobase-members"></a>Элементы Кксапобасе

Показывает члены класса [**кксапобасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) .

## <a name="public-constructors"></a>Открытые конструкторы



|                                |                                                     |
|--------------------------------|-----------------------------------------------------|
| [**кксапобасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) | Конструирует объект [**кксапобасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) . |



 

## <a name="public-methods"></a>Открытые методы



|                                                                                                                        |                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddRef**](/previous-versions/windows/desktop/legacy/ee418448(v=vs.85)) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                   | Увеличивает значение счетчика ссылок объекта КСАПО.<br/>                                                                                                         |
| [**КалЦинпутфрамес**](/windows/win32/api/xapo/nf-xapo-ixapo-calcinputframes) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                     | Возвращает количество входных кадров, необходимых для создания заданного числа выходных кадров.<br/>                                                            |
| [**Калкаутпутфрамес**](/windows/win32/api/xapo/nf-xapo-ixapo-calcoutputframes) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                   | Возвращает количество выходных кадров, необходимых для создания заданного числа входных кадров.<br/>                                                            |
| [**Жетрегистратионпропертиес**](/windows/win32/api/xapo/nf-xapo-ixapo-getregistrationproperties) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo)) | Возвращает свойства регистрации КСАПО.<br/>                                                                                                       |
| [**Инициализировать**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                               | Выполняет любую инициализацию, зависящую от влияния.<br/>                                                                                                          |
| [**Исинпутформатсуппортед**](/windows/win32/api/xapo/nf-xapo-ixapo-isinputformatsupported) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))       | Запросы, если для заданного формата вывода поддерживается определенный входной формат.<br/>                                                                            |
| [**Исаутпутформатсуппортед**](/windows/win32/api/xapo/nf-xapo-ixapo-isoutputformatsupported) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))     | Запросы, если для заданного входного формата поддерживается определенный формат вывода.<br/>                                                                            |
| [**Локкфорпроцесс**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                       | Уведомляет о КСАПО [**процесса**](/windows/win32/api/xapo/nf-xapo-ixapo-process) форматов потока.<br/>                                                             |
| [**QueryInterface**](/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                   | Извлекает запрошенный указатель интерфейса, если КСАПО поддерживает его.<br/>                                                                                    |
| [**Выпуск**](/previous-versions/windows/desktop/legacy/ee418458(v=vs.85)) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                 | Уменьшает значение счетчика ссылок объекта КСАПО и удаляет объект, если счетчик ссылок становится равным нулю.<br/>                                             |
| [**Сброс**](/windows/win32/api/xapo/nf-xapo-ixapo-reset) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                         | Возвращает объект в состояние, в котором он находился сразу после вызова [**локкфорпроцесс**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) .<br/>                             |
| [**Унлоккфорпроцесс**](/windows/win32/api/xapo/nf-xapo-ixapo-unlockforprocess) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                   | Противоположность Локкфорпроцесс: переменные, выделенные во время [**локкфорпроцесс**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) , должны быть освобождены в этом методе.<br/> |



 

## <a name="protected-methods"></a>Защищенные методы



|                                                                                          |                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**жетрегистратионпропертиесинтернал**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-getregistrationpropertiesinternal) | Возвращает указатель на структуру [**\_ \_ свойств регистрации ксапо**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties), содержащую свойства регистрации, с которыми был создан ксапо.<br/> |
| [**IsLocked**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-islocked)                                                   | Проверяет, заблокирован ли КСАПО.<br/>                                                                                                                                                |
| LONG m \_ лреференцекаунт<br/>                                                       | Счетчик ссылок COM объекта КСАПО.<br/>                                                                                                                                       |
| [**процесссру**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-processthru)                                             | Вызывается реализацией [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , когда ксапо отключена для обработки в ходе выполнения.<br/>                                                  |
| [**валидатеформатдефаулт**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-validateformatdefault)                         | Проверяет, попадает ли звуковой формат в поддерживаемые диапазоны по умолчанию.<br/>                                                                                                     |
| [**валидатеформатпаир**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-validateformatpair)                               | Проверяет, поддерживается ли конфигурация пар входного и выходного форматов в отношении флагов свойств КСАПО.<br/>                                                            |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Класс Кксапобасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)
</dt> </dl>

 

 
