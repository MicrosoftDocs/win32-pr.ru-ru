---
title: Использование обратного вызова OnStatus
description: Использование обратного вызова OnStatus
ms.assetid: 598e2d13-709b-42a3-ae06-b8c7d208ca9e
keywords:
- Пакет SDK для формата Windows Media, метод обратного вызова OnStatus
- Windows Media Format SDK, интерфейс Ивмстатускаллбакк
- Метод обратного вызова OnStatus, сведения
- ивмстатускаллбакк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e96b8d7fd75fd8a1d97a56c8b09304c51d0238
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103987174"
---
# <a name="using-the-onstatus-callback"></a><span data-ttu-id="ed6cc-107">Использование обратного вызова OnStatus</span><span class="sxs-lookup"><span data-stu-id="ed6cc-107">Using the OnStatus Callback</span></span>

<span data-ttu-id="ed6cc-108">Метод обратного вызова [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) вызывается несколькими объектами в пакете SDK формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ed6cc-108">The [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method is called by several objects in the Windows Media Format SDK.</span></span> <span data-ttu-id="ed6cc-109">**OnStatus** получает сообщения, представляющие изменения в состоянии операций пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="ed6cc-109">**OnStatus** receives messages that represent changes in the status of SDK operations.</span></span>

<span data-ttu-id="ed6cc-110">Чтобы использовать метод обратного вызова **OnStatus** , необходимо реализовать в приложении класс, наследующий от интерфейса [**ивмстатускаллбакк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) .</span><span class="sxs-lookup"><span data-stu-id="ed6cc-110">To use the **OnStatus** callback method, you must implement a class in your application that inherits from the [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) interface.</span></span> <span data-ttu-id="ed6cc-111">Включите код для вашей версии **OnStatus** в класс.</span><span class="sxs-lookup"><span data-stu-id="ed6cc-111">Include code for your version of **OnStatus** in the class.</span></span> <span data-ttu-id="ed6cc-112">Несколько примеров реализации **OnStatus** можно найти в образцах, поставляемых с этим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="ed6cc-112">Several examples of **OnStatus** implementations can be found in the samples included with this SDK.</span></span> <span data-ttu-id="ed6cc-113">Дополнительные сведения о примерах см. в разделе [примеры приложений](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="ed6cc-113">For more information about the samples, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="ed6cc-114">Необходимо связать реализацию функции обратного вызова состояния с различными объектами пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="ed6cc-114">You must associate your implementation of the status callback with various objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="ed6cc-115">Для каждого объекта существует другой способ выполнения этой ассоциации.</span><span class="sxs-lookup"><span data-stu-id="ed6cc-115">Each object has a different way of making this association.</span></span> <span data-ttu-id="ed6cc-116">Список методов, связывающих определенные объекты, см. на странице справочника по **ивмстатускаллбакк** .</span><span class="sxs-lookup"><span data-stu-id="ed6cc-116">For a list of the methods that associate specific objects, see the **IWMStatusCallback** reference page.</span></span>

<span data-ttu-id="ed6cc-117">Сообщения о состоянии, которые могут быть получены параметром **OnStatus** , определяются в типе перечисления [**\_ состояния ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) .</span><span class="sxs-lookup"><span data-stu-id="ed6cc-117">The status messages that can be received by **OnStatus** are defined in the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type.</span></span>

<span data-ttu-id="ed6cc-118">Вы можете выбрать сообщения для перехвата и игнорировать их.</span><span class="sxs-lookup"><span data-stu-id="ed6cc-118">You can choose which messages to trap and which to ignore.</span></span> <span data-ttu-id="ed6cc-119">Однако для некоторых функций требуется реагирование на некоторые сообщения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="ed6cc-119">However, responding to some status messages is required for certain features.</span></span> <span data-ttu-id="ed6cc-120">Например, при использовании асинхронного модуля чтения метод [**ивмреадер:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) открывает файл асинхронно.</span><span class="sxs-lookup"><span data-stu-id="ed6cc-120">For example, when using the asynchronous reader, the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method opens a file asynchronously.</span></span> <span data-ttu-id="ed6cc-121">Единственный способ определить, когда файл был открыт, — это перехват \_ сообщения МВт Opened.</span><span class="sxs-lookup"><span data-stu-id="ed6cc-121">The only way to tell when the file has been opened is to trap the MWT\_OPENED message.</span></span> <span data-ttu-id="ed6cc-122">Как правило, сообщения, на которые вы отвечаете, являются уведомлениями о завершении асинхронных задач.</span><span class="sxs-lookup"><span data-stu-id="ed6cc-122">Typically, the messages you respond to are notifications of the completion of asynchronous tasks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed6cc-123">См. также</span><span class="sxs-lookup"><span data-stu-id="ed6cc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed6cc-124">**Использование методов обратного вызова**</span><span class="sxs-lookup"><span data-stu-id="ed6cc-124">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




