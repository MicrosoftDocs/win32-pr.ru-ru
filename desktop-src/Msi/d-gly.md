---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: d6dd73e7-657f-4f71-8e9b-70369cb21972
title: D (установщик Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e2673f845d85db88d55cbcd53838f7e682dbe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810390"
---
# <a name="d-windows-installer"></a>D (установщик Windows)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) р [. J K](i-gly.md) L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**Функция базы данных**
</dt> <dd>

Обращается к базе данных установщика. Эти функции предоставляются главным образом для использования [*средствами разработки пакетов установщика*](i-gly.md) , и они не предназначены для использования при вызове служб установщика. Дополнительные сведения см. в разделе [функции базы данных](database-functions.md) и [Справочник по функциям установщика](installer-function-reference.md).

</dd> <dt>

<span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**маркер базы данных**
</dt> <dd>

Требуется для работы с базой данных. Дополнительные сведения см. [в разделе Получение маркера базы данных](obtaining-a-database-handle.md).

</dd> <dt>

<span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**Дельта исправления**
</dt> <dd>

Разностное обновление — это установщик Windows исправление с разностным сжатием, созданное с помощью средства, такого как Patchwiz.dll, которое поддерживает разностное сжатие. Исправления, использующие разностное сжатие, могут уменьшить размер обновления, предоставляя только различия (разности) между существующими файлами на целевом компьютере и новыми файлами. Затем нужные новые файлы будут синтезированы на основе существующих файлов и загруженных дельты. Дополнительные сведения о технологии разностного сжатия см. в разделе [интерфейс программирования приложений для разностного сжатия](https://msdn.microsoft.com/library/ms811406.aspx).

</dd> </dl>

 

 



