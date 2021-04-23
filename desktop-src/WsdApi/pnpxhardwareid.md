---
description: Указывает идентификатор оборудования PnP-X для службы.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Пнпксхардвареид, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55e5e38b669a289545225df96fad05e55069b474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692809"
---
# <a name="pnpxhardwareid-element"></a><span data-ttu-id="b7b63-103">Пнпксхардвареид, элемент</span><span class="sxs-lookup"><span data-stu-id="b7b63-103">PnPXHardwareId element</span></span>

<span data-ttu-id="b7b63-104">Указывает идентификатор оборудования PnP-X для службы.</span><span class="sxs-lookup"><span data-stu-id="b7b63-104">Specifies the PnP-X Hardware Identifier of the service.</span></span> <span data-ttu-id="b7b63-105">Устройство PnP соответствует этому элементу с описанием оборудования, указанным в \[ разделе ПНПКСДЕВИЦЕ \] INF-файла устройства.</span><span class="sxs-lookup"><span data-stu-id="b7b63-105">PnP matches this element with the hardware description(s) provided in the \[PnpxDevice\] section of the device's INF file.</span></span> <span data-ttu-id="b7b63-106">На основе этих сведений Служба PnP выбирает и загружает наиболее подходящий драйвер устройства.</span><span class="sxs-lookup"><span data-stu-id="b7b63-106">Based on this information, the PnP service selects and loads the most appropriate device driver.</span></span>

## <a name="usage"></a><span data-ttu-id="b7b63-107">Использование</span><span class="sxs-lookup"><span data-stu-id="b7b63-107">Usage</span></span>

``` syntax
<PnPXHardwareId/>
```

## <a name="attributes"></a><span data-ttu-id="b7b63-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b7b63-108">Attributes</span></span>

<span data-ttu-id="b7b63-109">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b7b63-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b7b63-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b7b63-110">Child elements</span></span>

<span data-ttu-id="b7b63-111">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="b7b63-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b7b63-112">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b7b63-112">Parent elements</span></span>



| <span data-ttu-id="b7b63-113">Элемент</span><span class="sxs-lookup"><span data-stu-id="b7b63-113">Element</span></span>                             | <span data-ttu-id="b7b63-114">Описание</span><span class="sxs-lookup"><span data-stu-id="b7b63-114">Description</span></span>                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7b63-115">**внутрипроцессных**</span><span class="sxs-lookup"><span data-stu-id="b7b63-115">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="b7b63-116">Определяет элементы для служб, определенных узлом службы.</span><span class="sxs-lookup"><span data-stu-id="b7b63-116">Defines elements for the services defined by the service host.</span></span> <br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b7b63-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7b63-117">Remarks</span></span>

<span data-ttu-id="b7b63-118">Чтобы указать более одного идентификатора оборудования, разделяйте идентификаторы пробелами, например "Пнпкс \_ самплесервице \_ Хвид \_ 1 пнпкс \_ самплесервице \_ хвид \_ 2 пнпкс \_ SampleService1 \_ хвид \_ 3".</span><span class="sxs-lookup"><span data-stu-id="b7b63-118">To specify more than one hardware ID, separate the identifiers with a space character, for example, "PnPX\_SampleService\_HWID\_1 PnPX\_SampleService\_HWID\_2 PnPX\_SampleService1\_HWID\_3".</span></span>

## <a name="element-information"></a><span data-ttu-id="b7b63-119">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b7b63-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="b7b63-120">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="b7b63-120">Minimum supported system</span></span><br/> | <span data-ttu-id="b7b63-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7b63-121">Windows Vista</span></span> |
| <span data-ttu-id="b7b63-122">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="b7b63-122">Can be empty</span></span>                        | <span data-ttu-id="b7b63-123">Да</span><span class="sxs-lookup"><span data-stu-id="b7b63-123">Yes</span></span>           |



 

 




