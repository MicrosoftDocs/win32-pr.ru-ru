---
description: ICE66 использует таблицы в базе данных для определения схемы, которую должна использовать база данных.
ms.assetid: 7cf929a0-2c4c-40ca-a902-dfd9dcd203b8
title: ICE66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea1436ad791941c96c0484a02f40a60fc9939e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810912"
---
# <a name="ice66"></a><span data-ttu-id="0522b-103">ICE66</span><span class="sxs-lookup"><span data-stu-id="0522b-103">ICE66</span></span>

<span data-ttu-id="0522b-104">ICE66 использует таблицы в базе данных для определения схемы, которую должна использовать база данных.</span><span class="sxs-lookup"><span data-stu-id="0522b-104">ICE66 uses the tables in the database to determine which schema your database should use.</span></span>

<span data-ttu-id="0522b-105">Некоторые функциональные возможности могут быть доступны только в том случае, если пакет установлен в системе с текущей версией установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="0522b-105">Some functionality may only be available if the package is installed on a system with a current Windows Installer version.</span></span>

## <a name="result"></a><span data-ttu-id="0522b-106">Результат</span><span class="sxs-lookup"><span data-stu-id="0522b-106">Result</span></span>

<span data-ttu-id="0522b-107">ICE66 отправляет предупреждение, если в базе данных используется неправильная схема.</span><span class="sxs-lookup"><span data-stu-id="0522b-107">ICE66 posts a warning if your database is using the wrong schema.</span></span>

## <a name="example"></a><span data-ttu-id="0522b-108">Пример</span><span class="sxs-lookup"><span data-stu-id="0522b-108">Example</span></span>

<span data-ttu-id="0522b-109">ICE66 сообщает следующее предупреждение для приведенного примера.</span><span class="sxs-lookup"><span data-stu-id="0522b-109">ICE66 reports the following warning for the example shown.</span></span>

``` syntax
WARNING: Complete functionality of the IsolatedComponents table is only available with Windows Installer versions 1.1 or greater. Your schema is 100.
```

<span data-ttu-id="0522b-110">Это предупреждение можно пропустить, если вы хотите, чтобы пакет был установлен с использованием текущей версии установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="0522b-110">This warning can be ignored if you want your package to be installed using a current Windows Installer version.</span></span> <span data-ttu-id="0522b-111">Например, если вы хотите, чтобы пакет был установлен только в версии 2,0 или более поздней, измените схему пакета (PID \_ PAGECOUNT) на 200.</span><span class="sxs-lookup"><span data-stu-id="0522b-111">For example, if you want your package to be installable only on version 2.0 or later, change your package schema (PID\_PAGECOUNT) to 200.</span></span>

[<span data-ttu-id="0522b-112">Таблица Исолатедкомпонент</span><span class="sxs-lookup"><span data-stu-id="0522b-112">IsolatedComponent Table</span></span>](isolatedcomponent-table.md)



| <span data-ttu-id="0522b-113">\_Общий компонент</span><span class="sxs-lookup"><span data-stu-id="0522b-113">Component\_Shared</span></span> | <span data-ttu-id="0522b-114">\_Приложение компонента</span><span class="sxs-lookup"><span data-stu-id="0522b-114">Component\_Application</span></span> |
|-------------------|------------------------|
| <span data-ttu-id="0522b-115">Component1</span><span class="sxs-lookup"><span data-stu-id="0522b-115">Component1</span></span>        | <span data-ttu-id="0522b-116">Component2</span><span class="sxs-lookup"><span data-stu-id="0522b-116">Component2</span></span>             |



 

[<span data-ttu-id="0522b-117">Сводный поток информации</span><span class="sxs-lookup"><span data-stu-id="0522b-117">Summary Information Stream</span></span>](summary-information-stream.md)



| <span data-ttu-id="0522b-118">пидт</span><span class="sxs-lookup"><span data-stu-id="0522b-118">PIDt</span></span>           | <span data-ttu-id="0522b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0522b-119">Value</span></span> |
|----------------|-------|
| <span data-ttu-id="0522b-120">Идентификатор процесса \_ PAGECOUNT</span><span class="sxs-lookup"><span data-stu-id="0522b-120">PID\_PAGECOUNT</span></span> | <span data-ttu-id="0522b-121">100</span><span class="sxs-lookup"><span data-stu-id="0522b-121">100</span></span>   |



 

## <a name="table-used-during-execution"></a><span data-ttu-id="0522b-122">Таблица, используемая во время выполнения:</span><span class="sxs-lookup"><span data-stu-id="0522b-122">Table used during execution:</span></span>

[<span data-ttu-id="0522b-123">\_Таблица Columns</span><span class="sxs-lookup"><span data-stu-id="0522b-123">\_Columns table</span></span>](-columns-table.md)

## <a name="related-topics"></a><span data-ttu-id="0522b-124">См. также</span><span class="sxs-lookup"><span data-stu-id="0522b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0522b-125">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="0522b-125">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



