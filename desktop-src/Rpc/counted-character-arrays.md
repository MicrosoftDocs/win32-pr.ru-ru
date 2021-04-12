---
title: Подсчет массивов символов
description: Атрибут \ size = \_ \ указывает верхнюю границу массива, а атрибут \ length = \_ \ указывает число передаваемых элементов массива.
ms.assetid: bed10259-3034-4be8-91f5-5201c2e19c6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360652436a73b445aa2dbb013e0e05145154e20e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487985"
---
# <a name="counted-character-arrays"></a><span data-ttu-id="7f465-103">Подсчет массивов символов</span><span class="sxs-lookup"><span data-stu-id="7f465-103">Counted Character Arrays</span></span>

<span data-ttu-id="7f465-104">Атрибут \[ [size \_ имеет](/windows/desktop/Midl/size-is) значение, \] указывающее верхнюю границу массива, а \[ [Длина атрибута length \_ ](/windows/desktop/Midl/length-is) \] указывает число передаваемых элементов массива.</span><span class="sxs-lookup"><span data-stu-id="7f465-104">The \[ [size\_is](/windows/desktop/Midl/size-is)\] attribute indicates the upper bound of the array while the \[ [length\_is](/windows/desktop/Midl/length-is)\] attribute indicates the number of array elements to transmit.</span></span> <span data-ttu-id="7f465-105">В дополнение к массиву, прототип удаленной процедуры должен содержать любые переменные, представляющие длину или размер, которые определяют переданные элементы массива (они могут быть отдельными параметрами или объединены со строкой в структуре).</span><span class="sxs-lookup"><span data-stu-id="7f465-105">In addition to the array, the remote procedure prototype must include any variables representing length or size that determine the transmitted array elements (they can be separate parameters or bundled with the string in a structure).</span></span> <span data-ttu-id="7f465-106">Эти атрибуты можно использовать с массивами двухбайтовых символов или однобайтовых символов точно так же, как массивы других типов.</span><span class="sxs-lookup"><span data-stu-id="7f465-106">These attributes can be used with wide-character or single-byte character arrays just as they would be with arrays of other types.</span></span>

<span data-ttu-id="7f465-107">Сведения в этом разделе описывают прототипы параметров удаленной процедуры для массивов символов.</span><span class="sxs-lookup"><span data-stu-id="7f465-107">The information in this section describes remote procedure parameter prototypes for character arrays.</span></span> <span data-ttu-id="7f465-108">Он разделен на следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="7f465-108">It is divided into the following topics:</span></span>

-   <span data-ttu-id="7f465-109">[\[в, out и Size \_ — \] прототип](-in-out-size-is-prototype.md)</span><span class="sxs-lookup"><span data-stu-id="7f465-109">[\[in, out, size\_is\] Prototype](-in-out-size-is-prototype.md)</span></span>
-   <span data-ttu-id="7f465-110">[\[в, размер \_ и, размер \_ — \] прототип](-in-size-is-and-out-size-is-prototype.md)</span><span class="sxs-lookup"><span data-stu-id="7f465-110">[\[in, size\_is and out, size\_is\] Prototype](-in-size-is-and-out-size-is-prototype.md)</span></span>

 

 