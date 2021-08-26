---
description: 'Дополнительные сведения: <span id=vhd.vhd_functions></span> функции виртуального диска'
MS-HAID: vhd.vhd\_functions
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Функции виртуального диска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32133e3afa8402de8483a68eb4957b261b46e556
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477220"
---
# <a name="span-idvhdvhd_functionsspanvirtual-disk-functions"></a><span id="vhd.vhd_functions"></span>Функции виртуального диска

В виртуальных дисках используются следующие функции.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>В этом разделе


| Раздел | Описание | 
|-------|-------------|
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>апплиснапшотвхдсет</strong></a></p> | <p>Применение моментального снимка текущего виртуального диска для файлов набора виртуальных жестких дисков.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>аддвиртуалдискпарент</strong></a></p> | <p>Присоединяет родительский объект к виртуальному диску, открытому с флагом <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> .</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>аттачвиртуалдиск</strong></a></p> | <p>Подключает виртуальный жесткий диск (VHD) или файл образа диска DVD (ISO), находя соответствующий поставщик VHD для выполнения вложения.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>бреакмиррорвиртуалдиск</strong></a></p> | <p>Прерывает ранее инициированную операцию зеркального отображения и устанавливает зеркальное отображение в качестве активного виртуального диска.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>компактвиртуалдиск</strong></a></p> | <p>Уменьшает размер файла резервного хранилища виртуального жесткого диска (VHD).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>креатевиртуалдиск</strong></a></p> | <p>Создает файл образа виртуального жесткого диска (VHD) либо с помощью параметров по умолчанию, либо с помощью существующего виртуального диска или физического диска.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>делетеснапшотвхдсет</strong></a></p> | <p>Удаляет моментальный снимок из файла набора виртуальных жестких дисков.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>делетевиртуалдискметадата</strong></a></p> | <p>Удаляет метаданные с виртуального диска.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>детачвиртуалдиск</strong></a></p> | <p>Отсоединяет виртуальный жесткий диск (VHD) или файл образа компакт-диска или DVD, находя соответствующий поставщик виртуальных дисков для выполнения операции.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>енумератевиртуалдискметадата</strong></a></p> | <p>Перечисляет метаданные, связанные с виртуальным диском.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>експандвиртуалдиск</strong></a></p> | <p>Увеличивает размер фиксированного или динамически расширяемого виртуального жесткого диска (VHD).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>жетсторажедепенденциинформатион</strong></a></p> | <p>Возвращает связи между виртуальными жесткими дисками (VHD) или файлом образа компакт-диска или диска DVD (ISO) или томами, содержащимися на этих дисках, и их родительским диском или томом.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>жетвиртуалдискинформатион</strong></a></p> | <p>Извлекает сведения о виртуальном жестком диске.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>жетвиртуалдискметадата</strong></a></p> | <p>Извлекает указанные метаданные из виртуального диска.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>жетвиртуалдископератионпрогресс</strong></a></p> | <p>Проверяет ход выполнения асинхронной операции виртуального жесткого диска (VHD).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>жетвиртуалдискфисикалпас</strong></a></p> | <p>Извлекает путь к объекту физического устройства, который содержит виртуальный жесткий диск (VHD) или файл образа компакт-диска или диска DVD (ISO).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>мержевиртуалдиск</strong></a></p> | <p>Слияние дочернего виртуального жесткого диска (VHD) в цепочке разностного с одним или несколькими родительскими виртуальными дисками в цепочке.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>миррорвиртуалдиск</strong></a></p> | <p>Инициирует операцию зеркального отображения для виртуального диска.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>модифивхдсет</strong></a></p> | <p>Изменяет внутреннее содержимое файла виртуального диска. Можно использовать для установки активного листа или для исправления записей моментального снимка.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>опенвиртуалдиск</strong></a></p> | <p>Открывает виртуальный жесткий диск (VHD) или файл образа компакт-диска или диска DVD (ISO) для использования.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>куеричанжесвиртуалдиск</strong></a></p> | <p>Извлекает сведения об изменениях в указанных областях виртуального жесткого диска (VHD), которые отслеживаются с помощью отказоустойчивого отслеживания изменений (RCT).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>равсксивиртуалдиск</strong></a></p> | <p>Выдает встроенный SCSI-запрос непосредственно на виртуальный жесткий диск.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ресизевиртуалдиск</strong></a></p> | <p>Изменяет размер виртуального диска.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>сетвиртуалдискинформатион</strong></a></p> | <p>Задает сведения о виртуальном жестком диске (VHD).</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>сетвиртуалдискметадата</strong></a></p> | <p>Задает элемент метаданных для виртуального диска.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>такеснапшотвхдсет</strong></a></p> | <p>Создает моментальный снимок текущего виртуального диска для файлов набора виртуальных жестких дисков.</p> | 


 

 

 
