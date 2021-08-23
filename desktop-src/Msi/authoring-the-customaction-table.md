---
description: Введите записи для пяти примеров пользовательских действий, созданных в предыдущем разделе, в таблицу CustomAction. Дополнительные сведения о заполнении таблицы CustomAction для этого типа настраиваемого действия см. в разделе Тип настраиваемого действия 1.
ms.assetid: 56828105-bd72-426d-833f-f756c577c77f
title: Создание таблицы CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b618da6e88718aa59483b3b25c007ff0b41eb89f6e1dc18a7eb31563632dc54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066084"
---
# <a name="authoring-the-customaction-table"></a>Создание таблицы CustomAction

Введите записи для пяти примеров пользовательских действий, созданных в предыдущем разделе, в [таблицу CustomAction](customaction-table.md). Дополнительные сведения о заполнении таблицы CustomAction для этого типа настраиваемого действия см. в разделе [тип настраиваемого действия 1](custom-action-type-1.md).

[Таблица CustomAction](customaction-table.md)



| Действие            | Тип  | Источник      | Назначение                |
|-------------------|-------|-------------|-----------------------|
| процессаккаунтс   | 1     | Process.dll | процессусераккаунтс   |
| унинсталлаккаунтс | 1     | Process.dll | унинсталлусераккаунтс |
| CreateAccount     | 11265 | Create.dll  | креатеусераккаунт     |
| RemoveAccount     | 11265 | Remove.dll  | ремовеусераккаунт     |
| роллбаккаккаунт   | 9473  | Remove.dll  | ремовеусераккаунт     |



 

исходный код C++ для библиотек динамической компоновки предоставляется в пакете SDK для установщик Windows. Чтобы создать файл Process.dll, используйте Process. cpp. Создайте файл Create.dll с помощью CREATE. cpp. Используйте Remove. cpp для создания Remove.dll. Добавьте эти файлы библиотеки динамической компоновки в двоичную таблицу.

[Двоичная таблица](binary-table.md)



| Имя        | Данные            |
|-------------|-----------------|
| Process.dll | {*двоичные данные*} |
| Create.dll  | {*двоичные данные*} |
| Remove.dll  | {*двоичные данные*} |



 

Продолжайте [добавлять пользовательскую таблицу кустомусераккаунтс](adding-a-custom-customuseraccounts-table.md).

 

 



