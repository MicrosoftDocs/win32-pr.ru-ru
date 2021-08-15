---
description: Совместимость со схемой CIM
ms.assetid: 3738914d-dd33-4999-b37f-b4bb94689cd4
ms.tgt_platform: multiple
title: Совместимость со схемой CIM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3d87f1e40a52998f3a53a9b06f0572d8916b4a53663354ca5ffde67beaeed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319790"
---
# <a name="cim-schema-compatibility"></a>Совместимость со схемой CIM

ключевым компонентом инфраструктуры инструментарий управления Windows (WMI) (WMI) является объектно-ориентированная модель управляемых сущностей в системе. Модель соответствует стандарту, поддерживаемому задачей «Управление рабочим столом» ([DMTF](https://www.dmtf.org/standards/wsman)) и называется модель CIM (CIM). Схема CIM предоставляет единый механизм описания данных для любых данных, которые они предоставляют.

начиная с версии Windows 7 WMI совместим с версией схемы CIM 2.17.1 ( [https://www.dmtf.org/standards/cim/cim\_schema\_v2171/](https://www.dmtf.org/standards/cim/cim_schema_v2171) ). теперь пользователи могут компилировать схему, определенную в формате DMTF, на Windows компьютере.

## <a name="benefits-of-cim-schema-version-2171-compatibility"></a>Преимущества совместимости схемы CIM версии 2.17.1

-   когда пользователь скачивает файлы схемы CIM версии 2.17.1 или DMTF MOF, их можно успешно скомпилировать на целевом Windows компьютере.
-   Версия схемы CIM 2.17.1 добавлена поддержка BIOS, принтеров, стандартных сообщений, состояния операционной системы, современных парадигм управления питанием, виртуализации и безопасности.
-   Версия схемы CIM 2.1.7.1 предлагает дополнительную поддержку профилей. Дополнительные сведения см. в разделе [перекрестное сопоставление связей между пространствами имен](cross-namespace-association-traversal.md)

 

 



