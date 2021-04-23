---
description: Защищаемые объекты используют формат маски доступа, в котором четыре старших бита указывают общие права доступа.
ms.assetid: e18cede9-9bf7-4866-850b-5d7fa43a5b0f
title: Универсальные права доступа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adff14aa259222bc37096b8a94f30cffb5ab0876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816024"
---
# <a name="generic-access-rights"></a><span data-ttu-id="c9462-103">Универсальные права доступа</span><span class="sxs-lookup"><span data-stu-id="c9462-103">Generic Access Rights</span></span>

<span data-ttu-id="c9462-104">Защищаемые объекты используют [Формат маски доступа](access-mask-format.md) , в котором четыре старших бита указывают общие права доступа.</span><span class="sxs-lookup"><span data-stu-id="c9462-104">Securable objects use an [access mask format](access-mask-format.md) in which the four high-order bits specify generic access rights.</span></span> <span data-ttu-id="c9462-105">Каждый тип защищаемого объекта сопоставляет эти биты с набором стандартных и зависящих от объекта прав доступа.</span><span class="sxs-lookup"><span data-stu-id="c9462-105">Each type of securable object maps these bits to a set of its standard and object-specific access rights.</span></span> <span data-ttu-id="c9462-106">Например, объект файла Windows сопоставляет универсальный \_ бит чтения с \_ элементом управления для чтения и синхронизирует стандартные права доступа, а также разрешения на доступ к объектам для чтения и чтения файлов \_ \_ , \_ Чтение \_ атрибутов EA и File read data \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c9462-106">For example, a Windows file object maps the GENERIC\_READ bit to the READ\_CONTROL and SYNCHRONIZE standard access rights and to the FILE\_READ\_DATA, FILE\_READ\_EA, and FILE\_READ\_ATTRIBUTES object-specific access rights.</span></span> <span data-ttu-id="c9462-107">Другие типы объектов сопоставляют универсальный \_ бит чтения с любым набором прав доступа, подходящим для этого типа объекта.</span><span class="sxs-lookup"><span data-stu-id="c9462-107">Other types of objects map the GENERIC\_READ bit to whatever set of access rights is appropriate for that type of object.</span></span>

<span data-ttu-id="c9462-108">С помощью универсальных прав доступа можно указать тип доступа, необходимый при открытии маркера для объекта.</span><span class="sxs-lookup"><span data-stu-id="c9462-108">You can use generic access rights to specify the type of access you need when you are opening a handle to an object.</span></span> <span data-ttu-id="c9462-109">Обычно это проще, чем указывать все соответствующие стандартные и специальные права.</span><span class="sxs-lookup"><span data-stu-id="c9462-109">This is typically simpler than specifying all the corresponding standard and specific rights.</span></span>

<span data-ttu-id="c9462-110">В следующей таблице показаны константы, определенные для общих прав доступа.</span><span class="sxs-lookup"><span data-stu-id="c9462-110">The following table shows the constants defined for the generic access rights.</span></span>



| <span data-ttu-id="c9462-111">Константа</span><span class="sxs-lookup"><span data-stu-id="c9462-111">Constant</span></span>         | <span data-ttu-id="c9462-112">Универсальное значение</span><span class="sxs-lookup"><span data-stu-id="c9462-112">Generic meaning</span></span>            |
|------------------|----------------------------|
| <span data-ttu-id="c9462-113">УНИВЕРСАЛЬНые \_ все</span><span class="sxs-lookup"><span data-stu-id="c9462-113">GENERIC\_ALL</span></span>     | <span data-ttu-id="c9462-114">Все возможные права доступа</span><span class="sxs-lookup"><span data-stu-id="c9462-114">All possible access rights</span></span> |
| <span data-ttu-id="c9462-115">УНИВЕРСАЛЬНое \_ выполнение</span><span class="sxs-lookup"><span data-stu-id="c9462-115">GENERIC\_EXECUTE</span></span> | <span data-ttu-id="c9462-116">Доступ для выполнения</span><span class="sxs-lookup"><span data-stu-id="c9462-116">Execute access</span></span>             |
| <span data-ttu-id="c9462-117">УНИВЕРСАЛЬНое \_ чтение</span><span class="sxs-lookup"><span data-stu-id="c9462-117">GENERIC\_READ</span></span>    | <span data-ttu-id="c9462-118">Доступ для чтения</span><span class="sxs-lookup"><span data-stu-id="c9462-118">Read access</span></span>                |
| <span data-ttu-id="c9462-119">УНИВЕРСАЛЬНая \_ запись</span><span class="sxs-lookup"><span data-stu-id="c9462-119">GENERIC\_WRITE</span></span>   | <span data-ttu-id="c9462-120">Доступ на запись</span><span class="sxs-lookup"><span data-stu-id="c9462-120">Write access</span></span>               |



 

<span data-ttu-id="c9462-121">Приложения, определяющие закрытые защищаемые объекты, также могут использовать универсальные права доступа.</span><span class="sxs-lookup"><span data-stu-id="c9462-121">Applications that define private securable objects can also use the generic access rights.</span></span>

 

 



