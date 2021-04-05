---
title: Создание диалогового окна для выбора форматов с ограниченным доступом
description: Создание диалогового окна для выбора форматов с ограниченным доступом
ms.assetid: 486ba928-e06d-4ab0-a642-ba0fe16c8291
keywords:
- Диспетчер аудиосжатия (ACM), создание диалоговых окон
- ACM (диспетчер аудиосжатия), создание диалоговых окон
- Примеры ACM, создание диалоговых окон
- Создание диалоговых окон
- Функция Акмформатчусе
- Диспетчер аудиосжатия (ACM), выбор ограниченных форматов
- ACM (диспетчер аудиосжатия), выбор ограниченных форматов
- Примеры ACM, выбор ограниченных форматов
- выбор форматов с ограниченным доступом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800945f4003c0fbe47d7916e0a1bf707745ff6d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068107"
---
# <a name="producing-a-dialog-box-for-selecting-restricted-formats"></a><span data-ttu-id="30634-112">Создание диалогового окна для выбора форматов с ограниченным доступом</span><span class="sxs-lookup"><span data-stu-id="30634-112">Producing a Dialog Box for Selecting Restricted Formats</span></span>

<span data-ttu-id="30634-113">Может потребоваться использовать диалоговое окно, созданное функцией [**акмформатчусе**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , но ограничить или управлять форматами в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="30634-113">You might want to use the dialog box created by the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, but limit or control the formats in the dialog box.</span></span> <span data-ttu-id="30634-114">Это можно сделать с помощью \_ \_ флага енаблехук акмформатчусе стилеф, чтобы привязать процедуру диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="30634-114">You can do this by using the ACMFORMATCHOOSE\_STYLEF\_ENABLEHOOK flag to hook the dialog procedure.</span></span> <span data-ttu-id="30634-115">Затем приложение может отфильтровать форматы, реагируя на сообщение [**mm \_ ACM \_ форматчусе**](mm-acm-formatchoose.md) в процедуре сообщения для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="30634-115">The application can then filter the formats by responding to the [**MM\_ACM\_FORMATCHOOSE**](mm-acm-formatchoose.md) message in the message procedure for the dialog box.</span></span>

 

 




