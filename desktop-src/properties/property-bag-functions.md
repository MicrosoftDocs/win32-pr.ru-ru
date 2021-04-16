---
description: В этом разделе описывается набор вспомогательных функций Windows, используемых с объектами Ипропертибаг.
ms.assetid: 4ef85855-7eb6-43ec-bf29-1223eaf1a0cc
title: Функции контейнера свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c86a2e3ce61805702641f893d51f5c4aa26b0ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712155"
---
# <a name="property-bag-functions"></a>Функции контейнера свойств

В этом разделе описывается набор вспомогательных функций Windows, используемых с объектами [**ипропертибаг**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) .



| Раздел                                                                       | Содержимое                                                                                                                     |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**Пспропертибаг \_ Удаление**](/windows/win32/api/propsys/nf-propsys-pspropertybag_delete)                     | Удаляет свойство из контейнера свойств.<br/>                                                                           |
| [**Пспропертибаг \_ реадбул**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbool)                 | Считывает значение **логического** типа данных свойства в контейнере свойств.<br/>                                                    |
| [**Пспропертибаг \_ реадбстр**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbstr)                 | Считывает значение данных **BSTR** из свойства в контейнере свойств.<br/>                                                    |
| [**Пспропертибаг \_ реаддворд**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readdword)               | Считывает значение **DWORD** данных из свойства в контейнере свойств.<br/>                                                     |
| [**Пспропертибаг \_ реадгуид**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readguid)                 | Считывает значение данных GUID из свойства в контейнере свойств.<br/>                                                      |
| [**Пспропертибаг \_ ReadInt**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readint)                   | Считывает значение данных **типа int** из свойства в контейнере свойств.<br/>                                                    |
| [**Пспропертибаг \_ реадлонг**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readlong)                 | Считывает **длинное** значение данных из свойства в контейнере свойств.<br/>                                                    |
| [**Пспропертибаг \_ реадпоинтл**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpointl)             | Получает координаты свойств, хранящиеся в [**точечной**](/previous-versions//dd162807(v=vs.85)) структуре указанного контейнера свойств.<br/>    |
| [**Пспропертибаг \_ реадпоинтс**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpoints)             | Получает координаты свойств, хранящиеся в структуре [**точек**](/previous-versions//dd162808(v=vs.85)) указанного контейнера свойств.<br/>    |
| [**Пспропертибаг \_ реадпропертикэй**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpropertykey)   | Считывает ключ свойства свойства в указанном контейнере свойств.<br/>                                                 |
| [**Пспропертибаг \_ реадректл**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readrectl)               | Получает координаты прямоугольника, хранящегося в свойстве, содержащемся в указанном контейнере свойств.<br/>              |
| [**Пспропертибаг \_ реадшорт**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readshort)               | Считывает значение **короткого** значения данных свойства в контейнере свойств.<br/>                                                   |
| [**Пспропертибаг \_ реадстр**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstr)                   | Считывает значение **строковых** данных свойства в контейнере свойств.<br/>                                                  |
| [**Пспропертибаг \_ реадстраллок**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstralloc)         | Считывает **строковое** значение данных из свойства в контейнере свойств и выделяет память для считываемых строк.<br/> |
| [**Пспропертибаг \_ реадстреам**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstream)             | Считывает поток данных, хранящийся в заданном свойстве, который содержится в указанном контейнере свойств.<br/>                           |
| [**Пспропертибаг \_ реадтипе**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readtype)                 | Считывает тип значения данных свойства, хранящегося в контейнере свойств.<br/>                                      |
| [**Пспропертибаг \_ реадулонглонг**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readulonglong)       | Считывает значение данных **улонглонг** из свойства в контейнере свойств.<br/>                                               |
| [**Пспропертибаг \_ реадункновн**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readunknown)           | Считывает заданное свойство неизвестного значения данных в контейнере свойств.<br/>                                                |
| [**Пспропертибаг \_ вритебул**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebool)               | Задает значение **логического** типа данных свойства в контейнере свойств.<br/>                                                     |
| [**Пспропертибаг \_ вритебстр**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebstr)               | Задает значение данных **BSTR** из свойства в контейнере свойств.<br/>                                                     |
| [**Пспропертибаг \_ вритедворд**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writedword)             | Устанавливает значение **DWORD** данных из свойства в контейнере свойств.<br/>                                                      |
| [**Пспропертибаг \_ вритегуид**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeguid)               | Задает значение данных GUID из свойства в контейнере свойств.<br/>                                                       |
| [**Пспропертибаг \_ вритеинт**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeint)                 | Задает значение данных **типа int** из свойства в контейнере свойств.<br/>                                                     |
| [**Пспропертибаг \_ врителонг**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writelong)               | Задает значение **типа Long** для данных из свойства в контейнере свойств.<br/>                                                     |
| [**Пспропертибаг \_ вритепоинтл**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepointl)           | Хранит координаты свойств, хранящиеся в [**точечной**](/previous-versions//dd162807(v=vs.85)) структуре указанного контейнера свойств.<br/>       |
| [**Пспропертибаг \_ вритепоинтс**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepoints)           | Хранит координаты свойств, хранящиеся в структуре [**точек**](/previous-versions//dd162808(v=vs.85)) указанного контейнера свойств.<br/>       |
| [**Пспропертибаг \_ вритепропертикэй**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepropertykey) | Задает ключ свойства свойства в указанном контейнере свойств.<br/>                                                  |
| [**Пспропертибаг \_ вритеректл**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writerectl)             | Хранит координаты прямоугольника, хранящегося в свойстве, содержащемся в указанном контейнере свойств.<br/>                 |
| [**Пспропертибаг \_ вритешорт**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeshort)             | Задает **короткое** значение данных свойства в контейнере свойств.<br/>                                                    |
| [**Пспропертибаг \_ вритестр**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestr)                 | Задает **строковое** значение данных свойства в контейнере свойств.<br/>                                                   |
| [**Пспропертибаг \_ вритестреам**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestream)           | Задает поток данных, хранящийся в заданном свойстве, содержащемся в указанном контейнере свойств.<br/>                            |
| [**Пспропертибаг \_ вритеулонглонг**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeulonglong)     | Задает значение данных **улонглонг** из свойства в контейнере свойств.<br/>                                                |
| [**Пспропертибаг \_ вритеункновн**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeunknown)         | Задает заданное свойство неизвестного значения данных в контейнере свойств.<br/>                                                 |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Функции PROPVARIANT и VARIANT](./functions-propvarutil.md)
</dt> <dt>

[Функции](functions.md)
</dt> </dl>

 

 
