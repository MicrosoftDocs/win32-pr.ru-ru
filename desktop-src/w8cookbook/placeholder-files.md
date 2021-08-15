---
title: Файлы заполнителей
description: Файлы заполнителей
ms.assetid: E14655DA-CEA0-4106-B882-C9E9116FC234
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8891fef6c7fc54a66c093507b1831ab7cc6525ea96d685d06cf6fa8d9ded1e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452504"
---
# <a name="placeholder-files"></a>Файлы заполнителей

## <a name="platform"></a>Платформа

**клиенты —** Windows 8.1  
**серверы —** Windows Server 2012 R2  

## <a name="description"></a>Описание

файлы заполнителей позволяют пользователям просматривать Microsoft OneDrive файлы и управлять ими независимо от подключения. файлы заполнителей представляют пространство имен OneDrive, даже если файлы не кэшируются локально. Они содержат метаданные файлов и миниатюрные изображения фотографий.

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



 

 




