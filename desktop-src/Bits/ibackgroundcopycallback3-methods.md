---
title: Методы IBackgroundCopyCallback3
description: Интерфейс IBackgroundCopyCallback3 предоставляет следующие методы.
ms.assetid: FF0BA13F-63DA-46A4-ACC6-DE72AC20EAA2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f13aa1c97006084007e747f2766868c25e5b998
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654203"
---
# <a name="ibackgroundcopycallback3-methods"></a><span data-ttu-id="c5599-103">Методы IBackgroundCopyCallback3</span><span class="sxs-lookup"><span data-stu-id="c5599-103">IBackgroundCopyCallback3 Methods</span></span>

<span data-ttu-id="c5599-104">Интерфейс [**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c5599-104">The [**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c5599-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="c5599-105">In this section</span></span>



| <span data-ttu-id="c5599-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="c5599-106">Topic</span></span>                                                                                             | <span data-ttu-id="c5599-107">Описание</span><span class="sxs-lookup"><span data-stu-id="c5599-107">Description</span></span>                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5599-108">**Метод Филеранжестрансферред**</span><span class="sxs-lookup"><span data-stu-id="c5599-108">**FileRangesTransferred method**</span></span>](/windows/desktop/api/Bits10_1/nf-bits10_1-ibackgroundcopycallback3-filerangestransferred)<br/> | <span data-ttu-id="c5599-109">Служба BITS вызывает реализацию метода [**филеранжестрансферред**](/windows/desktop/api/Bits10_1/nf-bits10_1-ibackgroundcopycallback3-filerangestransferred) при загрузке одного или нескольких диапазонов файлов.</span><span class="sxs-lookup"><span data-stu-id="c5599-109">BITS calls your implementation of the [**FileRangesTransferred**](/windows/desktop/api/Bits10_1/nf-bits10_1-ibackgroundcopycallback3-filerangestransferred) method when one or more file ranges have been downloaded.</span></span> <span data-ttu-id="c5599-110">Диапазоны файлов добавляются в задание с помощью метода [**IBackgroundCopyFile6:: рекуестфилеранжес**](/windows/desktop/api/Bits10_1/nf-bits10_1-ibackgroundcopyfile6-requestfileranges) .</span><span class="sxs-lookup"><span data-stu-id="c5599-110">File ranges are added to the job using the [**IBackgroundCopyFile6::RequestFileRanges**](/windows/desktop/api/Bits10_1/nf-bits10_1-ibackgroundcopyfile6-requestfileranges) method.</span></span><br/> |



 

 

 





