---
description: Поставщик служб каталогов дублирует классы и экземпляры из Active Directory в пространство имен протокола LDAP облегченного доступа к каталогу.
ms.assetid: 0215b614-cb10-4195-837d-bf81d523c560
ms.tgt_platform: multiple
title: Сопоставление Active Directory WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e94072ec0a95a8f64a072c7df5efd3973fc6a864e64bdca80c2841beac9097f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555194"
---
# <a name="mapping-active-directory-to-wmi"></a>Сопоставление Active Directory WMI

Поставщик служб каталогов дублирует классы и экземпляры из Active Directory в пространство имен протокола LDAP облегченного доступа к каталогу. Из-за фундаментальных различий в двух средах нельзя просто переименовать Active Directory классы и экземпляры и, надеюсь, получить правильный доступ к этим классам и экземплярам в WMI. Вместо этого поставщик служб каталогов следует правилам именования, чтобы сохранить связи между классами Active Directory и экземплярами.

Следующие разделы содержат сведения о сопоставлении Active Directory классах и экземплярах:

-   [Сопоставление классов Active Directory](mapping-active-directory-classes.md)
-   [Сопоставление экземпляров Active Directory](mapping-active-directory-instances.md)

> [!Note]  
> Дополнительные сведения о поддержке и установке этого компонента в определенной операционной системе см. в статье [доступность компонентов WMI в операционной системе](operating-system-availability-of-wmi-components.md).

 

 

 



