---
description: Чтобы изменить изображение, хранящееся в расширенном метафайле, приложение должно выполнить задачи, описанные в следующей процедуре.
ms.assetid: 19d9c523-cff8-47e1-bbf2-16d8991dac3b
title: Редактирование расширенного метафайла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c86dc9cc609d616bf82ae3f0a13d8d63e827e3eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155630"
---
# <a name="editing-an-enhanced-metafile"></a><span data-ttu-id="4a4c7-103">Редактирование расширенного метафайла</span><span class="sxs-lookup"><span data-stu-id="4a4c7-103">Editing an Enhanced Metafile</span></span>

<span data-ttu-id="4a4c7-104">Чтобы изменить изображение, хранящееся в расширенном метафайле, приложение должно выполнить задачи, описанные в следующей процедуре.</span><span class="sxs-lookup"><span data-stu-id="4a4c7-104">To edit a picture stored in an enhanced metafile, an application must perform the tasks described in the following procedure.</span></span>

<span data-ttu-id="4a4c7-105">**Изменение изображения, хранящегося в расширенном метафайле**</span><span class="sxs-lookup"><span data-stu-id="4a4c7-105">**To edit a picture stored in an enhanced metafile**</span></span>

1.  <span data-ttu-id="4a4c7-106">Используйте проверку попадания для захвата координат курсора и получения позиции объекта (линии, дуги, прямоугольника, эллипса, многоугольника или неравномерные фигуры), которую пользователь хочет изменить.</span><span class="sxs-lookup"><span data-stu-id="4a4c7-106">Use hit-testing to capture the cursor coordinates and retrieve the position of the object (line, arc, rectangle, ellipse, polygon, or irregular shape) that the user wants to alter.</span></span>
2.  <span data-ttu-id="4a4c7-107">Преобразуйте эти координаты в логические (или в мир) единицы.</span><span class="sxs-lookup"><span data-stu-id="4a4c7-107">Convert these coordinates to logical (or world) units.</span></span>
3.  <span data-ttu-id="4a4c7-108">Вызовите функцию [**енуменхметафиле**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) и изучите каждую запись метафайла.</span><span class="sxs-lookup"><span data-stu-id="4a4c7-108">Call the [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) function and examine each metafile record.</span></span>
4.  <span data-ttu-id="4a4c7-109">Определить, соответствует ли заданная запись функции рисования GDI.</span><span class="sxs-lookup"><span data-stu-id="4a4c7-109">Determine whether a given record corresponds to a GDI drawing function.</span></span>
5.  <span data-ttu-id="4a4c7-110">Если это так, определите, соответствуют ли координаты, хранящиеся в записи, с линией, дугой, эллипс или другим графическим элементом, пересекающим координаты, заданные пользователем.</span><span class="sxs-lookup"><span data-stu-id="4a4c7-110">If it does, determine whether the coordinates stored in the record correspond to the line, arc, ellipse, or other graphics element that intersects the coordinates specified by the user.</span></span>
6.  <span data-ttu-id="4a4c7-111">При поиске записи, которая соответствует выходным данным, которые пользователь хочет изменить, удалите объект на экране, соответствующий исходной записи.</span><span class="sxs-lookup"><span data-stu-id="4a4c7-111">Upon finding the record that corresponds to the output that the user wants to alter, erase the object on the screen that corresponds to the original record.</span></span>
7.  <span data-ttu-id="4a4c7-112">Удалите соответствующую запись из метафайла, сохранив указатель в его расположении.</span><span class="sxs-lookup"><span data-stu-id="4a4c7-112">Delete the corresponding record from the metafile, saving a pointer to its location.</span></span>
8.  <span data-ttu-id="4a4c7-113">Разрешение пользователю перерисовки или замены объекта.</span><span class="sxs-lookup"><span data-stu-id="4a4c7-113">Permit the user to redraw or replace the object.</span></span>
9.  <span data-ttu-id="4a4c7-114">Преобразуйте функции GDI, используемые для рисования нового объекта, в одну или несколько записей расширенных метафайлов.</span><span class="sxs-lookup"><span data-stu-id="4a4c7-114">Convert the GDI functions used to draw the new object into one or more enhanced-metafile records.</span></span>
10. <span data-ttu-id="4a4c7-115">Храните эти записи в расширенном метафайле.</span><span class="sxs-lookup"><span data-stu-id="4a4c7-115">Store these records in the enhanced metafile.</span></span>

 

 



