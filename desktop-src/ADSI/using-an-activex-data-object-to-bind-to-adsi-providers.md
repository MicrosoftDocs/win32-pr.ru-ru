---
title: Использование объекта данных ActiveX для привязки к поставщикам ADSI
description: Так как ADSI также является поставщиком OLE DB, для подключения к поставщикам ADSI можно использовать объект данных ActiveX (ADO).
ms.assetid: b42d804b-f1eb-4085-88aa-015a92309ee8
ms.tgt_platform: multiple
keywords:
- Интерфейс ADSI объектов данных ActiveX
- Интерфейс ADSI объектов данных ActiveX использование ADO для привязки к поставщикам ADSI
- поставщики услуг ADSI, использование объекта данных ActiveX для привязки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4efb64da28d5c4c2596fcf889e3b3db88b77205c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067307"
---
# <a name="using-an-activex-data-object-to-bind-to-adsi-providers"></a>Использование объекта данных ActiveX для привязки к поставщикам ADSI

Так как ADSI также является поставщиком OLE DB, для подключения к поставщикам ADSI можно использовать объект данных ActiveX (ADO). Как и в случае с другими поставщиками ADO, для подключения к поставщику OLE DB необходимо создать новый объект соединения и, при необходимости, указать учетные данные. Имя поставщика OLE DB ADSI — **адсдсубжект**.

Пример:


```VB
Dim con As New Connection 
'VBScript use: con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
con.Open "YourDescriptionHere"
```



В предыдущем примере вы подключены от имени текущего пользователя. Чтобы указать другие учетные данные, используйте свойства соединения:


```VB
con.Provider = "ADsDSOObject"
con.Properties("User ID") = "jeffsmith"
con.Properties("Password") = "guesswhat?"
con.Properties("Encrypt Password") = True
con.Open "YourDescriptionHere"
```



ADSI OLE DB определяет следующие свойства соединения.



| Свойство           | Тип данных   | Значение по умолчанию   |
|--------------------|-------------|-----------|
| "Идентификатор пользователя"          | **ОСВОБОЖДАЕМОЙ**    | **NULL**  |
| "Пароль".         | **ОСВОБОЖДАЕМОЙ**    | **NULL**  |
| "Зашифровать пароль" | **BOOLEAN** | **FALSE** |
| "Флаг ADSI"        | **Long**    | 0         |



 

С помощью OLE DB ADO невозможно выполнить привязку к определенному объекту. Однако можно запросить конкретный объект и возвратить результирующий набор. Только поставщики ADSI, которые поддерживают [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , имеют преимущества от использования ADO в качестве модели программирования.

Свойство флага ADSI используется для указания параметра проверки подлинности привязки. Это свойство может быть сочетанием флагов из перечисления [**объявлений \_ проверки \_ подлинности**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) .

 

 




