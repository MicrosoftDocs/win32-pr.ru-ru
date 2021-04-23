---
title: Преобразование цветового пространства
description: Преобразование цветового пространства
ms.assetid: f5f1ec99-b3b9-4420-bf64-3872d9bbe650
keywords:
- Windows Media Format SDK, преобразование цветового пространства
- Расширенный формат систем (ASF), преобразование цветового пространства
- ASF (Расширенный системный формат), преобразование цветового пространства
- преобразование цветового пространства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbc284995cbc72aee148e12977dad9f4476b29c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253263"
---
# <a name="color-space-conversion"></a><span data-ttu-id="861b4-107">Преобразование цветового пространства</span><span class="sxs-lookup"><span data-stu-id="861b4-107">Color Space Conversion</span></span>

<span data-ttu-id="861b4-108">Часто существует разница между глубиной цвета сжатого видеоформата в профиле и входным форматом.</span><span class="sxs-lookup"><span data-stu-id="861b4-108">There is often a difference between the color depth of the compressed video format in the profile and the input format.</span></span> <span data-ttu-id="861b4-109">В этом случае исходное видео должно быть преобразовано, чтобы соответствовать цветовому пространству назначения.</span><span class="sxs-lookup"><span data-stu-id="861b4-109">When this happens, the source video must be converted to conform to the color space of the destination.</span></span> <span data-ttu-id="861b4-110">Модуль записи обрабатывает этот процесс, с внутренним преобразователем цветового пространства.</span><span class="sxs-lookup"><span data-stu-id="861b4-110">The writer handles this process, communicating with an internal color-space converter.</span></span>

<span data-ttu-id="861b4-111">Читатель также взаимодействует с преобразователем цветового пространства для согласования любых различий между сжатым форматом и выходным форматом.</span><span class="sxs-lookup"><span data-stu-id="861b4-111">The reader also communicates with the color-space converter to reconcile any difference between the compressed format and the output format.</span></span>

<span data-ttu-id="861b4-112">Как и при выполнении всех преобразований данных, преобразование между глубиной цвета может уменьшить качество выходных данных.</span><span class="sxs-lookup"><span data-stu-id="861b4-112">As with all transforms performed on data, converting between color depths can reduce the quality of the output.</span></span> <span data-ttu-id="861b4-113">По возможности следует использовать форматы входных и выходных данных с той же глубиной цвета, что и в сжатом формате.</span><span class="sxs-lookup"><span data-stu-id="861b4-113">When possible, you should use input and output formats with the same color depth as the compressed format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="861b4-114">См. также</span><span class="sxs-lookup"><span data-stu-id="861b4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="861b4-115">**Функции записи файлов**</span><span class="sxs-lookup"><span data-stu-id="861b4-115">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="861b4-116">**Работа с входными данными**</span><span class="sxs-lookup"><span data-stu-id="861b4-116">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="861b4-117">**Работа с выходами**</span><span class="sxs-lookup"><span data-stu-id="861b4-117">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




