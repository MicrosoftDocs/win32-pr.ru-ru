---
title: Объектная модель агента
description: Объектная модель агента
ms.assetid: 4ec6ec3f-9772-4e29-9482-b9860092f053
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a97bcc104cb7835c3335b22bcfd185b152b1c290
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "104565507"
---
# <a name="the-agent-object-model"></a><span data-ttu-id="e06aa-103">Объектная модель агента</span><span class="sxs-lookup"><span data-stu-id="e06aa-103">The Agent Object Model</span></span>

<span data-ttu-id="e06aa-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e06aa-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="e06aa-105">Объектная модель Microsoft Agent состоит из следующих объектов:</span><span class="sxs-lookup"><span data-stu-id="e06aa-105">The Microsoft Agent Object Model consists of the following objects:</span></span>

-   <span data-ttu-id="e06aa-106">Запрос</span><span class="sxs-lookup"><span data-stu-id="e06aa-106">Request</span></span>
-   <span data-ttu-id="e06aa-107">Агент (элемент управления)</span><span class="sxs-lookup"><span data-stu-id="e06aa-107">Agent (control)</span></span>
-   <span data-ttu-id="e06aa-108">Символы (коллекция)</span><span class="sxs-lookup"><span data-stu-id="e06aa-108">Characters (collection)</span></span>
-   <span data-ttu-id="e06aa-109">Знак</span><span class="sxs-lookup"><span data-stu-id="e06aa-109">Character</span></span>
-   <span data-ttu-id="e06aa-110">Команды (коллекция)</span><span class="sxs-lookup"><span data-stu-id="e06aa-110">Commands (collection)</span></span>
-   <span data-ttu-id="e06aa-111">Get-Help</span><span class="sxs-lookup"><span data-stu-id="e06aa-111">Command</span></span>
-   <span data-ttu-id="e06aa-112">Появится</span><span class="sxs-lookup"><span data-stu-id="e06aa-112">Balloon</span></span>
-   <span data-ttu-id="e06aa-113">Аниматионнамес (коллекция)</span><span class="sxs-lookup"><span data-stu-id="e06aa-113">AnimationNames (collection)</span></span>
-   <span data-ttu-id="e06aa-114">спичинпут</span><span class="sxs-lookup"><span data-stu-id="e06aa-114">SpeechInput</span></span>
-   <span data-ttu-id="e06aa-115">аудиуутпут</span><span class="sxs-lookup"><span data-stu-id="e06aa-115">AudioOutput</span></span>
-   <span data-ttu-id="e06aa-116">коммандсвиндов</span><span class="sxs-lookup"><span data-stu-id="e06aa-116">CommandsWindow</span></span>
-   <span data-ttu-id="e06aa-117">Страница свойств</span><span class="sxs-lookup"><span data-stu-id="e06aa-117">PropertySheet</span></span>

<span data-ttu-id="e06aa-118">Эти объекты организованы в следующую иерархию.</span><span class="sxs-lookup"><span data-stu-id="e06aa-118">These objects are organized in the following hierarchy.</span></span> <span data-ttu-id="e06aa-119">(Пунктирная линия, следующая за объектом, указывает, что может существовать несколько объектов.)</span><span class="sxs-lookup"><span data-stu-id="e06aa-119">(The dotted line following an object indicates that multiple objects can exist.)</span></span>

![Схема, на которой показана иерархия объектов, начиная с "Request".](images/pro358.gif)

 

 




