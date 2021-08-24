---
description: В примере кода Пропертедит показано, как преобразовать каноническое имя свойства в PROPERTYKEY, задать для хранилища свойств значение, равное значению элемента, и записать данные обратно в файловый поток.
ms.assetid: 5918b4f6-6b6f-4229-8f29-1c41f80b3b02
title: PropertyEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944419f990c8f1f8b52706dbab0b08102829e77a5bfa8a91c72a5bc16eddfa63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944673"
---
# <a name="propertyedit"></a>PropertyEdit

В примере кода Пропертедит показано, как преобразовать каноническое имя свойства в PROPERTYKEY, задать для хранилища свойств значение, равное значению элемента, и записать данные обратно в файловый поток.

В этом разделе содержатся следующие подразделы.

-   [Требования](#requirements)
-   [Загрузка образца](#downloading-the-sample)
-   [Создание примера](#building-the-sample)
-   [Запуск примера](#running-the-sample)
-   [Связанные темы](#related-topics)

## <a name="requirements"></a>Requirements (Требования)



| Продукт     | Минимальная версия продукта |
|-------------|-------------------------|
| Windows     | Windows 7               |
| Пакет Windows SDK | 7,0                     |



 

## <a name="downloading-the-sample"></a>Загрузка образца

Этот образец доступен в следующих расположениях.



| Расположение      | URL-адрес пути                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub  | [Пример Пропертедит](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/PropertyEdit)    |



 

 

> [!Note]  
> для всех версий Windows, включая Windows 7, рекомендуется загружать образцы непосредственно из GitHub для наиболее актуальной версии.

 

## <a name="building-the-sample"></a>Построение образца

Чтобы построить образец из командной строки, выполните следующую команду:

1.  Откройте окно командной строки и перейдите в каталог проекта **пропертедит** . 
2.  Введите `msbuild PropertyEdit.sln`.

чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):

1.  откройте обозреватель Windows и перейдите в каталог проекта **пропертедит** .
2.  Дважды щелкните значок файла Пропертедит. sln, чтобы открыть проект в Visual Studio.
    > [!Note]  
    > Расширение имени файла. sln не отображается в разделе Параметры папки по умолчанию. в этом случае его можно определить по его уникальному значку или описанию типа "Microsoft Visual Studio решение".

     

3.  В меню **Построение** выберите пункт **Построить решение**.

## <a name="running-the-sample"></a>Запуск примера

1.  перейдите в каталог, содержащий новый исполняемый файл, используя окно командной строки или проводник Windows.
2.  в командной строке введите `PropertyEdit.exe` или в Windows Explorer дважды щелкните значок PropertyEdit.exe.

## <a name="related-topics"></a>Связанные темы

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

 

 
