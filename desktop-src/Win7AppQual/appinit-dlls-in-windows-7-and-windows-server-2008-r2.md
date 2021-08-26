---
description: AppInit_DLLs в Windows 7 и Windows Server 2008 R2
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: AppInit_DLLs в Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8741039952b0ea15d32b19bc48d4197ea13751bc492ff82fc8e67b1662d0b682
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031074"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a>\_библиотеки dll библиотеки в Windows 7 и Windows Server 2008 R2

## <a name="platform"></a>Платформа

**клиенты** — Windows 7  
**серверы** — Windows Server 2008 R2  









## <a name="feature-impact"></a>Воздействие на функции

 **Серьезность** — низкая  
**Частота** -низкая  





## <a name="description"></a>Описание

\_Библиотеки DLL библиотеки — это механизм, позволяющий загружать произвольный список библиотек DLL в каждый процесс пользовательского режима в системе. корпорация майкрософт изменяет библиотеки библиотеки dll в Windows 7 и Windows Server 2008 R2 для добавления нового требования подписывания кода. Это поможет повысить надежность и производительность системы, а также улучшить видимость происхождения программного обеспечения.

## <a name="configuration"></a>Конфигурация

значения, хранящиеся в разделе « \_ \_ программное обеспечение на локальном компьютере» \\ \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows key в реестре, определяют поведение \_ инфраструктуры библиотек dll библиотеки. Следующие значения реестра описаны в таблице ниже.



<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Описание</th>
<th>Примеры значений</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">LoadAppInit_DLLs (REG_DWORD) $ {Remove} $<br />
</td>
<td rowspan="2">Глобально включает или отключает AppInit_DLLs. $ {Remove} $<br />
</td>
<td>0x0 — AppInit_DLLs отключены.</td>
</tr>
<tr class="even">
<td>0x1 — AppInit_DLLs включены.</td>


</tr>
<tr class="odd">
<td>AppInit_DLLs (REG_SZ)</td>
<td>Разделенный запятыми список библиотек DLL для загрузки. Полный путь к библиотеке DLL должен быть указан с использованием коротких имен.</td>
<td>C:\ РОГРАММА ~ 1 \ WID288 ~ 1 \ MICROS ~1.DLL</td>
</tr>
<tr class="even">
<td rowspan="2">RequireSignedAppInit_DLLs (REG_DWORD) $ {Remove} $<br />
</td>
<td rowspan="2">Загружать только подписанные на код библиотеки DLL. $ {Remove} $<br />
</td>
<td>0x0 — Загрузка любых библиотек DLL.</td>
</tr>
<tr class="odd">
<td>0x1 — загружать только подписанные кодом библиотеки DLL.</td>


</tr>
</tbody>
</table>



 

**Windows 7**

Все библиотеки DLL, загруженные \_ инфраструктурой библиотек DLL библиотеки, должны быть подписаны кодом. в интересах совместимости приложений операционная система Windows 7 будет загружать все библиотеки dll библиотеки. однако корпорация майкрософт рекомендует всем разработчикам приложений подписывать свои библиотеки dll, чтобы помочь повысить надежность Windows и подготовить подписывание кода в будущих версиях Windows. \_раздел реестра рекуиресигнедаппинит dllss управляет этим поведением, и его значение в Windows 7 по умолчанию равно 0.

**Windows Server 2008 R2**

Все библиотеки DLL, загруженные \_ инфраструктурой библиотек DLL библиотеки, должны быть подписаны кодом. \_раздел реестра рекуиресигнедаппинит dllss управляет этим поведением и его значением в Windows Server 2008 R2 по умолчанию имеет значение 1.

## <a name="links-to-other-resources"></a>Ссылки на другие ресурсы

<dl>

[библиотеки dll библиотеки в Windows 7 и Windows Server 2008 R2](/windows-hardware/drivers/install/)  
</dl>

 

 
