---
title: Открытие и закрытие файлов
description: Открытие и закрытие файлов
ms.assetid: 72655d33-f685-4205-a982-f7cd20c59f22
keywords:
- Функция Авифилеопен
- Функция Авифилерелеасе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68e1c51c4747e03bf4f18a8e6c560e45798e1c8c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105684822"
---
# <a name="opening-and-closing-files"></a><span data-ttu-id="060c2-105">Открытие и закрытие файлов</span><span class="sxs-lookup"><span data-stu-id="060c2-105">Opening and Closing Files</span></span>

<span data-ttu-id="060c2-106">Перед чтением или записью приложение должно открыть файл AVI.</span><span class="sxs-lookup"><span data-stu-id="060c2-106">An application must open an AVI file before reading or writing.</span></span> <span data-ttu-id="060c2-107">Чтобы открыть файл AVI, используйте функцию [**авифилеопен**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) .</span><span class="sxs-lookup"><span data-stu-id="060c2-107">To open an AVI file, use the [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) function.</span></span> <span data-ttu-id="060c2-108">**Авифилеопен** возвращает адрес интерфейса AVI, который содержит маркер открытого файла и увеличивает счетчик ссылок файла.</span><span class="sxs-lookup"><span data-stu-id="060c2-108">**AVIFileOpen** returns the address of an AVI file interface that contains the handle of the open file and increments the reference count of the file.</span></span>

<span data-ttu-id="060c2-109">Функция **авифилеопен** поддерживает флаги, используемые с функцией [OpenFile](/documentation/) .</span><span class="sxs-lookup"><span data-stu-id="060c2-109">The **AVIFileOpen** function supports the OF flags used with the [OpenFile](/documentation/) function.</span></span> <span data-ttu-id="060c2-110">Если приложение записывает в существующий файл, оно должно включать \_ флаг записи в **авифилеопен**.</span><span class="sxs-lookup"><span data-stu-id="060c2-110">If an application writes to an existing file, it must include the OF\_WRITE flag in **AVIFileOpen**.</span></span> <span data-ttu-id="060c2-111">Аналогичным образом, если приложение создает и записывает в новый файл, необходимо включить в \_ \_ **авифилеопен** флаги Create и Write.</span><span class="sxs-lookup"><span data-stu-id="060c2-111">Similarly, if your application creates and writes to a new file, you must include the OF\_CREATE and OF\_WRITE flags in **AVIFileOpen**.</span></span>

<span data-ttu-id="060c2-112">При открытии файла с помощью **авифилеопен** можно использовать обработчик файлов по умолчанию или указать пользовательский обработчик файлов для чтения и записи в файл и его потоки данных.</span><span class="sxs-lookup"><span data-stu-id="060c2-112">When you open a file using **AVIFileOpen**, you can use a default file handler or you can specify a custom file handler to read and write to the file and its data streams.</span></span> <span data-ttu-id="060c2-113">В любом случае Авифиле выполняет поиск нужного обработчика файлов в реестре.</span><span class="sxs-lookup"><span data-stu-id="060c2-113">In either case, AVIFile searches the registry for the correct file handler to use.</span></span> <span data-ttu-id="060c2-114">Необходимо убедиться, что пользовательские обработчики файлов находятся в реестре, прежде чем приложение сможет получить к ним доступ.</span><span class="sxs-lookup"><span data-stu-id="060c2-114">You must ensure custom file handlers are in the registry before an application can access them.</span></span>

<span data-ttu-id="060c2-115">Значение счетчика ссылок для файла можно увеличить с помощью функции [**авифилеаддреф**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) .</span><span class="sxs-lookup"><span data-stu-id="060c2-115">You can increment the reference count of a file by using the [**AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) function.</span></span> <span data-ttu-id="060c2-116">Например, это может потребоваться при передаче обработчика файлового интерфейса другому приложению или при необходимости сохранения файла при использовании функции, которая обычно закрывает файл.</span><span class="sxs-lookup"><span data-stu-id="060c2-116">For example, you might want to do this when passing a handle of the file interface to another application, or when you want to keep a file open while using a function that would normally close the file.</span></span>

<span data-ttu-id="060c2-117">Вы можете закрыть файл с помощью функции [**авифилерелеасе**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) .</span><span class="sxs-lookup"><span data-stu-id="060c2-117">You can close a file by using the [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) function.</span></span> <span data-ttu-id="060c2-118">Функция **авифилерелеасе** уменьшает счетчик ссылок файла AVI, сохраняет изменения, внесенные в файл, а когда число ссылок достигает нуля, закрывает файл.</span><span class="sxs-lookup"><span data-stu-id="060c2-118">The **AVIFileRelease** function decrements the reference count of an AVI file, saves changes made to the file, and when the reference count reaches zero, closes the file.</span></span> <span data-ttu-id="060c2-119">Приложения должны сбалансировать количество ссылок, включив вызов **авифилерелеасе** для каждого использования [**авифилеопен**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) и **авифилеаддреф**.</span><span class="sxs-lookup"><span data-stu-id="060c2-119">Your applications should balance the reference count by including a call to **AVIFileRelease** for each use of [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) and **AVIFileAddRef**.</span></span>

> [!Note]  
> <span data-ttu-id="060c2-120">Приложение может открыть файл с одним или несколькими потоками программы.</span><span class="sxs-lookup"><span data-stu-id="060c2-120">An application can open a file with one or more program threads.</span></span> <span data-ttu-id="060c2-121">Однако для достижения наилучшей производительности только один поток должен иметь доступ к файлу в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="060c2-121">However, for the best possible performance, only one thread should access the file at any one time.</span></span>

 

 

 