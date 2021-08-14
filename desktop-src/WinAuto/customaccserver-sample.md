---
title: Пример Кустомакксервер
description: Пример Кустомакксервер
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ebf1ecde2821208d788b20b5cb0fc1a00403c1607fb4604eb92845daf49d41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325993"
---
# <a name="customaccserver-sample"></a>Пример Кустомакксервер

В этом разделе содержатся следующие подразделы.

-   [Описание](#description)
-   [Сведения о загрузке](#download-information)
-   [Минимальные требования](#minimum-requirements)
-   [Создание примера](#building-the-sample)
-   [Запуск примера](#running-the-sample)
-   [Связанные темы](#related-topics)

## <a name="description"></a>Описание

В этом примере показано, как реализовать сервер Microsoft Active Accessibility для простого пользовательского элемента управления. Доступный объект для элемента управления состоит из корневого элемента (списка) и его потомков (элементов списка).

## <a name="download-information"></a>Сведения о загрузке

пример кустомакксервер устанавливается в составе [пакета средств разработки Microsoft Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) и доступен в следующем расположении.



| Расположение    | Путь или URL-адрес                                                                           |
|-------------|------------------------------------------------------------------------------------|
| Пакет Windows SDK | % Program files% \\ Microsoft sdk \\ Windows \\ \[ номер версии \] \\ примеры \\ винуи \\ msaa |



 

## <a name="minimum-requirements"></a>Минимальные требования



| Продукт          | Версия                         |
|------------------|---------------------------------|
| Операционная система | Windows XP, Windows Server 2003 |
| Пакет Windows SDK      | 7.0                             |
| Visual Studio    | 2008                            |



 

## <a name="building-the-sample"></a>Построение образца

чтобы построить пример с помощью Visual Studio 2008:

1.  запустите средство настройки пакета Microsoft Windows Software Development Kit (sdk), поставляемое вместе с пакетом sdk, чтобы добавить каталоги включения пакета sdk в Visual Studio.
2.  откройте обозреватель Windows и перейдите в каталог проекта.
3.  Дважды щелкните значок файла. sln (решение), чтобы открыть проект в Visual Studio.
4.  В меню **Сборка** выберите пункт **построить решение** , чтобы выполнить сборку решения. Приложение будет построено в \\ каталоге отладки или выпуска по умолчанию \\ .

чтобы построить пример из командной строки, см. раздел создание образцов в заметках о выпуске Windows SDK в следующем расположении:% Program files% \\ Microsoft sdk \\ Windows \\ v 7.0 \\ReleaseNotes.htm

## <a name="running-the-sample"></a>Запуск примера

Для выполнения образца:

1.  перейдите в каталог, содержащий новый исполняемый файл, используя командную строку или обозреватель Windows.
2.  введите AccServer.exe в командной строке или дважды щелкните значок AccServer.exe, чтобы запустить его из проводника Windows.

чтобы запустить из Visual Studio, нажмите клавишу F5 или выберите команду **начать отладку** в меню **отладка** .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Примеры](samples.md)
</dt> </dl>

 

 




