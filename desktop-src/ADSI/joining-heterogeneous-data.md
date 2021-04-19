---
title: Соединение разнородных данных
description: Типичные организации хранят данные в нескольких разнородных базах данных. Данные отдела кадров могут храниться в SQL Server, а данные управления учетной записью хранятся в каталоге. Другие данные могут храниться в собственных форматах.
ms.assetid: 45281b42-5cb2-42f9-9c7c-f3e3174b0f9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e1099028bc85dc6492eade0315b7308b4c6aaa9
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314617"
---
# <a name="joining-heterogeneous-data"></a>Соединение разнородных данных

Типичные организации хранят данные в нескольких разнородных базах данных. Данные отдела кадров могут храниться в SQL Server, а данные управления учетной записью хранятся в каталоге. Другие данные могут храниться в собственных форматах.

В SQL Server 7,0, ADSI и поставщике OLE DB можно объединить данные из Active Directory с данными в SQL Server и создать представление Объединенных данных.

**Соединение Active Directory данных с SQL Server данными**

1.  Запуск **анализатора запросов SQL** (запуск \| программ \| Microsoft SQL Server 7,0)
2.  Войдите на компьютер SQL Server.
3.  Выполните следующую строку (выделите ее и нажмите клавиши CTRL + E):

    ```sql
    EXEC sp_addlinkedserver 'ADSI', 'Active Directory Service Interfaces', 
    'ADSDSOObject', 'adsdatasource'
    GO
    ```

    

    В этой строке для системной хранимой процедуры [ \_ аддлинкедсервер](https://msdn.microsoft.com/library/Aa259589.aspx) используются следующие аргументы:

    -   «ADSI» — это аргумент **сервера** , который будет именем этого связанного сервера.
    -   "Active Directory Services" — это аргумент **срвпродукт** , который представляет собой имя источника данных OLE DB, добавляемого в качестве связанного сервера.
    -   "Адсдсубжект" — это **аргумент \_ имени поставщика** и указывает, что вы используете поставщик OLE DB.
    -   "адсдатасаурце" — это **\_ аргумент источника данных**, который представляет собой имя источника данных, интерпретируемое поставщиком OLE DB.

    Теперь можно использовать связанный сервер для доступа к Active Directory из SQL Server.

4.  В следующем примере выполняется запрос с помощью инструкции [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) . Эта инструкция имеет два аргумента: ADSI, то есть имя только что созданного связанного сервера и Инструкция запроса. Инструкция запроса содержит следующие элементы:

    -   Инструкция [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) содержит список данных, которые будут получены из службы каталогов. Для указания искомых данных необходимо использовать отображаемое имя LDAP.
    -   Инструкция [from](https://msdn.microsoft.com/library/Aa258869.aspx) содержит имя связанного сервера каталогов, из которого будут получены эти сведения.
    -   Оператор [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) предоставляет условия поиска. В этом примере выполняется поиск пользователей.

    Введите и выполните:

    ```sql
    SELECT * FROM OPENQUERY( ADSI, 
        'SELECT name, adsPath 
         FROM 'LDAP://DC=Fabrikam,DC=com' 
         WHERE objectCategory = 'Person' AND objectClass= 'user'')
    ```

    

    Также можно использовать [диалект LDAP](ldap-dialect.md)ADSI. Пример:

    ```sql
    SELECT * FROM OPENQUERY(ADSI,
        '<LDAP://DC=Fabrikam,DC=COM>;(&(objectCategory=Person)(objectClass=user));name, adspath;subtree')
    ```

    

    В предыдущем примере запрос LDAP состоит из четырех частей:

    -   " \<LDAP://DC=Fabrikam,DC=COM> " — это различающееся имя сервера каталогов для поиска.
    -   "(& (objectCategory = Person) (objectClass = пользователь))" является фильтром поиска LDAP (см. [синтаксис фильтра поиска](search-filter-syntax.md)).
    -   «Name, ADsPath» — это имена извлекаемых атрибутов (с использованием формата отображаемого имени LDAP).
    -   "поддерево" указывает [область](scope-of-query.md) поиска.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание и исполнение представления](creating-and-executing-a-view.md)
</dt> </dl>

 

 




