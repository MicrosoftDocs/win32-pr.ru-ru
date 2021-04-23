---
description: Пропертикэйс и GUID в портативных устройствах Windows
ms.assetid: 3f9e9f29-37dd-47b0-997e-de81966efce2
title: Пропертикэйс и GUID в портативных устройствах Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28cbe76b76eda04852cd1afcbb11b85b0a185d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911124"
---
# <a name="propertykeys-and-guids-in-windows-portable-devices"></a><span data-ttu-id="be980-103">Пропертикэйс и GUID в портативных устройствах Windows</span><span class="sxs-lookup"><span data-stu-id="be980-103">PROPERTYKEYs and GUIDs in Windows Portable Devices</span></span>

<span data-ttu-id="be980-104">Свойство или команда определяется структурой PROPERTYKEY.</span><span class="sxs-lookup"><span data-stu-id="be980-104">A property or command is identified by a PROPERTYKEY structure.</span></span> <span data-ttu-id="be980-105">Структура PROPERTYKEY состоит из двух частей: GUID (элемент fmtid) и DWORD (элемент PID).</span><span class="sxs-lookup"><span data-stu-id="be980-105">A PROPERTYKEY structure is made up of two parts: a GUID (the fmtid member) and a DWORD (the pid member).</span></span> <span data-ttu-id="be980-106">Часть идентификатора GUID используется для указания категории, которой принадлежит свойство или команда (т. е. связанные свойства относятся к одной и той же категории, а связанные команды относятся к одной и той же категории, поэтому они будут иметь одинаковые fmtid).</span><span class="sxs-lookup"><span data-stu-id="be980-106">The GUID part is used to indicate the category the property or command belongs to (that is, related properties belong to the same category and related commands belong to the same category; therefore they will have the same fmtid).</span></span> <span data-ttu-id="be980-107">Часть DWORD указывает на свойство или идентификатор команды и используется для различения отдельных свойств или команд в категории свойства или команды (то есть значения PID для свойств или команд в той же категории будут отличаться).</span><span class="sxs-lookup"><span data-stu-id="be980-107">The DWORD part indicates the property or command ID, and is used to distinguish the individual properties or commands within a property or command category (that is, the pid values for properties or commands in the same category will be different).</span></span>

<span data-ttu-id="be980-108">В разделе Reference этого документа описаны все значения PROPERTYKEY, определенные модулем WPD. Эти значения соответствуют командам, свойствам и ресурсам.</span><span class="sxs-lookup"><span data-stu-id="be980-108">The reference section of this document describes all the PROPERTYKEY values defined by WPD; these values correspond to commands, properties, and resources.</span></span> <span data-ttu-id="be980-109">При создании настраиваемого значения PROPERTYKEY необходимо определить новую категорию **GUID** . не используйте повторно значения **GUID** WPD или риск конфликта с существующими и будущими пропертикэйс, указанными в параметре WPD.</span><span class="sxs-lookup"><span data-stu-id="be980-109">If you create a custom PROPERTYKEY value, you should define a new **GUID** category; do not reuse the WPD **GUID** values or you risk conflicting with existing and future WPD-specified PROPERTYKEYs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be980-110">См. также</span><span class="sxs-lookup"><span data-stu-id="be980-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be980-111">**Общие сведения о приложении**</span><span class="sxs-lookup"><span data-stu-id="be980-111">**Application Overview**</span></span>](application-overview.md)
</dt> <dt>

[<span data-ttu-id="be980-112">**Команды**</span><span class="sxs-lookup"><span data-stu-id="be980-112">**Commands**</span></span>](commands.md)
</dt> <dt>

[<span data-ttu-id="be980-113">**Идентификаторы GUID формата объектов**</span><span class="sxs-lookup"><span data-stu-id="be980-113">**Object Format GUIDs**</span></span>](object-format-guids.md)
</dt> <dt>

[<span data-ttu-id="be980-114">**Свойства и атрибуты**</span><span class="sxs-lookup"><span data-stu-id="be980-114">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> <dt>

[<span data-ttu-id="be980-115">**Требования к объектам**</span><span class="sxs-lookup"><span data-stu-id="be980-115">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



