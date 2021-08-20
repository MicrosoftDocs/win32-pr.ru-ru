---
title: Обработка ошибок COM в Java и Visual Basic
description: Обработка ошибок COM в Java и Visual Basic
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba8e179ca3e7a1d57fdae63e8ad20d14a6fff358fab1fff24bfe7ae8df185d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048522"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a>Обработка ошибок COM в Java и Visual Basic

Существует три интерфейса и три функции, которые можно использовать в COM для обеспечения обработки ошибок при программировании на Java или Microsoft Visual Basic. в Java и Visual Basic вызов метода не возвращает **HRESULT** в качестве возвращаемого значения. Вместо этого эти языки используют COM-интерфейсы и функции для получения значений **HRESULT** и для управления ошибками или исключениями. (Исключения — это события, которые выходят за рамки управления программой, например проблемы с файлами или недопустимые параметры.)

В следующей таблице приведены три интерфейса, обеспечивающие поддержку для **HRESULT** s.



|  Интерфейс                                                                        |  Описание                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**икреатирроринфо**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | Задает сведения об ошибке.<br/>                                                                                   |
| [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | Возвращает сведения из объекта ошибки.<br/>                                                                 |
| [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | Определяет объект как поддерживающий интерфейс [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .<br/> |



 

Три функции, которые обеспечивают поддержку для **HRESULT** s, перечислены и кратко описаны в следующей таблице.



|    Интерфейс       |       Описание       |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**креатирроринфо**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | Создает экземпляр универсального объекта Error.<br/>                                                                                                            |
| [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | Получает указатель сведений об ошибке, заданный предыдущим вызовом [**сетерроринфо**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) в текущем логическом потоке.<br/> |
| [**сетерроринфо**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | Задает объект сведений об ошибке для текущего потока выполнения.<br/>                                                                                    |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Обработка ошибок в COM](error-handling-in-com.md)
</dt> </dl>

 

