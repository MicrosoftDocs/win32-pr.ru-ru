---
description: Можно обновить значения неключевых свойств экземпляров класса представления Union. Изменения, вносимые в экземпляр класса представления, будут переданы обратно экземплярам исходного класса, образуя класс представления Union.
ms.assetid: 375c9bc8-9f7b-42b4-a841-cf6af88887de
ms.tgt_platform: multiple
title: Обновление представления объединения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b051147ab40aacbf9032c5a0998d5894148985c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155806"
---
# <a name="updating-a-union-view"></a><span data-ttu-id="dfb0c-104">Обновление представления объединения</span><span class="sxs-lookup"><span data-stu-id="dfb0c-104">Updating a Union View</span></span>

<span data-ttu-id="dfb0c-105">Можно обновить значения неключевых свойств экземпляров класса представления Union.</span><span class="sxs-lookup"><span data-stu-id="dfb0c-105">You can update the values of nonkey properties of union view class instances.</span></span> <span data-ttu-id="dfb0c-106">Изменения, вносимые в экземпляр класса представления, будут переданы обратно экземплярам исходного класса, образуя класс представления Union.</span><span class="sxs-lookup"><span data-stu-id="dfb0c-106">The changes you make to the view class instance will be propagated back to the source class instances that form the union view class.</span></span>

<span data-ttu-id="dfb0c-107">На изменения экземпляров класса представления влияют следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="dfb0c-107">The following restrictions apply to changes to view class instances:</span></span>

-   <span data-ttu-id="dfb0c-108">Нельзя создавать новые экземпляры классов представлений.</span><span class="sxs-lookup"><span data-stu-id="dfb0c-108">You cannot create new instances of view classes.</span></span>
-   <span data-ttu-id="dfb0c-109">Обновления поддерживаются только в классах Union. представления соединения и ассоциации создают экземпляры представлений только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dfb0c-109">Only union classes support updates; join and association views create read-only view instances.</span></span>
-   <span data-ttu-id="dfb0c-110">Успешное обновление зависит от того, является ли экземпляр источника обновляемым.</span><span class="sxs-lookup"><span data-stu-id="dfb0c-110">Success of an update depends on whether a source instance is updateable.</span></span> <span data-ttu-id="dfb0c-111">Если свойство экземпляра представления соответствует свойству исходного экземпляра, доступному только для чтения, попытки изменить свойство View завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="dfb0c-111">If a view instance property maps to a read-only property of a source instance, attempts to modify the view property fail.</span></span>

 

 



