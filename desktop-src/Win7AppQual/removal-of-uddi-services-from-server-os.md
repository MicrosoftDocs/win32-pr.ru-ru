---
description: .
ms.assetid: 5ebc8c4c-acee-4658-8d36-30fbb17b1ef1
title: Удаление служб UDDI с серверной операционной системы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7681167177b850ba44ac0fc26e019c7393008b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651124"
---
# <a name="removal-of-uddi-services-from-server-operating-system"></a><span data-ttu-id="c2a7d-103">Удаление служб UDDI с серверной операционной системы</span><span class="sxs-lookup"><span data-stu-id="c2a7d-103">Removal of UDDI Services from Server Operating System</span></span>

## <a name="affected-platform"></a><span data-ttu-id="c2a7d-104">Затронутая платформа</span><span class="sxs-lookup"><span data-stu-id="c2a7d-104">Affected Platform</span></span>

<span data-ttu-id="c2a7d-105">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c2a7d-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="c2a7d-106">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="c2a7d-106">Feature Impact</span></span>

<span data-ttu-id="c2a7d-107">**Серьезность** — средний</span><span class="sxs-lookup"><span data-stu-id="c2a7d-107">**Severity** - Medium</span></span>  
<span data-ttu-id="c2a7d-108">**Частота** -низкая</span><span class="sxs-lookup"><span data-stu-id="c2a7d-108">**Frequency** - Low</span></span>  

## <a name="description"></a><span data-ttu-id="c2a7d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="c2a7d-109">Description</span></span>

<span data-ttu-id="c2a7d-110">Корпорация Майкрософт удалила роль сервера служб UDDI (универсальное описание, обнаружение и интеграция) из Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c2a7d-110">Microsoft has removed the UDDI (Universal Description, Discovery, and Integration) Services server role from Windows Server 2008 R2.</span></span> <span data-ttu-id="c2a7d-111">Будущие выпуски служб UDDI будут входить в состав продукта Microsoft BizTalk.</span><span class="sxs-lookup"><span data-stu-id="c2a7d-111">Future releases of UDDI Services will be part of the Microsoft BizTalk product.</span></span> <span data-ttu-id="c2a7d-112">При повторном выравнивании и консолидации продукта Корпорация Майкрософт будет лучше обслуживать на рынке архитектуры, ориентированной на службы (SOA).</span><span class="sxs-lookup"><span data-stu-id="c2a7d-112">This product realignment and consolidation positions Microsoft to better serve the services-oriented architecture (SOA) market.</span></span>

<span data-ttu-id="c2a7d-113">Первым выпуском служб UDDI, выпущенным в Windows Server 2008, будет соответствие стандартам UDDI v 3.0.</span><span class="sxs-lookup"><span data-stu-id="c2a7d-113">The first post-Windows Server 2008 release of UDDI Services will be UDDI v3.0 standards compliant.</span></span> <span data-ttu-id="c2a7d-114">Он будет поставляться как часть выпуска BizTalk Server 2009.</span><span class="sxs-lookup"><span data-stu-id="c2a7d-114">It will ship as part of the BizTalk Server 2009 release.</span></span> <span data-ttu-id="c2a7d-115">Чтобы обеспечить удовлетворительное взаимодействие с пользователем, мы предлагаем пакет установки служб UDDI v3 для Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c2a7d-115">To meet our commitment to provide a satisfactory user experience, we will offer a UDDI Services v3 installation package for Windows Server 2008 R2.</span></span>

## <a name="manifestation"></a><span data-ttu-id="c2a7d-116">Проявление</span><span class="sxs-lookup"><span data-stu-id="c2a7d-116">Manifestation</span></span>

<span data-ttu-id="c2a7d-117">Наличие предыдущих версий компонентов служб UDDI в системе блокирует обновление до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c2a7d-117">The presence of previous versions of UDDI Services components on the system blocks an upgrade to Windows Server 2008 R2.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="c2a7d-118">Снижение влияния</span><span class="sxs-lookup"><span data-stu-id="c2a7d-118">Mitigation of Impact</span></span>

<span data-ttu-id="c2a7d-119">Пользователи, которые развернули сайт служб UDDI с Windows Server 2003 или Windows Server 2008, могут не обновлять серверы, на которых работают службы UDDI, до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c2a7d-119">Users who have deployed a UDDI Services site from Windows Server 2003 or Windows Server 2008 can choose not to upgrade the servers running the UDDI Services to Windows Server 2008 R2.</span></span> <span data-ttu-id="c2a7d-120">Они также могут перемещать службы UDDI на выделенные поля Windows Server 2003 или Windows Server 2008, если необходимо обновить текущие поля служб UDDI.</span><span class="sxs-lookup"><span data-stu-id="c2a7d-120">They can also move the UDDI Services to dedicated Windows Server 2003 or Windows Server 2008 boxes if they have to upgrade the current UDDI Services boxes.</span></span>

## <a name="solution"></a><span data-ttu-id="c2a7d-121">Решение</span><span class="sxs-lookup"><span data-stu-id="c2a7d-121">Solution</span></span>

<span data-ttu-id="c2a7d-122">Рекомендуемое решение — развернуть службы UDDI версии 3.0 с BizTalk Server 2009 на компьютере под Windows Server 2008 R2, а затем перенести старый сайт на новый сайт.</span><span class="sxs-lookup"><span data-stu-id="c2a7d-122">The recommended solution is to deploy UDDI Services v3.0 from BizTalk Server 2009 onto a Windows Server 2008 R2 machine, and then to migrate the old site to the new site.</span></span> <span data-ttu-id="c2a7d-123">Службы UDDI версии 3.0 обеспечивают обратную совместимость со службами UDDI 2,0, поэтому все приложения, использующие службы UDDI, не затрагиваются.</span><span class="sxs-lookup"><span data-stu-id="c2a7d-123">UDDI Services v3.0 provides backward compatibility with UDDI Services 2.0, so any applications that are using UDDI Services will be unaffected.</span></span>

<span data-ttu-id="c2a7d-124">Для этого выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c2a7d-124">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="c2a7d-125">Настройте новый сайт служб UDDI версии 3.0 на компьютере, который уже загружен с Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c2a7d-125">Set up a new UDDI Services v3.0 site on a machine already loaded with Windows Server 2008 R2.</span></span> <span data-ttu-id="c2a7d-126">(Примечание. в распределенной настройке сайт UDDI версии 3.0 может состоять из нескольких компьютеров Windows Server 2008 R2.)</span><span class="sxs-lookup"><span data-stu-id="c2a7d-126">(Note: In a distributed setup, a UDDI v3.0 site can consist of more than one Windows Server 2008 R2 machines.)</span></span>
2.  <span data-ttu-id="c2a7d-127">Используйте средство переноса данных UDDI для переноса данных из старой базы данных служб UDDI в новую базу данных.</span><span class="sxs-lookup"><span data-stu-id="c2a7d-127">Use the UDDI data migration tool to migrate the data from the old UDDI Services database to the new database.</span></span>
3.  <span data-ttu-id="c2a7d-128">Создайте резервную копию старой базы данных служб UDDI, чтобы обеспечить возможность отката.</span><span class="sxs-lookup"><span data-stu-id="c2a7d-128">Back up the old UDDI Services database to ensure rollback capability.</span></span>
4.  <span data-ttu-id="c2a7d-129">Удалите старое программное обеспечение служб UDDI, а затем обновите эти поля до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c2a7d-129">Uninstall the old UDDI Services software and then upgrade those boxes to Windows Server 2008 R2.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="c2a7d-130">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="c2a7d-130">Links to Other Resources</span></span>

-   [<span data-ttu-id="c2a7d-131">Веб-сайт служб Microsoft UDDI</span><span class="sxs-lookup"><span data-stu-id="c2a7d-131">Microsoft UDDI Services website</span></span>](https://msdn.microsoft.com/biztalk/dd789428.aspx)
-   [<span data-ttu-id="c2a7d-132">Спецификации UDDI</span><span class="sxs-lookup"><span data-stu-id="c2a7d-132">UDDI specifications</span></span>](http://uddi.xml.org/specification)
-   [<span data-ttu-id="c2a7d-133">Загрузка служб UDDI версии 3.0 для Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c2a7d-133">UDDI Services v3.0 download for Windows Server 2008 R2</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=e4761835-70f0-4e8d-96c5-64818d54e06e)

 

 



