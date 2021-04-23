---
description: Сетевой монитор большой двоичный объект (BLOB) — это общая структура данных, которая содержит сведения о конфигурации и расположении сетевых карт (NIC).
ms.assetid: 910bf929-aa89-434d-83c3-07c80c627405
title: сетевой монитор большие двоичные объекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce6dd6ca8643eabe8ab49387c0ef39eb49b6f2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684676"
---
# <a name="network-monitor-blobs"></a><span data-ttu-id="e7199-103">сетевой монитор большие двоичные объекты</span><span class="sxs-lookup"><span data-stu-id="e7199-103">Network Monitor BLOBs</span></span>

<span data-ttu-id="e7199-104">Сетевой монитор большой двоичный объект (BLOB) — это общая структура данных, которая содержит сведения о конфигурации и расположении сетевых карт (NIC).</span><span class="sxs-lookup"><span data-stu-id="e7199-104">The Network Monitor binary large object (BLOB) is a generic data structure that contains configuration and location information of network interface cards (NICs).</span></span> <span data-ttu-id="e7199-105">Используйте большие двоичные объекты для представления сетевых карт и фильтрации записей в списке сетевых адаптеров.</span><span class="sxs-lookup"><span data-stu-id="e7199-105">Use BLOBs to represent NICs and to filter entries in a list of NICs.</span></span> <span data-ttu-id="e7199-106">Большие двоичные объекты также могут содержать данные конкретного приложения, не затрагивая другие данные, которые они содержат.</span><span class="sxs-lookup"><span data-stu-id="e7199-106">BLOBS can also contain application-specific data without affecting the other data that they hold.</span></span> <span data-ttu-id="e7199-107">Реализация BLOB-объектов непрозрачна для всех уровней, которым необходим доступ к BLOB-объектам с помощью API больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="e7199-107">BLOB implementation is opaque to all levels that must access BLOBs with BLOB APIs.</span></span>

## <a name="blob-structure"></a><span data-ttu-id="e7199-108">Структура большого двоичного объекта</span><span class="sxs-lookup"><span data-stu-id="e7199-108">BLOB Structure</span></span>

<span data-ttu-id="e7199-109">Большой двоичный объект можно рассматривать как иерархическое дерево, используемое для обозначения строк.</span><span class="sxs-lookup"><span data-stu-id="e7199-109">A BLOB can be considered as a hierarchical tree used to designate strings.</span></span> <span data-ttu-id="e7199-110">Это дерево имеет три слоя: владелец, Категория и тег.</span><span class="sxs-lookup"><span data-stu-id="e7199-110">This tree has three layers: Owner, Category, and Tag.</span></span> <span data-ttu-id="e7199-111">Owner — это строка, указывающая, что в общем, кто считывает запись.</span><span class="sxs-lookup"><span data-stu-id="e7199-111">Owner is a string that indicates, in general, who reads an entry.</span></span> <span data-ttu-id="e7199-112">Эта категория также является строкой, которая обозначает общее функциональное группирование тегов под владельцем.</span><span class="sxs-lookup"><span data-stu-id="e7199-112">The Category is also a string, which designates a general functional grouping of tags under the owner.</span></span> <span data-ttu-id="e7199-113">Тег — это фактическое имя записи.</span><span class="sxs-lookup"><span data-stu-id="e7199-113">The Tag is the actual name of the entry.</span></span>

<span data-ttu-id="e7199-114">Ниже перечислены структурные характеристики больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="e7199-114">The structural characteristics of BLOBs include:</span></span>

-   <span data-ttu-id="e7199-115">Вспомогательные объекты BLOB в пределах одного процесса защищаются друг от друга мьютексом, встроенным в каждый большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="e7199-115">BLOB helpers within one process are protected from one another by a mutex built into each BLOB.</span></span>
-   <span data-ttu-id="e7199-116">Каждый большой двоичный объект имеет внутренний номер версии, чтобы вспомогательные методы могли работать как с текущими, так и с будущими формами больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="e7199-116">Each BLOB has an internal version number so that the helpers can handle both present and future BLOB forms.</span></span> <span data-ttu-id="e7199-117">При отправке большого двоичного объекта на другой компьютер с помощью удаленного вызова процедуры могут возникать конфликты версий.</span><span class="sxs-lookup"><span data-stu-id="e7199-117">Version conflicts may occur if you send a BLOB to another computer via a remote procedure call.</span></span>
-   <span data-ttu-id="e7199-118">Сам BLOB-объект является указателем на void.</span><span class="sxs-lookup"><span data-stu-id="e7199-118">The BLOB itself is a pointer to a void.</span></span> <span data-ttu-id="e7199-119">Имейте в виду, что приложения должны выделить большие двоичные объекты с модификатором **const** , чтобы избежать изменения содержимого.</span><span class="sxs-lookup"><span data-stu-id="e7199-119">Be aware that applications should allocate BLOBs with the **const** modifier to avoid altering the contents.</span></span>
-   <span data-ttu-id="e7199-120">Все обозначения, а также их значения являются строками.</span><span class="sxs-lookup"><span data-stu-id="e7199-120">Each of the designators, as well as their values, are strings.</span></span> <span data-ttu-id="e7199-121">Имейте в виду, что строки, возвращаемые функциями **GetString** , фактически являются указателями на большой двоичный объект и не должны изменяться.</span><span class="sxs-lookup"><span data-stu-id="e7199-121">Be aware that the strings returned by **GetString** functions are actually pointers into the BLOB and should not be changed.</span></span> <span data-ttu-id="e7199-122">По этой причине эти строки должны быть указаны как **const char** _ \_ px \*, чтобы предотвратить случайное изменение этих строк приложениями.</span><span class="sxs-lookup"><span data-stu-id="e7199-122">For this reason, these strings must be specified as **const char** _\_pX\* to keep applications from accidentally changing them.</span></span>

<span data-ttu-id="e7199-123">Как правило, все параметры с указателем **const** позволяют вызывающей стороне отменять изменения значений, а не запрещать их изменение.</span><span class="sxs-lookup"><span data-stu-id="e7199-123">In general, all parameters with the **const** designator encourage the caller to refrain from changing the values rather than prohibit the helper functions from changing them.</span></span> <span data-ttu-id="e7199-124">Фактически, вспомогательные функции обычно изменяют эти значения.</span><span class="sxs-lookup"><span data-stu-id="e7199-124">In fact, the helper functions will usually change those values.</span></span>

 

 



