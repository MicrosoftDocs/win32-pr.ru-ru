---
description: Указывает идентификатор оборудования PnP-X для службы.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Пнпксхардвареид, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0ffc389ca6df363439dd6463b3f86ca756359e8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996531"
---
# <a name="pnpxhardwareid-element"></a><span data-ttu-id="66a23-103">Пнпксхардвареид, элемент</span><span class="sxs-lookup"><span data-stu-id="66a23-103">PnPXHardwareId element</span></span>

<span data-ttu-id="66a23-104">Указывает идентификатор оборудования PnP-X для службы.</span><span class="sxs-lookup"><span data-stu-id="66a23-104">Specifies the PnP-X Hardware Identifier of the service.</span></span> <span data-ttu-id="66a23-105">Устройство PnP соответствует этому элементу с описанием оборудования, указанным в \[ разделе ПНПКСДЕВИЦЕ \] INF-файла устройства.</span><span class="sxs-lookup"><span data-stu-id="66a23-105">PnP matches this element with the hardware description(s) provided in the \[PnpxDevice\] section of the device's INF file.</span></span> <span data-ttu-id="66a23-106">На основе этих сведений Служба PnP выбирает и загружает наиболее подходящий драйвер устройства.</span><span class="sxs-lookup"><span data-stu-id="66a23-106">Based on this information, the PnP service selects and loads the most appropriate device driver.</span></span>

## <a name="usage"></a><span data-ttu-id="66a23-107">Использование</span><span class="sxs-lookup"><span data-stu-id="66a23-107">Usage</span></span>

``` syntax
<PnPXHardwareId/>
```

## <a name="attributes"></a><span data-ttu-id="66a23-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="66a23-108">Attributes</span></span>

<span data-ttu-id="66a23-109">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="66a23-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="66a23-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="66a23-110">Child elements</span></span>

<span data-ttu-id="66a23-111">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="66a23-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="66a23-112">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="66a23-112">Parent elements</span></span>



| <span data-ttu-id="66a23-113">Элемент</span><span class="sxs-lookup"><span data-stu-id="66a23-113">Element</span></span>                             | <span data-ttu-id="66a23-114">Описание</span><span class="sxs-lookup"><span data-stu-id="66a23-114">Description</span></span>                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="66a23-115">**внутрипроцессных**</span><span class="sxs-lookup"><span data-stu-id="66a23-115">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="66a23-116">Определяет элементы для служб, определенных узлом службы.</span><span class="sxs-lookup"><span data-stu-id="66a23-116">Defines elements for the services defined by the service host.</span></span> <br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="66a23-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="66a23-117">Remarks</span></span>

<span data-ttu-id="66a23-118">Чтобы указать более одного идентификатора оборудования, разделяйте идентификаторы пробелами, например "Пнпкс \_ самплесервице \_ Хвид \_ 1 пнпкс \_ самплесервице \_ хвид \_ 2 пнпкс \_ SampleService1 \_ хвид \_ 3".</span><span class="sxs-lookup"><span data-stu-id="66a23-118">To specify more than one hardware ID, separate the identifiers with a space character, for example, "PnPX\_SampleService\_HWID\_1 PnPX\_SampleService\_HWID\_2 PnPX\_SampleService1\_HWID\_3".</span></span>

## <a name="element-information"></a><span data-ttu-id="66a23-119">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="66a23-119">Element information</span></span>



| <span data-ttu-id="66a23-120">Метка</span><span class="sxs-lookup"><span data-stu-id="66a23-120">Label</span></span> | <span data-ttu-id="66a23-121">Значение</span><span class="sxs-lookup"><span data-stu-id="66a23-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="66a23-122">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="66a23-122">Minimum supported system</span></span><br/> | <span data-ttu-id="66a23-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66a23-123">Windows Vista</span></span> |
| <span data-ttu-id="66a23-124">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="66a23-124">Can be empty</span></span>                        | <span data-ttu-id="66a23-125">Да</span><span class="sxs-lookup"><span data-stu-id="66a23-125">Yes</span></span>           |



 

 




