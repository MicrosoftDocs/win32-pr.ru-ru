---
description: Регион обновления определяет часть окна, которая является неактуальной или недопустимой и нуждается в перерисовки.
ms.assetid: 21228620-9491-4e1b-8658-15e9605951f2
title: Регион обновления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e670bac065782a1e09c4d142f964aaea97d4b96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997914"
---
# <a name="the-update-region"></a><span data-ttu-id="14b76-103">Регион обновления</span><span class="sxs-lookup"><span data-stu-id="14b76-103">The Update Region</span></span>

<span data-ttu-id="14b76-104">*Регион обновления* определяет часть окна, которая является неактуальной или недопустимой и нуждается в перерисовки.</span><span class="sxs-lookup"><span data-stu-id="14b76-104">The *update region* identifies the portion of a window that is out-of-date or invalid and in need of redrawing.</span></span> <span data-ttu-id="14b76-105">В системе используется регион обновления для создания сообщений [**WM \_ Paint**](wm-paint.md) для приложений и для минимального времени, затрачиваемого на обновление содержимого окон.</span><span class="sxs-lookup"><span data-stu-id="14b76-105">The system uses the update region to generate [**WM\_PAINT**](wm-paint.md) messages for applications and to minimize the time applications spend bringing the contents of their windows up to date.</span></span> <span data-ttu-id="14b76-106">Система добавляет в область обновления только недопустимую часть окна, что требует прорисовки только этой части.</span><span class="sxs-lookup"><span data-stu-id="14b76-106">The system adds only the invalid portion of the window to the update region, requiring only that portion to be drawn.</span></span>

<span data-ttu-id="14b76-107">Когда система определяет, что окно нуждается в обновлении, оно устанавливает в качестве размера области обновления недействительную часть окна.</span><span class="sxs-lookup"><span data-stu-id="14b76-107">When the system determines that a window needs updating, it sets the dimensions of the update region to the invalid portion of the window.</span></span> <span data-ttu-id="14b76-108">Установка региона обновления не приводит к немедленному выводе приложения.</span><span class="sxs-lookup"><span data-stu-id="14b76-108">Setting the update region does not immediately cause the application to draw.</span></span> <span data-ttu-id="14b76-109">Вместо этого приложение продолжит получать сообщения из очереди сообщений приложения, пока не останется сообщений.</span><span class="sxs-lookup"><span data-stu-id="14b76-109">Instead, the application continues retrieving messages from the application message queue until no messages remain.</span></span> <span data-ttu-id="14b76-110">Затем система проверяет регион обновления, и если область не пуста (не РАВНа NULL), она отправляет сообщение [**WM \_ Paint**](wm-paint.md) в процедуру окна.</span><span class="sxs-lookup"><span data-stu-id="14b76-110">The system then checks the update region, and if the region is not empty (non-NULL), it sends a [**WM\_PAINT**](wm-paint.md) message to the window procedure.</span></span>

<span data-ttu-id="14b76-111">Приложение может использовать регион обновления для создания сообщений [**WM \_ Paint**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="14b76-111">An application can use the update region to generate its [**WM\_PAINT**](wm-paint.md) messages.</span></span> <span data-ttu-id="14b76-112">Например, приложение, которое загружает данные из открытых файлов, обычно задает область обновления при загрузке, чтобы новые данные рисулись во время обработки следующего сообщения **WM \_ Paint** .</span><span class="sxs-lookup"><span data-stu-id="14b76-112">For example, an application that loads data from open files typically sets the update region while loading so that new data is drawn during processing of the next **WM\_PAINT** message.</span></span> <span data-ttu-id="14b76-113">В общем случае приложение не должно рисовать во время изменения данных, но направлять все операции рисования с помощью сообщения **WM \_ Paint** .</span><span class="sxs-lookup"><span data-stu-id="14b76-113">In general, an application should not draw at the time its data changes, but route all drawing operations through the **WM\_PAINT** message.</span></span>

 

 



