---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26e7eaae-f540-47d1-99ec-6af0fd223039
title: D (служба теневого копирования томов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25af02bd43c5130fa7ce60ed08ec4ab822ff1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692361"
---
# <a name="d-volume-shadow-copy-service"></a>D (служба теневого копирования томов)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) D [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [р](vssgloss-h.md) [. J](vssgloss-i.md) K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_database_component"></span><span id="BASE.VSSGLOSS_DATABASE_COMPONENT"></span>**компонент базы данных**
</dt> <dd>

Группа файлов, используемая базой данных и определяемая модулем записи, которая должна обрабатываться как единица во время операций резервного копирования и восстановления. См. также [*компонент*](vssgloss-c.md)"компонент [*файловой группы*](vssgloss-f.md)".

</dd> <dt>

<span id="base.vssgloss_default_provider"></span><span id="BASE.VSSGLOSS_DEFAULT_PROVIDER"></span>**поставщик по умолчанию**
</dt> <dd>

См. раздел [*поставщик системы*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_deleted_shadow_copy"></span><span id="BASE.VSSGLOSS_DELETED_SHADOW_COPY"></span>**Удаленная теневая копия**
</dt> <dd>

Удаленные теневые копии недоступны, и их нельзя сделать доступными в будущем.

</dd> <dt>

<span id="base.vssgloss_dependency"></span><span id="BASE.VSSGLOSS_DEPENDENCY"></span>**зависимостей**
</dt> <dd>

См. раздел [*зависимость компонентов*](vssgloss-c.md).

</dd> <dt>

<span id="base.vssgloss_device_object"></span><span id="BASE.VSSGLOSS_DEVICE_OBJECT"></span>**Объект устройства**
</dt> <dd>

Строка, указывающая "root" теневого копирования тома. На файлы и каталоги на тенев скопированном томе можно ссылаться, добавляя строку объекта устройства в соответствующий путь на исходном томе. Как получено в виде элемента **m \_ пвсзснапшотдевицеобжект** структуры [**\_ \_ снимков VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) , объект устройства не имеет обратной косой черты (" \\ ").

</dd> <dt>

<span id="base.vssgloss_diff_area"></span><span id="BASE.VSSGLOSS_DIFF_AREA"></span>**область копирования**
</dt> <dd>

Расположение на томе, где хранятся *разностные данные* . Это также называется дисковым пространством теневого копирования.

</dd> <dt>

<span id="base.vssgloss_differenced_files"></span><span id="BASE.VSSGLOSS_DIFFERENCED_FILES"></span>**файлы различий**
</dt> <dd>

Файлы, участвующие в операции добавочного или разностного резервного копирования, реализованные путем обновления целых файлов (в отличие от изменения разделов этих файлов с помощью частичной поддержки файлов). Например, если для реализации разностной резервной копии весь файл (а не только измененный раздел) копируется на носитель резервной копии, то этот файл является файлом различий. См. также [*операции добавочного резервного копирования*](vssgloss-i.md), *операции разностного резервного копирования*, [*Частичная поддержка файлов*](vssgloss-p.md).

</dd> <dt>

<span id="base.vssgloss_differential_backup_operations"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_BACKUP_OPERATIONS"></span>**операции разностного резервного копирования**
</dt> <dd>

Операция резервного копирования или восстановления выполнена только для файлов, созданных или измененных с момента последнего полного резервного копирования. См. также [*добавочные операции резервного копирования*](vssgloss-i.md), [*Частичная поддержка файлов*](vssgloss-p.md)и *файлы с разной разницей*.

</dd> <dt>

<span id="base.vssgloss_differential_data"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_DATA"></span>**разностные данные**
</dt> <dd>

Данные, которые могут быть применены к исходному тому для создания тома теневых копий. Это также называется копированием данных при записи, но в этой документации используется термин разностные данные.

</dd> <dt>

<span id="base.vssgloss_directed_targeting"></span><span id="BASE.VSSGLOSS_DIRECTED_TARGETING"></span>**направлено нацеливание**
</dt> <dd>

Режим восстановления, с помощью которого модуль записи указывает, что при восстановлении файла его (исходный файл) следует повторно сопоставить. Файл можно восстановить в новое расположение для восстановления и (или) диапазоны данных, восстановленные в другое смещение с расположением для восстановления.

</dd> </dl>

 

 



