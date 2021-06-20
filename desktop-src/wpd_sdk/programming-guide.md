---
title: Программное руководством по программированию WPD
description: Это руководство по программированию посвящено выполнению образцов задач с помощью интерфейсов и методов WPD, обнаруженных в интерфейсах.
ms.assetid: 87777b0b-a7a0-4032-99bb-92b717d3c452
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db13d50942c28cd4937d27a745d61d7a30a01a15
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409867"
---
# <a name="wpd-programming-guide"></a><span data-ttu-id="1ff1a-103">Программное руководством по программированию WPD</span><span class="sxs-lookup"><span data-stu-id="1ff1a-103">WPD programming guide</span></span>

<span data-ttu-id="1ff1a-104">Первичный источник для этого руководством по программированию — это пример, поставляемый с пакетом SDK для портативных устройств Windows (WPD).</span><span class="sxs-lookup"><span data-stu-id="1ff1a-104">The primary source for this programming guide is a sample that ships with the Windows Portable Devices (WPD) Software Development Kit (SDK).</span></span> <span data-ttu-id="1ff1a-105">Этот пример с именем WpdApiSample.exe состоит из семи модулей. cpp.</span><span class="sxs-lookup"><span data-stu-id="1ff1a-105">This sample, named WpdApiSample.exe, consists of seven .cpp modules.</span></span> <span data-ttu-id="1ff1a-106">Шесть из этих модулей содержат код, демонстрирующий 26 задач, которые приложение может выполнить с помощью программного интерфейса (API) WPD.</span><span class="sxs-lookup"><span data-stu-id="1ff1a-106">Six of these modules contain the code that demonstrates 26 tasks that an application can accomplish using the WPD application programming interface (API).</span></span>

<span data-ttu-id="1ff1a-107">Исключения, приведенные выше, являются разделами, описывающими: задачи службы устройств, контекстное меню и расширения страниц свойств. Эти разделы не были взяты из Впдаписампле.</span><span class="sxs-lookup"><span data-stu-id="1ff1a-107">The exceptions to the above are the topics that describe: device service tasks, the context menu and property sheet extensions; these topics were not taken from WpdApiSample.</span></span> <span data-ttu-id="1ff1a-108">Задачи службы устройств основаны на образце с именем Впдсервицеаписампле.</span><span class="sxs-lookup"><span data-stu-id="1ff1a-108">The device service tasks are based on the sample named WpdServiceApiSample.</span></span> <span data-ttu-id="1ff1a-109">Расширения контекстного меню и страницы свойств — это фрагменты кода, взятые из приложений, которые не поставляются с Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="1ff1a-109">The context menu and property sheet extensions are snippets taken from applications that do not ship with the Windows SDK.</span></span>

<span data-ttu-id="1ff1a-110">В следующих разделах основное внимание уделяется задачам, выполняемым этими примерами, и объясняется, как каждый из них выполняется с помощью интерфейсов WPD и ряда методов, найденных в этих интерфейсах.</span><span class="sxs-lookup"><span data-stu-id="1ff1a-110">The following sections focus on the tasks accomplished by these samples and explain how each is accomplished using the WPD interfaces and a number of the methods found in these interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ff1a-111">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="1ff1a-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ff1a-112">**Портативные устройства Windows**</span><span class="sxs-lookup"><span data-stu-id="1ff1a-112">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
