---
description: Демонстрирует написание обработчика, используемого для отображения предварительного просмотра файла в панели предварительного просмотра проводника Windows или других узлов обработчика просмотра.
title: 'Пример: обработчик просмотра рецепта'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2C926922-48C0-46f5-8928-67007C6FF957
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05208010c90c7185a777bb75f5de1e67bdb5bc14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985784"
---
# <a name="recipe-preview-handler-sample"></a>Пример: обработчик просмотра рецепта

Демонстрирует написание обработчика, используемого для отображения предварительного просмотра файла в панели предварительного просмотра проводника Windows или других узлов обработчика просмотра.

В этом разделе содержатся следующие подразделы.

-   [Требования](#requirements)
-   [Загрузка образца](#downloading-the-sample)
-   [Создание примера](#building-the-sample)
-   [Запуск примера](#running-the-sample)
-   [Отмена регистрации библиотеки DLL обработчика просмотра примера](#unregistering-the-sample-preview-handler-dll)
-   [См. также](#related-topics)

## <a name="requirements"></a>Требования



| Продукт                                | Минимальная версия продукта |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows SDK | 7.0                     |



 

## <a name="downloading-the-sample"></a>Загрузка образца

| Расположение      | URL-адрес пути                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Пример РеЦипепревиевхандлер](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/RecipePreviewHandler) |

## <a name="building-the-sample"></a>Построение образца

Чтобы построить образец из командной строки, выполните следующую команду:

1.  Откройте окно командной строки и перейдите в каталог проекта **реЦипепревиевхандлер** . Например, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler`.
2.  Введите `msbuild PreviewHandlerSDKSample.sln`.

Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):

1.  Откройте проводник Windows и перейдите в каталог проекта **реЦипепревиевхандлер** .
2.  Дважды щелкните значок файла Превиевхандлерсдксампле. sln, чтобы открыть проект в Visual Studio.
    > [!Note]  
    > Расширение имени файла. sln не отображается в разделе Параметры папки по умолчанию. В этом случае его можно определить по его уникальному значку или описанию типа "Microsoft Visual Studio решение".

     

3.  В меню **Сборка** выберите пункт **построить решение**.

> [!Note]  
> Если целевой системой является 64-разрядный (x64), этот пример обработчика просмотра должен быть построен как 64-разрядное приложение.

 

## <a name="running-the-sample"></a>Запуск примера

1.  Откройте окно командной строки и перейдите к созданному каталогу проекта **реЦипепревиевхандлер** . Например, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler`. Введите `regsvr32.exe PreviewHandlerSDKSample.dll` , чтобы зарегистрировать обработчик.
2.  Откройте проводник Windows и отобразите панель предварительного просмотра, если она еще не отображается.
    -   **Windows 7**. Нажмите кнопку панели предварительного просмотра.
    -   **Windows Vista**. Щелкните меню **Упорядочить** , перейдите в подменю **Макет** и выберите **область просмотра**.
3.  С помощью проводника Windows перейдите в каталог проекта **реЦипепревиевхандлер** .
4.  Выберите файл example. рецепт.

Чтобы оба 32-разрядных (x86) и 64-разрядных (x64) выходных данных работали в 64-разрядной версии Windows, установите значение **AppID** на суррогатный узел WOW64 `{534A1E02-D58F-44f0-B58B-36CBED287C7C}` , как показано в следующем коде.


```
{HKEY_CURRENT_USER,   
 L"Software\\Classes\\CLSID\\" SZ_CLSID_RecipePreviewHandler,
 L"AppID",
 L"{534A1E02-D58F-44f0-B58B-36CBED287C7C}"}
```



## <a name="unregistering-the-sample-preview-handler-dll"></a>Отмена регистрации библиотеки DLL обработчика просмотра примера

-   Откройте окно командной строки и введите, `regsvr32.exe /u PreviewHandlerSDKSample.dll` чтобы отменить регистрацию обработчика.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
</dt> <dt>

[**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe)
</dt> <dt>

[Идентификаторы модели пользователя приложения (Аппусермоделидс)](appids.md)
</dt> </dl>

 

 
