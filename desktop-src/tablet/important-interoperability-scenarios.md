---
description: 'Чтобы приложение для планшетных ПК могло эффективно работать с рукописным вводом, это приложение должно иметь следующие возможности:'
ms.assetid: 64a7b773-35c9-42f7-aec4-7fed34fa84d9
title: Важные сценарии взаимодействия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6dca3bcbf52d673131122615fa5a08317dbf10c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647153"
---
# <a name="important-interoperability-scenarios"></a><span data-ttu-id="f040a-103">Важные сценарии взаимодействия</span><span class="sxs-lookup"><span data-stu-id="f040a-103">Important Interoperability Scenarios</span></span>

<span data-ttu-id="f040a-104">Чтобы приложение для планшетных ПК могло эффективно работать с рукописным вводом, это приложение должно иметь следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="f040a-104">For a Tablet PC application to operate with ink effectively, that application should be able to:</span></span>

-   <span data-ttu-id="f040a-105">Сохранение документа в собственном двоичном формате приложения без потери рукописного ввода документа.</span><span class="sxs-lookup"><span data-stu-id="f040a-105">Save a document in the application's native binary format without losing the document's ink.</span></span>
-   <span data-ttu-id="f040a-106">Сохраните документ в любом формате, который приложение обычно поддерживает (например, HTML или RTF) без потери рукописного ввода документа.</span><span class="sxs-lookup"><span data-stu-id="f040a-106">Save a document in any format the application normally supports (for example, HTML or Rich Text Format (RTF)) without losing the document's ink.</span></span>
-   <span data-ttu-id="f040a-107">Копирование рукописного ввода из одного приложения в другое с помощью буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="f040a-107">Copy ink from one application to another by using the Clipboard.</span></span> <span data-ttu-id="f040a-108">Это работает, если другое приложение распознает только конкретный формат, например HTML, RTF или точечный рисунок (BMP).</span><span class="sxs-lookup"><span data-stu-id="f040a-108">This works if the other application only recognizes a specific format, such as HTML, RTF, or bitmap (BMP).</span></span> <span data-ttu-id="f040a-109">Он также работает, распознает ли целевое приложение рукописный ввод.</span><span class="sxs-lookup"><span data-stu-id="f040a-109">It also works whether the destination application recognizes ink.</span></span> <span data-ttu-id="f040a-110">Если он распознает рукописный ввод, конечное приложение может интерпретировать рукописные данные, скопированные как рукописные, а не как изображение.</span><span class="sxs-lookup"><span data-stu-id="f040a-110">If it does recognize ink, the destination application is able to interpret the ink that has been copied as ink and not just as an image.</span></span>
-   <span data-ttu-id="f040a-111">Копирование рукописного ввода вместе с текстом между двумя приложениями, распознающими рукописный ввод, каждый из которых содержит несколько объектов [**рукописного ввода**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f040a-111">Copy ink, along with text, between two applications that recognize ink, each of which has more than one [**Ink**](inkdisp-class.md) object.</span></span> <span data-ttu-id="f040a-112">Для этого требуется HTML, RTF или аналогичный формат.</span><span class="sxs-lookup"><span data-stu-id="f040a-112">This requires HTML, RTF, or a similar format.</span></span>
-   <span data-ttu-id="f040a-113">Копирование рукописного ввода между двумя приложениями, каждый из которых имеет один объект [**рукописного ввода**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f040a-113">Copy ink between two applications, each of which has one [**Ink**](inkdisp-class.md) object.</span></span> <span data-ttu-id="f040a-114">Для этого достаточно формата рукописного ввода (ISF).</span><span class="sxs-lookup"><span data-stu-id="f040a-114">Ink Serialized Format (ISF) is sufficient for this.</span></span>
-   <span data-ttu-id="f040a-115">Копирование рукописного ввода из приложения, имеющего несколько объектов [**рукописного ввода**](inkdisp-class.md) , в приложение, имеющее только один объект **рукописного ввода** .</span><span class="sxs-lookup"><span data-stu-id="f040a-115">Copy ink from an application that has more than one [**Ink**](inkdisp-class.md) object to an application that has only one **Ink** object.</span></span> <span data-ttu-id="f040a-116">В этом случае приложение, имеющее более одного объекта **рукописного ввода** , должно иметь возможность создавать сериализованный формат рукописного ввода (ISF).</span><span class="sxs-lookup"><span data-stu-id="f040a-116">In this case, the application that has more than one **Ink** object must be able to produce Ink Serialized Format (ISF).</span></span>
-   <span data-ttu-id="f040a-117">Копирование рукописного ввода из приложения, имеющего один объект [**рукописного ввода**](inkdisp-class.md) , в приложение, имеющее более одного объекта **рукописного ввода** .</span><span class="sxs-lookup"><span data-stu-id="f040a-117">Copy ink from an application that has one [**Ink**](inkdisp-class.md) object to an application that has more than one **Ink** object.</span></span> <span data-ttu-id="f040a-118">В этом случае приложение, имеющее более одного объекта **рукописного ввода** , должно иметь возможность распознать ISF.</span><span class="sxs-lookup"><span data-stu-id="f040a-118">In this case, the application that has more than one **Ink** object must be able to recognize ISF.</span></span>

 

 



