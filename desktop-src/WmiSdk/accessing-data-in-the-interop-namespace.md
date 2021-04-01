---
description: Поставщики ассоциаций позволяют клиентам инструментарий управления Windows (WMI) (WMI) просматривать и получать профили и связанные экземпляры классов из разных пространств имен.
ms.assetid: 00c654d1-a5de-40c5-a190-99382949486a
ms.tgt_platform: multiple
title: Доступ к данным в пространстве имен Interop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a217a7a44651b1a6c94476b53193eedac7f0d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999378"
---
# <a name="accessing-data-in-the-interop-namespace"></a>Доступ к данным в пространстве имен Interop

Поставщики ассоциаций позволяют клиентам инструментарий управления Windows (WMI) (WMI) просматривать и получать профили и связанные экземпляры классов из разных пространств имен.

Поставщики ассоциаций и классы находятся в \\ \\ корневом \\ пространстве имен взаимодействия. Дополнительные сведения см. в разделе [перекрестное сопоставление связей между пространствами имен](cross-namespace-association-traversal.md) и [запись поставщика взаимосвязей](writing-an-association-provider-for-interop.md).

Поставщики ассоциаций предоставляют стандартные профили, например профиль питания. В следующих примерах используется профиль управления питанием для демонстрации обнаружения и доступа к данным через пространство имен Interop.

Windows PowerShell предоставляет простой механизм для прохода по соответствующей ассоциации, получения профиля устройства и вызова метода.

## <a name="enumerating-profiles-in-the-rootinterop-namespace"></a>Перечисление профилей в пространстве имен root или Interop

Следующая команда Windows PowerShell перечисляет поддерживаемые профили распределенного управления Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) на компьютере с Windows 7.


```PowerShell
Get-WmiObject CIM_RegisteredProfile  -namespace root\interop
```



## <a name="retrieving-instances-of-a-specific-device-profile"></a>Получение экземпляров определенного профиля устройства

Следующая команда Windows PowerShell возвращает все экземпляры указанного профиля через [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)):


```PowerShell
Get-WmiObject -namespace root\interop -query "Associators of {CIM_RegisteredProfile.InstanceID='Power Supply'}"
```



## <a name="assigning-the-power-profile-to-a-variable"></a>Назначение профиля питания переменной

Следующая команда Windows PowerShell присваивает экземпляр профиля управления питанием переменной:


```PowerShell
$pplan = Get-WmiObject -query "Select * from Win32_PowerPlan" -Namespace root\cimv2\power
```



## <a name="enumerating-the-power-plans-on-a-computer"></a>Перечисление схем управления питанием на компьютере

Следующая команда Windows PowerShell перечисляет доступные планы профиля управления питанием:


```PowerShell
$pplan
```



## <a name="calling-a-method"></a>Вызов метода

Следующая команда Windows PowerShell вызывает метод [**Activate**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) для схемы управления питанием:


```PowerShell
$pplan[2].Activate()
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Просмотр связей между пространствами имен](cross-namespace-association-traversal.md)
</dt> <dt>

[Написание поставщика ассоциаций](writing-an-association-provider-for-interop.md)
</dt> <dt>

[**\_РЕГИСТЕРЕДПРОФИЛЕ CIM**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[**\_PowerPlan Win32**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))
</dt> </dl>

 

 
