---
description: Настройка политик IPSec и сопоставлений безопасности для IPv6 выполняется с Ipsec6.exe.
ms.assetid: 9a0c8e48-bc57-461d-9ade-54b75f7aa56d
title: Ipsec6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b373e8ab0dc54c3c8ee2fae8bc05722a9ac6aa64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711028"
---
# <a name="ipsec6exe"></a>Ipsec6.exe

Настройка политик IPSec и сопоставлений безопасности для IPv6 выполняется с Ipsec6.exe. Ниже приведены Ipsec6.exe подкоманды.

<dl> <dt>

<span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>**ipsec6 SP \[** _Интерфейс_*_\]_*
</dt> <dd>

Отображает активные политики безопасности. Кроме того, отображает активные политики безопасности для определенного интерфейса.

</dd> <dt>

<span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**ipsec6 SA**
</dt> <dd>

Отображает активные сопоставления безопасности.

</dd> <dt>

<span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 c \[** _Имя файла (без расширения)_*_\]_*
</dt> <dd>

Создает файлы, используемые для настройки политик безопасности и сопоставлений безопасности. Создает *файл filename*. SPD для политик безопасности и *filename*. sad для сопоставлений безопасности. Используйте созданные файлы в качестве шаблонов для настройки политик безопасности или сопоставлений безопасности. Файлы можно изменить в текстовом редакторе. Чтобы вызвать конфигурацию, содержащуюся в файлах SPD и SAD, используйте команду **ipsec6** .

</dd> <dt>

<span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 a \[** _Имя файла (без расширения)_*_\]_*
</dt> <dd>

Добавляет политики *безопасности в файле filename.* SPD и сопоставления безопасности в файле *filename*. sad в список активных политик безопасности и сопоставлений безопасности.

</dd> <dt>

<span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 i \[**  *_\] \[_* _Имя файла политики (без расширения)_*_\]_*
</dt> <dd>

Добавляет политики безопасности в *файл* filename. SPD и сопоставления безопасности в файле *filename*. sad в список активных политик безопасности и сопоставлений безопасности, на которые ссылается номер политики.

</dd> <dt>

<span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**ipsec6 d \[ Type = SP SA \] \[** _индекснумбер_*_\]_*
</dt> <dd>

Удаляет политики безопасности или сопоставления безопасности из списка активных политик безопасности и сопоставлений безопасности, которые указываются по номеру индекса (отображается с помощью **ipsec6 SP** или **ipsec6 SA**).

</dd> </dl>

 

 



