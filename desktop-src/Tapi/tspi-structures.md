---
description: Структуры данных, используемые ТСПИ, идентичны тем, которые определены в структурах TAPI, за исключением ТУИСПИКРЕАТЕДИАЛОГИНСТАНЦЕПАРАМС.
ms.assetid: 99d966ea-49b5-4a84-83a1-99dc8465c751
title: Структуры ТСПИ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e3468171bc160ca03ac9f5501a9eba7fd9221ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683390"
---
# <a name="tspi-structures"></a><span data-ttu-id="207f9-103">Структуры ТСПИ</span><span class="sxs-lookup"><span data-stu-id="207f9-103">TSPI Structures</span></span>

<span data-ttu-id="207f9-104">Структуры данных, используемые ТСПИ, идентичны тем, которые определены в [структурах TAPI](./tapi-structures.md), за исключением [**туиспикреатедиалогинстанцепарамс**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams).</span><span class="sxs-lookup"><span data-stu-id="207f9-104">The data structures TSPI uses are identical to those defined in [TAPI Structures](./tapi-structures.md), with the exception of [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams).</span></span>

<span data-ttu-id="207f9-105">В случае большей части больших структур данных ответственность за заполнение элементов делится на поставщика услуг и TAPI.</span><span class="sxs-lookup"><span data-stu-id="207f9-105">In the case of most of the larger data structures, the responsibility for filling in members is divided between the service provider and TAPI.</span></span> <span data-ttu-id="207f9-106">Поставщик услуг должен сохранять значения, которые находятся в членах, принадлежащих TAPI.</span><span class="sxs-lookup"><span data-stu-id="207f9-106">The service provider must preserve the values present in members owned by TAPI.</span></span> <span data-ttu-id="207f9-107">Описание элементов, которые должны быть заданы поставщиком услуг и которые должны быть сохранены, приводится в разделе функции в функциях, ссылающихся на эту структуру данных.</span><span class="sxs-lookup"><span data-stu-id="207f9-107">The description of which members must be set by the service provider and which must be preserved is provided in the Functions section in the functions that refer to that data structure.</span></span>

<span data-ttu-id="207f9-108">Для каждой структуры в разделе Reference перечислены следующие элементы.</span><span class="sxs-lookup"><span data-stu-id="207f9-108">For each structure, the reference section lists the following items:</span></span>

-   <span data-ttu-id="207f9-109">Назначение структуры</span><span class="sxs-lookup"><span data-stu-id="207f9-109">The purpose of the structure</span></span>
-   <span data-ttu-id="207f9-110">Описание значений или полей</span><span class="sxs-lookup"><span data-stu-id="207f9-110">A description of the values or fields</span></span>
-   <span data-ttu-id="207f9-111">Описание расширяемости структуры</span><span class="sxs-lookup"><span data-stu-id="207f9-111">A description of the structure's extensibility</span></span>
-   <span data-ttu-id="207f9-112">Необязательные комментарии по использованию структуры</span><span class="sxs-lookup"><span data-stu-id="207f9-112">Optional comments about using the structure</span></span>
-   <span data-ttu-id="207f9-113">Необязательные ссылки на другие функции, сообщения, константы или структуры.</span><span class="sxs-lookup"><span data-stu-id="207f9-113">Optional references to other functions, messages, constants, or structures.</span></span>

<span data-ttu-id="207f9-114">Память для всех структур данных, представление которых публикуется и совместно используется интерфейсом TAPI и поставщиком услуг, выделено TAPI или приложением с помощью TAPI.</span><span class="sxs-lookup"><span data-stu-id="207f9-114">Memory for all data structures whose representation is published and shared by both TAPI and the service provider is allocated by TAPI or an application using TAPI.</span></span> <span data-ttu-id="207f9-115">TAPI передает указатель на функцию ТСПИ, которая возвращает информацию.</span><span class="sxs-lookup"><span data-stu-id="207f9-115">TAPI passes a pointer to the TSPI function that returns the information.</span></span> <span data-ttu-id="207f9-116">ТСПИ заполняет структуру данных запрашиваемой информацией.</span><span class="sxs-lookup"><span data-stu-id="207f9-116">TSPI fills the data structure with the requested information.</span></span> <span data-ttu-id="207f9-117">Если операция является асинхронной, сведения недоступны, пока обратный вызов асинхронного ответа не указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="207f9-117">If the operation is asynchronous, the information is not available until the asynchronous reply callback indicates success.</span></span>

> [!Note]  
> <span data-ttu-id="207f9-118">Некоторые структуры включают поля Размер и смещение для определения расположения и длины строк в переменной части структуры.</span><span class="sxs-lookup"><span data-stu-id="207f9-118">Some structures include Size and Offset fields for defining the location and length of strings in the variable portion of the structure.</span></span> <span data-ttu-id="207f9-119">Если поставщик услуг запрашивает добавление строки, но строка не доступна, поставщик услуг должен указать это условие одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="207f9-119">If the service provider is requested to add a string but no string is available, the service provider must indicate this condition in one of these ways:</span></span>
>
> -   <span data-ttu-id="207f9-120">Задайте для полей Размер и смещение значение 0.</span><span class="sxs-lookup"><span data-stu-id="207f9-120">Set both the Size and Offset fields to 0.</span></span>
> -   <span data-ttu-id="207f9-121">Задайте для поля смещения ненулевое значение, а для параметра size — 0.</span><span class="sxs-lookup"><span data-stu-id="207f9-121">Set the Offset field to nonzero but Size to 0.</span></span>
> -   <span data-ttu-id="207f9-122">Задайте для поля смещение значение ненулевой, установите размер равным 1 и байт со смещением до 0.</span><span class="sxs-lookup"><span data-stu-id="207f9-122">Set the Offset field to nonzero, Size to 1, and the byte at the Offset to 0.</span></span>

 

 

 
