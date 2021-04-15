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
# <a name="placeholder-files"></a><span data-ttu-id="b50a8-103">Файлы заполнителей</span><span class="sxs-lookup"><span data-stu-id="b50a8-103">Placeholder files</span></span>

## <a name="platform"></a><span data-ttu-id="b50a8-104">Платформа</span><span class="sxs-lookup"><span data-stu-id="b50a8-104">Platform</span></span>

<span data-ttu-id="b50a8-105">**Клиенты —** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b50a8-105">**Clients -** Windows 8.1</span></span>  
<span data-ttu-id="b50a8-106">**Серверы —** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b50a8-106">**Servers -** Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="b50a8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b50a8-107">Description</span></span>

<span data-ttu-id="b50a8-108">Файлы заполнителей позволяют пользователям просматривать файлы Microsoft OneDrive и управлять ими независимо от подключения.</span><span class="sxs-lookup"><span data-stu-id="b50a8-108">Placeholder files enable users to view and manage Microsoft OneDrive files regardless of connectivity.</span></span> <span data-ttu-id="b50a8-109">Файлы заполнителей представляют пространство имен OneDrive, даже если файлы не кэшируются локально.</span><span class="sxs-lookup"><span data-stu-id="b50a8-109">Placeholder files represent the OneDrive namespace, even when files are not cached locally.</span></span> <span data-ttu-id="b50a8-110">Они содержат метаданные файлов и миниатюрные изображения фотографий.</span><span class="sxs-lookup"><span data-stu-id="b50a8-110">They contain file metadata and thumbnail images of photos.</span></span>

## <a name="manifestation"></a><span data-ttu-id="b50a8-111">Проявление</span><span class="sxs-lookup"><span data-stu-id="b50a8-111">Manifestation</span></span>

<span data-ttu-id="b50a8-112">Для конечных пользователей и разработчиков файлы заполнителей выглядят и ведут себя почти так же, как локальные файлы.</span><span class="sxs-lookup"><span data-stu-id="b50a8-112">To end users and developers, placeholder files look and behave almost the same as the local files.</span></span>

<span data-ttu-id="b50a8-113">Если приложение использует общее диалоговое окно файла для перечисления файловой системы, ваше приложение не будет затронуты.</span><span class="sxs-lookup"><span data-stu-id="b50a8-113">If your app uses the Common File Dialog to enumerate the file system, your app will not be impacted.</span></span> <span data-ttu-id="b50a8-114">Когда пользователь пытается открыть файл из стандартного диалогового окна/File, содержимое файла будет скачано и будет передано в приложение.</span><span class="sxs-lookup"><span data-stu-id="b50a8-114">When the user tries to open the file from the common /file Dialog, the file content will be downloaded and will be passed to your app.</span></span>

<span data-ttu-id="b50a8-115">Если приложение напрямую обращается к файловой системе, приложение может воспользоваться преимуществами файлов заполнителей, следуя приведенным ниже рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="b50a8-115">If your app accesses the file system directly, then your app may take advantage of the placeholder files by using the guidelines below.</span></span>

## <a name="solution"></a><span data-ttu-id="b50a8-116">Решение</span><span class="sxs-lookup"><span data-stu-id="b50a8-116">Solution</span></span>

-   <span data-ttu-id="b50a8-117">Заполнители скрыты по соглашению на основе атрибутов</span><span class="sxs-lookup"><span data-stu-id="b50a8-117">Placeholders are hidden by convention based on attributes</span></span>
-   <span data-ttu-id="b50a8-118">Идентификация заполнителей с помощью кода тега повторного анализа идентификатор операции ввода-вывода \_ \_ \_ \_ заполнитель файла тега</span><span class="sxs-lookup"><span data-stu-id="b50a8-118">Identify placeholders using reparse tag ID IO\_REPARSE\_TAG\_FILE\_PLACEHOLDER</span></span>

<span data-ttu-id="b50a8-119">Используйте модель данных оболочки для беспрепятственного поведения:</span><span class="sxs-lookup"><span data-stu-id="b50a8-119">Use the shell data model for seamless behavior:</span></span>

-   <span data-ttu-id="b50a8-120">Использование Шкреатеитемфромпарсингнаме () для создания элемента оболочки</span><span class="sxs-lookup"><span data-stu-id="b50a8-120">Use SHCreateItemFromParsingName() to create a shell item</span></span>
-   <span data-ttu-id="b50a8-121">Привязка к потоку с помощью интерфейса IShellItem:: Биндтохандлер ( \_ поток бхид)</span><span class="sxs-lookup"><span data-stu-id="b50a8-121">Bind to the stream using IShellItem::BindToHandler(BHID\_Stream)</span></span>
-   <span data-ttu-id="b50a8-122">Обработчик свойств пользователя для доступа к свойству (IShellItem2:: Жетпропертихандлер)</span><span class="sxs-lookup"><span data-stu-id="b50a8-122">User property handler for property access (IShellItem2::GetPropertyHandler)</span></span>
-   <span data-ttu-id="b50a8-123">Пользовательская оболочка thumbnailhandler для получения эскизов изображений для заполнителей</span><span class="sxs-lookup"><span data-stu-id="b50a8-123">User shell thumbnailhandler to get thumbnail images for placeholders</span></span>
-   <span data-ttu-id="b50a8-124">Укажите Суппортедпротоколс = \* для реализации команды, если команда выполняет привязку к потоку через биндтохандлер</span><span class="sxs-lookup"><span data-stu-id="b50a8-124">Specify SupportedProtocols=\* on your verb implementation if the verb binds to the stream via BindToHandler</span></span>


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



 

 




