---
title: Нарушение потоков D1105
ms.assetid: 2c6cf90b-ce9e-4ea9-849d-22170f65ffb0
description: Потоковый интерфейс аренды был одновременно обращен к нескольким потокам.
keywords:
- Direct2D о нарушении потоков D1105
topic_type:
- apiref
api_name:
- D1105 Threading Violation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fe83baa32be8ae18948ae5a80e3e0b218cd4fa4a
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2021
ms.locfileid: "105658172"
---
# <a name="d1105-threading-violation"></a><span data-ttu-id="8faf4-104">D1105: нарушение потоков</span><span class="sxs-lookup"><span data-stu-id="8faf4-104">D1105: Threading Violation</span></span>

<span data-ttu-id="8faf4-105">\[ *Интерфейсный* поток аренды \] был одновременно обращен к нескольким потокам.</span><span class="sxs-lookup"><span data-stu-id="8faf4-105">A rental threaded interface \[*interface*\] was simultaneously accessed from multiple threads.</span></span>

## <a name="placeholders"></a><span data-ttu-id="8faf4-106">Заполнители</span><span class="sxs-lookup"><span data-stu-id="8faf4-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="8faf4-107"><span id="interface"></span><span id="INTERFACE"></span>*взаимодействия*</span><span class="sxs-lookup"><span data-stu-id="8faf4-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="8faf4-108">Адрес интерфейса, доступ к которому осуществлялся несколькими потоками.</span><span class="sxs-lookup"><span data-stu-id="8faf4-108">The address of the interface that was accessed by multiple threads.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="8faf4-109">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="8faf4-109">Possible Causes</span></span>

<span data-ttu-id="8faf4-110">Использование экземпляра объекта из одной и той же однопотоковой фабрики из двух разных потоков.</span><span class="sxs-lookup"><span data-stu-id="8faf4-110">Using an object instance from the same single-threaded factory from two different threads.</span></span>

 

 




