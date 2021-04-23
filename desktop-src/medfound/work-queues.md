---
description: В Microsoft Media Foundation Рабочая очередь — это эффективный способ выполнения асинхронных операций в другом потоке.
ms.assetid: f886d096-b1f5-42e4-8888-501b58bffd50
title: Рабочие очереди
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b1e5e8a0a3776f718f645550813bf008b38aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264743"
---
# <a name="work-queues"></a><span data-ttu-id="de8da-103">Рабочие очереди</span><span class="sxs-lookup"><span data-stu-id="de8da-103">Work Queues</span></span>

<span data-ttu-id="de8da-104">В Microsoft Media Foundation Рабочая очередь — это эффективный способ выполнения асинхронных операций в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="de8da-104">In Microsoft Media Foundation, a work queue is an efficient way to perform asynchronous operations on another thread.</span></span>

<span data-ttu-id="de8da-105">Этот раздел содержит следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="de8da-105">This section contains the following topics.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de8da-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="de8da-106">Topic</span></span></th>
<th><span data-ttu-id="de8da-107">Описание</span><span class="sxs-lookup"><span data-stu-id="de8da-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="de8da-108"><a href="using-work-queues.md">Использование рабочих очередей</a></span><span class="sxs-lookup"><span data-stu-id="de8da-108"><a href="using-work-queues.md">Using Work Queues</a></span></span></td>
<td><span data-ttu-id="de8da-109">Описывает, как приложение или компонент может использовать рабочие очереди для выполнения асинхронных операций.</span><span class="sxs-lookup"><span data-stu-id="de8da-109">Describes how an application or component can use work queues to perform asynchronous operations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de8da-110"><a href="writing-an-asynchronous-method.md">Создание асинхронного метода</a></span><span class="sxs-lookup"><span data-stu-id="de8da-110"><a href="writing-an-asynchronous-method.md">Writing an Asynchronous Method</a></span></span></td>
<td><span data-ttu-id="de8da-111">Описывает, как написать асинхронный метод, следующий за шаблоном Begin/End, описанным в разделе <a href="asynchronous-callback-methods.md">асинхронные методы обратного вызова</a>.</span><span class="sxs-lookup"><span data-stu-id="de8da-111">Describes how to write an asynchronous method that follows the Begin/End pattern described in <a href="asynchronous-callback-methods.md">Asynchronous Callback Methods</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de8da-112"><a href="custom-asynchronous-result-objects.md">Пользовательские объекты асинхронных результатов</a></span><span class="sxs-lookup"><span data-stu-id="de8da-112"><a href="custom-asynchronous-result-objects.md">Custom Asynchronous Result Objects</a></span></span></td>
<td><span data-ttu-id="de8da-113">Описывает, как создать пользовательскую реализацию интерфейса <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>имфасинкресулт</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="de8da-113">Describes how to create a custom implementation of the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>IMFAsyncResult</strong></a> interface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="de8da-114">Большинство приложений должны использовать реализацию акции, предоставляемую <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult"><strong>мфкреатеасинкресулт</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de8da-114">Most applications should use the stock implementation provided by <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult"><strong>MFCreateAsyncResult</strong></a>.</span></span> <span data-ttu-id="de8da-115">Этот раздел предназначен для приложений с расширенными требованиями.</span><span class="sxs-lookup"><span data-stu-id="de8da-115">This topic is for applications with advanced requirements.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de8da-116"><a href="media-foundation-work-queue-and-threading-improvements.md">Усовершенствования рабочей очереди и потоков</a></span><span class="sxs-lookup"><span data-stu-id="de8da-116"><a href="media-foundation-work-queue-and-threading-improvements.md">Work Queue and Threading Improvements</a></span></span></td>
<td><span data-ttu-id="de8da-117">Описание усовершенствований в Windows 8 для рабочих очередей и многопоточности на Media Foundationной платформе.</span><span class="sxs-lookup"><span data-stu-id="de8da-117">Describes improvements in Windows 8 for work queues and threading in the Media Foundation platform.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="de8da-118">См. также</span><span class="sxs-lookup"><span data-stu-id="de8da-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de8da-119">Media Foundation API платформы</span><span class="sxs-lookup"><span data-stu-id="de8da-119">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 




