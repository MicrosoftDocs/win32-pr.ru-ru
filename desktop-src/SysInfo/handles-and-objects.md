---
description: Объект — это структура данных, представляющая системный ресурс, например файл, поток или графическое изображение.
ms.assetid: 26aaad09-c1e1-46e8-9cd3-7d795a10d900
title: Дескрипторы и объекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b5a35d55571a01f2f186f4e756401582474949f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912784"
---
# <a name="handles-and-objects"></a><span data-ttu-id="1758c-103">Дескрипторы и объекты</span><span class="sxs-lookup"><span data-stu-id="1758c-103">Handles and Objects</span></span>

<span data-ttu-id="1758c-104">*Объект* — это структура данных, представляющая системный ресурс, например файл, поток или графическое изображение.</span><span class="sxs-lookup"><span data-stu-id="1758c-104">An *object* is a data structure that represents a system resource, such as a file, thread, or graphic image.</span></span> <span data-ttu-id="1758c-105">Приложение не может напрямую обращаться к данным объекта или системному ресурсу, который представляет объект.</span><span class="sxs-lookup"><span data-stu-id="1758c-105">An application cannot directly access object data or the system resource that an object represents.</span></span> <span data-ttu-id="1758c-106">Вместо этого приложение должно получить *обработчик* объекта, который можно использовать для проверки или изменения системного ресурса.</span><span class="sxs-lookup"><span data-stu-id="1758c-106">Instead, an application must obtain an object *handle*, which it can use to examine or modify the system resource.</span></span> <span data-ttu-id="1758c-107">Каждый обработчик имеет запись в таблице внутреннего обслуживания.</span><span class="sxs-lookup"><span data-stu-id="1758c-107">Each handle has an entry in an internally maintained table.</span></span> <span data-ttu-id="1758c-108">Эти записи содержат адреса ресурсов и средства для обнаружения типа ресурса.</span><span class="sxs-lookup"><span data-stu-id="1758c-108">These entries contain the addresses of the resources and the means to identify the resource type.</span></span>

-   [<span data-ttu-id="1758c-109">Об дескрипторах и объектах</span><span class="sxs-lookup"><span data-stu-id="1758c-109">About Handles and Objects</span></span>](about-handles-and-objects.md)
-   [<span data-ttu-id="1758c-110">Категории объектов</span><span class="sxs-lookup"><span data-stu-id="1758c-110">Object Categories</span></span>](object-categories.md)
-   [<span data-ttu-id="1758c-111">Обработчик и ссылка на объект</span><span class="sxs-lookup"><span data-stu-id="1758c-111">Handle and Object Reference</span></span>](handle-and-object-reference.md)

 

 



