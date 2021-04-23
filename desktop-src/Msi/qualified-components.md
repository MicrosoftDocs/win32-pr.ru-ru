---
description: Квалифицированный компонент — это метод одноуровневого косвенного обращения, аналогичный указателю.
ms.assetid: b483fa7d-d31d-4855-89e5-f733541cd92d
title: Компоненты с квалификаторами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2197aade7f3efd5d73e666c190c4447cac9fe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909464"
---
# <a name="qualified-components"></a><span data-ttu-id="f0760-103">Компоненты с квалификаторами</span><span class="sxs-lookup"><span data-stu-id="f0760-103">Qualified Components</span></span>

<span data-ttu-id="f0760-104">Квалифицированный компонент — это метод одноуровневого косвенного обращения, аналогичный указателю.</span><span class="sxs-lookup"><span data-stu-id="f0760-104">A qualified component is a method of single-level indirection, similar to a pointer.</span></span> <span data-ttu-id="f0760-105">Квалифицированные компоненты в основном используются для группирования компонентов с параллельными функциями в категории.</span><span class="sxs-lookup"><span data-stu-id="f0760-105">Qualified components are primarily used to group components with parallel functionality into categories.</span></span> <span data-ttu-id="f0760-106">Например, если в [таблице Component](component-table.md) есть 30 компонентов, которые относятся к одному шаблону Microsoft Word Fax, локализованному на 30 языков, их можно объединить в категорию компонентов с квалификаторами с помощью [таблицы публишкомпонент](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="f0760-106">For example, if you have 30 components listed in the [Component table](component-table.md) that are the same Microsoft Word fax template localized into 30 languages, you can group these together into a category of qualified components by using the [PublishComponent table](publishcomponent-table.md).</span></span>

<span data-ttu-id="f0760-107">Квалифицированные компоненты добавляются в таблицу Component так же, как обычные компоненты.</span><span class="sxs-lookup"><span data-stu-id="f0760-107">Qualified components are entered in the Component table in the same way as ordinary components.</span></span> <span data-ttu-id="f0760-108">Каждый компонент должен иметь уникальный идентификатор GUID компонента и идентификатор компонента, указанные в таблице Component.</span><span class="sxs-lookup"><span data-stu-id="f0760-108">Every component must have a unique component ID GUID and component identifier specified in the Component table.</span></span> <span data-ttu-id="f0760-109">Кроме того, квалифицированные компоненты связаны с GUID категории и квалификатором текстовой строки в таблице Публишкомпонент.</span><span class="sxs-lookup"><span data-stu-id="f0760-109">In addition, qualified components are associated with a category GUID and a text-string qualifier in the PublishComponent table.</span></span> <span data-ttu-id="f0760-110">На полные компоненты ссылается GUID категории и квалификатор, который просто указывает на обычный компонент в таблице Component.</span><span class="sxs-lookup"><span data-stu-id="f0760-110">Qualified components are referenced by the category GUID and the qualifier, which just points to the ordinary component in the Component table.</span></span>

<span data-ttu-id="f0760-111">Например, идентификатор GUID уникального компонента может указывать на разные языковые версии библиотеки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0760-111">For example, a qualified component ID GUID can point to different language versions of a resource DLL.</span></span> <span data-ttu-id="f0760-112">В этом случае Группа локализованных библиотек DLL ресурсов состоит из категории, а строки идентификаторов национальных настроек (LCID) обычно используются в качестве квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="f0760-112">In this case, the group of localized resource DLLs comprises the category and the numeric locale identifiers (LCID) strings are commonly used as the qualifiers.</span></span> <span data-ttu-id="f0760-113">Разработчик может создать пакет установки, использующий эти компоненты для следующих задач:</span><span class="sxs-lookup"><span data-stu-id="f0760-113">A developer could author an installation package that uses these qualified components to do the following:</span></span>

-   <span data-ttu-id="f0760-114">Найдите путь к определенной языковой версии библиотеки ресурсов с помощью [**мсипровидекуалифиедкомпонент**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) или [**мсипровидекуалифиедкомпонентекс**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) и установите ресурс.</span><span class="sxs-lookup"><span data-stu-id="f0760-114">Find the path to a particular language version of the resource DLL using [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) or [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) and install the resource.</span></span>
-   <span data-ttu-id="f0760-115">Определите все языковые версии библиотеки DLL ресурсов, которые представлены путем вызова [**мсиенумкомпоненткуалифиерс**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span><span class="sxs-lookup"><span data-stu-id="f0760-115">Determine all of the language versions of the resource DLL that are present by calling [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>
-   <span data-ttu-id="f0760-116">Подготовьте приложение для поддержки дополнительных языков.</span><span class="sxs-lookup"><span data-stu-id="f0760-116">Prepare the application to support additional languages.</span></span> <span data-ttu-id="f0760-117">В будущем языковой пакет для приложения может использовать квалифицированный компонент для добавления дополнительных языковых версий библиотеки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0760-117">A future language pack for the application can use the qualified component to add more language versions of the resource DLL.</span></span>

<span data-ttu-id="f0760-118">Дополнительные сведения см. [в разделе Использование компонентов с квалификаторами](using-qualified-components.md).</span><span class="sxs-lookup"><span data-stu-id="f0760-118">For more information, see [Using Qualified Components](using-qualified-components.md).</span></span>

 

 



