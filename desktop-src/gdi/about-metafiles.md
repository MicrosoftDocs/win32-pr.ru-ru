---
description: Внутри метафайл представляет собой массив структур переменной длины, называемый записями метафайлов.
ms.assetid: 222f9b8b-d759-49f9-a3ea-ac59f85263b8
title: О метафайлах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdba8b3c0a13c6c5799563b05e189829a0734427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811345"
---
# <a name="about-metafiles"></a><span data-ttu-id="3a387-103">О метафайлах</span><span class="sxs-lookup"><span data-stu-id="3a387-103">About Metafiles</span></span>

<span data-ttu-id="3a387-104">Внутри метафайл представляет собой массив структур переменной длины, называемый *записями метафайлов*.</span><span class="sxs-lookup"><span data-stu-id="3a387-104">Internally, a metafile is an array of variable-length structures called *metafile records*.</span></span> <span data-ttu-id="3a387-105">Первые записи в метафайле указывают общие сведения, такие как разрешение устройства, на котором было создано изображение, размеры изображения и т. д.</span><span class="sxs-lookup"><span data-stu-id="3a387-105">The first records in the metafile specify general information such as the resolution of the device on which the picture was created, the dimensions of the picture, and so on.</span></span> <span data-ttu-id="3a387-106">Остальные записи, которые составляют основную часть любого метафайла, соответствуют функциям интерфейса графических устройств (GDI), необходимым для рисования изображения.</span><span class="sxs-lookup"><span data-stu-id="3a387-106">The remaining records, which constitute the bulk of any metafile, correspond to the graphics device interface (GDI) functions required to draw the picture.</span></span> <span data-ttu-id="3a387-107">Эти записи хранятся в метафайле после создания специального контекста устройства для метафайлов.</span><span class="sxs-lookup"><span data-stu-id="3a387-107">These records are stored in the metafile after a special metafile device context is created.</span></span> <span data-ttu-id="3a387-108">Этот контекст устройства метафайла используется для всех операций рисования, необходимых для создания изображения.</span><span class="sxs-lookup"><span data-stu-id="3a387-108">This metafile device context is then used for all drawing operations required to create the picture.</span></span> <span data-ttu-id="3a387-109">Когда система обрабатывает функцию GDI, связанную с КОНТРОЛЛЕРом метафайла, она преобразует функцию в соответствующие данные и сохраняет эти данные в записи, присоединенной к метафайлу.</span><span class="sxs-lookup"><span data-stu-id="3a387-109">When the system processes a GDI function associated with a metafile DC, it converts the function into the appropriate data and stores this data in a record appended to the metafile.</span></span>

<span data-ttu-id="3a387-110">После завершения изображения и сохранения последней записи в метафайл можно передать метафайл в другое приложение, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3a387-110">After a picture is complete and the last record is stored in the metafile, you can pass the metafile to another application by:</span></span>

-   <span data-ttu-id="3a387-111">Использование буфера обмена</span><span class="sxs-lookup"><span data-stu-id="3a387-111">Using the clipboard</span></span>
-   <span data-ttu-id="3a387-112">Внедрение в другой файл</span><span class="sxs-lookup"><span data-stu-id="3a387-112">Embedding it within another file</span></span>
-   <span data-ttu-id="3a387-113">Сохранение на диске</span><span class="sxs-lookup"><span data-stu-id="3a387-113">Storing it on disk</span></span>
-   <span data-ttu-id="3a387-114">Многократное воспроизведение</span><span class="sxs-lookup"><span data-stu-id="3a387-114">Playing it repeatedly</span></span>

<span data-ttu-id="3a387-115">Метафайл *воспроизводится* , когда его записи преобразуются в команды устройства и обрабатываются соответствующим устройством.</span><span class="sxs-lookup"><span data-stu-id="3a387-115">A metafile is *played* when its records are converted to device commands and processed by the appropriate device.</span></span>

<span data-ttu-id="3a387-116">Существует два типа метафайлов:</span><span class="sxs-lookup"><span data-stu-id="3a387-116">There are two types of metafiles:</span></span>

-   [<span data-ttu-id="3a387-117">Метафайлы с улучшенными форматами</span><span class="sxs-lookup"><span data-stu-id="3a387-117">Enhanced-format metafiles</span></span>](enhanced-format-metafiles.md)
-   [<span data-ttu-id="3a387-118">Метафайлы в формате Windows</span><span class="sxs-lookup"><span data-stu-id="3a387-118">Windows-format metafiles</span></span>](windows-format-metafiles.md)

 

 



