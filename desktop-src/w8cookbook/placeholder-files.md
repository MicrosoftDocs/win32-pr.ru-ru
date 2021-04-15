---
title: Файлы заполнителей
description: Файлы заполнителей
ms.assetid: E14655DA-CEA0-4106-B882-C9E9116FC234
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c15037b0daec7a6521a299b6c4587c956e0be3
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "105661789"
---
# <a name="placeholder-files"></a>Файлы заполнителей

## <a name="platform"></a>Платформа

**Клиенты —** Windows 8.1  
**Серверы —** Windows Server 2012 R2  

## <a name="description"></a>Описание

Файлы заполнителей позволяют пользователям просматривать файлы Microsoft OneDrive и управлять ими независимо от подключения. Файлы заполнителей представляют пространство имен OneDrive, даже если файлы не кэшируются локально. Они содержат метаданные файлов и миниатюрные изображения фотографий.

## <a name="manifestation"></a>Проявление

Для конечных пользователей и разработчиков файлы заполнителей выглядят и ведут себя почти так же, как локальные файлы.

Если приложение использует общее диалоговое окно файла для перечисления файловой системы, ваше приложение не будет затронуты. Когда пользователь пытается открыть файл из стандартного диалогового окна/File, содержимое файла будет скачано и будет передано в приложение.

Если приложение напрямую обращается к файловой системе, приложение может воспользоваться преимуществами файлов заполнителей, следуя приведенным ниже рекомендациям.

## <a name="solution"></a>Решение

-   Заполнители скрыты по соглашению на основе атрибутов
-   Идентификация заполнителей с помощью кода тега повторного анализа идентификатор операции ввода-вывода \_ \_ \_ \_ заполнитель файла тега

Используйте модель данных оболочки для беспрепятственного поведения:

-   Использование Шкреатеитемфромпарсингнаме () для создания элемента оболочки
-   Привязка к потоку с помощью интерфейса IShellItem:: Биндтохандлер ( \_ поток бхид)
-   Обработчик свойств пользователя для доступа к свойству (IShellItem2:: Жетпропертихандлер)
-   Пользовательская оболочка thumbnailhandler для получения эскизов изображений для заполнителей
-   Укажите Суппортедпротоколс = \* для реализации команды, если команда выполняет привязку к потоку через биндтохандлер


```
#include <winnth> //for IO_REPARSE_TAG_FILE_PLACEHOLDER
//  Helper that indicates this is a 
bool IsFilePlaceholder(WIN32_FIND_DATA const &findData)
{
  return (findData.dwFileAttributes & FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
}
bool IsFilePlaceholder(_In_PCWSTR filePath)
{
  bool isPlaceholder = false;
  WIN32_FIND_DATA findData;
  HANDLE hFind = FindFirstFile(filePath, &findData);
  if (hFind ! = INVALID_HANDLE_VALUE)
  {
    isPlaceholder = (findData.dwFileAttributes &    FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
    FindClose(hFind);
  }
  Return isPlaceholder;
}
```



 

 




