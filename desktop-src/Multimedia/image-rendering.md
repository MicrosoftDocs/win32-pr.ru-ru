---
title: Рендеринг изображений
description: Рендеринг изображений
ms.assetid: de87f288-f1bd-471c-b594-e9dbde3cff0a
keywords:
- Дравдиб, отрисовка изображения
- Дравдиб, рисование DIB
- Функция Дравдибдрав
- Функция Дравдибжетбуффер
- Функция Дравдибупдате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e0d3f4d770a3acc290273b14ec14ff4b6efa30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068544"
---
# <a name="image-rendering"></a><span data-ttu-id="083c2-108">Рендеринг изображений</span><span class="sxs-lookup"><span data-stu-id="083c2-108">Image Rendering</span></span>

<span data-ttu-id="083c2-109">После вызова [**дравдибопен**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) для создания дравдиб DC (см. [дравдиб Operations](drawdib-operations.md)) можно нарисовать изображение DIB на экране с помощью функции [**дравдибдрав**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) .</span><span class="sxs-lookup"><span data-stu-id="083c2-109">After you call [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) to create a DrawDib DC (see [DrawDib Operations](drawdib-operations.md)), you can draw a DIB to the screen by using the [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) function.</span></span> <span data-ttu-id="083c2-110">**Дравдибдрав** отменяет цветные точечные рисунки при отображении их с помощью 8-разрядных видеоадаптеров.</span><span class="sxs-lookup"><span data-stu-id="083c2-110">**DrawDibDraw** dithers true-color bitmaps when displaying them with 8-bit display adapters.</span></span>

<span data-ttu-id="083c2-111">[**Дравдибдрав**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) также поддерживает прозрачное воспроизведение видео при отображении сжатых растровых изображений.</span><span class="sxs-lookup"><span data-stu-id="083c2-111">[**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) also supports video compressors transparently when displaying compressed bitmaps.</span></span> <span data-ttu-id="083c2-112">Доступ к буферу, содержащему распакованное изображение, можно получить с помощью функции [**дравдибжетбуффер**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) .</span><span class="sxs-lookup"><span data-stu-id="083c2-112">You can access the buffer that contains the decompressed image by using the [**DrawDibGetBuffer**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) function.</span></span> <span data-ttu-id="083c2-113">**Дравдибжетбуффер** возвращает **значение NULL** при прорисовке несжатого точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="083c2-113">**DrawDibGetBuffer** returns **NULL** when drawing an uncompressed bitmap.</span></span> <span data-ttu-id="083c2-114">Необходимо подготовить приложение к обработке сжатых и несжатых точечных рисунков.</span><span class="sxs-lookup"><span data-stu-id="083c2-114">You should prepare your application to handle compressed and uncompressed bitmaps.</span></span>

<span data-ttu-id="083c2-115">Вы можете обновить изображение или часть изображения, отображаемого приложением, с помощью макроса [**дравдибупдате**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) .</span><span class="sxs-lookup"><span data-stu-id="083c2-115">You can refresh an image or a portion of an image displayed by your application by using the [**DrawDibUpdate**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) macro.</span></span>

## <a name="related-topics"></a><span data-ttu-id="083c2-116">См. также</span><span class="sxs-lookup"><span data-stu-id="083c2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="083c2-117">О функциях Дравдиб</span><span class="sxs-lookup"><span data-stu-id="083c2-117">About the DrawDib Functions</span></span>](about-the-drawdib-functions.md)
</dt> </dl>

 

 




