---
description: 'Дополнительные сведения: члены экземпляров'
title: Члены экземпляра
TOCTitle: Instance members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Instance
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance_members(v=EXCHG.10)
ms:contentKeyID: 55103299
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 8ba8dad079feba566dbb8fca873fcea19af778ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897969"
---
# <a name="instance-members"></a>Члены экземпляра

Включить защищенные члены  
Включить унаследованные члены  

Класс, инкапсулирующий [JET_INSTANCE](./jet-instance-structure.md) в удаляемом объекте. Экземпляр должен быть закрыт последним, а закрытие экземпляра освобождает все остальные ресурсы для экземпляра.

Тип [экземпляра](./instance-class.md) предоставляет следующие члены.

## <a name="constructors"></a>Конструкторы

<table>
<thead>
<tr class="header">
<th> </th>
<th>Имя</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn350924(v=exchg.10).md">Экземпляр (строка)</a></td>
<td>Инициализирует новый экземпляр класса экземпляра. Базовый JET_INSTANCE выделяется, но не инициализируется.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn350927(v=exchg.10).md">Экземпляр (строка, строка)</a></td>
<td>Инициализирует новый экземпляр класса экземпляра. Базовый JET_INSTANCE выделяется, но не инициализируется.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn350948(v=exchg.10).md">Экземпляр (строка, строка, Термгрбит)</a></td>
<td>Инициализирует новый экземпляр класса экземпляра. Базовый JET_INSTANCE выделяется, но не инициализируется.</td>
</tr>
</tbody>
</table>


Начало

## <a name="properties"></a>Свойства

<table>
<thead>
<tr class="header">
<th> </th>
<th>Имя</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.isclosed#System_Runtime_InteropServices_SafeHandle_IsClosed">IsClosed</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid.isinvalid#Microsoft_Win32_SafeHandles_SafeHandleZeroOrMinusOneIsInvalid_IsInvalid">Недопустимый</a></td>
<td>(Наследуется от <a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid">сафехандлезерурминусонеисинвалид</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn350941(v=exchg.10).md">жетинстанце</a></td>
<td>Возвращает JET_INSTANCE, который содержит этот экземпляр.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn350962(v=exchg.10).md">Параметры</a></td>
<td>Возвращает Инстанцепараметерс для данного экземпляра.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><a href="dn350964(v=exchg.10).md">термгрбит</a></td>
<td>Возвращает или задает Термгрбит для данного экземпляра.</td>
</tr>
</tbody>
</table>


Начало

## <a name="methods"></a>Методы

<table>
<thead>
<tr class="header">
<th> </th>
<th>Имя</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.close#System_Runtime_InteropServices_SafeHandle_Close">Закрыть</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousaddref#System_Runtime_InteropServices_SafeHandle_DangerousAddRef_System_Boolean__">данжераусаддреф</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousgethandle#System_Runtime_InteropServices_SafeHandle_DangerousGetHandle">DangerousGetHandle</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousrelease#System_Runtime_InteropServices_SafeHandle_DangerousRelease">данжераусрелеасе</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose">Dispose ()</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose_System_Boolean_">Dispose (логическое значение)</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Равно</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.finalize#System_Runtime_InteropServices_SafeHandle_Finalize">Finalize</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn350932(v=exchg.10).md">Init ()</a></td>
<td>Инициализируйте JET_INSTANCE.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn350954(v=exchg.10).md">Init (Инитгрбит)</a></td>
<td>Инициализируйте JET_INSTANCE.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn350934(v=exchg.10).md">Init (JET_RSTINFO, Инитгрбит)</a></td>
<td>Инициализируйте JET_INSTANCE. Для этого API требуется по крайней мере версия ESENT для Vista.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="dn350956(v=exchg.10).md">ReleaseHandle</a></td>
<td>Освобождение маркера для этого экземпляра. (Переопределяет <a href="/dotnet/api/system.runtime.interopservices.safehandle.releasehandle#System_Runtime_InteropServices_SafeHandle_ReleaseHandle">SafeHandle. ReleaseHandle ()</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandle#System_Runtime_InteropServices_SafeHandle_SetHandle_System_IntPtr_">сесандле</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandleasinvalid#System_Runtime_InteropServices_SafeHandle_SetHandleAsInvalid">сесандлеасинвалид</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn350935(v=exchg.10).md">Термин</a></td>
<td>Завершите JET_INSTANCE.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><a href="dn350960(v=exchg.10).md">ToString</a></td>
<td>Возвращает <a href="/dotnet/api/system.string">строку</a> , представляющую текущий <a href="dn350923(v=exchg.10).md">экземпляр</a>. (Переопределяет <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</td>
</tr>
</tbody>
</table>


Начало

## <a name="operators"></a>Операторы

<table>
<thead>
<tr class="header">
<th> </th>
<th>Имя</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Открытый оператор" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn350950(v=exchg.10).md">Неявный (экземпляр JET_INSTANCE)</a></td>
<td>Предоставьте неявное преобразование объекта экземпляра в структуру JET_INSTANCE. Это делается так, что экземпляр можно использовать в любом месте, где требуется JET_INSTANCE.</td>
</tr>
</tbody>
</table>


Начало

## <a name="fields"></a>Поля

<table>
<thead>
<tr class="header">
<th> </th>
<th>name</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.protfield(exchg.10).gif" title="Защищенное поле" alt="Protected field" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.handle">справиться</a></td>
<td>(Наследуется от <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс экземпляра](./instance-class.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
