---
description: Глоссарий терминов, используемых в документации по пакету SDK для виртуализации Windows.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 365D0295-EA0B-4B40-8272-DFF62B2A6F3D
title: Глоссарий Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: badb8fdfd25c4b7e11529778ab2cbd3c8cee5f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272074"
---
# <a name="hyper-v-glossary"></a>Глоссарий Hyper-V

В этом разделе содержится глоссарий терминов, используемых в документации по пакету SDK для виртуализации Windows.

<dl> <dt>

<span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**вязывания**
</dt> <dd>

Процесс, с помощью которого службы и уровни программного обеспечения связываются вместе. При установке сетевой службы устанавливаются отношения привязки и зависимости для служб.

</dd> <dt>

<span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**Создание**
</dt> <dd>

Моментальный снимок виртуальной машины, который позволяет администратору восстановить виртуальную машину в ее состояние на момент создания контрольной точки.

</dd> <dt>

<span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**свернут**
</dt> <dd>

Уменьшение размера динамически расширяющегося виртуального жесткого диска за счет удаления неиспользуемого пространства из VHD-файла.

</dd> <dt>

<span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**Разностный виртуальный жесткий диск**
</dt> <dd>

Виртуальный жесткий диск, на котором хранятся изменения в связанном родительском виртуальном жестком диске, чтобы сохранить родительский объект без изменений. Разностный диск — это отдельный VHD-файл, связанный с VHD-файлом родительского диска. Изменения продолжают накапливаться на разностном диске, пока он не будет объединен с родительским диском.

</dd> <dt>

<span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**динамически расширяемый виртуальный жесткий диск**
</dt> <dd>

Виртуальный жесткий диск, размер которого увеличивается каждый раз при его изменении. Этот тип виртуального жесткого диска запускается в виде файла VHD размером 3 КБ и может увеличиваться до максимального размера, указанного при создании файла. Единственным способом уменьшения размера файла является Обнуление удаленных данных и последующее сжатие виртуального жесткого диска.

</dd> <dt>

<span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**виртуальный жесткий диск фиксированного размера**
</dt> <dd>

Виртуальный жесткий диск с фиксированным размером, который определяется и для которого выделяется пространство при создании диска. При добавлении или удалении данных размер диска не изменяется.

</dd> <dt>

<span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**Виртуальная машина поколения 1**
</dt> <dd>

Виртуальная машина, которая содержит то же виртуальное оборудование, что и версии Hyper-V до Windows 8.1 и Windows Server 2012 R2

</dd> <dt>

<span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**Виртуальная машина поколения 2**
</dt> <dd>

Виртуальная машина (VM), которая содержит упрощенную виртуальную модель оборудования и использует встроенное по UEFI вместо BIOS. На этой виртуальной машине удаляются большинство эмулированных устройств, что снижает сложность управления и повышает уровень уязвимости.

</dd> <dt>

<span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**Гостевая операционная система**
</dt> <dd>

Операционная система, работающая на виртуальной машине.

</dd> <dt>

<span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**Службы Integration Services**
</dt> <dd>

Набор служб и драйверов программного обеспечения, обеспечивающий максимальную производительность и повышающий удобство работы пользователей в виртуальной машине. Службы Integration Services доступны только для поддерживаемых гостевых операционных систем.

</dd> <dt>

<span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**пара "ключ-значение"**
</dt> <dd>

Набор элементов данных, содержащий уникальный идентификатор, называемый ключом, и значение, которое является реальными данными для ключа.

</dd> <dt>

<span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**физический компьютер**
</dt> <dd>

Аппаратный компьютер, а не на виртуальную машину, основанную на программном обеспечении.

</dd> <dt>

<span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**сохраненное состояние**
</dt> <dd>

Способ хранения виртуальной машины, чтобы его можно было быстро возобновить, как и портативный компьютер в спящем режиме. При помещении работающей виртуальной машины в сохраненное состояние Virtual Server и Hyper-V останавливают виртуальную машину, записывают данные, которые находятся в памяти, во временные файлы, а также останавливают потребление системных ресурсов. Восстановление виртуальной машины из сохраненного состояния возвращает ее в то же состояние, в котором она находилась при сохранении состояния.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**Виртуальный гибкий диск**
</dt> <dd>

Файловая версия физического гибкого диска. Виртуальный гибкий диск хранится в виде файла с расширением VFD.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**виртуальный жесткий диск**
</dt> <dd>

Среда хранения для виртуальной машины. Она может находиться в любой топологии хранилища, к которой может получить доступ операционная система узла, включая внешние устройства, сети хранения данных и хранилище, подключенное к сети. Расширение имени файла —. VHD.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**Виртуальная машина**
</dt> <dd>

Компьютер в пределах компьютера, реализованный в программном обеспечении. Виртуальная машина эмулирует полную аппаратную систему, от процессора до сетевой карты, в автономной изолированной программной среде, обеспечивая одновременную работу несовместимых операционных систем. Каждая дочерняя операционная система выполняется в собственной изолированной программной виртуальной машине.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**Конфигурация виртуальной машины**
</dt> <dd>

Конфигурация ресурсов, назначенных виртуальной машине. К примерам относятся такие устройства, как диски и сетевые адаптеры, а также память и процессоры.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**Служба управления виртуальными машинами**
</dt> <dd>

Служба Hyper-V, обеспечивающая доступ к виртуальным машинам для управления.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**моментальный снимок виртуальной машины**
</dt> <dd>

Файловый снимок состояния, данных диска и конфигурации виртуальной машины в конкретный момент времени.

</dd> <dt>

<span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**Виртуальная сеть**
</dt> <dd>

Виртуальная версия коммутатора физической сети. Виртуальную сеть можно настроить для предоставления доступа к локальным или внешним сетевым ресурсам для одной или нескольких виртуальных машин.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**Диспетчер виртуальной сети**
</dt> <dd>

Служба Hyper-V, используемая для создания виртуальных сетей и управления ими.

</dd> <dt>

<span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**виртуальный коммутатор**
</dt> <dd>

См. раздел виртуальная сеть.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**Изменение размера VHDX**
</dt> <dd>

Операция, которая сжимает или развертывает виртуальный жесткий диск.

</dd> </dl>

 

 



