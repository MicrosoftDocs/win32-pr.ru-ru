---
title: D1102 слишком много открытых дескрипторов
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: Обнаружено большое количество неосвобожденных интерфейсов. В настоящее время имеются неосвобожденные интерфейсы, выделенные этой библиотекой DLL.
keywords:
- D1102 слишком много открытых дескрипторов Direct2D
topic_type:
- apiref
api_name:
- D1102 Too Many Opened Handles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: e3c12c2e2a7b47535e830c6ed65a828a16672bbf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783588"
---
# <a name="d1102-too-many-opened-handles"></a><span data-ttu-id="b66e6-105">D1102: слишком много открытых дескрипторов</span><span class="sxs-lookup"><span data-stu-id="b66e6-105">D1102: Too Many Opened Handles</span></span>

<span data-ttu-id="b66e6-106">Обнаружено большое количество неосвобожденных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="b66e6-106">A large number of unreleased interfaces were found.</span></span> <span data-ttu-id="b66e6-107">В настоящее время существует \[  \] Неосвобожденный набор интерфейсов, выделенных этой библиотекой DLL.</span><span class="sxs-lookup"><span data-stu-id="b66e6-107">Currently there are \[*number*\] unreleased interfaces allocated by this DLL.</span></span>

## <a name="placeholders"></a><span data-ttu-id="b66e6-108">Заполнители</span><span class="sxs-lookup"><span data-stu-id="b66e6-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="b66e6-109"><span id="number"></span><span id="NUMBER"></span>*Нумерация*</span><span class="sxs-lookup"><span data-stu-id="b66e6-109"><span id="number"></span><span id="NUMBER"></span>*number*</span></span>
</dt> <dd>

<span data-ttu-id="b66e6-110">Число неосвобожденных интерфейсов, выделенных этой библиотекой DLL.</span><span class="sxs-lookup"><span data-stu-id="b66e6-110">The number of unreleased interfaces allocated by this DLL.</span></span>

</dd> </dl> 

|             |         |
|-------------|---------|
| <span data-ttu-id="b66e6-111">Уровень ошибки</span><span class="sxs-lookup"><span data-stu-id="b66e6-111">Error Level</span></span> | <span data-ttu-id="b66e6-112">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="b66e6-112">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="b66e6-113">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="b66e6-113">Possible Causes</span></span>

<span data-ttu-id="b66e6-114">Создано большое количество ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b66e6-114">A large number of resources were created.</span></span> <span data-ttu-id="b66e6-115">Хотя Direct2D не имеет верхней границы количества доступных ресурсов (за исключением памяти), отладочный слой выдает это информационное сообщение при обнаружении 1001 активных объектов, 2001 активных объектов или 3001 активных объектов и т. д., так как это может указывать на утечку в приложении.</span><span class="sxs-lookup"><span data-stu-id="b66e6-115">Although Direct2D has no upper bound on the number of available resources (except memory), the debug layer issues this informational message when it encounters 1001 live objects, 2001 live objects, or 3001 live objects etc, because this might indicate a leak in the application.</span></span>

 

 




