---
description: ICE55 проверяет, что все объекты Локкпермиссион существуют и имеют допустимые значения разрешений.
ms.assetid: e23e43ce-942f-4f6b-b5fd-cf366f7a7fe5
title: ICE55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239093e3502a1731c3248918750c18aa1b3e1f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265831"
---
# <a name="ice55"></a>ICE55

ICE55 проверяет, что все объекты Локкпермиссион существуют и имеют допустимые значения разрешений.

## <a name="result"></a>Результат

ICE55 сообщение об ошибке, если LockObject, указанный в [таблице локкпермиссионс](lockpermissions-table.md) , не существует или если в столбце разрешений не указан уровень привилегий.

## <a name="example"></a>Пример

ICE55 сообщит о следующих ошибках в примере.

``` syntax
LockObject 'File1'.'File'.''.'guest' in the LockPermissions table 
    has a null Permission value. 
Could not find item 'File3' in table 'File' which is referenced 
    in the LockPermissions table.
```

[Таблица локкпермиссионс](lockpermissions-table.md) (частичная)



| LockObject | Таблица | Домен | Пользователь  | Разрешение |
|------------|-------|--------|-------|------------|
| Файл1      | Файл  |        | guest |            |
| Файл3      | Файл  |        | guest | 1          |



 

[Таблица файлов](file-table.md) (частичная)



| Файл  | Версия | Язык |
|-------|---------|----------|
| Файл1 | Файл2   |          |
| Файл2 | 1.0.0.0 | 1033     |



 

Объект file1 имеет значение NULL в столбце разрешений. Каждая строка должна иметь значение в столбце permissions. Чтобы устранить эту ошибку, укажите числовое значение в этом столбце. Если для этого объекта привилегии не требуются, следует удалить строку.

Объект Файл3, описанный в таблице Локкпермиссионс, не перечислен в таблице File. Чтобы устранить эту ошибку, обратитесь к допустимому объекту.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



