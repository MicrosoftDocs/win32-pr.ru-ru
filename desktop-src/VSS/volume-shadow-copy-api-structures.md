---
description: В API теневого копирования томов определены следующие структуры.
ms.assetid: 20cf12e4-4611-4e39-9f6f-e29f15e58b36
title: Структуры API теневого копирования томов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f95527f505430e0283b44d233605febb5695cada3f9740e850945f58e751f3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590556"
---
# <a name="volume-shadow-copy-api-structures"></a>Структуры API теневого копирования томов

В API теневого копирования томов определены следующие структуры.



| structure                                                           | Описание                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_КОМПОНЕНТИНФО VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)                     | Содержит сведения об определенном компоненте.                                                                                                                                                                                                                       |
| [**\_ \_ prop области копирования \_ VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_area_prop)                 | Описывает связи между исходными томами, содержащими исходные данные файлов и тома, содержащие область хранения теневых копий.                                                                                                                                |
| [**\_prop для \_ тома \_ diff в VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_volume_prop)             | Описывает том области хранения теневых копий.                                                                                                                                                                                                                        |
| [**\_ \_ prop объекта для службы VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop)             | Описание свойств тома, тома хранилища теневых копий или области хранения теневых копий.                                                                                                                                                                    |
| [**\_ \_ объединение объектов для службы VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-__midl___midl_itf_vsmgmt_0000_0000_0001)           | Объединение структур [**prop для \_ тома \_ VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_prop), [**\_ \_ \_ props в VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_volume_prop)и структуры " [**\_ \_ \_ prop" области копирования VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_area_prop) , используемой структурой [**\_ \_ \_ prop объекта службы VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop) . |
| [**\_prop объекта \_ VSS**](/windows/desktop/api/Vss/ns-vss-vss_object_prop)                        | Описание свойств поставщика, тома, теневой копии или набора теневых копий.                                                                                                                                                                                    |
| [**\_объединение объектов \_ VSS**](/windows/desktop/api/Vss/ns-vss-__midl___midl_itf_vss_0000_0000_0001)                      | Объединение структур свойств [**\_ snapshot \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) и [**\_ \_ prop поставщика**](/windows/desktop/api/Vss/ns-vss-vss_provider_prop) VSS, используемых структурой [**\_ \_ свойств объекта VSS**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) .                                                                    |
| [**\_prop поставщика \_ VSS**](/windows/desktop/api/Vss/ns-vss-vss_provider_prop)                    | Задает свойства поставщика теневого копирования.                                                                                                                                                                                                                          |
| [**\_prop для моментального снимка VSS \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)                    | Содержит свойства набора теневых копий или теневого копирования.                                                                                                                                                                                                        |
| [**\_prop тома \_ VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_prop)                        | Описание свойств тома источника теневой копии.                                                                                                                                                                                                            |
| [**\_ \_ сведения о защите томов VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info) | Содержит сведения о уровне защиты теневого копирования тома.                                                                                                                                                                                                 |



 

 

 



