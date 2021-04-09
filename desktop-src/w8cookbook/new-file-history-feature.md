---
title: Новая функция истории файлов
description: Новая функция истории файлов
ms.assetid: B1EE4638-5591-483B-AA09-600E242ED50B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70aad84f4d052d6a872c7b0cfc979d0fa05cb84
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "104134703"
---
# <a name="new-file-history-feature"></a><span data-ttu-id="167d5-103">Новая функция истории файлов</span><span class="sxs-lookup"><span data-stu-id="167d5-103">New File History feature</span></span>

## <a name="platform"></a><span data-ttu-id="167d5-104">Платформа</span><span class="sxs-lookup"><span data-stu-id="167d5-104">Platform</span></span>

<span data-ttu-id="167d5-105">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="167d5-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="167d5-106">Описание</span><span class="sxs-lookup"><span data-stu-id="167d5-106">Description</span></span>

<span data-ttu-id="167d5-107">Новая функция журнала файлов заменяет существующую функцию резервного копирования и восстановления и обеспечивает защиту пользовательских файлов, хранящихся в библиотеках пользователей.</span><span class="sxs-lookup"><span data-stu-id="167d5-107">The new File History feature replaces the existing Backup and Restore function, and offers protection for user files stored in user libraries.</span></span> <span data-ttu-id="167d5-108">Предоставляется набор интерфейсов API, позволяющих разработчикам программно включать журнал файлов и выбирать конкретный целевой объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="167d5-108">A set of APIs is provided that allows developers to programmatically enable File History and select a specific storage target.</span></span> <span data-ttu-id="167d5-109">Документация по этим API-интерфейсам доступна на сайте MSDN.</span><span class="sxs-lookup"><span data-stu-id="167d5-109">Documentation for these APIs is available on MSDN.</span></span>

<span data-ttu-id="167d5-110">Это может повлиять на рабочие процессы, связанные с защитой данных и документацией, которые зависят от функции резервного копирования и восстановления Windows.</span><span class="sxs-lookup"><span data-stu-id="167d5-110">It may affect workflows related to data protection and documentation that depend on the Windows Backup and Restore feature.</span></span>

<span data-ttu-id="167d5-111">Мы не рекомендуем использовать обе функции одновременно.</span><span class="sxs-lookup"><span data-stu-id="167d5-111">We do not recommend using both features at the same time.</span></span> <span data-ttu-id="167d5-112">Журнал файлов проверяет, существует ли расписание резервного копирования и является ли оно активным. Если он найден, он не позволит пользователям включать его.</span><span class="sxs-lookup"><span data-stu-id="167d5-112">File History checks if a Backup schedule exists and is active and if it finds one, it will not let users to turn it on.</span></span> <span data-ttu-id="167d5-113">В этом случае пользователям, желающим использовать журнал файлов, придется удалить расписание архивации Windows.</span><span class="sxs-lookup"><span data-stu-id="167d5-113">In this case, users who want to use File History will have to delete the Windows Backup schedule.</span></span>

## <a name="manifestation"></a><span data-ttu-id="167d5-114">Проявление</span><span class="sxs-lookup"><span data-stu-id="167d5-114">Manifestation</span></span>

<span data-ttu-id="167d5-115">Рабочие процессы могут быть прерваны, а документация по предыдущему методу для доступа к функции резервного копирования и восстановления Windows потребуется обновить, чтобы отразить эти изменения.</span><span class="sxs-lookup"><span data-stu-id="167d5-115">Workflows may be interrupted and documentation for the previous method for accessing the Windows Backup and Restore feature will need to be updated to reflect these changes.</span></span>

## <a name="solution"></a><span data-ttu-id="167d5-116">Решение</span><span class="sxs-lookup"><span data-stu-id="167d5-116">Solution</span></span>

<span data-ttu-id="167d5-117">Пересмотреть приложения, содержащие рабочие процессы, на которые отрицательно повлияла новая функция журнала файлов, для устранения конфликтов и внедрения нового набора API.</span><span class="sxs-lookup"><span data-stu-id="167d5-117">Revise apps that contain workflows that are adversely impacted by the new File History feature to remove any conflicts and incorporate the new set of APIs.</span></span>

## <a name="tests"></a><span data-ttu-id="167d5-118">Тесты</span><span class="sxs-lookup"><span data-stu-id="167d5-118">Tests</span></span>

<span data-ttu-id="167d5-119">API позволяет разработчикам определить, включен ли журнал файлов.</span><span class="sxs-lookup"><span data-stu-id="167d5-119">The API allows developers to determine if File History is turned on.</span></span>

 

 




