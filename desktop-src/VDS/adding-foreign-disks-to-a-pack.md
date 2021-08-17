---
description: Добавление внешних дисков в пакет
ms.assetid: 4018c742-1d23-47b9-a787-69bf8847b54a
title: Добавление внешних дисков в пакет
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26b83dd76cdc3f1637c07d8d9d818fdaf61fb093151f23aea06f0e9c7f81d6a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755459"
---
# <a name="adding-foreign-disks-to-a-pack"></a>Добавление внешних дисков в пакет

\[начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API Windows служба хранилища управления](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Чаще всего внешний диск — это динамический диск, который выделяется на одном компьютере и физически перемещается на другой компьютер. Однако любой диск, принадлежащий к пакету, отличному от сетевого пакета, считается внешним диском, принадлежащим к внешнему пакету диска.

В иностранном пакете установлен флаг **VDS \_ ПКФ \_ FOREIGN** , установленный в элементе **улфлагс** структуры [**\_ \_ prop пакета VDS**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) . Внешние пакеты всегда находятся вне сети.

В следующей процедуре описывается импорт одного или нескольких внешних дисков.

**Импорт одного или нескольких внешних дисков**

1.  Перемещение дисков на новый компьютер.
2.  На новом компьютере используйте метод [**ивдссервице:: reenumerat**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) для установки внешних дисков.
3.  Выберите пакет в Интернете, который будет использоваться в качестве целевого для получения внешних дисков. Если отсутствует сетевой пакет, используйте метод [**ивдссвпровидер:: креатепакк**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) для создания нового пустого пакета.
4.  Используйте метод [**ивдспакк:: мигратедискс**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) для импорта дисков в новый динамический пакет.
5.  Используйте метод [**ивдссвпровидер:: куерипаккс**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) , чтобы перечислить пакеты и [**Свойства ивдспакк::**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) GetEnumerator, чтобы определить, какой пакет теперь является веб-пакетом.

При создании нового пустого целевого пакета внешние диски фактически не переносятся в этот пакет. Вместо этого внешний пакет помечается как подключенный, для него снимается **\_ \_ внешний флаг VDS ПКФ** (так что пакет больше не является внешним), а созданный целевой пакет отбрасывается.

> [!Note]  
> Используйте метод [**ивдспакк:: адддиск**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) для добавления нераспределенных дисков — дисков, не заявленных поставщиком, в пакет. Нераспределенный диск не может быть внешним.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование VDS](using-vds.md)
</dt> <dt>

[**Ивдссервице:: перечисление**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**Ивдссвпровидер:: Креатепакк**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[**Ивдспакк:: Мигратедискс**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks)
</dt> <dt>

[**Ивдспакк:: Адддиск**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> </dl>

 

 
