---
description: Приложение с поддержкой рукописного ввода взаимодействует с системой распознавания через интерфейсы API платформы Tablet PC.
ms.assetid: 0ea6881f-d2d7-4646-9c41-53d1c03ea55b
title: Архитектура API распознавания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72838b77e11092cacd4adb998c669167940ecad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571728"
---
# <a name="recognition-api-architecture"></a><span data-ttu-id="b240f-103">Архитектура API распознавания</span><span class="sxs-lookup"><span data-stu-id="b240f-103">Recognition API Architecture</span></span>

<span data-ttu-id="b240f-104">Приложение с поддержкой рукописного ввода взаимодействует с системой распознавания через интерфейсы API платформы Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="b240f-104">An ink-enabled application communicates with the recognition system through the Tablet PC Platform APIs.</span></span> <span data-ttu-id="b240f-105">Для этого в приложениях используется объект [**иинкрекогнизер**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) .</span><span class="sxs-lookup"><span data-stu-id="b240f-105">Applications use the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object to accomplish this.</span></span> <span data-ttu-id="b240f-106">Платформа Tablet PC взаимодействует с распознавателем с помощью интерфейсов в стиле C, описанных в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="b240f-106">The Tablet PC Platform interacts with your recognizer by using the C-style interfaces that are documented in this section.</span></span> <span data-ttu-id="b240f-107">На следующем рисунке область внутри пунктирной линии показывает, что описано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="b240f-107">In the following illustration, the area inside the dashed line shows what is documented in this section.</span></span>

![Иллюстрация архитектуры распознавания с выделенным распознавателем](images/96ee7367-7b8a-4794-99c1-bcac9daed645.gif)

<span data-ttu-id="b240f-109">Пользовательский распознаватель должен включать в себя краткое руководство. h (устанавливается по умолчанию в C: \\ Program Files \\ Microsoft Tablet PC Platform SDK \\ include).</span><span class="sxs-lookup"><span data-stu-id="b240f-109">A custom recognizer must include Recapis.h (installed by default in C:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include).</span></span> <span data-ttu-id="b240f-110">Если не указано иное, Библиотека динамической компоновки (DLL) должна экспортировать все функции API, даже если вы решили, чтобы некоторые из них возвращали E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="b240f-110">Except where noted, your dynamic-link library (DLL) must export all of the API functions, even if you choose to have some of them return E\_NOTIMPL.</span></span>

<span data-ttu-id="b240f-111">При отсутствии каких-либо обстоятельств ваш распознаватель будет вызываться непосредственно приложением с поддержкой рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="b240f-111">Under no circumstances will your recognizer be called directly by an ink-enabled application.</span></span> <span data-ttu-id="b240f-112">Вместо этого приложения будут вызывать API автоматизации или управляемые API для получения результатов от распознавателя.</span><span class="sxs-lookup"><span data-stu-id="b240f-112">Instead, applications will call either the Automation APIs or the Managed APIs to get results from your recognizer.</span></span>

 

 



