---
title: Диспетчер документов
description: Диспетчер документов
ms.assetid: e30087b6-524a-481e-845d-0348bac3830a
keywords:
- Платформа текстовых служб (TSF), диспетчер документов
- TSF (платформа текстовых служб), диспетчер документов
- текстовые службы, диспетчер документов
- Приложения с поддержкой TSF, диспетчер документов
- Диспетчер документов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2182782218ad6a8aa0a70f296f639560307249
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774450"
---
# <a name="document-manager"></a><span data-ttu-id="96f29-108">Диспетчер документов</span><span class="sxs-lookup"><span data-stu-id="96f29-108">Document Manager</span></span>

## <a name="applications"></a><span data-ttu-id="96f29-109">Приложения</span><span class="sxs-lookup"><span data-stu-id="96f29-109">Applications</span></span>

<span data-ttu-id="96f29-110">Чтобы создать объект диспетчера документов, приложение вызывает [ITfThreadMgr:: креатедокументмгр](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr).</span><span class="sxs-lookup"><span data-stu-id="96f29-110">To create a document manager object an application calls [ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr).</span></span> <span data-ttu-id="96f29-111">Приложение создает отдельный объект диспетчера документов для каждого отдельного документа, который обслуживает приложение.</span><span class="sxs-lookup"><span data-stu-id="96f29-111">The application creates a separate document manager object for each individual document that the application maintains.</span></span> <span data-ttu-id="96f29-112">Приложение использует диспетчер документов для создания контекстов редактирования, добавления контекста в стек контекста и удаления контекста из стека контекста.</span><span class="sxs-lookup"><span data-stu-id="96f29-112">The application uses the document manager to create edit contexts, add a context to the context stack and remove a context from the context stack.</span></span>

## <a name="text-services"></a><span data-ttu-id="96f29-113">Текстовые службы</span><span class="sxs-lookup"><span data-stu-id="96f29-113">Text Services</span></span>

<span data-ttu-id="96f29-114">Служба текстового объекта никогда не создает объект диспетчера документов.</span><span class="sxs-lookup"><span data-stu-id="96f29-114">A text service never creates a document manager object.</span></span> <span data-ttu-id="96f29-115">Вместо этого служба текстового объекта получает текущий активный объект диспетчера документов путем вызова [ITfThreadMgr::](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)GetObject.</span><span class="sxs-lookup"><span data-stu-id="96f29-115">Instead, the text service obtains the currently active document manager object by calling [ITfThreadMgr::GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus).</span></span> <span data-ttu-id="96f29-116">Служба текстового ввода использует диспетчер документов для получения контекста в верхней части стека.</span><span class="sxs-lookup"><span data-stu-id="96f29-116">A text service uses the document manager to obtain the context at the top of the stack.</span></span>

<span data-ttu-id="96f29-117">Служба текстового ввода также может использовать диспетчер документов для создания собственного контекста и добавления и удаления из стека контекста.</span><span class="sxs-lookup"><span data-stu-id="96f29-117">A text service can also use the document manager to create its own context and add and remove it from the context stack.</span></span> <span data-ttu-id="96f29-118">Обычно это делается, когда текстовая служба должна отображать некоторый модальный пользовательский интерфейс, например, когда отображается список слов, позволяющий пользователю выбрать слово.</span><span class="sxs-lookup"><span data-stu-id="96f29-118">This is normally done when the text service must display some modal user interface, such as when a list of words is displayed to enable the user to select a word.</span></span> <span data-ttu-id="96f29-119">При отображении списка служба текста помещает собственный контекст в стек.</span><span class="sxs-lookup"><span data-stu-id="96f29-119">When the list is displayed, the text service places its own context on the stack.</span></span> <span data-ttu-id="96f29-120">Когда список слов закрывается, служба текстового ввода удаляет его контекст из стека.</span><span class="sxs-lookup"><span data-stu-id="96f29-120">When the word list is dismissed, the text service removes its context from the stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96f29-121">См. также</span><span class="sxs-lookup"><span data-stu-id="96f29-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96f29-122">ITfDocumentMgr</span><span class="sxs-lookup"><span data-stu-id="96f29-122">ITfDocumentMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[<span data-ttu-id="96f29-123">ITfThreadMgr:: Креатедокументмгр</span><span class="sxs-lookup"><span data-stu-id="96f29-123">ITfThreadMgr::CreateDocumentMgr</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr)
</dt> <dt>

[<span data-ttu-id="96f29-124">ITfThreadMgr:: Focus</span><span class="sxs-lookup"><span data-stu-id="96f29-124">ITfThreadMgr::GetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> </dl>

 

 




