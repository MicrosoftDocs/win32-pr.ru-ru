---
title: APIP для развертывание пакета
description: Сведения об API развертывания пакетов, который можно использовать для установки, обновления и удаления пакетов приложений в системе. Каждый пакет приложения содержит файлы, составляющие приложение Windows, и файл манифеста, описывающий программное обеспечение для Windows.
ms.assetid: E2D408E1-6048-4D15-8BF4-69FF6ACF7BD2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a7559739d721781101fad804ebb040333c71c9
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "105700837"
---
# <a name="package-deployment-api"></a><span data-ttu-id="1728b-104">APIP для развертывание пакета</span><span class="sxs-lookup"><span data-stu-id="1728b-104">Package deployment API</span></span>

<span data-ttu-id="1728b-105">Сведения об API развертывания пакетов, который можно использовать для установки, обновления и удаления пакетов приложений в системе.</span><span class="sxs-lookup"><span data-stu-id="1728b-105">Learn about the package deployment API, which you can use to install, update, and uninstall app packages on the system.</span></span> <span data-ttu-id="1728b-106">Каждый пакет приложения содержит файлы, составляющие приложение Windows, и файл манифеста, описывающий программное обеспечение для Windows.</span><span class="sxs-lookup"><span data-stu-id="1728b-106">Each app package contains the files that constitute a Windows app, and a manifest file that describes the software to Windows.</span></span>

## <a name="windows-runtime-reference"></a><span data-ttu-id="1728b-107">Справочные материалы по среде выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="1728b-107">Windows Runtime reference</span></span>

-   [<span data-ttu-id="1728b-108">**Windows.Management.Deployment**</span><span class="sxs-lookup"><span data-stu-id="1728b-108">**Windows.Management.Deployment**</span></span>](/uwp/api/Windows.Management.Deployment)

## <a name="related-topics"></a><span data-ttu-id="1728b-109">См. также</span><span class="sxs-lookup"><span data-stu-id="1728b-109">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1728b-110">**Примеры**</span><span class="sxs-lookup"><span data-stu-id="1728b-110">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="1728b-111">Пример добавления пакета приложения (Аддпаккаже)</span><span class="sxs-lookup"><span data-stu-id="1728b-111">Add app package sample (AddPackage)</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PackageManagerAddPackage)
</dt> <dt>

[<span data-ttu-id="1728b-112">Пример перечисления пакетов приложений (Финдпаккажес)</span><span class="sxs-lookup"><span data-stu-id="1728b-112">Enumerate app packages sample (FindPackages)</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PackageManagerFindPackages)
</dt> <dt>

[<span data-ttu-id="1728b-113">Перечислить пакеты приложений по имени и образцу издателя (Финдпаккажесбинамеандпублишер)</span><span class="sxs-lookup"><span data-stu-id="1728b-113">Enumerate app packages by name and publisher sample (FindPackagesByNameAndPublisher)</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PackageManagerFindPackagesByNameAndPublisher)
</dt> <dt>

[<span data-ttu-id="1728b-114">Пример перечисления пакетов приложений по идентификатору безопасности пользователя (Финдпаккажесбюсерсекуритид)</span><span class="sxs-lookup"><span data-stu-id="1728b-114">Enumerate app packages by user SID sample (FindPackagesByUserSecurityId)</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PackageManagerFindPackagesByUserSecurityIda)
</dt> <dt>

[<span data-ttu-id="1728b-115">Пример удаления пакета приложения (Ремовепаккаже)</span><span class="sxs-lookup"><span data-stu-id="1728b-115">Remove app package sample (RemovePackage)</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PackageManagerRemovePackage)
</dt> <dt>

<span data-ttu-id="1728b-116">**Основные понятия**</span><span class="sxs-lookup"><span data-stu-id="1728b-116">**Concepts**</span></span>
</dt> <dt>

<span data-ttu-id="1728b-117">[Пакеты и развертывание приложений](/previous-versions/windows/apps/hh464929(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="1728b-117">[App packages and deployment](/previous-versions/windows/apps/hh464929(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="1728b-118">Словарь терминов</span><span class="sxs-lookup"><span data-stu-id="1728b-118">Glossary</span></span>](appx-packaging-glossary.md)
</dt> <dt>

<span data-ttu-id="1728b-119">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1728b-119">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1728b-120">Схема манифеста пакета приложений</span><span class="sxs-lookup"><span data-stu-id="1728b-120">App package manifest schema</span></span>](/uwp/schemas/appxpackage/appx-package-manifest)
</dt> <dt>

[<span data-ttu-id="1728b-121">API для упаковки</span><span class="sxs-lookup"><span data-stu-id="1728b-121">Packaging API</span></span>](interfaces.md)
</dt> <dt>

[<span data-ttu-id="1728b-122">API запросов пакетов</span><span class="sxs-lookup"><span data-stu-id="1728b-122">Package query API</span></span>](functions.md)
</dt> </dl>

 

 