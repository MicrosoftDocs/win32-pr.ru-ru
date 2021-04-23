---
description: Установщик Windows может настраивать установку программного обеспечения с помощью значений переменных, определенных в пакете установки или пользователем.
ms.assetid: b7b715e7-e92c-4b84-b60d-a0ff8412749b
title: Сведения о свойствах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc5d8154533cfebf4163983a149a547372ef4a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264213"
---
# <a name="about-properties"></a><span data-ttu-id="b762d-103">Сведения о свойствах</span><span class="sxs-lookup"><span data-stu-id="b762d-103">About Properties</span></span>

<span data-ttu-id="b762d-104">Установщик Windows может настраивать установку программного обеспечения с помощью значений переменных, определенных в пакете установки или пользователем.</span><span class="sxs-lookup"><span data-stu-id="b762d-104">Windows Installer can configure software installation by using the values of variables defined in an installation package or by the user.</span></span>

<span data-ttu-id="b762d-105">Во время установки установщик Windows использует три категории глобальных переменных:</span><span class="sxs-lookup"><span data-stu-id="b762d-105">Windows Installer uses three categories of global variables during an installation:</span></span>

-   <span data-ttu-id="b762d-106">Закрытые свойства. установщик использует закрытые свойства внутри, а их значения должны быть созданы в базе данных установки или установлены на значения, определенные операционной средой.</span><span class="sxs-lookup"><span data-stu-id="b762d-106">Private properties: The installer uses private properties internally and their values must be authored into the installation database or set to values determined by the operating environment.</span></span>
-   <span data-ttu-id="b762d-107">Открытые свойства: открытые свойства могут быть созданы в базе данных и изменены пользователем или системным администратором в командной строке путем применения преобразования или путем взаимодействия с созданным пользовательским интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="b762d-107">Public properties: Public properties can be authored into the database and changed by a user or system administrator on the command line, by applying a transform, or by interacting with an authored user interface.</span></span>
-   <span data-ttu-id="b762d-108">Ограниченные открытые свойства. в целях безопасности автор пакета установки может ограничивать общие свойства, которые может изменять пользователь.</span><span class="sxs-lookup"><span data-stu-id="b762d-108">Restricted public properties: For security purposes, the author of an installation package can restrict the public properties a user can change.</span></span>

<span data-ttu-id="b762d-109">Не все свойства должны быть определены в каждом пакете, существует небольшой набор обязательных свойств, которые должны быть определены в каждом пакете.</span><span class="sxs-lookup"><span data-stu-id="b762d-109">Not all properties need to be defined in every package, there is a small set of required properties that must be defined in every package.</span></span> <span data-ttu-id="b762d-110">Установщик устанавливает значения свойств в определенном порядке приоритета.</span><span class="sxs-lookup"><span data-stu-id="b762d-110">The installer sets the values of properties in a particular order of precedence.</span></span>

[<span data-ttu-id="b762d-111">Закрытые свойства</span><span class="sxs-lookup"><span data-stu-id="b762d-111">Private Properties</span></span>](private-properties.md)

[<span data-ttu-id="b762d-112">Открытые свойства</span><span class="sxs-lookup"><span data-stu-id="b762d-112">Public Properties</span></span>](public-properties.md)

[<span data-ttu-id="b762d-113">Ограниченные открытые свойства</span><span class="sxs-lookup"><span data-stu-id="b762d-113">Restricted Public Properties</span></span>](restricted-public-properties.md)

[<span data-ttu-id="b762d-114">Обязательные свойства</span><span class="sxs-lookup"><span data-stu-id="b762d-114">Required Properties</span></span>](required-properties.md)

[<span data-ttu-id="b762d-115">Порядок приоритета свойств</span><span class="sxs-lookup"><span data-stu-id="b762d-115">Order of Property Precedence</span></span>](order-of-property-precedence.md)

## <a name="related-topics"></a><span data-ttu-id="b762d-116">См. также</span><span class="sxs-lookup"><span data-stu-id="b762d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b762d-117">Использование свойств</span><span class="sxs-lookup"><span data-stu-id="b762d-117">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="b762d-118">Справочник по свойствам</span><span class="sxs-lookup"><span data-stu-id="b762d-118">Property Reference</span></span>](property-reference.md)
</dt> </dl>

 

 



