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
ms.openlocfilehash: b9254986bebadeffafaa832817f59194bfc58e12
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908862"
---
# <a name="fourccmap-class"></a><span data-ttu-id="5bcd0-103">Класс Фаурккмап</span><span class="sxs-lookup"><span data-stu-id="5bcd0-103">FOURCCMap class</span></span>

![Иерархия классов фаурккмап](images/fourcc01.png)

<span data-ttu-id="5bcd0-105">Класс **фаурккмап** обеспечивает преобразование между подтипами носителя **GUID** и тегами носителя старого стиля **FourCC** 32-bit.</span><span class="sxs-lookup"><span data-stu-id="5bcd0-105">The **FOURCCMap** class provides conversion between **GUID** media subtypes and old-style **FOURCC** 32-bit media tags.</span></span> <span data-ttu-id="5bcd0-106">В исходных интерфейсах Windows Media API типы мультимедиа были помечены как 32-битовые значения, созданные из 4 8-разрядных символов и известные как **FourCC** s.</span><span class="sxs-lookup"><span data-stu-id="5bcd0-106">In the original Windows multimedia APIs, media types were tagged with 32-bit values created from four 8-bit characters and were known as **FOURCC** s.</span></span> <span data-ttu-id="5bcd0-107">Типы мультимедиа DirectShow имеют **GUID** для подтипа, частично так как они проще создавать (для создания нового объекта **FourCC** требуется его регистрация в корпорации Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="5bcd0-107">DirectShow media types have **GUID** s for the subtype, partly because these are simpler to create (creation of a new **FOURCC** requires its registration with Microsoft).</span></span> <span data-ttu-id="5bcd0-108">Так как объекты типа **FourCC** уникальны, сопоставление "один к одному" стало возможным благодаря выделению диапазона 4 000 000 000 **GUID** s, представляющих **FourCC**.</span><span class="sxs-lookup"><span data-stu-id="5bcd0-108">Because **FOURCC** s are unique, a one-to-one mapping has been made possible by allocating a range of 4,000 million **GUID** s representing **FOURCC** s.</span></span> <span data-ttu-id="5bcd0-109">Этот диапазон — все **идентификаторы GUID** в формате:</span><span class="sxs-lookup"><span data-stu-id="5bcd0-109">This range is all **GUID** s of the form:</span></span>

`XXXXXXXX-0000-0010-8000-00AA00389B71`

<span data-ttu-id="5bcd0-110">Этот класс упрощает преобразование между **GUID** s и **FourCC**.</span><span class="sxs-lookup"><span data-stu-id="5bcd0-110">This class simplifies conversion between **GUID** s and **FOURCC** s.</span></span> <span data-ttu-id="5bcd0-111">Это относится только к совместимости.</span><span class="sxs-lookup"><span data-stu-id="5bcd0-111">This is for compatibility only.</span></span> <span data-ttu-id="5bcd0-112">Рекомендуется представить все новые подтипы мультимедиа с помощью **GUID** s, созданного Guidgen.exe или аналогичного средства, а не путем сопоставления **FourCC** s.</span><span class="sxs-lookup"><span data-stu-id="5bcd0-112">It is recommended that all new media subtypes be represented by **GUID** s created by Guidgen.exe or a similar tool, and not by mapping **FOURCC** s.</span></span>

<span data-ttu-id="5bcd0-113">Объект является производным от **идентификатора GUID** без дополнительных элементов данных и может быть приведен к **идентификатору GUID**.</span><span class="sxs-lookup"><span data-stu-id="5bcd0-113">The object is derived from a **GUID**, with no extra data members, and can be cast to a **GUID**.</span></span> <span data-ttu-id="5bcd0-114">Объект может быть передан объектом **FourCC** во время создания.</span><span class="sxs-lookup"><span data-stu-id="5bcd0-114">The object can be passed a **FOURCC** at construction time.</span></span> <span data-ttu-id="5bcd0-115">Конструктор по умолчанию инициализирует **FourCC** как ноль.</span><span class="sxs-lookup"><span data-stu-id="5bcd0-115">The default constructor will initialize the **FOURCC** to zero.</span></span>

<span data-ttu-id="5bcd0-116">Методы [**жетфауркк**](fourccmap-getfourcc.md) и [**сетфауркк**](fourccmap-setfourcc.md) не проверяют, соответствуют ли фиксированные части **идентификатора GUID** диапазону **FourCC** .</span><span class="sxs-lookup"><span data-stu-id="5bcd0-116">The [**GetFOURCC**](fourccmap-getfourcc.md) and [**SetFOURCC**](fourccmap-setfourcc.md) methods do not check that the fixed portions of the **GUID** correspond to the **FOURCC** range.</span></span> <span data-ttu-id="5bcd0-117">Таким же, при приведении указателя на **идентификатор GUID** в указатель на **FourCC** и последующем установке или получении поля **FourCC** необходимо также отдельно проверить, что **идентификатор GUID** находится в диапазоне **FourCC** .</span><span class="sxs-lookup"><span data-stu-id="5bcd0-117">Thus, if you cast a pointer to a **GUID** into a pointer to a **FOURCC** and then set or get the **FOURCC** field, you also need to check separately that the **GUID** is within the **FOURCC** range.</span></span>

## <a name="member-functions"></a><span data-ttu-id="5bcd0-118">Функции элементов</span><span class="sxs-lookup"><span data-stu-id="5bcd0-118">Member Functions</span></span>



| <span data-ttu-id="5bcd0-119">Метка</span><span class="sxs-lookup"><span data-stu-id="5bcd0-119">Label</span></span> | <span data-ttu-id="5bcd0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5bcd0-120">Value</span></span> |
|------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="5bcd0-121">**фаурккмап**</span><span class="sxs-lookup"><span data-stu-id="5bcd0-121">**FOURCCMap**</span></span>](fourccmap-fourccmap.md) | <span data-ttu-id="5bcd0-122">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="5bcd0-122">Constructor method.</span></span>                                      |
| [<span data-ttu-id="5bcd0-123">**жетфауркк**</span><span class="sxs-lookup"><span data-stu-id="5bcd0-123">**GetFOURCC**</span></span>](fourccmap-getfourcc.md) | <span data-ttu-id="5bcd0-124">Извлекает объект **FourCC** из объекта **фаурккмап** .</span><span class="sxs-lookup"><span data-stu-id="5bcd0-124">Retrieves the **FOURCC** from a **FOURCCMap** object.</span></span>    |
| [<span data-ttu-id="5bcd0-125">**сетфауркк**</span><span class="sxs-lookup"><span data-stu-id="5bcd0-125">**SetFOURCC**</span></span>](fourccmap-setfourcc.md) | <span data-ttu-id="5bcd0-126">Задает часть **FourCC** объекта **фаурккмап** .</span><span class="sxs-lookup"><span data-stu-id="5bcd0-126">Sets the **FOURCC** portion of the **FOURCCMap** object.</span></span> |



 

 

 



