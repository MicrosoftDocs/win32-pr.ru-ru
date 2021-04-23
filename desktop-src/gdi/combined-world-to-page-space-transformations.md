---
description: Пять преобразований из Интернета в страницу можно объединить в одну матрицу размером 3 на 3.
ms.assetid: d17ba826-8e8d-4121-8afd-0f256121b54c
title: Объединение преобразований «из Интернета в мир»
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b770ef614fe1538a528de640cacc5ad54b28c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985025"
---
# <a name="combined-world-to-page-space-transformations"></a><span data-ttu-id="c61a1-103">Объединение преобразований «из Интернета в мир»</span><span class="sxs-lookup"><span data-stu-id="c61a1-103">Combined World-to-Page Space Transformations</span></span>

<span data-ttu-id="c61a1-104">Пять преобразований из Интернета в страницу можно объединить в одну матрицу размером 3 на 3.</span><span class="sxs-lookup"><span data-stu-id="c61a1-104">The five world-to-page transformations can be combined into a single 3-by-3 matrix.</span></span> <span data-ttu-id="c61a1-105">Функцию [**комбинетрансформ**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform) можно использовать для объединения двух мировых пространств в преобразования страничного пространства.</span><span class="sxs-lookup"><span data-stu-id="c61a1-105">The [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform) function can be used to combine two world-space to page-space transformations.</span></span> <span data-ttu-id="c61a1-106">Объединенные преобразования можно использовать для изменения выходных данных, связанных с конкретным контекстом устройства (DC), путем вызова функции [**сетворлдтрансформ**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) и предоставления элементов для этой матрицы.</span><span class="sxs-lookup"><span data-stu-id="c61a1-106">The combined transformations can be used to alter output associated with a particular device context (DC) by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function and supplying the elements for this matrix.</span></span> <span data-ttu-id="c61a1-107">Когда приложение вызывает **сетворлдтрансформ**, оно сохраняет элементы матрицы 3 на 3 в структуре [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) .</span><span class="sxs-lookup"><span data-stu-id="c61a1-107">When an application calls **SetWorldTransform**, it stores the elements of the 3-by-3 matrix in an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span> <span data-ttu-id="c61a1-108">Члены этой структуры соответствуют двум первым столбцам матрицы размером 3 на 3. Последний столбец матрицы не требуется, так как его значения являются константами.</span><span class="sxs-lookup"><span data-stu-id="c61a1-108">The members of this structure correspond to the first two columns of a 3-by-3 matrix; the last column of the matrix is not required because its values are constant.</span></span>

<span data-ttu-id="c61a1-109">Элементы текущей матрицы преобразования мира можно реанимированным, вызвав функцию [**жетворлдтрансформ**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) и указав указатель на структуру [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) .</span><span class="sxs-lookup"><span data-stu-id="c61a1-109">The elements of the current world transformation matrix can be revived by calling the [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) function and supplying a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span>

 

 



