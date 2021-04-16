---
description: Пример кода OpenSearch демонстрирует создание федеративной службы поиска с помощью протокола OpenSearch и файла дескриптора OpenSearch (. OSDX-) (соединителя поиска).
ms.assetid: 792884e4-826b-4474-82e1-1680d4d8b602
title: OpenSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8656efec434744d14714529d1e7b0d01a5349ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423726"
---
# <a name="opensearch"></a>OpenSearch

Пример кода OpenSearch демонстрирует создание федеративной службы поиска с помощью протокола [OpenSearch](https://github.com/dewitt/opensearch) и файла дескриптора OpenSearch (. OSDX-) (соединителя поиска).

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
| GitHub  | [Пример OpenSearch](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/OpenSearch)      |



 

 

> [!Note]  
> Для всех версий Windows, включая Windows 7, рекомендуется загрузить примеры непосредственно из GitHub, чтобы получить самую последнюю версию.

 

## <a name="building-the-sample"></a>Построение образца

Чтобы построить образец из командной строки, выполните следующую команду:

1.  Откройте окно командной строки и перейдите в каталог проекта **адвентуресеарч** . 
2.  Введите `msbuild AdventureSearch.sln`.

Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):

1.  Откройте проводник Windows и перейдите в каталог проекта **адвентуресеарч** .
2.  Дважды щелкните значок файла Адвентуресеарч. sln, чтобы открыть проект в Visual Studio.
    > [!Note]  
    > Расширение имени файла. sln не отображается в разделе Параметры папки по умолчанию. В этом случае его можно определить по его уникальному значку или описанию типа "Microsoft Visual Studio решение".

     

3.  В меню **Сборка** выберите пункт **построить решение**.

## <a name="running-the-sample"></a>Запуск примера

1.  Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.
2.  В командной строке введите `AdventureSearch.exe` или в проводнике Windows дважды щелкните значок AdventureSearch.exe.
3.  В командной строке введите `GetOSDX.exe` или в проводнике Windows дважды щелкните значок GetOSDX.exe.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[Обзор схемы описания соединителя поиска](search-sconn-desc-schema-entry.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Федеративный поиск в Windows](-search-federated-search-overview.md)
</dt> <dt>

[Поиск примеров кода](-search-samples-ovw.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[Схема описания библиотеки](../shell/library-schema-entry.md)
</dt> </dl>

 

 
