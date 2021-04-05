---
description: Класс Фаурккмап обеспечивает преобразование между подтипами носителя GUID и тегами носителя старого стиля FOURCC 32-bit.
ms.assetid: f77f1da9-34f6-44a0-9f1a-7db2e5a26268
title: Класс Фаурккмап
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap
api_type:
- COM
api_location: ''
ms.openlocfilehash: fd30a0f04d98b4c6ba4b7716a1a72d527873dbff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140019"
---
# <a name="fourccmap-class"></a><span data-ttu-id="56dea-103">Класс Фаурккмап</span><span class="sxs-lookup"><span data-stu-id="56dea-103">FOURCCMap class</span></span>

![Иерархия классов фаурккмап](images/fourcc01.png)

<span data-ttu-id="56dea-105">Класс **фаурккмап** обеспечивает преобразование между подтипами носителя **GUID** и тегами носителя старого стиля **FourCC** 32-bit.</span><span class="sxs-lookup"><span data-stu-id="56dea-105">The **FOURCCMap** class provides conversion between **GUID** media subtypes and old-style **FOURCC** 32-bit media tags.</span></span> <span data-ttu-id="56dea-106">В исходных интерфейсах Windows Media API типы мультимедиа были помечены как 32-битовые значения, созданные из 4 8-разрядных символов и известные как **FourCC** s.</span><span class="sxs-lookup"><span data-stu-id="56dea-106">In the original Windows multimedia APIs, media types were tagged with 32-bit values created from four 8-bit characters and were known as **FOURCC** s.</span></span> <span data-ttu-id="56dea-107">Типы мультимедиа DirectShow имеют **GUID** для подтипа, частично так как они проще создавать (для создания нового объекта **FourCC** требуется его регистрация в корпорации Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="56dea-107">DirectShow media types have **GUID** s for the subtype, partly because these are simpler to create (creation of a new **FOURCC** requires its registration with Microsoft).</span></span> <span data-ttu-id="56dea-108">Так как объекты типа **FourCC** уникальны, сопоставление "один к одному" стало возможным благодаря выделению диапазона 4 000 000 000 **GUID** s, представляющих **FourCC**.</span><span class="sxs-lookup"><span data-stu-id="56dea-108">Because **FOURCC** s are unique, a one-to-one mapping has been made possible by allocating a range of 4,000 million **GUID** s representing **FOURCC** s.</span></span> <span data-ttu-id="56dea-109">Этот диапазон — все **идентификаторы GUID** в формате:</span><span class="sxs-lookup"><span data-stu-id="56dea-109">This range is all **GUID** s of the form:</span></span>

`XXXXXXXX-0000-0010-8000-00AA00389B71`

<span data-ttu-id="56dea-110">Этот класс упрощает преобразование между **GUID** s и **FourCC**.</span><span class="sxs-lookup"><span data-stu-id="56dea-110">This class simplifies conversion between **GUID** s and **FOURCC** s.</span></span> <span data-ttu-id="56dea-111">Это относится только к совместимости.</span><span class="sxs-lookup"><span data-stu-id="56dea-111">This is for compatibility only.</span></span> <span data-ttu-id="56dea-112">Рекомендуется представить все новые подтипы мультимедиа с помощью **GUID** s, созданного Guidgen.exe или аналогичного средства, а не путем сопоставления **FourCC** s.</span><span class="sxs-lookup"><span data-stu-id="56dea-112">It is recommended that all new media subtypes be represented by **GUID** s created by Guidgen.exe or a similar tool, and not by mapping **FOURCC** s.</span></span>

<span data-ttu-id="56dea-113">Объект является производным от **идентификатора GUID** без дополнительных элементов данных и может быть приведен к **идентификатору GUID**.</span><span class="sxs-lookup"><span data-stu-id="56dea-113">The object is derived from a **GUID**, with no extra data members, and can be cast to a **GUID**.</span></span> <span data-ttu-id="56dea-114">Объект может быть передан объектом **FourCC** во время создания.</span><span class="sxs-lookup"><span data-stu-id="56dea-114">The object can be passed a **FOURCC** at construction time.</span></span> <span data-ttu-id="56dea-115">Конструктор по умолчанию инициализирует **FourCC** как ноль.</span><span class="sxs-lookup"><span data-stu-id="56dea-115">The default constructor will initialize the **FOURCC** to zero.</span></span>

<span data-ttu-id="56dea-116">Методы [**жетфауркк**](fourccmap-getfourcc.md) и [**сетфауркк**](fourccmap-setfourcc.md) не проверяют, соответствуют ли фиксированные части **идентификатора GUID** диапазону **FourCC** .</span><span class="sxs-lookup"><span data-stu-id="56dea-116">The [**GetFOURCC**](fourccmap-getfourcc.md) and [**SetFOURCC**](fourccmap-setfourcc.md) methods do not check that the fixed portions of the **GUID** correspond to the **FOURCC** range.</span></span> <span data-ttu-id="56dea-117">Таким же, при приведении указателя на **идентификатор GUID** в указатель на **FourCC** и последующем установке или получении поля **FourCC** необходимо также отдельно проверить, что **идентификатор GUID** находится в диапазоне **FourCC** .</span><span class="sxs-lookup"><span data-stu-id="56dea-117">Thus, if you cast a pointer to a **GUID** into a pointer to a **FOURCC** and then set or get the **FOURCC** field, you also need to check separately that the **GUID** is within the **FOURCC** range.</span></span>

## <a name="member-functions"></a><span data-ttu-id="56dea-118">Функции элементов</span><span class="sxs-lookup"><span data-stu-id="56dea-118">Member Functions</span></span>



|                                          |                                                          |
|------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="56dea-119">**фаурккмап**</span><span class="sxs-lookup"><span data-stu-id="56dea-119">**FOURCCMap**</span></span>](fourccmap-fourccmap.md) | <span data-ttu-id="56dea-120">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="56dea-120">Constructor method.</span></span>                                      |
| [<span data-ttu-id="56dea-121">**жетфауркк**</span><span class="sxs-lookup"><span data-stu-id="56dea-121">**GetFOURCC**</span></span>](fourccmap-getfourcc.md) | <span data-ttu-id="56dea-122">Извлекает объект **FourCC** из объекта **фаурккмап** .</span><span class="sxs-lookup"><span data-stu-id="56dea-122">Retrieves the **FOURCC** from a **FOURCCMap** object.</span></span>    |
| [<span data-ttu-id="56dea-123">**сетфауркк**</span><span class="sxs-lookup"><span data-stu-id="56dea-123">**SetFOURCC**</span></span>](fourccmap-setfourcc.md) | <span data-ttu-id="56dea-124">Задает часть **FourCC** объекта **фаурккмап** .</span><span class="sxs-lookup"><span data-stu-id="56dea-124">Sets the **FOURCC** portion of the **FOURCCMap** object.</span></span> |



 

 

 



