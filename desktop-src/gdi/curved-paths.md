---
description: Кривые пути
ms.assetid: 1ee9e6c6-5f8d-4727-b5f9-4b179c5371f1
title: Кривые пути
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe27e20d7c5c3f59ea4bd38b46049088ae9d409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898442"
---
# <a name="curved-paths"></a><span data-ttu-id="bb691-103">Кривые пути</span><span class="sxs-lookup"><span data-stu-id="bb691-103">Curved Paths</span></span>

<span data-ttu-id="bb691-104">Приложение может выполнить сведение кривых в пути путем вызова функции [**флаттенпас**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) .</span><span class="sxs-lookup"><span data-stu-id="bb691-104">An application can flatten the curves in a path by calling the [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) function.</span></span> <span data-ttu-id="bb691-105">Эта функция особенно полезна для приложений, которые соответствуют тексту на контуре контура, который содержит кривые.</span><span class="sxs-lookup"><span data-stu-id="bb691-105">This function is especially useful for applications that fit text onto the contour of a path which contains curves.</span></span> <span data-ttu-id="bb691-106">Чтобы вписать текст, приложение должно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="bb691-106">To fit the text, the application must perform the following steps:</span></span>

1.  <span data-ttu-id="bb691-107">Создайте путь, по которому отображается текст.</span><span class="sxs-lookup"><span data-stu-id="bb691-107">Create the path where the text appears.</span></span>
2.  <span data-ttu-id="bb691-108">Вызовите функцию [**флаттенпас**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) , чтобы преобразовать кривые в контуре в сегменты линии.</span><span class="sxs-lookup"><span data-stu-id="bb691-108">Call the [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) function to convert the curves in a path into line segments.</span></span>
3.  <span data-ttu-id="bb691-109">Вызовите функцию [**Multipath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) , чтобы получить эти сегменты линии.</span><span class="sxs-lookup"><span data-stu-id="bb691-109">Call the [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) function to retrieve those line segments.</span></span>
4.  <span data-ttu-id="bb691-110">Вычислите длину каждой строки и ширину каждого символа в строке.</span><span class="sxs-lookup"><span data-stu-id="bb691-110">Calculate the length of each line and the width of each character in the string.</span></span>
5.  <span data-ttu-id="bb691-111">Используйте данные ширины строки и ширины символов для размещения каждого символа вдоль кривой.</span><span class="sxs-lookup"><span data-stu-id="bb691-111">Use line-width and character-width data to position each character along the curve.</span></span>

 

 



