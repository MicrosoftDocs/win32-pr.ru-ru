---
title: Перечисления ВМДМ
description: Сведения о перечислениях, определяемых диспетчер устройств Windows Media, таких как WMDM_ENUM_PROP_VALID_VALUES_FORM и WMDM_FIND_SCOPE.
ms.assetid: 205fe651-a712-4d9a-9ebf-bf7e8ec05ed0
keywords:
- Диспетчер устройств Windows Media, перечисления
- Диспетчер устройств, перечисления
- Справочник по программированию, перечисления
- Справочник по диспетчер устройств Windows Media, перечисления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec50acdfcf780f65a638c3761f3f6164d29afb74
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "112067921"
---
# <a name="wmdm-enumerations"></a><span data-ttu-id="e6307-107">Перечисления ВМДМ</span><span class="sxs-lookup"><span data-stu-id="e6307-107">WMDM enumerations</span></span>

<span data-ttu-id="e6307-108">В этом разделе документируется функция пакета SDK для Windows Media диспетчер устройств.</span><span class="sxs-lookup"><span data-stu-id="e6307-108">This topic documents a feature of the Windows Media Device Manager SDK.</span></span> <span data-ttu-id="e6307-109">Рекомендуется выполнить миграцию приложения для использования API переносных устройств Windows.</span><span class="sxs-lookup"><span data-stu-id="e6307-109">We recommend that you migrate your application to use the Windows Portable Devices API.</span></span> <span data-ttu-id="e6307-110">Дополнительные сведения см. в пакете SDK для переносных устройств Windows.</span><span class="sxs-lookup"><span data-stu-id="e6307-110">For more information, see the Windows Portable Devices SDK.</span></span>

<span data-ttu-id="e6307-111">Диспетчер устройств Windows Media определяет следующие перечисления.</span><span class="sxs-lookup"><span data-stu-id="e6307-111">Windows Media Device Manager defines the following enumerations.</span></span>



| <span data-ttu-id="e6307-112">Тип перечисления</span><span class="sxs-lookup"><span data-stu-id="e6307-112">Enumeration type</span></span>                                                                  | <span data-ttu-id="e6307-113">Описание</span><span class="sxs-lookup"><span data-stu-id="e6307-113">Description</span></span>                                                                                     |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6307-114">**\_ \_ \_ форма допустимых \_ значений \_ вмдм enum Prop**</span><span class="sxs-lookup"><span data-stu-id="e6307-114">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md) | <span data-ttu-id="e6307-115">Описывает возможные формы допустимых значений для свойства.</span><span class="sxs-lookup"><span data-stu-id="e6307-115">Describes possible forms of valid values for a property.</span></span>                                        |
| [<span data-ttu-id="e6307-116">**ВМДМ \_ Поиск \_ области**</span><span class="sxs-lookup"><span data-stu-id="e6307-116">**WMDM\_FIND\_SCOPE**</span></span>](wmdm-find-scope.md)                                      | <span data-ttu-id="e6307-117">Определяет область объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="e6307-117">Defines the scope of the storage object.</span></span>                                                        |
| [<span data-ttu-id="e6307-118">**ВМДМ \_ форматкоде**</span><span class="sxs-lookup"><span data-stu-id="e6307-118">**WMDM\_FORMATCODE**</span></span>](wmdm-formatcode.md)                                       | <span data-ttu-id="e6307-119">Определяет список кодов форматов, описывающих типы содержимого, передаваемые на устройство и с устройства.</span><span class="sxs-lookup"><span data-stu-id="e6307-119">Defines a list of format codes that describe types of content transferred to and from a device.</span></span> |
| [<span data-ttu-id="e6307-120">**\_тип сеанса \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="e6307-120">**WMDM\_SESSION\_TYPE**</span></span>](wmdm-session-type.md)                                  | <span data-ttu-id="e6307-121">Определяет тип сеанса.</span><span class="sxs-lookup"><span data-stu-id="e6307-121">Defines the session type.</span></span>                                                                       |
| [<span data-ttu-id="e6307-122">**\_ \_ режим перечисления вмдм в хранилище \_**</span><span class="sxs-lookup"><span data-stu-id="e6307-122">**WMDM\_STORAGE\_ENUM\_MODE**</span></span>](wmdm-storage-enum-mode.md)                       | <span data-ttu-id="e6307-123">Определяет способ перечисления содержимого в хранилище.</span><span class="sxs-lookup"><span data-stu-id="e6307-123">Defines how the content on the storage is to be enumerated.</span></span>                                     |
| [<span data-ttu-id="e6307-124">**\_ \_ тип данных тега вмдм**</span><span class="sxs-lookup"><span data-stu-id="e6307-124">**WMDM\_TAG\_DATATYPE**</span></span>](wmdm-tag-datatype.md)                                  | <span data-ttu-id="e6307-125">Определяет тип данных.</span><span class="sxs-lookup"><span data-stu-id="e6307-125">Defines a data type.</span></span>                                                                            |
| [<span data-ttu-id="e6307-126">**вмдммессаже**</span><span class="sxs-lookup"><span data-stu-id="e6307-126">**WMDMMessage**</span></span>](wmdmmessage.md)                                                | <span data-ttu-id="e6307-127">Определяет типы сообщений и состояния.</span><span class="sxs-lookup"><span data-stu-id="e6307-127">Defines message types and states.</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="e6307-128">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e6307-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6307-129">**Справочник по программированию**</span><span class="sxs-lookup"><span data-stu-id="e6307-129">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 




