---
description: Показывает члены класса Кксапопараметерсбасе.
ms.assetid: C2113358-07DE-426E-AF26-BD8ED9902192
title: Элементы Кксапопараметерсбасе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 554aa66b4166bc3d0de4db685e0f6e7b54e6ebf5
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423874"
---
# <a name="cxapoparametersbase-members"></a>Элементы Кксапопараметерсбасе

Показывает члены класса [**кксапопараметерсбасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) .

## <a name="public-constructors"></a>Открытые конструкторы



|    Конструктор                                                |     Описание                                                                    |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**кксапопараметерсбасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) | Конструирует объект [**кксапопараметерсбасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) . |



 

## <a name="public-methods"></a>Открытые методы



|        Метод                                                                                                                      |     Описание                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddRef**](/previous-versions/windows/desktop/legacy/ee418448(v=vs.85)) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                         | Увеличивает значение счетчика ссылок объекта КСАПО.<br/>                                                                                                         |
| [**бегинпроцесс**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess)                                                                     | Возвращает текущие параметры процесса. <br/>                                                                                                              |
| [**КалЦинпутфрамес**](/windows/win32/api/xapo/nf-xapo-ixapo-calcinputframes) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                           | Возвращает количество входных кадров, необходимых для создания заданного числа выходных кадров.<br/>                                                            |
| [**Калкаутпутфрамес**](/windows/win32/api/xapo/nf-xapo-ixapo-calcoutputframes) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                         | Возвращает количество выходных кадров, необходимых для создания заданного числа входных кадров.<br/>                                                            |
| [**ендпроцесс**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess)                                                                         | Уведомляет [**кксапопараметерсбасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) о том, что ксапо завершил доступ к текущим параметрам процесса. <br/>                     |
| [**Parameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters) (наследуется от [**иксапопараметерс**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)) | Возвращает параметры, зависящие от влияния. <br/>                                                                                                                     |
| [**Жетрегистратионпропертиес**](/windows/win32/api/xapo/nf-xapo-ixapo-getregistrationproperties) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))       | Возвращает свойства регистрации КСАПО.<br/>                                                                                                       |
| [**Инициализировать**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                     | Выполняет любую инициализацию, зависящую от влияния.<br/>                                                                                                          |
| [**Исинпутформатсуппортед**](/windows/win32/api/xapo/nf-xapo-ixapo-isinputformatsupported) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))             | Запросы, если для заданного формата вывода поддерживается определенный входной формат.<br/>                                                                            |
| [**Исаутпутформатсуппортед**](/windows/win32/api/xapo/nf-xapo-ixapo-isoutputformatsupported) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))           | Запросы, если для заданного входного формата поддерживается определенный формат вывода.<br/>                                                                            |
| [**Локкфорпроцесс**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                             | Уведомляет о КСАПО [**процесса**](/windows/win32/api/xapo/nf-xapo-ixapo-process) форматов потока.<br/>                                                             |
| [**онсетпараметерс**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-onsetparameters)                                                               | Вызывается методом [**иксапопараметерс:: SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) , чтобы разрешить проверку параметров, определяемых пользователем. <br/>          |
| [**параметерсчанжед**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-parameterschanged)                                                           | Указывает, вызывалось ли [**иксапопараметерс:: SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) с момента последнего прохода обработки. <br/>       |
| [**QueryInterface**](/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                         | Извлекает запрошенный указатель интерфейса, если КСАПО поддерживает его.<br/>                                                                                    |
| [**Выпуск**](/previous-versions/windows/desktop/legacy/ee418458(v=vs.85)) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                       | Уменьшает значение счетчика ссылок объекта КСАПО и удаляет объект, если счетчик ссылок становится равным нулю.<br/>                                             |
| [**Сброс**](/windows/win32/api/xapo/nf-xapo-ixapo-reset) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                               | Возвращает объект в состояние, в котором он находился сразу после вызова [**локкфорпроцесс**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) .<br/>                             |
| [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) (наследуется от [**иксапопараметерс**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)) | Задает параметры, относящиеся к конкретному результату.<br/>                                                                                                                      |
| [**Унлоккфорпроцесс**](/windows/win32/api/xapo/nf-xapo-ixapo-unlockforprocess) (наследуется от [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                         | Противоположность Локкфорпроцесс: переменные, выделенные во время [**локкфорпроцесс**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) , должны быть освобождены в этом методе.<br/> |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Класс Кксапопараметерсбасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase)
</dt> </dl>

 

 
