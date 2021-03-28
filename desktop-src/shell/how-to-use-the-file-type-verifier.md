---
description: В этом разделе описывается использование средства проверки типа файлов, предоставляемого в пакете SDK для Windows 7.
ms.assetid: 96FCA74B-DEB2-49D1-B670-EBD8BE0783F1
title: Использование средства проверки типов файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f083897499f972f945867a0c02318df192e734d9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/28/2021
ms.locfileid: "104273155"
---
# <a name="how-to-use-the-file-type-verifier"></a><span data-ttu-id="da4c3-103">Использование средства проверки типов файлов</span><span class="sxs-lookup"><span data-stu-id="da4c3-103">How to Use the File Type Verifier</span></span>

<span data-ttu-id="da4c3-104">В этом разделе описывается использование средства проверки типа файлов, предоставляемого в [пакете SDK для Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="da4c3-104">This topic describes how to use the File Type Verifier that is provided in the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="da4c3-105">Если программа создает типы файлов, с которыми пользователи взаимодействуют из оболочки Windows (обычно хранятся в известной пользователем папке, например **«Мои документы**»), очень важно проверить приложение и убедиться, что создаваемые им файлы правильно зарегистрированы, и обеспечить высококачественное взаимодействие с пользователем при просмотре и поиске файлов.</span><span class="sxs-lookup"><span data-stu-id="da4c3-105">If your program creates file types that users are expected to interact with from the Windows Shell (typically stored in a user's known folder such as **My Documents**), it is very important to test your application and verify that the files it creates are properly registered and provide a high-quality user experience when browsing and searching files.</span></span> <span data-ttu-id="da4c3-106">Это особенно важно, если предполагается, что пользователи будут запускать приложения в Windows 7, которые полагаются на обработчики типов файлов высокого качества для многих функций оболочки.</span><span class="sxs-lookup"><span data-stu-id="da4c3-106">This is especially important if you expect users to run your applications on Windows 7, which relies on high-quality file type handlers for many of the Shell features.</span></span>

<span data-ttu-id="da4c3-107">Чтобы проверить тип файла с помощью средства проверки типа файлов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="da4c3-107">To verify your file type using the File Type Verifier, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="da4c3-108">Инструкции</span><span class="sxs-lookup"><span data-stu-id="da4c3-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="da4c3-109">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="da4c3-109">Step 1:</span></span>

<span data-ttu-id="da4c3-110">Установите приложение в тестовой среде и скопируйте в него средство проверки типа файла.</span><span class="sxs-lookup"><span data-stu-id="da4c3-110">Install the application on your test environment, and copy the File Type Verifier to that environment.</span></span> <span data-ttu-id="da4c3-111">Средство проверки типов файлов доступно в [пакете SDK для Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="da4c3-111">The File Type Verifier is available in the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

### <a name="step-2"></a><span data-ttu-id="da4c3-112">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="da4c3-112">Step 2:</span></span>

<span data-ttu-id="da4c3-113">Используйте приложение, чтобы создать файл для тестирования.</span><span class="sxs-lookup"><span data-stu-id="da4c3-113">Use your application to create a file to be tested.</span></span>

### <a name="step-3"></a><span data-ttu-id="da4c3-114">Шаг 3.</span><span class="sxs-lookup"><span data-stu-id="da4c3-114">Step 3:</span></span>

<span data-ttu-id="da4c3-115">Запустите средство проверки типов файлов.</span><span class="sxs-lookup"><span data-stu-id="da4c3-115">Start the File Type Verifier.</span></span>

### <a name="step-4"></a><span data-ttu-id="da4c3-116">Шаг 4.</span><span class="sxs-lookup"><span data-stu-id="da4c3-116">Step 4:</span></span>

<span data-ttu-id="da4c3-117">Выберите категорию для типа файлов, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="da4c3-117">Select the category for your file type, as shown in the following screen shot.</span></span>

![Снимок экрана, на котором показана функция перетаскивания.](images/file-assoc/filetypeverifier1.png)

<span data-ttu-id="da4c3-119">Выбор категории определяет набор тестов, которые будут запускаться инструментом.</span><span class="sxs-lookup"><span data-stu-id="da4c3-119">The category selection determines the set of tests that will be run by the tool.</span></span> <span data-ttu-id="da4c3-120">Если тип может находиться в нескольких категориях (например, файл TIF может быть рисунком или документом в зависимости от содержимого), снова запустите средство с каждой соответствующей категорией.</span><span class="sxs-lookup"><span data-stu-id="da4c3-120">If your type could fall under more than one category (for example, a TIF file might be a Picture or a Document depending on the content), run the tool again with each appropriate category.</span></span>

### <a name="step-5"></a><span data-ttu-id="da4c3-121">Шаг 5.</span><span class="sxs-lookup"><span data-stu-id="da4c3-121">Step 5:</span></span>

<span data-ttu-id="da4c3-122">С помощью проводника Windows выберите файл для проверки и перетащите его на целевой объект в поле Проверка типа файла, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="da4c3-122">Using Windows Explorer, locate a file to be tested and use the mouse to drag it to the target in File Type Verifier, as shown in the following screen shot.</span></span>

![снимок экрана, демонстрирующий функцию перетаскивания](images/file-assoc/filetypeverifier2.png)

### <a name="step-6"></a><span data-ttu-id="da4c3-124">Шаг 6.</span><span class="sxs-lookup"><span data-stu-id="da4c3-124">Step 6:</span></span>

<span data-ttu-id="da4c3-125">Дождитесь, пока средство проверки типа файлов пройдет серию тестов.</span><span class="sxs-lookup"><span data-stu-id="da4c3-125">Wait for the File Type Verifier tool to proceed through a series of tests.</span></span> <span data-ttu-id="da4c3-126">Ход выполнения тестирования отображается индикатором выполнения, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="da4c3-126">The progress of the testing is shown by the progress bar, as in the following screen shot.</span></span>

![снимок экрана, отображающий индикатор выполнения](images/file-assoc/filetypeverifier3.png)

### <a name="step-7"></a><span data-ttu-id="da4c3-128">Шаг 7.</span><span class="sxs-lookup"><span data-stu-id="da4c3-128">Step 7:</span></span>

<span data-ttu-id="da4c3-129">Проверьте сводку результатов проверки типов файлов документов, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="da4c3-129">Review the results summary of your Document file type tests, as shown in the following screen shot.</span></span>

![снимок экрана, отображающий сводку результатов](images/file-assoc/filetypeverifier4.png)

### <a name="step-8"></a><span data-ttu-id="da4c3-131">Шаг 8.</span><span class="sxs-lookup"><span data-stu-id="da4c3-131">Step 8:</span></span>

<span data-ttu-id="da4c3-132">Щелкните любой из результатов на странице Сводка, чтобы просмотреть подробный журнал.</span><span class="sxs-lookup"><span data-stu-id="da4c3-132">Click any of the results on the summary page to view the detailed log.</span></span> <span data-ttu-id="da4c3-133">На следующем снимке экрана показан пример журнала для обработчика просмотра.</span><span class="sxs-lookup"><span data-stu-id="da4c3-133">An example log for a preview handler is shown in the following screen shot.</span></span>

![снимок экрана с журналом обработчика просмотра](images/file-assoc/filetypeverifier5.png)

### <a name="step-9"></a><span data-ttu-id="da4c3-135">Шаг 9.</span><span class="sxs-lookup"><span data-stu-id="da4c3-135">Step 9:</span></span>

<span data-ttu-id="da4c3-136">Чтобы сохранить копию файла журнала, щелкните **сохранить файл журнала** в нижней части окна журнала и выберите подходящее расположение для хранения на компьютере.</span><span class="sxs-lookup"><span data-stu-id="da4c3-136">To save a copy of the log file, click **Save Log File** at the bottom of the log display and choose an appropriate location for storing it on your computer.</span></span>

### <a name="step-10"></a><span data-ttu-id="da4c3-137">Шаг 10.</span><span class="sxs-lookup"><span data-stu-id="da4c3-137">Step 10:</span></span>

<span data-ttu-id="da4c3-138">Если сообщается об ошибках, внесите соответствующие изменения в приложение и снова запустите средство, чтобы убедиться, что ошибки больше не отображаются в тестах.</span><span class="sxs-lookup"><span data-stu-id="da4c3-138">If failures are reported, make the appropriate changes in your application and run the tool again to verify that the failures are no longer showing up in the tests.</span></span> <span data-ttu-id="da4c3-139">Если выводятся предупреждения, оцените их и решите, относятся ли они к конкретному типу файлов, и внесите необходимые изменения в приложение.</span><span class="sxs-lookup"><span data-stu-id="da4c3-139">If warnings are reported, evaluate them and decide whether they are relevant for your particular file type and make the appropriate changes to your application as necessary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da4c3-140">См. также</span><span class="sxs-lookup"><span data-stu-id="da4c3-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da4c3-141">Пакет SDK для Windows 7</span><span class="sxs-lookup"><span data-stu-id="da4c3-141">Windows 7 SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
</dt> </dl>

 

 



