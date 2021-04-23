---
description: Добавление внешних дисков в пакет
ms.assetid: 4018c742-1d23-47b9-a787-69bf8847b54a
title: Добавление внешних дисков в пакет
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fbfa2ff3d00857fd4e1b92e78f1760c25ce516b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349282"
---
# <a name="adding-foreign-disks-to-a-pack"></a><span data-ttu-id="41f3e-103">Добавление внешних дисков в пакет</span><span class="sxs-lookup"><span data-stu-id="41f3e-103">Adding Foreign Disks to a Pack</span></span>

<span data-ttu-id="41f3e-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="41f3e-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="41f3e-105">Чаще всего внешний диск — это динамический диск, который выделяется на одном компьютере и физически перемещается на другой компьютер.</span><span class="sxs-lookup"><span data-stu-id="41f3e-105">Most commonly, a foreign disk is a dynamic disk that is allocated on one computer and physically moved to another computer.</span></span> <span data-ttu-id="41f3e-106">Однако любой диск, принадлежащий к пакету, отличному от сетевого пакета, считается внешним диском, принадлежащим к внешнему пакету диска.</span><span class="sxs-lookup"><span data-stu-id="41f3e-106">However, any disk that belongs to a pack other than the online pack is considered to be a foreign disk that belongs to a foreign disk pack.</span></span>

<span data-ttu-id="41f3e-107">В иностранном пакете установлен флаг **VDS \_ ПКФ \_ FOREIGN** , установленный в элементе **улфлагс** структуры [**\_ \_ prop пакета VDS**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) .</span><span class="sxs-lookup"><span data-stu-id="41f3e-107">A foreign pack has the **VDS\_PKF\_FOREIGN** flag set in the **ulFlags** member of the [**VDS\_PACK\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) structure.</span></span> <span data-ttu-id="41f3e-108">Внешние пакеты всегда находятся вне сети.</span><span class="sxs-lookup"><span data-stu-id="41f3e-108">Foreign packs are always offline.</span></span>

<span data-ttu-id="41f3e-109">В следующей процедуре описывается импорт одного или нескольких внешних дисков.</span><span class="sxs-lookup"><span data-stu-id="41f3e-109">The following procedure describes how to import one or more foreign disks.</span></span>

<span data-ttu-id="41f3e-110">**Импорт одного или нескольких внешних дисков**</span><span class="sxs-lookup"><span data-stu-id="41f3e-110">**To import one or more foreign disks**</span></span>

1.  <span data-ttu-id="41f3e-111">Перемещение дисков на новый компьютер.</span><span class="sxs-lookup"><span data-stu-id="41f3e-111">Move disks to the new computer.</span></span>
2.  <span data-ttu-id="41f3e-112">На новом компьютере используйте метод [**ивдссервице:: reenumerat**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) для установки внешних дисков.</span><span class="sxs-lookup"><span data-stu-id="41f3e-112">On the new computer, use the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method to install the foreign disks.</span></span>
3.  <span data-ttu-id="41f3e-113">Выберите пакет в Интернете, который будет использоваться в качестве целевого для получения внешних дисков.</span><span class="sxs-lookup"><span data-stu-id="41f3e-113">Select the online pack to be the target pack that receives the foreign disks.</span></span> <span data-ttu-id="41f3e-114">Если отсутствует сетевой пакет, используйте метод [**ивдссвпровидер:: креатепакк**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) для создания нового пустого пакета.</span><span class="sxs-lookup"><span data-stu-id="41f3e-114">If no online pack exists, use the [**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) method to create a new empty pack.</span></span>
4.  <span data-ttu-id="41f3e-115">Используйте метод [**ивдспакк:: мигратедискс**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) для импорта дисков в новый динамический пакет.</span><span class="sxs-lookup"><span data-stu-id="41f3e-115">Use the [**IVdsPack::MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) method to import the disks to the new dynamic pack.</span></span>
5.  <span data-ttu-id="41f3e-116">Используйте метод [**ивдссвпровидер:: куерипаккс**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) , чтобы перечислить пакеты и [**Свойства ивдспакк::**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) GetEnumerator, чтобы определить, какой пакет теперь является веб-пакетом.</span><span class="sxs-lookup"><span data-stu-id="41f3e-116">Use the [**IVdsSwProvider::QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) method to enumerate the packs and [**IVdsPack::GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) to determine which pack is now the online pack.</span></span>

<span data-ttu-id="41f3e-117">При создании нового пустого целевого пакета внешние диски фактически не переносятся в этот пакет.</span><span class="sxs-lookup"><span data-stu-id="41f3e-117">If you create a new empty target pack, the foreign disks are not actually migrated to that pack.</span></span> <span data-ttu-id="41f3e-118">Вместо этого внешний пакет помечается как подключенный, для него снимается **\_ \_ внешний флаг VDS ПКФ** (так что пакет больше не является внешним), а созданный целевой пакет отбрасывается.</span><span class="sxs-lookup"><span data-stu-id="41f3e-118">Instead, the foreign pack is marked online, the **VDS\_PKF\_FOREIGN** flag for the pack is cleared (so the pack is no longer foreign), and the target pack that you created is discarded.</span></span>

> [!Note]  
> <span data-ttu-id="41f3e-119">Используйте метод [**ивдспакк:: адддиск**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) для добавления нераспределенных дисков — дисков, не заявленных поставщиком, в пакет.</span><span class="sxs-lookup"><span data-stu-id="41f3e-119">Use the [**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) method to add unallocated disks—disks not claimed by a provider—to a pack.</span></span> <span data-ttu-id="41f3e-120">Нераспределенный диск не может быть внешним.</span><span class="sxs-lookup"><span data-stu-id="41f3e-120">An unallocated disk cannot be foreign.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="41f3e-121">См. также</span><span class="sxs-lookup"><span data-stu-id="41f3e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41f3e-122">Использование VDS</span><span class="sxs-lookup"><span data-stu-id="41f3e-122">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="41f3e-123">**Ивдссервице:: перечисление**</span><span class="sxs-lookup"><span data-stu-id="41f3e-123">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="41f3e-124">**Ивдссвпровидер:: Креатепакк**</span><span class="sxs-lookup"><span data-stu-id="41f3e-124">**IVdsSwProvider::CreatePack**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[<span data-ttu-id="41f3e-125">**Ивдспакк:: Мигратедискс**</span><span class="sxs-lookup"><span data-stu-id="41f3e-125">**IVdsPack::MigrateDisks**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks)
</dt> <dt>

[<span data-ttu-id="41f3e-126">**Ивдспакк:: Адддиск**</span><span class="sxs-lookup"><span data-stu-id="41f3e-126">**IVdsPack::AddDisk**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> </dl>

 

 
