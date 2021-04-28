---
description: AppInit_DLLs в Windows 7 и Windows Server 2008 R2
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: AppInit_DLLs в Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4820fcb9840bbec139ff78f3c6cc082b2dca4eeb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088712"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a>Библиотеки \_ библиотеки DLL в Windows 7 и Windows Server 2008 R2

## <a name="platform"></a>Платформа

**Клиенты** — Windows 7  
**Серверы** — Windows Server 2008 R2  









## <a name="feature-impact"></a>Воздействие на функции

 **Серьезность** — низкая  
**Частота** -низкая  





## <a name="description"></a>Описание

\_Библиотеки DLL библиотеки — это механизм, позволяющий загружать произвольный список библиотек DLL в каждый процесс пользовательского режима в системе. Корпорация Майкрософт изменяет средство библиотеки DLL в Windows 7 и Windows Server 2008 R2 для добавления нового требования подписывания кода. Это поможет повысить надежность и производительность системы, а также улучшить видимость происхождения программного обеспечения.

## <a name="configuration"></a>Параметр Configuration

Значения, хранящиеся в разделе « \_ \_ \\ программное обеспечение локального компьютера» \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows в реестре, определяют поведение \_ инфраструктуры библиотек DLL библиотеки. Следующие значения реестра описаны в таблице ниже.



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

Все библиотеки DLL, загруженные \_ инфраструктурой библиотек DLL библиотеки, должны быть подписаны кодом. В интересах совместимости приложений операционная система Windows 7 будет загружать все библиотеки библиотеки DLL. Однако корпорация Майкрософт рекомендует всем разработчикам приложений подписывать свои библиотеки DLL, чтобы помочь повысить надежность Windows и подготовить подписывание кода в будущих версиях Windows. \_Раздел реестра рекуиресигнедаппинит dllss управляет этим поведением, и его значение в Windows 7 по умолчанию равно 0.

**Windows Server 2008 R2**

Все библиотеки DLL, загруженные \_ инфраструктурой библиотек DLL библиотеки, должны быть подписаны кодом. \_Раздел реестра рекуиресигнедаппинит dllss управляет этим поведением, и его значение в Windows Server 2008 R2 по умолчанию равно 1.

## <a name="links-to-other-resources"></a>Ссылки на другие ресурсы

<dl>

[Библиотеки библиотеки DLL в Windows 7 и Windows Server 2008 R2](/windows-hardware/drivers/install/)  
</dl>

 

 
