---
description: ICE62 выполняет расширенные проверки в таблице Исолатедкомпонент для данных, которые могут привести к непредвиденному поведению.
ms.assetid: 649d3989-8121-4303-aa3e-63bc6649f445
title: ICE62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb5c2fd3f3305c791851fb3bd7480edc5e17f361c40719e8091930188dfa991c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528244"
---
# <a name="ice62"></a>ICE62

ICE62 выполняет расширенные проверки в [таблице исолатедкомпонент](isolatedcomponent-table.md) для данных, которые могут привести к непредвиденному поведению.

Сбой исправления ошибки, обнаруженной ICE62, может привести к сбою системы изолированных компонентов различными способами. Например, если бит Шареддллрефкаунт не задан для общего компонента, регистрация для компонента может быть удалена, когда другое приложение использует это значение ComponentId и удалено.

## <a name="result"></a>Результат

ICE62 отправляет предупреждение или ошибку при обнаружении в таблице Исолатедкомпонент данных, которые могут привести к непредвиденному поведению.

## <a name="example"></a>Пример

ICE62 сообщает о следующих ошибках и предупреждении для приведенных примеров.

``` syntax
The component 'Component2' is listed as an isolated application 
component in the IsolatedComponent table, but the key path is not a file.
```

Component2 указан в качестве компонента приложения для изоляции Component1. Однако Component2 имеет путь к разделу реестра и не предоставляет допустимый путь к исполняемому файлу, используемый для изоляции компонента.

Чтобы устранить эту ошибку, используйте другой компонент в качестве приложения для изолированного компонента Component1.

``` syntax
The component 'Component1' is listed as an isolated shared component in the 
IsolatedComponent table, but is not marked with the SharedDllRefCount component attribute.
```

Component1 указан как изолированный общий компонент, но не имеет установленного бита Шареддллрефкаунт. Это может привести к неправильному времени существования компонента. Если другое приложение использует этот компонент (изолированное или не установлено) и удаляется, регистрация для компонента будет удалена, но изолированная копия этого приложения останется. Это приводит к проблемам с восстановлением и удалением.

Чтобы устранить эту ошибку, установите бит Шареддллрефкаунт для компонента.

``` syntax
The isolated shared component 'Component1' is not installed by the same feature as 
(or a parent feature of) its isolated application component 'Component2' (which is installed by feature 'Feature2').
```

Component1 и Component2 устанавливаются различными компонентами. Component1 устанавливается с помощью Feature1, а Component2 устанавливается с помощью Feature2. Feature1 не является родителем Feature2, поэтому приложение может быть установлено, но не является изолированным компонентом, нарушая изоляцию.

Чтобы устранить эту ошибку, добавьте запись в таблицу Феатурекомпонентс, связывающую Component1 с той же функцией, что и (или родительская функция) функции, устанавливающей Component2.

``` syntax
WARNING: The isolated shared component 'Component1' (referenced in the IsolatedComponent table) 
is conditionalized. Isolated shared component conditions should never change from TRUE to FALSE after the first install of the product.
```

Component1 имеет условие в таблице Component. Если это условие когда-либо изменится со значения TRUE на FALSE в течение времени существования установки на компьютере, то изолированный компонент может быть потерян без сведений о регистрации.

Чтобы устранить это предупреждение, удалите условие или создайте условие, чтобы оно никогда не изменялось с TRUE на FALSE.

``` syntax
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component2') that are installed to the directory 'TARGETDIR'.
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component3') that are installed to the directory 'TARGETDIR'.
```

Component1 изолированы как для Component2, так и для Component3, а два компонента также устанавливаются в один и тот же каталог. Приложения совместно используют изолированный компонент, но если одно приложение удаляется, общий компонент удаляется, а другие приложения теряют изолированный компонент.

Чтобы устранить это предупреждение, установите приложения в разные каталоги или проверьте, действительно ли для некоторых приложений требуется изолированный компонент.

[Таблица Исолатедкомпонент](isolatedcomponent-table.md)



| \_Общий компонент | \_Приложение компонента |
|-------------------|------------------------|
| Component1        | Component2             |
| Component1        | Component3             |



 

[Таблица компонентов](component-table.md)



| Компонент  | ComponentId | Каталог\_ | Атрибуты | Условие   | Путь   |
|------------|-------------|-------------|------------|-------------|-----------|
| Component1 |             | Dir1        | 0          | микондитион | Файл1     |
| Component2 |             | TARGETDIR   | 4          |             | Registry2 |
| Component3 |             | TARGETDIR   | 0          |             | Файл3     |



 

[феатурекомпонентстабле](featurecomponents-table.md)



| Компонент\_ | Компонент\_ |
|-----------|-------------|
| Feature1  | Component1  |
| Feature2  | Component2  |
| Feature1  | Component3  |



 

[Таблица компонентов](feature-table.md) (частичная)



| Компонент  | \_Родительский компонент функции |
|----------|-----------------|
| Feature1 |                 |
| Feature2 |                 |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



