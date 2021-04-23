---
description: В следующих разделах описывается использование встроенных свойств установщика и дополнительные свойства, определяемые автором пакета.
ms.assetid: 5a2f1cd4-2bbd-414a-a814-8b9fdab434b4
title: Использование свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edab44953f6ccd210d5baa3c446363a1131dc745
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145316"
---
# <a name="using-properties"></a><span data-ttu-id="33c69-103">Использование свойств</span><span class="sxs-lookup"><span data-stu-id="33c69-103">Using Properties</span></span>

<span data-ttu-id="33c69-104">В следующих разделах описывается использование встроенных свойств установщика и дополнительные свойства, определяемые автором пакета.</span><span class="sxs-lookup"><span data-stu-id="33c69-104">The following sections describe using the built-in installer properties and additional properties defined by the package author.</span></span> <span data-ttu-id="33c69-105">Свойства могут быть либо [открытыми свойствами](public-properties.md) , либо [закрытыми свойствами](private-properties.md).</span><span class="sxs-lookup"><span data-stu-id="33c69-105">Properties can be either [public properties](public-properties.md) or [private properties](private-properties.md).</span></span> <span data-ttu-id="33c69-106">Каждое свойство, которое должно быть определено при инициализации установщика, должно иметь имя и начальное значение, перечисленные в [таблице свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="33c69-106">Every property that needs to be defined upon initialization of the installer must have its name and initial value listed in the [Property table](property-table.md).</span></span> <span data-ttu-id="33c69-107">Свойства, имеющие значение null, не перечислены в таблице свойств.</span><span class="sxs-lookup"><span data-stu-id="33c69-107">Properties having a Null value are not listed in the Property table.</span></span> <span data-ttu-id="33c69-108">Можно получить или задать свойства из программ и пользовательских действий, а также задать общие свойства из командной строки.</span><span class="sxs-lookup"><span data-stu-id="33c69-108">You can get or set properties from programs and custom actions and set public properties from the command line.</span></span> <span data-ttu-id="33c69-109">Процесс установки можно изменить с помощью свойств в условных инструкциях.</span><span class="sxs-lookup"><span data-stu-id="33c69-109">The installation process can be modified by using properties in conditional statements.</span></span>

[<span data-ttu-id="33c69-110">Ограничения по именам свойств</span><span class="sxs-lookup"><span data-stu-id="33c69-110">Restrictions on Property Names</span></span>](restrictions-on-property-names.md)

[<span data-ttu-id="33c69-111">Инициализация значений свойств</span><span class="sxs-lookup"><span data-stu-id="33c69-111">Initialization of Property Values</span></span>](initialization-of-property-values.md)

[<span data-ttu-id="33c69-112">Получение и задание свойств</span><span class="sxs-lookup"><span data-stu-id="33c69-112">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)

[<span data-ttu-id="33c69-113">Использование свойств в условных инструкциях</span><span class="sxs-lookup"><span data-stu-id="33c69-113">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)

[<span data-ttu-id="33c69-114">Использование свойства каталога в пути</span><span class="sxs-lookup"><span data-stu-id="33c69-114">Using a Directory Property in a Path</span></span>](using-a-directory-property-in-a-path.md)

> [!Note]  
> <span data-ttu-id="33c69-115">Не используйте свойства для паролей и других сведений, которые должны оставаться защищенными.</span><span class="sxs-lookup"><span data-stu-id="33c69-115">Do not use properties for passwords or other information that must remain secure.</span></span> <span data-ttu-id="33c69-116">Установщик может записать значение свойства, созданного в таблице свойств, или создать во время выполнения в журнале или системном реестре.</span><span class="sxs-lookup"><span data-stu-id="33c69-116">The installer may write the value of a property authored into the Property table or created at runtime into a log or the system registry.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="33c69-117">См. также</span><span class="sxs-lookup"><span data-stu-id="33c69-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33c69-118">Сведения о свойствах</span><span class="sxs-lookup"><span data-stu-id="33c69-118">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="33c69-119">Справочник по свойствам</span><span class="sxs-lookup"><span data-stu-id="33c69-119">Property Reference</span></span>](property-reference.md)
</dt> </dl>

 

 



