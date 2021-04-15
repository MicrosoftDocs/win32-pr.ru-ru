---
description: Пользовательский распознаватель жестов можно использовать независимо или в дополнение к GestureRecognizer. Создайте пользовательский распознаватель жестов в качестве Истилуссинкплугин, создайте Кустомстилусдата и включите подключаемый модуль в тот же Стилуссинкплугинколлектион, что и GestureRecognizer. В Истилуссинкплугин объедините уведомления жестов от распознавателей в уведомления, которые будут использоваться приложением.
ms.assetid: ed4e8f56-9137-47fd-a8f9-17eebfd06e97
title: Использование пользовательского распознавателя жестов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 376f567680cfe7e862f280d1b8e8dc35a2017316
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701453"
---
# <a name="using-a-custom-gesture-recognizer"></a><span data-ttu-id="bd144-104">Использование пользовательского распознавателя жестов</span><span class="sxs-lookup"><span data-stu-id="bd144-104">Using a Custom Gesture Recognizer</span></span>

<span data-ttu-id="bd144-105">Пользовательский распознаватель жестов можно использовать независимо или в дополнение к [**GestureRecognizer**](gesturerecognizer-class.md).</span><span class="sxs-lookup"><span data-stu-id="bd144-105">You can use a custom gesture recognizer independently, or in addition to the [**GestureRecognizer**](gesturerecognizer-class.md).</span></span>

<span data-ttu-id="bd144-106">Создайте пользовательский распознаватель жестов как [**истилуссинкплугин**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin), создайте [кустомстилусдата](/previous-versions/ms575208(v=vs.100))и включите подключаемый модуль в тот же [стилуссинкплугинколлектион](/previous-versions/ms824788(v=msdn.10)) , что и [**GestureRecognizer**](gesturerecognizer-class.md).</span><span class="sxs-lookup"><span data-stu-id="bd144-106">Create your custom gesture recognizer as an [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin), have it create [CustomStylusData](/previous-versions/ms575208(v=vs.100)), and include the plug-in in the same [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) as the [**GestureRecognizer**](gesturerecognizer-class.md).</span></span> <span data-ttu-id="bd144-107">В **истилуссинкплугин** объедините уведомления жестов от распознавателей в уведомления, которые будут использоваться приложением.</span><span class="sxs-lookup"><span data-stu-id="bd144-107">In the **IStylusSyncPlugin**, combine gesture notifications from both recognizers into notifications to be consumed by an application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd144-108">См. также</span><span class="sxs-lookup"><span data-stu-id="bd144-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd144-109">Доступ к вводу пера и управление им</span><span class="sxs-lookup"><span data-stu-id="bd144-109">Accessing and Manipulating Stylus Input</span></span>](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
