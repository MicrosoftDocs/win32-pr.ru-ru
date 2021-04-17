---
description: Поставщик служб каталогов дублирует классы и экземпляры из Active Directory в пространство имен протокола LDAP облегченного доступа к каталогу.
ms.assetid: 0215b614-cb10-4195-837d-bf81d523c560
ms.tgt_platform: multiple
title: Сопоставление Active Directory WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e0162f722eb8a053270ac2a8e75eaed4f1cd405
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663775"
---
# <a name="mapping-active-directory-to-wmi"></a>Сопоставление Active Directory WMI

Поставщик служб каталогов дублирует классы и экземпляры из Active Directory в пространство имен протокола LDAP облегченного доступа к каталогу. Из-за фундаментальных различий в двух средах нельзя просто переименовать Active Directory классы и экземпляры и, надеюсь, получить правильный доступ к этим классам и экземплярам в WMI. Вместо этого поставщик служб каталогов следует правилам именования, чтобы сохранить связи между классами Active Directory и экземплярами.

Следующие разделы содержат сведения о сопоставлении Active Directory классах и экземплярах:

-   [Сопоставление классов Active Directory](mapping-active-directory-classes.md)
-   [Сопоставление экземпляров Active Directory](mapping-active-directory-instances.md)

> [!Note]  
> Дополнительные сведения о поддержке и установке этого компонента в определенной операционной системе см. в статье [доступность компонентов WMI в операционной системе](operating-system-availability-of-wmi-components.md).

 

 

 



