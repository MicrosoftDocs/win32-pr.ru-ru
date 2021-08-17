---
description: ICE55 проверяет, что все объекты Локкпермиссион существуют и имеют допустимые значения разрешений.
ms.assetid: e23e43ce-942f-4f6b-b5fd-cf366f7a7fe5
title: ICE55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044b9993c6c50dce32c04f98d8e000f0faae4280d244c4656d7b0cbed7b49749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635145"
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
| Файл1      | File  |        | guest |            |
| Файл3      | File  |        | guest | 1          |



 

[Таблица файлов](file-table.md) (частичная)



| File  | Версия | Язык |
|-------|---------|----------|
| Файл1 | Файл2   |          |
| Файл2 | 1.0.0.0 | 1033     |



 

Объект file1 имеет значение NULL в столбце разрешений. Каждая строка должна иметь значение в столбце permissions. Чтобы устранить эту ошибку, укажите числовое значение в этом столбце. Если для этого объекта привилегии не требуются, следует удалить строку.

Объект Файл3, описанный в таблице Локкпермиссионс, не перечислен в таблице File. Чтобы устранить эту ошибку, обратитесь к допустимому объекту.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



