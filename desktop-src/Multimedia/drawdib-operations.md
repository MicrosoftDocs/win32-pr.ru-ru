---
title: Операции Дравдиб
description: Операции Дравдиб
ms.assetid: 785ad42e-0c77-44a4-b4ef-be2a0ee2b563
keywords:
- Дравдиб, о программе
- Дравдиб, доступ
- Дравдиб, открытие
- Дравдиб, операции
- Дравдиб, контекст устройства (DC)
- Контроллер домена (контекст устройства)
- Функция Дравдибопен
- Функция Дравдибклосе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc366287cdf481d70ef03aa82df5ea248673280b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487037"
---
# <a name="drawdib-operations"></a><span data-ttu-id="8c330-111">Операции Дравдиб</span><span class="sxs-lookup"><span data-stu-id="8c330-111">DrawDib Operations</span></span>

<span data-ttu-id="8c330-112">Доступ ко всей группе функций Дравдиб можно получить с помощью функции [**дравдибопен**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) .</span><span class="sxs-lookup"><span data-stu-id="8c330-112">You can access the entire group of DrawDib functions by using the [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) function.</span></span> <span data-ttu-id="8c330-113">Эта функция загружает библиотеку динамической компоновки (DLL), выделяет ресурсы памяти, создает контекст устройства Дравдиб (DC) и ведет подсчет ссылок на количество инициализированных контроллеров домена.</span><span class="sxs-lookup"><span data-stu-id="8c330-113">This function loads the dynamic-link library (DLL), allocates memory resources, creates a DrawDib device context (DC), and maintains a reference count of the number of DCs that are initialized.</span></span> <span data-ttu-id="8c330-114">**Дравдибопен** также возвращает маркер нового контроллера домена, который используется с другими функциями дравдиб.</span><span class="sxs-lookup"><span data-stu-id="8c330-114">**DrawDibOpen** also returns a handle of the new DC that you use with the other DrawDib functions.</span></span>

<span data-ttu-id="8c330-115">Вы можете освободить контроллер домена Дравдиб, когда вы завершите его использование с помощью функции [**дравдибклосе**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) .</span><span class="sxs-lookup"><span data-stu-id="8c330-115">You can release a DrawDib DC when you finish using it by using the [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) function.</span></span> <span data-ttu-id="8c330-116">**Дравдибклосе** также уменьшает число ссылок приложений, обращающихся к библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="8c330-116">**DrawDibClose** also decrements the reference count of the applications accessing the DLL.</span></span> <span data-ttu-id="8c330-117">Вызов **дравдибклосе** должен быть последней функцией дравдиб в приложении.</span><span class="sxs-lookup"><span data-stu-id="8c330-117">The call to **DrawDibClose** should be the last DrawDib function in your application.</span></span>

<span data-ttu-id="8c330-118">Вы можете создать столько контроллеров Дравдиб, сколько нужно.</span><span class="sxs-lookup"><span data-stu-id="8c330-118">You can create as many DrawDib DCs as you want.</span></span> <span data-ttu-id="8c330-119">Можно использовать несколько контроллеров домена Дравдиб для одновременного рисования нескольких растровых изображений.</span><span class="sxs-lookup"><span data-stu-id="8c330-119">You can use multiple DrawDib DCs to draw several bitmaps simultaneously.</span></span> <span data-ttu-id="8c330-120">Вы также можете создать несколько контроллеров домена Дравдиб с уникальными характеристиками, чтобы приложение могла выбрать и использовать контроллер домена с наиболее подходящими параметрами.</span><span class="sxs-lookup"><span data-stu-id="8c330-120">You can also create multiple DrawDib DCs, each with unique characteristics, so your application can choose and then use the DC with the most appropriate settings.</span></span> <span data-ttu-id="8c330-121">Например, можно создать два Дравдиб DCs в приложении: одно, которое отображает изображение при нормальном разрешении, а другое — увеличенную часть изображения.</span><span class="sxs-lookup"><span data-stu-id="8c330-121">For example, you can create two DrawDib DCs in an application: one that displays an image at its normal resolution, and the other that displays an enlarged portion of the image.</span></span>

<span data-ttu-id="8c330-122">Для эффективной работы Дравдиб функциям требуются сведения о видеоадаптере и его драйвере.</span><span class="sxs-lookup"><span data-stu-id="8c330-122">To run efficiently, DrawDib functions require information about the display adapter and its driver.</span></span> <span data-ttu-id="8c330-123">Профиль экрана получается путем запуска ряда тестов для видеоадаптера при первой попытке доступа к библиотеке DLL, содержащей функции Дравдиб.</span><span class="sxs-lookup"><span data-stu-id="8c330-123">The display profile is obtained by running a series of tests on the display adapter the first time the DLL containing the DrawDib functions is accessed.</span></span> <span data-ttu-id="8c330-124">Функции Дравдиб используют эти сведения для всех приложений.</span><span class="sxs-lookup"><span data-stu-id="8c330-124">The DrawDib functions use this information for all applications.</span></span> <span data-ttu-id="8c330-125">Эти тесты можно повторить при необходимости с помощью функции [**дравдибпрофиледисплай**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay) .</span><span class="sxs-lookup"><span data-stu-id="8c330-125">You can repeat these tests when necessary by using the [**DrawDibProfileDisplay**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay) function.</span></span>

> [!Note]  
> <span data-ttu-id="8c330-126">Извлечение и сохранение профиля дисплея обычно выполняется один раз.</span><span class="sxs-lookup"><span data-stu-id="8c330-126">Retrieving and storing the display profile is typically a one-time occurrence.</span></span> <span data-ttu-id="8c330-127">Однако если данные профиля удалены или в системе установлен другой драйвер экрана, Дравдиб повторно выполняет тесты.</span><span class="sxs-lookup"><span data-stu-id="8c330-127">If, however, the profile information is deleted or another display driver is installed in the system, DrawDib reruns the tests.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8c330-128">См. также</span><span class="sxs-lookup"><span data-stu-id="8c330-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c330-129">О функциях Дравдиб</span><span class="sxs-lookup"><span data-stu-id="8c330-129">About the DrawDib Functions</span></span>](about-the-drawdib-functions.md)
</dt> </dl>

 

 




