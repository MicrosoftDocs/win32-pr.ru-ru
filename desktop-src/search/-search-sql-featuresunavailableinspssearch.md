---
description: Язык запросов Microsoft Windows Search основан на язык SQL (SQL); Однако он не выполняет поиск в реляционной базе данных с пользовательскими таблицами или индексами.
ms.assetid: e81c436e-3a33-4b00-9860-9a54bc0eebbf
title: Функции SQL, недоступные в Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cf0e082a10a7775ca2d880be6153b7d99b6bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710909"
---
# <a name="sql-features-unavailable-in-microsoft-windows-search"></a><span data-ttu-id="c964d-103">Функции SQL, недоступные в Microsoft Windows Search</span><span class="sxs-lookup"><span data-stu-id="c964d-103">SQL Features Unavailable in Microsoft Windows Search</span></span>

<span data-ttu-id="c964d-104">Язык запросов Microsoft Windows Search основан на язык SQL (SQL); Однако он не выполняет поиск в реляционной базе данных с пользовательскими таблицами или индексами.</span><span class="sxs-lookup"><span data-stu-id="c964d-104">Microsoft Windows Search query language is based on Structured Query Language (SQL); however, it does not search in a relational database with user-defined tables or indexes.</span></span> <span data-ttu-id="c964d-105">По этой причине многие стандартные инструкции SQL и функции синтаксиса не применяются.</span><span class="sxs-lookup"><span data-stu-id="c964d-105">Because of this, many standard SQL statements and syntax features do not apply.</span></span> <span data-ttu-id="c964d-106">Ниже приведен список более значимых функций SQL, которые не поддерживаются в Windows Search.</span><span class="sxs-lookup"><span data-stu-id="c964d-106">The following is a list of the more significant SQL features that are not supported in Windows Search.</span></span>


-   <span data-ttu-id="c964d-107">ПАКЕТные инструкции</span><span class="sxs-lookup"><span data-stu-id="c964d-107">BATCH statements</span></span>
-   <span data-ttu-id="c964d-108">\_Функция объединения таблиц</span><span class="sxs-lookup"><span data-stu-id="c964d-108">COALESCE\_TABLE function</span></span>
-   <span data-ttu-id="c964d-109">Функция CONVERT (вместо этого используйте функции CAST)</span><span class="sxs-lookup"><span data-stu-id="c964d-109">CONVERT function (use the CAST functions instead)</span></span>
-   <span data-ttu-id="c964d-110">CREATE VIEW, инструкция</span><span class="sxs-lookup"><span data-stu-id="c964d-110">CREATE VIEW statement</span></span>
-   <span data-ttu-id="c964d-111">Язык описания данных</span><span class="sxs-lookup"><span data-stu-id="c964d-111">Data definition language</span></span>
-   <span data-ttu-id="c964d-112">DATASOURCE, инструкция</span><span class="sxs-lookup"><span data-stu-id="c964d-112">DATASOURCE statement</span></span>
-   <span data-ttu-id="c964d-113">Форматы даты и времени, отличные от метки даты и времени ISO</span><span class="sxs-lookup"><span data-stu-id="c964d-113">Date and Time formats other than ISO date and time stamp</span></span>
-   <span data-ttu-id="c964d-114">Инструкция DELETE</span><span class="sxs-lookup"><span data-stu-id="c964d-114">DELETE statement</span></span>
-   <span data-ttu-id="c964d-115">GRANT, инструкция</span><span class="sxs-lookup"><span data-stu-id="c964d-115">GRANT statement</span></span>
-   <span data-ttu-id="c964d-116">Схема информации</span><span class="sxs-lookup"><span data-stu-id="c964d-116">Information schema</span></span>
-   <span data-ttu-id="c964d-117">Инструкция INSERT</span><span class="sxs-lookup"><span data-stu-id="c964d-117">INSERT statement</span></span>
-   <span data-ttu-id="c964d-118">Типы данных OLE DB</span><span class="sxs-lookup"><span data-stu-id="c964d-118">OLE DB data types</span></span>
-   <span data-ttu-id="c964d-119">SQL-стандартные регулярные выражения (используйте CONTAINS или LIKE)</span><span class="sxs-lookup"><span data-stu-id="c964d-119">SQL-standard regular expressions (use CONTAINS or LIKE instead)</span></span>
-   <span data-ttu-id="c964d-120">Параметры для запросов SQL</span><span class="sxs-lookup"><span data-stu-id="c964d-120">Parameters to SQL queries</span></span>
-   <span data-ttu-id="c964d-121">Сравнение реляционных столбцов</span><span class="sxs-lookup"><span data-stu-id="c964d-121">Relational column comparison</span></span>
-   <span data-ttu-id="c964d-122">Заголовок идентификатора редакции</span><span class="sxs-lookup"><span data-stu-id="c964d-122">Revision ID header</span></span>
-   <span data-ttu-id="c964d-123">REVOKE, инструкция</span><span class="sxs-lookup"><span data-stu-id="c964d-123">REVOKE statement</span></span>
-   <span data-ttu-id="c964d-124">Псевдонимы областей или номера редакций</span><span class="sxs-lookup"><span data-stu-id="c964d-124">SCOPE aliases or revision numbers</span></span>
-   <span data-ttu-id="c964d-125">ВЫБРАТЬ все (автоматическое удаление дубликатов)</span><span class="sxs-lookup"><span data-stu-id="c964d-125">SELECT ALL (removes duplicates automatically)</span></span>
-   <span data-ttu-id="c964d-126">Хранимые процедуры</span><span class="sxs-lookup"><span data-stu-id="c964d-126">Stored procedures</span></span>
-   <span data-ttu-id="c964d-127">Расширение структурированного документа</span><span class="sxs-lookup"><span data-stu-id="c964d-127">Structured document expansion</span></span>
-   <span data-ttu-id="c964d-128">UNION ALL</span><span class="sxs-lookup"><span data-stu-id="c964d-128">UNION ALL</span></span>
-   <span data-ttu-id="c964d-129">Неизвестное ключевое слово</span><span class="sxs-lookup"><span data-stu-id="c964d-129">UNKNOWN keyword</span></span>
-   <span data-ttu-id="c964d-130">Инструкция UPDATE</span><span class="sxs-lookup"><span data-stu-id="c964d-130">UPDATE statement</span></span>

<span data-ttu-id="c964d-131">Поиск Windows не поддерживает тезаурусы и пропускаемые слова.</span><span class="sxs-lookup"><span data-stu-id="c964d-131">Windows Search does not support Thesaurus and Noise Words.</span></span>

 

 



