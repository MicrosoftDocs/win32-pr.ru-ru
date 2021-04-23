---
title: D1101 неизвестный маркер
ms.assetid: ae40058a-ea17-4262-87dc-0ce852c16c2a
description: В нее передан интерфейс, не выделенный этой библиотекой DLL.
keywords:
- D1101 неизвестный Handle Direct2D
topic_type:
- apiref
api_name:
- D1101 Unknown Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2a87491a02d3dea992f8dd767ad34cf83b2cbf40
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2021
ms.locfileid: "105658174"
---
# <a name="d1101-unknown-handle"></a><span data-ttu-id="c282d-104">D1101: неизвестный маркер</span><span class="sxs-lookup"><span data-stu-id="c282d-104">D1101: Unknown Handle</span></span>

<span data-ttu-id="c282d-105">\[  \] В нее не был передан интерфейс интерфейса, не выделенный этой библиотекой DLL.</span><span class="sxs-lookup"><span data-stu-id="c282d-105">An interface \[*interface*\] not allocated by this DLL was passed to it.</span></span>

## <a name="placeholders"></a><span data-ttu-id="c282d-106">Заполнители</span><span class="sxs-lookup"><span data-stu-id="c282d-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="c282d-107"><span id="interface"></span><span id="INTERFACE"></span>*взаимодействия*</span><span class="sxs-lookup"><span data-stu-id="c282d-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="c282d-108">Адрес интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c282d-108">The address of the interface.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="c282d-109">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="c282d-109">Possible Causes</span></span>

<span data-ttu-id="c282d-110">Недопустимое использование ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c282d-110">Invalid resource usage.</span></span> <span data-ttu-id="c282d-111">Ресурс, созданный за пределами Direct2D, используется с фабрикой Direct2D, или ресурсы, созданные в одной фабрике, использовались с ресурсом, созданным другой фабрикой.</span><span class="sxs-lookup"><span data-stu-id="c282d-111">The resource created outside of Direct2D is used with a Direct2D factory, or the resources created on one factory was used with a resource created by another factory.</span></span>

 

 




