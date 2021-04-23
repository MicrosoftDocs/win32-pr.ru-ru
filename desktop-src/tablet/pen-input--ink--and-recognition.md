---
description: Одной из интересных новых возможностей Tablet PC является система ввода с помощью пера.
ms.assetid: 8432617a-5ae7-44cb-a5f7-f3b2d8885846
title: Ввод, ввод и распознавание с помощью пера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a46d865e40d1779edaa2607b1754c45659609b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554138"
---
# <a name="pen-input-ink-and-recognition"></a><span data-ttu-id="9739d-103">Ввод, ввод и распознавание с помощью пера</span><span class="sxs-lookup"><span data-stu-id="9739d-103">Pen Input, Ink, and Recognition</span></span>

<span data-ttu-id="9739d-104">Одной из интересных новых возможностей Tablet PC является система ввода с помощью пера.</span><span class="sxs-lookup"><span data-stu-id="9739d-104">One interesting new feature of Tablet PC is the pen input system.</span></span> <span data-ttu-id="9739d-105">На всех компьютерах Tablet PC имеется Дигитайзер под экраном, который принимает ввод с помощью пера.</span><span class="sxs-lookup"><span data-stu-id="9739d-105">All Tablet PC computers have a digitizer beneath the screen that accepts pen input.</span></span> <span data-ttu-id="9739d-106">Этот новый механизм ввода требует думать о том, как создавать приложения специально для планшетных ПК.</span><span class="sxs-lookup"><span data-stu-id="9739d-106">This new input mechanism requires you to think about how to build applications specifically for Tablet PC.</span></span> <span data-ttu-id="9739d-107">Интерфейс прикладного программирования (API) платформы Tablet PC позволяет сделать это.</span><span class="sxs-lookup"><span data-stu-id="9739d-107">The Tablet PC platform application programming interface (API) helps you do this.</span></span>

## <a name="collection-data-management-and-recognition"></a><span data-ttu-id="9739d-108">Сбор, Управление данными и распознавание</span><span class="sxs-lookup"><span data-stu-id="9739d-108">Collection, Data Management, and Recognition</span></span>

<span data-ttu-id="9739d-109">Платформу для планшетных ПК можно разделить на три отдельные области:</span><span class="sxs-lookup"><span data-stu-id="9739d-109">The Tablet PC platform can be divided into three distinct areas:</span></span>

-   <span data-ttu-id="9739d-110">Коллекция рукописных данных (объекты, используемые для сбора рукописного ввода с дигитайзера).</span><span class="sxs-lookup"><span data-stu-id="9739d-110">Ink collection (objects that are used to collect ink from the digitizer).</span></span>
-   <span data-ttu-id="9739d-111">Управление рукописными данными (объекты, используемые для управления собранными красками).</span><span class="sxs-lookup"><span data-stu-id="9739d-111">Ink data management (objects that are used to manage the collected ink).</span></span>
-   <span data-ttu-id="9739d-112">Распознавание рукописного ввода (объекты, используемые для преобразования собранного рукописного ввода в другие типы данных, такие как текст).</span><span class="sxs-lookup"><span data-stu-id="9739d-112">Ink recognition (objects that are used to convert the collected ink into other types of data, such as text).</span></span>

<span data-ttu-id="9739d-113">На следующем рисунке на высоком уровне показано, как API сбора рукописного ввода (API), рукописный Управление данными API (рукописный ввод) и API распознавания рукописного ввода (API распознавания) работают вместе на платформе Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="9739d-113">The following image shows, at a high level, how the Ink Collection API (Pen API), Ink Data Management API (Ink API), and Ink Recognition API (Recognition API) work together in the Tablet PC platform.</span></span>

![иллустратон, показывающий, как API пера, API рукописного ввода и API распознавания работают вместе](images/aabc298b-fd64-435b-87bc-eb7cd11524e8.jpg)

<span data-ttu-id="9739d-115">API платформы Tablet PC доступен в управляемых API, а также в библиотеке COM.</span><span class="sxs-lookup"><span data-stu-id="9739d-115">The Tablet PC platform API is available in Managed APIs as well as a COM library.</span></span> <span data-ttu-id="9739d-116">В следующих разделах описываются объекты в API и показано, как приложения используют эти объекты:</span><span class="sxs-lookup"><span data-stu-id="9739d-116">The following topics describe the objects in the API and illustrate how applications use these objects:</span></span>

-   [<span data-ttu-id="9739d-117">Коллекция рукописных данных</span><span class="sxs-lookup"><span data-stu-id="9739d-117">Ink Collection</span></span>](ink-collection.md)
-   [<span data-ttu-id="9739d-118">Рукописные данные</span><span class="sxs-lookup"><span data-stu-id="9739d-118">Ink Data</span></span>](ink-data.md)
-   [<span data-ttu-id="9739d-119">Распознавание рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="9739d-119">Ink Recognition</span></span>](ink-recognition.md)
-   [<span data-ttu-id="9739d-120">Анализ рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="9739d-120">Ink Analysis</span></span>](ink-analysis.md)
-   [<span data-ttu-id="9739d-121">Распознавание рукописного текста в Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9739d-121">Handwriting Recognition in Windows Server 2008 R2</span></span>](handwriting-recognition-in-windows-server-2008-r2.md)

 

 



