---
description: ICE69 проверяет, что все подстроки формы \[ $componentkey \] в отформатированной строке не имеют перекрестных ссылок на компоненты.
ms.assetid: 6ab8f3b7-19e9-46f3-b09e-36bdb43d6f55
title: ICE69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bd00efc6b141bfa872470adcc9e88a63a2c52d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266133"
---
# <a name="ice69"></a>ICE69

ICE69 проверяет, что все подстроки формы \[ $componentkey \] в [отформатированной](formatted.md) строке не имеют перекрестных ссылок на компоненты. Ссылка на кросс-компоненты возникает, когда \[ \] свойство $componentkey форматированной строки ссылается на компонент, отличный от компонента, хранящегося в столбце Component \_ таблиц.

Проблемы с ссылками между компонентами возникают из-за того, как [отформатированные](formatted.md) строки вычисляются. Если компонент, на который ссылается \[ свойство $componentkey, \] уже установлен и не изменяется во время текущей установки (например, переустановка, перемещение в источник и т. д.), выражение \[ $componentkey \] вычисляется как null, так как состояние действия компонента в \[ $componentkey \] равно null. Аналогичные проблемы могут возникнуть во время операций обновления и восстановления.

## <a name="result"></a>Результат

ICE69 возвращает ошибку, если \[ $componentkey \] подстрока в [отформатированной](formatted.md) строке перекрестно ссылается на компонент в другой функции. ICE69 возвращает предупреждение, $componentkey если \[ \] подстрока в отформатированной строке перекрестно ссылается на компонент в той же функции. (Для определения этого сопоставления используется таблица [феатурекомпонентс](featurecomponents-table.md) . Он должен соответствовать той же функции для предупреждения. Создание ссылок на компоненты в родительских компонентах или на ссылки на компоненты в дочерних функциях считается ошибкой.)

ICE69 сообщает об ошибке, если \[ \# \] подстрока филекэй в [форматированной](formatted.md) строке ссылается на файл, который не указан в таблице [File](file-table.md) как принадлежащий тому же компоненту.

## <a name="example"></a>Пример

ICE69 сообщает о следующих примерах.

``` syntax
WARNING: "Mismatched component reference. Entry 'Test' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test'. Components are in the same feature."
ERROR: "Mismatched component reference. Entry 'Shortcut2' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test2'. Components are not in the same feature."
```

Чтобы устранить эту ошибку, не следует выполнять перекрестные ссылки на компоненты. Измените \[ $componentkey \] в соответствии с компонентом ярлыка.

[Таблица ярлыков](shortcut-table.md) (частичная)



| Сочетание клавиш  | Компонент\_ | Аргумент     |
|-----------|-------------|--------------|
| Тест      | QuickTest   | -v \[ $Test\] |
| Shortcut2 | QuickTest   | \[$Test 2\]   |



 

Таблицы [команд](verb-table.md) и [расширений](extension-table.md) — это особые случаи, в которых таблица команд ссылается на расширение, которое принадлежит компоненту. Однако расширение может принадлежать нескольким компонентам, так как первичный ключ для таблицы расширений состоит из столбцов расширения и компонента \_ . Вы можете логически использовать следующую ситуацию.

[Таблица команд](verb-table.md) (частичная)



| Расширение | Команда\_ | Аргумент                |
|-----------|--------|-------------------------|
| TST       | open   | -v \[ $comp 1 \] \[ $comp 2\] |



 

[Таблица расширения](extension-table.md) (частичная)



| Расширение | Компонент\_ |
|-----------|-------------|
| TST       | comp1       |
| TST       | Comp2       |



 

[Таблица Феатурекомпонентс](featurecomponents-table.md)



| Функция\_ | Компонент\_ |
|-----------|-------------|
| Feature1  | QuickTest   |
| Feature1  | Тест        |
| Feature2  | Test2       |



 

В этом случае необходимо убедиться, что по крайней мере одно из \[ \] свойств $componentkey имеет значение, отличное от NULL. Однако каждое \[ свойство $componentkey \] в столбце Argument таблицы Verb ( \[ $comp 1 \] и \[ $comp 2 \] в приведенном выше примере) должно ссылаться на возможный компонент, входящий в состав расширения, связанного с командой. Ссылка, например \[ $comp 3, приведет \] к появлению предупреждения от ICE69.

[Таблица AppID](appid-table.md) имеет схожую ситуацию с таблицей команд. Он использует [таблицу классов](class-table.md) для ссылки на ее компонент. В этом случае таблица AppId проверяется так же, как проверка Verb-Extension (теперь AppId-Class).

Столбец Argument таблицы класса проверяется как [ярлык](shortcut-table.md), [Реестр](registry-table.md)и аналогичные таблицы.

## <a name="table-used-during-execution-only-if-found"></a>Таблица, используемая во время выполнения (только если она найдена)

[инифиле](inifile-table.md)

[ремовеинифиле](removeinifile-table.md)

[Реестр](registry-table.md)

[ремоверегистри](removeregistry-table.md)

[ServiceControl](servicecontrol-table.md)

[сервицеинсталл](serviceinstall-table.md)

[Клавиша](shortcut-table.md)

[Команда](verb-table.md)

[Расширение](extension-table.md)

[Класс](class-table.md)

[AppId](appid-table.md)

[Среда](environment-table.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



