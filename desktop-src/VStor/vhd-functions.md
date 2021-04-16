---
description: 'Дополнительные сведения: <span id=vhd.vhd_functions></span> функции виртуального диска'
MS-HAID: vhd.vhd\_functions
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Функции виртуального диска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f31af2b24a55baa3c64bfe5bd9e09e0b9e2f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692325"
---
# <a name="span-idvhdvhd_functionsspanvirtual-disk-functions"></a><span id="vhd.vhd_functions"></span>Функции виртуального диска

В виртуальных дисках используются следующие функции.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>В этом разделе

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Раздел</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>апплиснапшотвхдсет</strong></a></p></td>
<td><p>Применение моментального снимка текущего виртуального диска для файлов набора виртуальных жестких дисков.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>аддвиртуалдискпарент</strong></a></p></td>
<td><p>Присоединяет родительский объект к виртуальному диску, открытому с флагом <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>аттачвиртуалдиск</strong></a></p></td>
<td><p>Подключает виртуальный жесткий диск (VHD) или файл образа диска DVD (ISO), находя соответствующий поставщик VHD для выполнения вложения.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>бреакмиррорвиртуалдиск</strong></a></p></td>
<td><p>Прерывает ранее инициированную операцию зеркального отображения и устанавливает зеркальное отображение в качестве активного виртуального диска.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>компактвиртуалдиск</strong></a></p></td>
<td><p>Уменьшает размер файла резервного хранилища виртуального жесткого диска (VHD).</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>креатевиртуалдиск</strong></a></p></td>
<td><p>Создает файл образа виртуального жесткого диска (VHD) либо с помощью параметров по умолчанию, либо с помощью существующего виртуального диска или физического диска.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>делетеснапшотвхдсет</strong></a></p></td>
<td><p>Удаляет моментальный снимок из файла набора виртуальных жестких дисков.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>делетевиртуалдискметадата</strong></a></p></td>
<td><p>Удаляет метаданные с виртуального диска.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>детачвиртуалдиск</strong></a></p></td>
<td><p>Отсоединяет виртуальный жесткий диск (VHD) или файл образа компакт-диска или DVD, находя соответствующий поставщик виртуальных дисков для выполнения операции.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>енумератевиртуалдискметадата</strong></a></p></td>
<td><p>Перечисляет метаданные, связанные с виртуальным диском.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>експандвиртуалдиск</strong></a></p></td>
<td><p>Увеличивает размер фиксированного или динамически расширяемого виртуального жесткого диска (VHD).</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>жетсторажедепенденциинформатион</strong></a></p></td>
<td><p>Возвращает связи между виртуальными жесткими дисками (VHD) или файлом образа компакт-диска или диска DVD (ISO) или томами, содержащимися на этих дисках, и их родительским диском или томом.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>жетвиртуалдискинформатион</strong></a></p></td>
<td><p>Извлекает сведения о виртуальном жестком диске.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>жетвиртуалдискметадата</strong></a></p></td>
<td><p>Извлекает указанные метаданные из виртуального диска.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>жетвиртуалдископератионпрогресс</strong></a></p></td>
<td><p>Проверяет ход выполнения асинхронной операции виртуального жесткого диска (VHD).</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>жетвиртуалдискфисикалпас</strong></a></p></td>
<td><p>Извлекает путь к объекту физического устройства, который содержит виртуальный жесткий диск (VHD) или файл образа компакт-диска или диска DVD (ISO).</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>мержевиртуалдиск</strong></a></p></td>
<td><p>Слияние дочернего виртуального жесткого диска (VHD) в цепочке разностного с одним или несколькими родительскими виртуальными дисками в цепочке.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>миррорвиртуалдиск</strong></a></p></td>
<td><p>Инициирует операцию зеркального отображения для виртуального диска.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>модифивхдсет</strong></a></p></td>
<td><p>Изменяет внутреннее содержимое файла виртуального диска. Можно использовать для установки активного листа или для исправления записей моментального снимка.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>опенвиртуалдиск</strong></a></p></td>
<td><p>Открывает виртуальный жесткий диск (VHD) или файл образа компакт-диска или диска DVD (ISO) для использования.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>куеричанжесвиртуалдиск</strong></a></p></td>
<td><p>Извлекает сведения об изменениях в указанных областях виртуального жесткого диска (VHD), которые отслеживаются с помощью отказоустойчивого отслеживания изменений (RCT).</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>равсксивиртуалдиск</strong></a></p></td>
<td><p>Выдает встроенный SCSI-запрос непосредственно на виртуальный жесткий диск.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ресизевиртуалдиск</strong></a></p></td>
<td><p>Изменяет размер виртуального диска.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>сетвиртуалдискинформатион</strong></a></p></td>
<td><p>Задает сведения о виртуальном жестком диске (VHD).</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>сетвиртуалдискметадата</strong></a></p></td>
<td><p>Задает элемент метаданных для виртуального диска.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>такеснапшотвхдсет</strong></a></p></td>
<td><p>Создает моментальный снимок текущего виртуального диска для файлов набора виртуальных жестких дисков.</p></td>
</tr>
</tbody>
</table>

 

 

 
