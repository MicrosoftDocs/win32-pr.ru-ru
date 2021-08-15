---
description: Добавление буквы диска к LUN
ms.assetid: 3f350312-3f1f-4020-90d0-85521ea9c7c8
title: Добавление буквы диска к LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 388c59a2e1b719e792855460f45fa0c04add7502f8e06aba56f0416a212a9aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755503"
---
# <a name="adding-a-drive-letter-to-a-lun"></a>Добавление буквы диска к LUN

\[начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API Windows служба хранилища управления](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Буквы дисков можно назначать объектам томов напрямую; Однако если диск является объектом LUN, вы можете выполнить несколько дополнительных действий.

**Назначение буквы диска объекту LUN**

1.  При необходимости снимите маску LUN для локального узла.
    > [!Note]  
    > Вы не можете выполнять административные операции с объектом LUN, который снят с маски на другой компьютер в текущем сеансе службы VDS.

     

2.  Вызовите метод [**ивдссервице:: reenumerat**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) на компьютере, на котором работает поставщик оборудования.
3.  Инициализируйте LUN как базовый диск следующим образом:
    1.  Вызовите метод [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) объекта LUN, чтобы запросить интерфейс [**ивдсдиск**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) .
    2.  Чтобы создать базовый пакет, вызовите метод [**ивдссвпровидер:: креатепакк**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) .
    3.  Вызовите метод [**ивдспакк:: адддиск**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) , чтобы добавить диск в новый пакет.
4.  Создайте раздел на диске и получите объект тома следующим образом:
    1.  Чтобы создать секцию, вызовите метод [**ивдскреатепартитионекс:: креатепартитионекс**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) .
    2.  Вызовите метод [**ивдсасинк:: wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) асинхронного объекта, возвращаемого [**креатепартитионекс**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) , чтобы получить идентификатор тома из структуры [**\_ асинхронного \_ вывода VDS**](/windows/desktop/api/Vds/ns-vds-vds_async_output) .
    3.  Передайте идентификатор тома в качестве параметра методу [**ивдссервице:: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) , чтобы получить указатель на объект тома.
5.  Чтобы назначить букву диска, вызовите метод [**ивдсволумемф:: аддакцесспас**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) .

> [!Note]  
> Метод [**ивдсадванцеддиск:: ассигндривелеттер**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter) назначает буквы дисков секциям без связанных томов, таких как разделы OEM или ESP. Его нельзя использовать для назначения буквы диска объекту LUN.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование VDS](using-vds.md)
</dt> <dt>

[**Ивдссервице:: перечисление**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**ивдсдиск**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[**Ивдссвпровидер:: Креатепакк**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[**Ивдспакк:: Адддиск**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> <dt>

[**Ивдскреатепартитионекс:: Креатепартитионекс**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex)
</dt> <dt>

[**Ивдсасинк:: wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[**\_асинхронный \_ вывод VDS**](/windows/desktop/api/Vds/ns-vds-vds_async_output)
</dt> <dt>

[**Ивдсволумемф:: Аддакцесспас**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath)
</dt> <dt>

[**Ивдсадванцеддиск:: Ассигндривелеттер**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter)
</dt> </dl>

 

 
