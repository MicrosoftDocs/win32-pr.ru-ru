---
description: Одноранговая инфраструктура не гарантирует порядок получения и обработки записей.
ms.assetid: 840aa931-c54c-463d-b37b-7d01c8a44409
title: Зависимости записей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a7cce0803ad25f4a67908256ad78c7abe4b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663290"
---
# <a name="record-dependencies"></a><span data-ttu-id="156ba-103">Зависимости записей</span><span class="sxs-lookup"><span data-stu-id="156ba-103">Record Dependencies</span></span>

<span data-ttu-id="156ba-104">Одноранговая инфраструктура не гарантирует порядок получения и обработки записей.</span><span class="sxs-lookup"><span data-stu-id="156ba-104">The Peer Infrastructure does not guarantee the order for receiving and processing records.</span></span> <span data-ttu-id="156ba-105">Если приложение имеет зависимости записей, то есть обработка или проверка одной записи полагается на другую запись, приложение должно иметь возможность обрабатывать ситуации, когда записи могут быть получены в произвольном и непредсказуемом порядке.</span><span class="sxs-lookup"><span data-stu-id="156ba-105">If your application has record dependencies, which means that the processing or validation of one record relies on another record, then your application must be able to handle situations when records might be received in an arbitrary and unpredictable order.</span></span> <span data-ttu-id="156ba-106">Например, приложение разговора может иметь два типа записей: запись, которая содержит сведения о конкретном пользователе, и запись, которая содержит сообщение разговора, ссылающееся на запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="156ba-106">For example, a chat application may have two types of records: a record that contains information about a specific user, and a record that contains a chat message that refers to the user record.</span></span>

<span data-ttu-id="156ba-107">Приложение должно иметь возможность обрабатывать ситуацию при получении записи сообщения разговора перед записью пользователя для сообщения разговора.</span><span class="sxs-lookup"><span data-stu-id="156ba-107">An application must be able to handle the situation when a chat message record is received before the user record for the chat message.</span></span> <span data-ttu-id="156ba-108">Одним из способов решения этой проблемы является ожидание записи пользователя с помощью **списка**, а также кэша и таймера.</span><span class="sxs-lookup"><span data-stu-id="156ba-108">One way to handle the situation is to wait for the user record by using a **stand-by list**, or a cache and timer.</span></span> <span data-ttu-id="156ba-109">Приложение может периодически проверять каждую запись в списке или кэше, а затем обрабатывает ситуацию при получении необходимой записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="156ba-109">The application can periodically examine each record in the list or cache, and then handle the situation when the required user record is received.</span></span>

<span data-ttu-id="156ba-110">Для управления зависимостями записей хорошо спроектированное приложение состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="156ba-110">To handle record dependencies, a well-designed application consists of the following:</span></span>

-   <span data-ttu-id="156ba-111">Всегда проверяет наличие зависимостей записей перед выполнением действия.</span><span class="sxs-lookup"><span data-stu-id="156ba-111">Always checks for record dependencies before performing an action.</span></span>
-   <span data-ttu-id="156ba-112">Предполагает условия, которые могут возникнуть при получении записей в непредвиденном порядке, а затем обрабатывает ситуацию.</span><span class="sxs-lookup"><span data-stu-id="156ba-112">Anticipates conditions that might occur when records are received in an unexpected order, and then handles the situation.</span></span>

 

 



