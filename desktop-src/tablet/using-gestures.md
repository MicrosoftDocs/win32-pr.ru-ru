---
description: Общие сведения об использовании жестов.
ms.assetid: 5bc80086-7acf-4f86-a9fb-a663de489f8b
title: Использование жестов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c267cff446d1bb6d092ba50bde21c1b3e25184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991086"
---
# <a name="using-gestures"></a><span data-ttu-id="91bed-103">Использование жестов</span><span class="sxs-lookup"><span data-stu-id="91bed-103">Using Gestures</span></span>

<span data-ttu-id="91bed-104">Платформа Tablet PC предоставляет средство распознавания жестов Майкрософт для поддержки жестов приложений.</span><span class="sxs-lookup"><span data-stu-id="91bed-104">The Tablet PC platform provides the Microsoft gesture recognizer for supporting application gestures.</span></span> <span data-ttu-id="91bed-105">Список жестов, поддерживаемых распознавателем Microsoft жеста, см. в таблице жестов приложений в перечислении [**ApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="91bed-105">For a list of gestures supported by the Microsoft gesture recognizer, see the table of application gestures in the [**ApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration.</span></span> <span data-ttu-id="91bed-106">Планшетный ПК также поддерживает системные жесты.</span><span class="sxs-lookup"><span data-stu-id="91bed-106">The Tablet PC also supports system gestures.</span></span> <span data-ttu-id="91bed-107">Список системных жестов, поддерживаемых планшетным ПК, см. в таблице системных жестов в перечислении [**системжестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) .</span><span class="sxs-lookup"><span data-stu-id="91bed-107">For a list of system gestures supported by the Tablet PC, see the table of system gestures in the [**SystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration.</span></span>

## <a name="microsoft-gesture-recognizer"></a><span data-ttu-id="91bed-108">Распознаватель жестов Майкрософт</span><span class="sxs-lookup"><span data-stu-id="91bed-108">Microsoft Gesture Recognizer</span></span>

<span data-ttu-id="91bed-109">Средство распознавания жестов Майкрософт можно использовать с помощью свойства [**режиме CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) объекта [**InkCollector**](inkcollector-class.md) , объекта [**InkOverlay**](inkoverlay-class.md) или элемента управления [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="91bed-109">You can employ the Microsoft gesture recognizer by using the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) property of the [**InkCollector**](inkcollector-class.md) object, the [**InkOverlay**](inkoverlay-class.md) object, or the [InkPicture](inkpicture-control-reference.md) control.</span></span> <span data-ttu-id="91bed-110">Если задать для свойства **режиме CollectionMode** смешанный режим (**инканджестуре**) или режим "только жесты" (**жестуреонли**), по умолчанию передает рукописный ввод в средство распознавания жестов Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="91bed-110">Setting the **CollectionMode** property to mixed mode (**InkAndGesture**) or gesture-only mode (**GestureOnly**) passes ink to the Microsoft gesture recognizer by default.</span></span> <span data-ttu-id="91bed-111">Можно применить средство распознавания жестов Майкрософт с элементом управления [InkEdit](inkedit-control-reference.md) , задав для свойства [**инкмоде**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) значение **инканджестуре**.</span><span class="sxs-lookup"><span data-stu-id="91bed-111">You can employ the Microsoft gesture recognizer with the [InkEdit](inkedit-control-reference.md) control by setting the [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) property to **InkAndGesture**.</span></span> <span data-ttu-id="91bed-112">Можно также использовать распознавание жестов с объектом [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) , добавив объект [**GestureRecognizer**](gesturerecognizer-class.md) в одну из его коллекций подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="91bed-112">You can also use gesture recognition with the [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) object by adding a [**GestureRecognizer**](gesturerecognizer-class.md) object to one of its plug-in collections.</span></span>

<span data-ttu-id="91bed-113">Однако если жесты, которые вы хотите использовать, не поддерживаются текущей версией распознавателя Microsoft жеста, вы можете создать свой распознаватель и использовать его совместно с распознавателем жестов Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="91bed-113">However, if the gestures that you want to use are not supported by the current version of the Microsoft gesture recognizer, you can build your own recognizer and use it in conjunction with the Microsoft gesture recognizer.</span></span> <span data-ttu-id="91bed-114">Это обеспечивает полную поддержку жестов в приложении.</span><span class="sxs-lookup"><span data-stu-id="91bed-114">This allows full support for the gestures in your application.</span></span>

<span data-ttu-id="91bed-115">Планшетный ПК использует перо для некоторых или всех входных данных.</span><span class="sxs-lookup"><span data-stu-id="91bed-115">The Tablet PC uses a pen for some or all input.</span></span> <span data-ttu-id="91bed-116">Это позволяет очень легко писать рукописные данные.</span><span class="sxs-lookup"><span data-stu-id="91bed-116">This makes it extremely easy to write ink.</span></span> <span data-ttu-id="91bed-117">Платформа Tablet PC предоставляет архитектуру для ввода с помощью пера, поддерживающего многоуровневую структуру жестов.</span><span class="sxs-lookup"><span data-stu-id="91bed-117">The Tablet PC platform delivers architecture for pen input that supports a tiered structure of gestures.</span></span> <span data-ttu-id="91bed-118">Жесты и сопоставление определяются, чтобы позволить пользователю писать и вызывать дополнительные жесты на новых поверхностях, сохраняя при этом жесты, вызывающие традиционные сообщения мыши других приложений на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="91bed-118">Gestures and mapping are defined to allow the user to write and invoke advanced gestures on new surfaces, while reserving gestures that invoke traditional mouse messages of other Windows-based applications.</span></span>

<span data-ttu-id="91bed-119">Платформа Tablet PC предоставляет два уровня жестов: системные жесты, также известные как системные события, и жесты приложения.</span><span class="sxs-lookup"><span data-stu-id="91bed-119">The Tablet PC platform introduces two levels of gestures: system gestures, also known as system events, and application gestures.</span></span> <span data-ttu-id="91bed-120">Архитектура пера поддерживает как жесты системы, так и приложения.</span><span class="sxs-lookup"><span data-stu-id="91bed-120">The pen architecture supports both system and application gestures.</span></span> <span data-ttu-id="91bed-121">Поддерживаются жесты приложения с одним росчерком и с несколькими обводками.</span><span class="sxs-lookup"><span data-stu-id="91bed-121">Both single-stroke and multiple-stroke application gestures are supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91bed-122">См. также</span><span class="sxs-lookup"><span data-stu-id="91bed-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91bed-123">Жесты приложения</span><span class="sxs-lookup"><span data-stu-id="91bed-123">Application Gestures</span></span>](application-gestures.md)
</dt> <dt>

[<span data-ttu-id="91bed-124">Жесты жестов</span><span class="sxs-lookup"><span data-stu-id="91bed-124">Flicks Gestures</span></span>](flicks-gestures.md)
</dt> <dt>

[<span data-ttu-id="91bed-125">Системные жесты</span><span class="sxs-lookup"><span data-stu-id="91bed-125">System Gestures</span></span>](system-gestures.md)
</dt> </dl>

 

 



