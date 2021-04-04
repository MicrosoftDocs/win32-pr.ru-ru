---
description: В примере кода Пропертедит показано, как преобразовать каноническое имя свойства в PROPERTYKEY, задать для хранилища свойств значение, равное значению элемента, и записать данные обратно в файловый поток.
ms.assetid: 5918b4f6-6b6f-4229-8f29-1c41f80b3b02
title: PropertyEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa248b9e86f8ab93cccba3d5d6b169d7e8699dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896934"
---
# <a name="propertyedit"></a>PropertyEdit

В примере кода Пропертедит показано, как преобразовать каноническое имя свойства в PROPERTYKEY, задать для хранилища свойств значение, равное значению элемента, и записать данные обратно в файловый поток.

В этом разделе содержатся следующие подразделы.

-   [Требования](#requirements)
-   [Загрузка образца](#downloading-the-sample)
-   [Создание примера](#building-the-sample)
-   [Запуск примера](#running-the-sample)
-   [См. также](#related-topics)

## <a name="requirements"></a>Требования



| Продукт     | Минимальная версия продукта |
|-------------|-------------------------|
| Windows     | Windows 7               |
| Пакет Windows SDK | 7.0                     |



 

## <a name="downloading-the-sample"></a>Загрузка образца

Этот образец доступен в следующих расположениях.



| Расположение      | URL-адрес пути                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub  | [Пример Пропертедит](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/PropertyEdit)    |



 

 

> [!Note]  
> Для всех версий Windows, включая Windows 7, рекомендуется загрузить примеры непосредственно из GitHub, чтобы получить самую последнюю версию.

 

## <a name="building-the-sample"></a>Построение образца

Чтобы построить образец из командной строки, выполните следующую команду:

1.  Откройте окно командной строки и перейдите в каталог проекта **пропертедит** . 
2.  Введите `msbuild PropertyEdit.sln`.

Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):

1.  Откройте проводник Windows и перейдите в каталог проекта **пропертедит** .
2.  Дважды щелкните значок файла Пропертедит. sln, чтобы открыть проект в Visual Studio.
    > [!Note]  
    > Расширение имени файла. sln не отображается в разделе Параметры папки по умолчанию. В этом случае его можно определить по его уникальному значку или описанию типа "Microsoft Visual Studio решение".

     

3.  В меню **Сборка** выберите пункт **построить решение**.

## <a name="running-the-sample"></a>Запуск примера

1.  Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.
2.  В командной строке введите `PropertyEdit.exe` или в проводнике Windows дважды щелкните значок PropertyEdit.exe.

## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Поиск примеров кода](-search-samples-ovw.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> <dt>

[Сведения о свойствах и обработчиках свойств](../properties/building-property-handlers-properties.md)
</dt> <dt>

[Схема описания свойства](/previous-versions//cc144127(v=vs.85))
</dt> </dl>

 

 
