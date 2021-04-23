---
description: Свойство SOURCELIST представляет собой разделенный точками с запятой список путей к сетевым или URL-адресам для пакета установки приложения.
ms.assetid: 9dc1e195-a108-4f8f-b008-e08fc7658fc0
title: Свойство SOURCELIST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5384504c337aeb9f1848f59efb2c6abaee5887b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651641"
---
# <a name="sourcelist-property"></a><span data-ttu-id="5df0a-103">Свойство SOURCELIST</span><span class="sxs-lookup"><span data-stu-id="5df0a-103">SOURCELIST property</span></span>

<span data-ttu-id="5df0a-104">Свойство **SourceList** представляет собой разделенный точками с запятой список путей к сетевым или URL-адресам для пакета установки приложения.</span><span class="sxs-lookup"><span data-stu-id="5df0a-104">The **SOURCELIST** property is a semicolon-delimited list of network or URL source paths to the application's installation package.</span></span> <span data-ttu-id="5df0a-105">Этот список добавляется к концу существующего исходного списка каждого пользователя для приложения.</span><span class="sxs-lookup"><span data-stu-id="5df0a-105">This list is appended to the end of each user's existing source list for the application.</span></span> <span data-ttu-id="5df0a-106">Установщик находит источник путем перечисления списка исходных путей и использует первое доступное место, которое он находит.</span><span class="sxs-lookup"><span data-stu-id="5df0a-106">The installer locates a source by enumerating the list of source paths and uses the first accessible location it finds.</span></span> <span data-ttu-id="5df0a-107">В оставшейся части установки можно использовать только этот источник.</span><span class="sxs-lookup"><span data-stu-id="5df0a-107">Only this source can be used for the remainder of the installation.</span></span> <span data-ttu-id="5df0a-108">Поэтому каждый путь, указанный в исходном списке, должен находиться в расположении с полным исходным кодом для приложения.</span><span class="sxs-lookup"><span data-stu-id="5df0a-108">Each path specified in the source list must therefore be to a location having a complete source for the application.</span></span> <span data-ttu-id="5df0a-109">Все дерево каталогов в каждом исходном расположении должно быть одинаковым и должно включать все необходимые исходные файлы, включая все CAB.</span><span class="sxs-lookup"><span data-stu-id="5df0a-109">The entire directory tree at each source location must be the same and must include all of the required source files, including any cabinets.</span></span> <span data-ttu-id="5df0a-110">В каждом расположении должен быть MSI файл с тем же именем файла и кодом продукта.</span><span class="sxs-lookup"><span data-stu-id="5df0a-110">Each location must have an .msi file with the same file name and product code.</span></span>

## <a name="default-value"></a><span data-ttu-id="5df0a-111">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5df0a-111">Default Value</span></span>

<span data-ttu-id="5df0a-112">Установщик проверяет только свойство **SourceList** , если продукт еще не объявлен или не установлен.</span><span class="sxs-lookup"><span data-stu-id="5df0a-112">The installer only checks the **SOURCELIST** property if the product has not already been advertised or installed.</span></span> <span data-ttu-id="5df0a-113">Во всех остальных случаях установщик использует существующий список источников, который находится в реестре.</span><span class="sxs-lookup"><span data-stu-id="5df0a-113">In all other cases the installer uses the existing source list that is in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="5df0a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5df0a-114">Remarks</span></span>

<span data-ttu-id="5df0a-115">Источники, добавленные с помощью свойства **SourceList** , добавляются непосредственно в конец списка для каждого типа источника и всегда поступают после источника по умолчанию, заданного свойством [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="5df0a-115">Sources added using the **SOURCELIST** property are added directly to the end of the list for each type of source and always come after the default source specified by the [**SourceDir**](sourcedir.md) property.</span></span>

<span data-ttu-id="5df0a-116">Для установщик Windows число источников в свойстве **SourceList** не ограничено.</span><span class="sxs-lookup"><span data-stu-id="5df0a-116">For Windows Installer the number of sources in the **SOURCELIST** property is unlimited.</span></span> <span data-ttu-id="5df0a-117">[**Мсисаурцелистаддсаурце**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) можно использовать для добавления сетевых источников.</span><span class="sxs-lookup"><span data-stu-id="5df0a-117">[**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) can be used to add network sources.</span></span>

## <a name="requirements"></a><span data-ttu-id="5df0a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5df0a-118">Requirements</span></span>



| <span data-ttu-id="5df0a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5df0a-119">Requirement</span></span> | <span data-ttu-id="5df0a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5df0a-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5df0a-121">Версия</span><span class="sxs-lookup"><span data-stu-id="5df0a-121">Version</span></span><br/> | <span data-ttu-id="5df0a-122">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5df0a-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5df0a-123">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5df0a-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5df0a-124">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5df0a-124">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5df0a-125">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="5df0a-125">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5df0a-126">См. также</span><span class="sxs-lookup"><span data-stu-id="5df0a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5df0a-127">Свойства</span><span class="sxs-lookup"><span data-stu-id="5df0a-127">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="5df0a-128">Отказоустойчивость источника</span><span class="sxs-lookup"><span data-stu-id="5df0a-128">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




