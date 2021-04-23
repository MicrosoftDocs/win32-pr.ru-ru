---
description: Описывает основные понятия ввода-вывода.
ms.assetid: 61b286a0-2f0d-48d1-a0b9-bb13f1ea1b0e
title: Основные понятия ввода-вывода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727ae7f2b34b7938de444a82c9c4dfdf89f52ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684367"
---
# <a name="io-concepts"></a><span data-ttu-id="2a459-103">Основные понятия ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="2a459-103">I/O Concepts</span></span>

<span data-ttu-id="2a459-104">В этом разделе описаны следующие основные понятия ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="2a459-104">The following I/O concepts are described in this section.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2a459-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="2a459-105">In this section</span></span>



| <span data-ttu-id="2a459-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="2a459-106">Topic</span></span>                                                                               | <span data-ttu-id="2a459-107">Описание</span><span class="sxs-lookup"><span data-stu-id="2a459-107">Description</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a459-108">Буферизация файла</span><span class="sxs-lookup"><span data-stu-id="2a459-108">File Buffering</span></span>](file-buffering.md)<br/>                                     | <span data-ttu-id="2a459-109">Описывает вопросы управления приложениями для буферизации файлов, которые также называются небуферизованными файлами ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="2a459-109">Describes considerations for application control of file buffering, also known as unbuffered file input/output (I/O).</span></span><br/>                                    |
| [<span data-ttu-id="2a459-110">Кэширование файлов</span><span class="sxs-lookup"><span data-stu-id="2a459-110">File Caching</span></span>](file-caching.md)<br/>                                         | <span data-ttu-id="2a459-111">Windows кэширует файловые данные, которые считываются с дисков и записываются на диски.</span><span class="sxs-lookup"><span data-stu-id="2a459-111">Windows caches file data that is read from disks and written to disks.</span></span><br/>                                                                                   |
| [<span data-ttu-id="2a459-112">Синхронный и асинхронный ввод-вывод</span><span class="sxs-lookup"><span data-stu-id="2a459-112">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)<br/> | <span data-ttu-id="2a459-113">Существует два типа синхронизации ввода-вывода: синхронный ввод-вывод и асинхронный ввод-вывод.</span><span class="sxs-lookup"><span data-stu-id="2a459-113">There are two types of input/output (I/O) synchronization: synchronous I/O and asynchronous I/O.</span></span> <span data-ttu-id="2a459-114">Асинхронный ввод-вывод также называется перекрытой операцией ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="2a459-114">Asynchronous I/O is also referred to as overlapped I/O.</span></span><br/> |
| [<span data-ttu-id="2a459-115">Отмена ожидающих операций ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="2a459-115">Canceling Pending I/O Operations</span></span>](canceling-pending-i-o-operations.md)<br/> | <span data-ttu-id="2a459-116">Предоставление пользователям возможности отменять запросы ввода-вывода, которые замедляют или блокируется, может повысить удобство использования и надежность приложения.</span><span class="sxs-lookup"><span data-stu-id="2a459-116">Allowing users to cancel I/O requests that are slow or blocked can enhance the usability and robustness of your application.</span></span><br/>                             |
| [<span data-ttu-id="2a459-117">Ввод-вывод с оповещением</span><span class="sxs-lookup"><span data-stu-id="2a459-117">Alertable I/O</span></span>](alertable-i-o.md)<br/>                                       | <span data-ttu-id="2a459-118">С помощью предупреждений I/O потоки приложений обрабатывают асинхронные запросы ввода-вывода только в том случае, если они находятся в состоянии оповещения.</span><span class="sxs-lookup"><span data-stu-id="2a459-118">Alertable I/O is the method by which application threads process asynchronous I/O requests only when they are in an alertable state.</span></span><br/>                     |
| [<span data-ttu-id="2a459-119">Порты завершения ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="2a459-119">I/O Completion Ports</span></span>](i-o-completion-ports.md)<br/>                         | <span data-ttu-id="2a459-120">Порты завершения ввода-вывода предоставляют эффективную потоковую модель для обработки нескольких асинхронных запросов ввода-вывода в многопроцессорной системе.</span><span class="sxs-lookup"><span data-stu-id="2a459-120">I/O completion ports provide an efficient threading model for processing multiple asynchronous I/O requests on a multiprocessor system.</span></span><br/>                  |



 

 

 




