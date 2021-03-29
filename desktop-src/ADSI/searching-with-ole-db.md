---
title: Поиск с помощью OLE DB
description: Для клиентов автоматизации, использующих объекты данных ActiveX (ADO) и всех клиентов, не поддерживающих автоматизацию, ADSI предоставляет поставщик OLE DB, поддерживающий подмножество интерфейсов OLE DB запросов.
ms.assetid: f4e48b60-82dd-4c39-879b-0bc8f40747d2
ms.tgt_platform: multiple
keywords:
- Поиск с помощью OLE DB ADSI
- запросы к ADSI, поиск с помощью OLE DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b6b0c056a63174233271b9b059ebffa9d4d841
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793891"
---
# <a name="searching-with-ole-db"></a>Поиск с помощью OLE DB

Для клиентов автоматизации, использующих объекты данных ActiveX (ADO) и всех клиентов, не поддерживающих автоматизацию, ADSI предоставляет поставщик OLE DB, поддерживающий подмножество интерфейсов OLE DB запросов. Клиентский код, который уже использует интерфейсы OLE DB для запросов, может использовать одни и те же интерфейсы для запросов к службам каталогов.

В реализации OLE DB Служба каталогов предоставляется как объект источника данных. Объекты источника данных являются фабриками для объектов сеанса и поддерживают [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) для подключения к каталогу, [метода IDBCreateSession](/previous-versions/windows/desktop/ms724076(v=vs.85)) для создания объекта сеанса, [интерфейс IDBProperties](/previous-versions/windows/desktop/ms719607(v=vs.85)) для передачи данных проверки подлинности в базовое пространство имен и предоставления команды запроса и [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist) для сохранения данных, необходимых для создания объекта источника данных в базовой службе каталогов.

**Выполнение Active Directory запроса с помощью OLE DB**

1.  Получите интерфейс [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) от поставщика OLE DB. В случае Active Directory используйте идентификатор класса **CLSID \_ адсдсубжект**.
2.  Создайте массив [DBPROP](/previous-versions/windows/desktop/ms717970(v=vs.85)) данных подключения, указав имя пользователя и пароль.
3.  Запросите интерфейс [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) , полученный на шаге 1, для интерфейса [интерфейс IDBProperties](/previous-versions/windows/desktop/ms719607(v=vs.85)) .
4.  Вызовите метод [интерфейс IDBProperties:: SetProperties](/previous-versions/windows/desktop/ms723049(v=vs.85)) , передав массив [DBPROP](/previous-versions/windows/desktop/ms717970(v=vs.85)) , созданный на шаге 2.
5.  Вызовите метод [IDBInitialize:: Initialize](/previous-versions/windows/desktop/ms718026(v=vs.85)) , чтобы установить соединение с поставщиком OLE DB. Это поставщик Active Directory, в данном случае.
6.  Запросите интерфейс [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) для интерфейса [метода IDBCreateSession](/previous-versions/windows/desktop/ms724076(v=vs.85)) .
7.  Вызовите метод [метода IDBCreateSession:: CreateSession](/previous-versions/windows/desktop/ms714942(v=vs.85)) , запрашивающий новый интерфейс типа [IDBCreateCommand](/previous-versions/windows/desktop/ms711625(v=vs.85)).
8.  Вызовите метод [IDBCreateCommand:: CreateCommand](/previous-versions/windows/desktop/ms709772(v=vs.85)) , чтобы создать интерфейс [ICommandText](/previous-versions/windows/desktop/ms714914(v=vs.85)) .
9.  Вызовите метод [ICommandText:: SetCommandText](/previous-versions/windows/desktop/ms709757(v=vs.85)) . Передайте предпочтительный диалект и фактический текст команды запроса в этом диалекте. В качестве диалекта можно использовать либо **DBGUID \_ лдапдиалект** , либо **DBGUID \_ дбскл** .
10. Вызов [ICommand:: Execute](/previous-versions/windows/desktop/ms718095(v=vs.85)); возвращается интерфейс [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) , который является интерфейсом к результирующему набору.
11. Запросите интерфейс [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) для интерфейса [IColumnsInfo](/previous-versions/windows/desktop/ms725401(v=vs.85)) .
12. Вызовите метод [IColumnsInfo:: GetColumnInfo](/previous-versions/windows/desktop/ms722704(v=vs.85)) , чтобы получить данные столбца о результирующем наборе.
13. Заполните массив структур [DBBINDING](/previous-versions/windows/desktop/ms716845(v=vs.85)) , описывающих поставщик OLE DB, как предоставить типы данных для каждого столбца в коде приложения. Этот шаг позволяет указать, какой тип содержится в определенном столбце. Кроме того, смещение столбцов относительно возвращаемой строки задается здесь для каждого столбца.
14. Запросите интерфейс [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) для интерфейса [IAccessor](/previous-versions/windows/desktop/ms719672(v=vs.85)) .
15. Вызовите метод [IAccessor:: CreateAccessor](/previous-versions/windows/desktop/ms720969(v=vs.85)) , который возвращает массив дескрипторов доступа. Затем этот массив используется для доступа к строкам результирующего набора.
16. Вызовите метод [IRowset:: GetNextRows](/previous-versions/windows/desktop/ms709827(v=vs.85)) , передав дескрипторы строк и число получаемых строк.
17. Вызовите метод [IRowset:: GetData](/previous-versions/windows/desktop/ms716988(v=vs.85)) , передав маркер строки из набора, возвращенного на шаге 16. Возвращается необработанный указатель на строку.

Дополнительные сведения о синтаксисе фильтра поиска см. в разделе [синтаксис фильтра поиска](search-filter-syntax.md).

Чтобы считать возвращенные необработанные данные строки, используйте структуру [DBBINDING](/previous-versions/windows/desktop/ms716845(v=vs.85)) , созданную на шаге 13, вычисляя смещения столбцов в необработанном указателе данных, возвращенном на шаге 17. Считывает часть состояния столбца для получения результата для этого столбца.

Дополнительные сведения и пример кода, демонстрирующий Поиск Active Directory с помощью поставщика OLE DB ADSI, см. в разделе [пример кода для использования OLE DB для поиска Active Directory](example-code-for-using-ole-db-to-search-active-directory.md).

 

 