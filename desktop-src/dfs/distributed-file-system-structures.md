---
description: Ниже приведены распределенная файловая система структуры DFS.
ms.assetid: f55ad3c0-0457-4d5a-a7d3-8eff744d573d
title: Структуры распределенная файловая система
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fc3351402c4721952cbfc4dc3fe3c6ac6d3a76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496581"
---
# <a name="distributed-file-system-structures"></a>Структуры распределенная файловая система

Ниже перечислены структуры распределенная файловая система (DFS).

## <a name="in-this-section"></a>Содержание раздела

<dl> <dt>

[**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)
</dt> <dd>

Входной буфер, используемый с кодом элемента управления [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)
</dd> <dt>

[Структура _DFS_INFO_1](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1)
</dt> <dd>
Содержит имя корня или ссылки распределенная файловая система (DFS).

</dd> <dt>

[Структура _DFS_INFO_2](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2)
</dt> <dd>
Содержит сведения о корне или ссылке распределенная файловая система (DFS). Эта структура содержит имя, состояние и число целевых объектов DFS для корня или ссылки.

</dd> <dt>

[Структура _DFS_INFO_3](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3)
</dt> <dd>
Содержит сведения о корне или ссылке распределенная файловая система (DFS). Эта структура содержит имя, состояние, количество целевых объектов DFS и сведения о каждом целевом объекте корня или ссылки.

</dd> <dt>

[Структура _DFS_INFO_4](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4)
</dt> <dd>
Содержит сведения о корне или ссылке распределенная файловая система (DFS). Эта структура содержит имя, состояние, **GUID**, время ожидания, количество целевых объектов и сведения о каждом целевом объекте корня или ссылки.

</dd> <dt>

[Структура _DFS_INFO_5](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5)
</dt> <dd>
Содержит сведения о корне или ссылке распределенная файловая система (DFS). Эта структура содержит имя, состояние, **GUID**, время ожидания, пространство имен, свойства корня или ссылки, размер метаданных и число целевых объектов для корня или ссылки.

</dd> <dt>

[Структура _DFS_INFO_6](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6)
</dt> <dd>
Содержит сведения о корне или ссылке распределенная файловая система (DFS). Эта структура содержит имя, состояние, **GUID**, время ожидания, пространство имен, свойства корня или ссылки, размер метаданных, число целевых объектов и сведения о каждом целевом объекте корня или ссылки.

</dd> <dt>

[Структура _DFS_INFO_7](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_7)
</dt> <dd>
Содержит сведения о пространстве имен DFS. Эта структура содержит **идентификатор GUID** версии для метаданных пространства имен.

</dd> <dt>

[Структура _DFS_INFO_8](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_8)
</dt> <dd>
Содержит имя, состояние, **GUID**, время ожидания, флаги свойств, размер метаданных, сведения о целевом объекте DFS и дескриптор безопасности точки повторного анализа ссылок для корня или ссылки.

</dd> <dt>

[Структура _DFS_INFO_9](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_9)
</dt> <dd>
Содержит имя, состояние, **GUID**, время ожидания, флаги свойств, размер метаданных, сведения о целевом объекте DFS, дескриптор безопасности точки повторного анализа канала и список целевых объектов DFS для корня или ссылки.

</dd> <dt>

[Структура _DFS_INFO_50](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_50)
</dt> <dd>
Содержит версию метаданных DFS и возможности существующего пространства имен DFS.

</dd> <dt>

[Структура _DFS_INFO_100](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100)
</dt> <dd>
Содержит комментарий, связанный с корнем или ссылкой распределенная файловая система (DFS).

</dd> <dt>

[Структура _DFS_INFO_101](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101)
</dt> <dd>
Описывает состояние хранилища в корне DFS, ссылке, корневом целевом объекте или целевом объекте ссылки.

</dd> <dt>

[Структура _DFS_INFO_102](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102)
</dt> <dd>
Содержит значение времени ожидания для связи с корнем распределенная файловая система (DFS) или ссылкой в именованном корне DFS.

</dd> <dt>

[Структура _DFS_INFO_103](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_103)
</dt> <dd>
Содержит свойства, задают определенные поведения для корня или ссылки DFS.

</dd> <dt>

[Структура _DFS_INFO_104](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104)
</dt> <dd>
Содержит приоритет корневого целевого объекта DFS или ссылки.

</dd> <dt>

[Структура _DFS_INFO_105](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_105)
</dt> <dd>
Содержит сведения об корне или ссылке DFS, включая комментарии, состояние, время ожидания и поведение DFS, заданные флагами свойств.

</dd> <dt>

[Структура _DFS_INFO_106](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106)
</dt> <dd>
Содержит состояние хранилища и приоритет для корня DFS или целевого объекта ссылки. Эта структура предназначена только для использования с функцией [**нетдфссетинфо**](netdfssetinfo.md) .

</dd> <dt>

[Структура _DFS_INFO_107](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_107)
</dt> <dd>
Содержит сведения об корне или ссылке DFS, включая комментарий, состояние, время ожидания, флаги свойств и дескриптор безопасности точки повторного анализа ссылок.

</dd> <dt>

[Структура _DFS_INFO_150](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_150)
</dt> <dd>
Содержит дескриптор безопасности для точки повторного анализа ссылки DFS.

</dd> <dt>

[Структура _DFS_INFO_200](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_200)
</dt> <dd>
Содержит имя пространства имен распределенная файловая система на основе домена (DFS).

</dd> <dt>

[Структура _DFS_INFO_300](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_300)
</dt> <dd>
Содержит имя и тип (на основе домена или автономной версии) пространства имен DFS.

</dd> <dt>

[Структура _DFS_STORAGE_INFO](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info)
</dt> <dd>
Содержит сведения о корне или ссылке DFS в пространстве имен DFS или в кэше, поддерживаемом клиентом DFS.

</dd> <dt>

[Структура _DFS_STORAGE_INFO_1](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info_1)
</dt> <dd>
Содержит сведения о целевом объекте DFS, включая имя целевого сервера DFS и имя общего ресурса, а также состояние и приоритет целевого объекта.

</dd> <dt>

[Структура _DFS_SUPPORTED_NAMESPACE_VERSION_INFO](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info)
</dt> <dd>
Содержит сведения о версии для пространства имен DFS.

</dd> <dt>

[Структура _DFS_TARGET_PRIORITY](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority)
</dt> <dd>
Содержит класс приоритета и ранг определенного целевого объекта DFS.

</dd> </dl>
