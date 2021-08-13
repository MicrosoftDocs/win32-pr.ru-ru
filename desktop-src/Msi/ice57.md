---
description: ICE57 проверяет, что отдельные компоненты не сочетают данные для каждого компьютера и пользователя. Это настраиваемое действие ICE проверяет записи реестра, файлы, пути к ключам каталогов и необъявленные ярлыки.
ms.assetid: 3c82efa7-9cf3-4bcd-8ec4-b81d1d7aa0a6
title: ICE57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d875264ed1fbc0f7dedac863c21801e5180ae879c9c255af7cf4b36e5d402970
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635165"
---
# <a name="ice57"></a>ICE57

ICE57 проверяет, что отдельные компоненты не сочетают данные для каждого компьютера и пользователя. Это настраиваемое действие ICE проверяет записи реестра, файлы, пути к ключам каталогов и необъявленные ярлыки.

Смешивание данных на уровне пользователя и на компьютере в одном компоненте может привести к частичной установке компонента только для некоторых пользователей в многопользовательской среде.

См. свойство [**ALLUSERS**](allusers.md) .

## <a name="result"></a>Результат

ICE57 отправляет сообщение об ошибке, если обнаруживает любой компонент, содержащий записи реестра для компьютера и пользователя, файлы, пути к ключам каталогов или необъявленные ярлыки.

## <a name="example"></a>Пример

ICE57reports следующие ошибки для показанного примера.

``` syntax
Component 'Component1' has both per-user and per-machine 
    data with a per-machine KeyPath. 
 
WARNING: Component 'Component2' has both per-user and 
    per-machine data with an HKCU Registry KeyPath. 
 
Component 'Component3' has a registry entry that 
    can be either per-user or per-machine and a per-machine KeyPath. 
 
Component 'Component4' has both per-user data and 
    a keypath that can be either per-user or per-machine.
```

[Таблица Component](component-table.md) (частичная)



| Компонент  | Каталог  | Атрибуты | Путь |
|------------|------------|------------|---------|
| Component1 | Каталог а | 0          | Файл а   |
| Component2 | Каталог а | 4          | регкэйб |
| Component3 | Каталог а | 0          | филек   |
| Component4 | Каталог а | 4          | регкэйд |



 

[Таблица реестра](registry-table.md) (частичная)



| Реестр | Root | Компонент\_ |
|----------|------|-------------|
| регкэйа  | 1    | Component1  |
| регкэйб  | 1    | Component2  |
| регкэйк  | –1   | Component3  |
| регкэйд  | –1   | Component4  |



 

[Таблица файлов](file-table.md) (частичная)



| Файл  | Компонент\_ |
|-------|-------------|
| Файл а | Component1  |
| филеб | Component2  |
| филек | Component3  |
| Подан | Component4  |



 

[Таблица каталога](directory-table.md)



| Каталог  | \_Родительский каталог | дефаултдир |
|------------|-------------------|------------|
| TARGETDIR  |                   | SourceDir  |
| Каталог а | TARGETDIR         | Каталог а |



 

Чтобы устранить ошибки, реорганизуйте приложение таким способом, чтобы каждый компонент содержал только ресурсы для отдельных пользователей или компьютеров, а не оба.

Первое сообщение об ошибке публикуется, так как Component1 содержит файл a (для компьютера) и раздел реестра HKCU Регкэйа (для каждого пользователя).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



