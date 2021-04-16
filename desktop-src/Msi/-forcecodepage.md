---
description: '\_Таблица форцекодепаже — это специальная таблица, используемая для изменения кодовой страницы пакета установки. Вы можете определить или задать кодовую страницу, экспортировав или импортировав текстовый файл архива с именем \_ форцекодепаже. IDT.'
ms.assetid: d95c205f-a800-4a63-a712-6f06675e4a8a
title: _ForceCodepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132843fa092409b26811afd6a4c1f3e7cf0544f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662988"
---
# <a name="_forcecodepage"></a><span data-ttu-id="411ef-104">\_форцекодепаже</span><span class="sxs-lookup"><span data-stu-id="411ef-104">\_ForceCodepage</span></span>

<span data-ttu-id="411ef-105">\_Таблица форцекодепаже — это специальная таблица, используемая для изменения кодовой страницы пакета установки.</span><span class="sxs-lookup"><span data-stu-id="411ef-105">The \_ForceCodepage table is a special table used for changing the code page of an installation package.</span></span> <span data-ttu-id="411ef-106">Вы можете определить или задать кодовую страницу, экспортировав или импортировав [текстовый файл архива](text-archive-files.md) с именем \_ форцекодепаже. IDT.</span><span class="sxs-lookup"><span data-stu-id="411ef-106">You can determine or set the code page by exporting or importing a [text archive file](text-archive-files.md) named \_ForceCodepage.idt.</span></span>

<span data-ttu-id="411ef-107">Формат \_ таблицы форцекодепаже состоит из двух пустых строк, за которыми следует третья строка, указывающая на числовую кодовую страницу.</span><span class="sxs-lookup"><span data-stu-id="411ef-107">The format of the \_ForceCodepage table is 2 blank lines followed by a third line that indicates the numeric code page.</span></span> <span data-ttu-id="411ef-108">Например, \_ файл форцекодепаже Table. IDT для базы данных японской версии будет выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="411ef-108">For example, a \_ForceCodepage table .idt file for a Japanese database would look as follows.</span></span> <span data-ttu-id="411ef-109">Числовая кодовая страница в данном случае — 932.</span><span class="sxs-lookup"><span data-stu-id="411ef-109">The numeric code page in this case is 932.</span></span>

``` syntax
<- this line blank
<- this line blank
932 _ForceCodepage
```

<span data-ttu-id="411ef-110">Дополнительные сведения об использовании \_ форцекодепаже для получения или задания кодовой страницы базы данных см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="411ef-110">For more information on how to use \_ForceCodepage to get or set the code page of a database see the following topics.</span></span>

-   [<span data-ttu-id="411ef-111">Обработка кодовой страницы (установщик Windows)</span><span class="sxs-lookup"><span data-stu-id="411ef-111">Code Page Handling (Windows Installer)</span></span>](code-page-handling-windows-installer-.md)
-   [<span data-ttu-id="411ef-112">Определение кодовой страницы базы данных установки</span><span class="sxs-lookup"><span data-stu-id="411ef-112">Determining an Installation Database's Code Page</span></span>](determining-an-installation-database-s-code-page.md)
-   [<span data-ttu-id="411ef-113">Настройка кодовой страницы базы данных</span><span class="sxs-lookup"><span data-stu-id="411ef-113">Setting the Code Page of a Database</span></span>](setting-the-code-page-of-a-database.md)

<span data-ttu-id="411ef-114">\_Таблица форцекодепаже представляет собой специальную таблицу псевдо, используемую для изменения кодовой страницы пакета установки.</span><span class="sxs-lookup"><span data-stu-id="411ef-114">The \_ForceCodepage table is a special pseudo table used for changing the code page of an installation package.</span></span> <span data-ttu-id="411ef-115">\_При неусловном использовании таблицы форцекодепаже база данных устанавливается в кодовую страницу без выполнения какой-либо проверки того, можно ли перевести данные, находящиеся в базе данных, в новую кодовую страницу.</span><span class="sxs-lookup"><span data-stu-id="411ef-115">Using the \_ForceCodepage table unconditionally sets the database to the code page without performing any validation as to whether the data currently in the database can be translated to the new code page.</span></span> <span data-ttu-id="411ef-116">Всегда рекомендуется, чтобы изменение кодовой страницы базы данных начинались с базы данных, не зависящей от языка.</span><span class="sxs-lookup"><span data-stu-id="411ef-116">It is always recommended that changing the code page of a database start with a language neutral database.</span></span>

 

 



