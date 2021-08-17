---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 50397050-3b5c-4683-972c-95d9f661b365
ms.tgt_platform: multiple
title: D (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2310ce8b14baf2b57634cfa36ef83c3dab239503632972b67bdc4cc6a9b1f602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117924160"
---
# <a name="d-wmi"></a>D (WMI)

[A](gloss-a.md) B [C](gloss-c.md) D [E](gloss-e.md) [F](gloss-f.md) G [р](gloss-h.md) [.](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_datetime"></span><span id="WMI.GLOSS_DATETIME"></span>**DateTime**
</dt> <dd>

См. раздел [*DateTime CIM*](gloss-c.md).

</dd> <dt>

<span id="wmi.gloss_decoupled_provider"></span><span id="WMI.GLOSS_DECOUPLED_PROVIDER"></span>**Несвязанный поставщик**
</dt> <dd>

Поставщик, который выполняется в отдельном от WMI процессе. Для инструментирования приложения рекомендуется использовать несвязанные поставщики, так как поставщик может управлять собственным временем существования, а не запускать каждый раз, когда пользователь обращается к поставщику через WMI.

</dd> <dt>

<span id="wmi.gloss_direct_access"></span><span id="WMI.GLOSS_DIRECT_ACCESS"></span>**прямой доступ**
</dt> <dd>

Способ доступа к свойствам и методам, предоставляемым WMI в скрипте, как если бы они были свойствами автоматизации и методами [**SWbemObject**](swbemobject.md).

Непосредственный доступ: `VolumeName = MyDisk.Properties_("VolumeName")`

Прямой доступ: `VolumeName = MyDisk.VolumeName`

</dd> <dt>

<span id="wmi.gloss_distributed_management_task_force"></span><span id="WMI.GLOSS_DISTRIBUTED_MANAGEMENT_TASK_FORCE"></span>**Распределенное управление задачей Force (DMTF)**
</dt> <dd>

Международная организация стандартов, которая работает с основными поставщиками технологий, включая Майкрософт, для разработки, внедрения и унификации стандартов управления и инициатив для настольных, корпоративных и Интернет сред.

</dd> <dt>

<span id="wmi.gloss_dmtf"></span><span id="WMI.GLOSS_DMTF"></span>**DMTF**
</dt> <dd>

См. раздел *распределенное управление Task Force (DMTF)*.

</dd> <dt>

<span id="wmi.gloss_dynamic_class"></span><span id="WMI.GLOSS_DYNAMIC_CLASS"></span>**динамический класс**
</dt> <dd>

Класс CIM, определение которого предоставляется [*поставщиком*](gloss-p.md) во время выполнения по мере необходимости. Динамические классы представляют [*управляемые объекты*](gloss-m.md) , зависящие от поставщика, и не хранятся в [*репозитории CIM*](gloss-c.md). Динамические классы поддерживают только *динамические экземпляры*.

</dd> <dt>

<span id="wmi.gloss_dynamic_instance"></span><span id="WMI.GLOSS_DYNAMIC_INSTANCE"></span>**динамический экземпляр**
</dt> <dd>

Экземпляр класса CIM, предоставляемый [*поставщиком*](gloss-p.md) при необходимости. Он не хранится в [*репозитории CIM*](gloss-c.md). Динамические экземпляры могут быть предоставлены либо для статических, либо для динамических классов. Динамически поддерживающие экземпляры класса позволяют поставщику предоставлять значения [*свойств*](gloss-p.md) , сопоставляемые в минуту.

</dd> </dl>

 

 



